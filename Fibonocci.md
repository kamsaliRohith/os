
#include<stdio.h>
#include<iostream>
using namepsace std;
int main(){
#include<iostream>
#include<pthread.h>
#include <unistd.h>
#include<stdlib.h>
#include<sys/wait.h>
using namespace std;
	 int size,first=0,second=1,third,n;
	 int a[1000];
void * cal(void * arg)
{
  for(int i=0;i<n;i++)
  {
	  	first=a[i];
	  	third=first+second;
	  	first=second;
	  	second=third;
  }
}
int main(){  cout<<"enter number of elements"<<endl;
	  cin>>n;
      pthread_t fd;
      pthread_create(&fd,NULL,cal,NULL);
      pthread_join(fd,NULL);
      wait(1);
        for(int i=0;i<n;i++)
  {   //cout<<"in parent thread"<<endl;
	  	cout<<a[i]<<" ";
	  	
  }
	
}
//to be tested
}
