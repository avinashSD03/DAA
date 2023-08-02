#include <stdio.h>
#include<stdlib.h>
int N,c=0;
void swap(int *a,int *b)
{
    int t=*a;
    *a=*b;
    *b=t;
}
void heapify(int H[],int n){
    for(int i=n/2;i>=1;i--){
        int pi=i,pv=H[pi];
        int hp=0;
        while(!hp && 2*pi<=n){
            int ci=2*pi;
            if(ci<n){
                c++;
                if(H[ci+1]>H[ci]) ci=ci+1;
            }
            c++;
            if(pv>H[ci]) hp=1;
            else{
                H[pi]=H[ci];
                pi=ci;
            }
        }
        H[pi]=pv;
    }
}
void heapSort(int H[],int n){
    for(int i=1;i<=N;i++){
        swap(&H[1],&H[n]);
        n-=1;
        int pi=1,PV=H[1],heap=0;
        while(!heap && 2*pi<=n){
            int ci=2*pi;
            if(ci<n){
                c++;
                if(H[ci+1]>H[ci])
                    ci=ci+1;
            }
            c++;
            if(PV>H[ci])
                heap=1;
            else{
                H[pi]=H[ci];
                pi=ci;
            }
        }
        H[pi]=PV;
    }
}
void main() {
    N=1;
    while(N<10000){
        if(N<10000) N*=10;
        else N*=2;
        int a[N+1];
        int n=N;
        for(int i=1;i<=N;i++)
            a[i]=N-i+1;
        //best case
        c=0;
        n=N;
        heapify(a,n);
        heapSort(a,n);
        printf("N: %d\tC: %d\n",N,c);
        
        //worst case
        c=0;
        n=N;
        heapify(a,n);
        heapSort(a,n);
        printf("N: %d\tC: %d\n",N,c);
    }
}
