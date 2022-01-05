# [Question](https://leetcode.com/problems/first-bad-version/)
## Code
public class Solution extends VersionControl {

    public int firstBadVersion(int n) {
        int f=1,e=n;
        while(f<=e){
            int m = f+(e-f)/2;
            if(isBadVersion(m)){
                e=m-1;
                if(e>0 && !isBadVersion(e))
                    return m;
            }
            else{
                f=m+1;
                if(isBadVersion(f))
                    return f;
            }
        }
        return f;
    }
}
