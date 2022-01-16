# Code

int[] arr = {1,2,3,4,5};O(n)
int[] arr1= {5,4,3,2,1};O(n^2)
int[] arr2= {2,3,4,5,1};O(2n)

public static void InsertionSort(int[] arr){

        for(int i=0;i<arr.length-1;i++){
            for(int j=i+1;j>0;j--){
                if(arr[j]>=arr[j-1]) break;

                int t=arr[j];
                arr[j]=arr[j-1];
                arr[j-1]=t;
            }
        }
}
