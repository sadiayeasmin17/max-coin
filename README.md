# max-coin

#include<iostream>
using namespace std;
int main()
{
    int n,j,d,swap,swap1,cl[50],i,owed,t[i],noc[i];
    cin>>n;
    int count=0;
    cout<<"enter denominations";
    for(i=0;i<n;i++)
    {
        cin>>cl[i];
    }
    cout<<"enter number for each coin";
     for(j=0;j<n;j++)
    {
        cin>>noc[i];
    }
    for(i=0;i<n;i++)
    {
        for(d=0;d<n-i-1;d++)
        {
            if(cl[d]>cl[d+1])
            {
                swap=cl[d];
                cl[d]=cl[d+1];
                cl[d+1]=swap;
            }
             
        }
    }
    for(j=0;j<n;j++)
    {
        for(d=0;d<n-i-1;d++)
        {
           
             if(noc[d]>noc[d+1])
            {
                swap1=noc[d];
                noc[d]=noc[d+1];
                noc[d+1]=swap1;
            }
        }
        count++;
    }
   
   
    cout<<"enter the amount owed";
    cin>>owed;
    for(i=0;i<n;i++)
    {
        
          t[i]=owed/cl[i];
          
          if(cl[i]<=count-j-1)
        {
          owed%=cl[i];
           t[i]=owed/cl[i]-cl[i];
        }
    
    }
    for(i=0;i<n;i++)
    {
        cout<<cl[i]<<"*"<<t[i]<<"="<<cl[i]*t[i]<<endl;
    }
}
