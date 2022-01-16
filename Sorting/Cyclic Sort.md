# Code

arr={1,2,3,4,5} --> O(n)
arr1={5,4,3,2,1} --> O(n)

public static void cyclicSort(int[] arr){

        for(int i=0;i<arr.length;i++){
            if(arr[i]!=i+1){
                swap(arr,i,arr[i]-1);i--;
            }
        }
        
}

private static void swap(int[] arr, int a, int b) {

        int t=arr[a];
        arr[a]=arr[b];
        arr[b]=t;
}
