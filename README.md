# pizza-boy
Algo program


#include <iostream>
#include <math.h>
using namespace std;
//distance between function
float distance_between(int a[i],int a[j],int x)
{
    int k,m,n;
    float l;
    m=a[i];
    n=a[j];
    if(m=!n && (m=n-l || m=n+l || m=n-l*x || m=n+l*x)){
        return l;
    }
    else if(m=!n && (m=n-x*l-l || m=n+x*l-l || m=n-x*l+l || m=n+x*l+l)){
        return l*rt(2);
    }
    else if(m=!n && (m=n-x*2-1 || m=n+x*2-1 || m=n-x*2+1 || m=n+x*2+1 || m=n-x-2 || m=n+x-2 || m=n-x+2 || m=n+x+2)){
        return rt(5);
    }
    else if(m=!n && (m=n-x*3-1 || m=n+x*3-1 || m=n-x*3+1 || m=n+x*3+1 || m=n-x-3 || m=n+x-3 || m=n-x+3 || m=n+x+3)){
        return rt(10);
    }
    else(m=!n && (m=n-x*4-1 || m=n+x*4-1 || m=n-x*4+1 || m=n+x*4+1 || m=n-x-4 || m=n+x-4 || m=n-x+4 || m=n+x+4)){
        return rt(17);
    }
}

//main function
int main()
{
    int x,b,i,j,k,c[11],l,m,a[101],d,z,near[11],e[11];
    float o,dist[11],min;
    cout<<"Select A Number Between 3-8 For Making A Square Shaped Map Of An Area Where We Will Provide Our Service \n"<<endl;
    cin>>x;
    if(x>8||x<3){
    cout<<"your chosen number is either too less or too large for us to make a profitable square map for our pizza delivery service \n"<<endl;
    cout<<"Retry next time, this program will not provife proper solution";
    }
    else
    cout<<"we will provide our service on this map only\n"<<endl;
//mapping program
    for(i=0; i<100; i++){
        b=i+1;
        a[i]=b;
    }
    for(k=0; k<x; k++) {
        cout<<endl;
        l=x*k;
     for(i=0; i<x; i++) {
        cout<<" **** ";
     }
     cout<<endl;
     for(j=0; j<x; j++) {
        m=j+l;
        if(m<9)
        cout<<" | "<<a[j+l]<<"| ";
        else
        cout<<" |"<<a[j+l]<<"| ";
     }
     cout<<endl;
     for(i=0; i<x; i++) {
        cout<<" **** ";
     }
    }
    cout<<endl<<endl;
//source location on map at mid of the area
    if(x%2==0)
    z=x*(x/2)+x/2;
    else
    z=x*(x-1)/2+(x+1)/2;
    cout<<"our soirce of pizza delivery location is "<<z<<endl<<endl;
    for(j=0;j<x*x;j++){
        if(a[j]==z)
        z=j;
    }
    for(i=0; i<x; i++){
    cout<<"dear costumer ["<<i+1<<"] choose your location on this map"<<endl;
    cin>>c[i];
    }
    cout<<"(delivery locations of costumer)/(address for pizza delivery boy to deliver pizza)"<<endl;
    for(i=0; i<x; i++){
    cout<<"sector"<<c[i]<<endl<<endl;
    }
    for(j=0; j<x*x; j++){
       for(i=0;i<x;i++){
          if(a[j]==c[i])
          a[d]=c[i];
       }
    }
//distance between program
    for(j=0;j<x*x;j++)
    {
       for(i=0;i<x;i++){
           if(c[i]==a[j]){
             o=distance_between(a[d],a[z],x);
             cout<<"distance of sector "<<a[d]<<"from our delivery position sector "<<a[z]<<" is ="<<o<<" units"<<endl;
             dist[i]=o;
             near[j]=i;
           }
       }
    min = dist[0];
    for (i = 0; i < n; i++)
     {
      if (min > dist[i])
      min = dist[i];
     }
     if(min==dist[i])
     min=dist[near[j]];
     cout<<"nearest to sector "<<a[z]<<" is sector "<<a[j]<<" at distance "<<min<<endl;
    }
    a[e[0]]=a[j];
    for(f=0;f>x-1;f++){
     for(j=0;j<x*x;j++)
     {
       for(i=0;i<x;i++){
           if(c[i]==a[j] && c[i]!=a[e[f]]){
             o=distance_between(a[d],a[e[f]],x);
             cout<<"distance of sector "<<a[d]<<"from sector "<<a[e[f]]<<" is ="<<o<<" units"<<endl;
             dist[i]=o;
             near[j]=i;
           }
       }
     min = dist[0];
     for (i = 0; i < n; i++)
      {
       if (min > dist[i])
       min = dist[i];
      }
     if(min==dist[i])
     min=dist[near[j]];
     cout<<"nearest to sector "<<a[e[f]]<<" is sector "<<a[j]<<" at distance "<<min<<endl;
    }
    a[e[f+1]]=a[j];
    }
    return 0;
}
