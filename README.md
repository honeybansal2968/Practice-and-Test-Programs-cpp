# Practice-and-Test-Programs-cpp
C++ programs for testing and practice.

// C++ program of linear Search

#include <bits/stdc++.h>
#include <chrono>
#include <ctime>
using namespace std;
using namespace chrono;
// int linearSearch(int arr[],int n , int key){
//     for(int i=0;i<n;++i){
//         if(arr[i]==key){
//             return i;
//         }
//     }
//     return -1;
// }

int linearSearch(int *arr,int n, int key){
    for(int i=0;i<n;++i){
        if(*(arr+i)==key){
            return i;
        }
    }
    return -1;
}
int main(){
    std::chrono::time_point<std::chrono::system_clock> start, end;
    
    int n;
    cout<<"Enter length of array: ";
    cin>>n;
    int arr[n];
    cout<<"Enter elements of array: ";
    for(int i=0;i<n;++i){
        cin>>arr[i];
    }
    int key;
    cout<<"Enter key: ";
    cin>>key;
    
    start = std::chrono::system_clock::now();
    cout<<linearSearch(arr,n,key);
    end = std::chrono::system_clock::now();
    std::chrono::duration<double> elapsed_seconds = end - start;
    cout<< "elapsed time: " << elapsed_seconds.count() <<endl;
}
