# 1097B-cf-

#include <iostream>
using namespace std;
int n,i,j,s,a[20];
int main(){
    cin>>n;
	for(i=0;i<n;i++)cin>>a[i];
	for(i=0;i<(1<<n);i++){
		for(j=s=0;j<n;j++)
		if(i&(1<<j))
		s+=a[j];
		else
		s-=a[j];
		if(s%360==0)return cout<<"YES",0;
	}
	cout<<"NO";
}
