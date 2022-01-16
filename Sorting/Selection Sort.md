# Code

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
