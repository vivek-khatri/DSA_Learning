# Code

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
