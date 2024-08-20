# WAVE-PRINT-IN-2D-ARRAY-c-
#include <iostream>
#include <vector>
using namespace std;
vector <int>waveprint(int arr[][100],int n,int m){
vector<int> ans;
    for(int col=0;col<m;col++){
        if(col%2!=0){
            for(int row=n-1;row>=0;row--){
                ans.push_back(arr[row][col]);
                
            }
        }
        else{
            for(int row=0;row<n;row++){
                ans.push_back(arr[row][col]);
            }
        }
    }
    return ans;
}
int main()
{
    int n;
    cout<<"enter the size of row"<<endl;
    cin>>n;
    int m;
    cout<<" enter the size of columns"<<endl;
    cin>>m;
    int arr[100][100];
    cout<<" enter the elements of array"<<endl;
    for(int row=0;row<n;row++){
        for(int col=0;col<m;col++){
            cin>>arr[row][col];
        }
    }
    for(int row=0;row<n;row++){
        for(int col=0;col<m;col++){
            cout<<arr[row][col]<<" ";
        }
        cout<<endl;
    }
    cout<<" printing the wave print ";
   // int num=waveprint(arr,n,m);
   vector<int> result=waveprint(arr,n,m);
   for(int i=0;i<result.size();i++){
       cout<<result[i]<<" ";
   }
    cout<<endl;
    
    return 0;
}
