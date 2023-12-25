#include<stdio.h>
int check(int s[], int n, int m){
    int fmin=s[0],smin=s[1],l;
     for(int i=2;i<n;i++){
        if(s[i]<fmin){
            smin=fmin;
            fmin=s[i];
        } 
        else if(s[i]<smin){
            smin=s[i];
        }}
    l=m-(fmin+smin);
    if(l>=0){
        return l;
    } 
    else{
        return m;
    }
}
int main()
{
    int n,s[n],m;
    printf("\nEnter the money:");
    scanf("%d",&m);
    printf("\nEnter the range:");
    scanf("%d",&n);
    printf("\nEnter the chocolate price:");
    for(int i=0;i<n;i++){
    scanf("%d",&s[i]);}
    int result = check(s,n,m);
    printf("%d\n",result);
    return 0;
}
