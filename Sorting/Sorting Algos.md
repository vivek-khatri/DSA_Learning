# Code

public class Selection_Bubble_InsertionSort {

    public static void main(String args[]){
        int[] arr = {1,2,3,4,5};
        int[] arr1= {5,4,3,2,1};
        int[] arr2= {2,3,4,5,1};

//        BubbleSort(arr); //O(n)

//        BubbleSort(arr1);//O(n^2)

//        BubbleSort(arr2);//O(n^2)

//Bubble Sort

//O(n) as on i=0 pass, no swaps in j. So algorithm will know that input is already sorted.

//O(n^2) as on all i, atleast one swap is necessary, so for each j if swapping happens at least 1 time(possibly last),


//        SelectionSort(arr); //O(n^2)

//        SelectionSort(arr1);//O(n^2)

//        SelectionSort(arr2);//O(n^2)

//Selection Sort

//O(n^2) Always


        InsertionSort(arr); //O(n)
        InsertionSort(arr1);//O(n^2)
        InsertionSort(arr2);//O(2n)


        System.out.println(Arrays.toString(arr));
        System.out.println(Arrays.toString(arr1));
        System.out.println(Arrays.toString(arr2));

    }
    
    
    
    
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

}
