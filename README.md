#include<iostream>
using namespace std;

void bubbleSort(int arr[],int n){
    for(int i = 1 ; i < n ; i++){
        for(int j = 0 ; j < n-i ; j++){
            if(arr[j] > arr[j+1]){
                swap(arr[j] , arr[j+1]);
            }
        }
    }
}

int printArr(int arr[],int size){
    for(int i = 0 ; i < size ; i++){
        cout << arr[i] << " ";
    }
    cout << endl;
}

int main() {
    int arr[6] = {2,4,6,1,7,9};

    int N = sizeof(arr) / sizeof(arr[0]);

    bubbleSort(arr,N);
    cout<<endl;
    cout<<"The sorted array is : ";
    printArr(arr,N);   
    cout<<endl;
    return 0;
}
