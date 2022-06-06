# reversearray-with-array
#include<bits/stdc++.h>
using namespace std;
   int reversearry(int arr[],int s,int e,int N){ ///note array is a pointer so it can change mains arrar//
    int temp=arr[s];
    arr[s]=arr[e];
    arr[e]=temp;
    if(s>=e){
        return 0;
    }
    else{
        s+=1;
        e-=1;
        return reversearry(arr,s,e,N);
    }
}
 void print(int a[],int NN){
      for(int i=0;i<NN;i++){
           cout<<a[i]<<" ";
      }
 }
int main(){
    int n;
    cin>>n;
    int arry[n];
    for(int i=0;i<n;i++){
        cin>>arry[i];
    }
    int end=n-1;
    reversearry(arry,0,end,n);
    print(arry,n);
    return 0;
}
