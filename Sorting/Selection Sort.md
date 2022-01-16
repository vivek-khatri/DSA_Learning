# Code

arr = {1,2,3,4,5} --> O(n^2)

arr1= {5,4,3,2,1} --> O(n^2)

arr2= {2,3,4,5,1} --> O(n^2)

public static void SelectionSort(int[] arr){

        for(int i=0;i<arr.length;i++){
            int m=i;
            for(int j=i+1;j<arr.length;j++){
                if(arr[j]<arr[m])
                    m=j;
            }
            int t=arr[m];
            arr[m]=arr[i];
            arr[i]=t;
        }
        
}
