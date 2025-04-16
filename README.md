# BinarySearch
Binary Search is a fast algorithm to find an element in a sorted list. Instead of checking each element one by one (like in Linear Search), it divides the list in half each time to narrow down the search.


#include <iostream>
using namespace std;
int binary_search(int arr[] , int left , int right , int value ){
while(left <= right){
    int mid = (left + right ) /2 ;

    if (arr[mid] == value){
        return mid ;
        cout<<"best case ! \n"<<endl;
    }
    else if (arr [mid] > value ){
        right=mid-1 ;
    }
    else{
        left=mid+1 ;
    }

}

return -1;
}


int main()
{
    int arr[] ={1,2,3,4,5,6,7,8,9,10};
    int size = sizeof(arr)/4;
    int value ;
    cout<<"enter the value : "<<endl;
    cin>>value;

    int left = 0 ;
    int right = size-1 ;


   int result = binary_search(arr, left , right , value ) ;
if (result == -1 ){
cout<<"not found "<<endl;
}
else {
cout<<"found in : "<<result<<endl;
}

    return 0;
}
