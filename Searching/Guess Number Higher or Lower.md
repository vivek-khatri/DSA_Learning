# [Question](https://leetcode.com/problems/guess-number-higher-or-lower/)
## Code
public class Solution extends GuessGame {

    public int guessNumber(int n) {
        int f=1,e=n;
        while(f<=e){
            int m = f+(e-f)/2;
            if(guess(m)<0)
                e=m-1;
            else if(guess(m)>0)
                f=m+1;
            else return m;
        }
        return e;
    }
}
