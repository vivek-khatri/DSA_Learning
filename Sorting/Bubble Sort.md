# Code

arr = {1,2,3,4,5} --> O(n)

arr1= {5,4,3,2,1} --> O(n^2)

arr2= {2,3,4,5,1} --> O(n^2)

public static void BubbleSort(int[] arr){

        for(int i=0;i<arr.length;i++){
            boolean unswapped = true;
            for(int j=1;j<arr.length-i;j++){
                if(arr[j-1]>arr[j]){
                    int t=arr[j-1];
                    arr[j-1]=arr[j];
                    arr[j]=t;
                    unswapped = false;
                }
            }
            if(unswapped) break;
        }
        
}
