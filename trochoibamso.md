#include <stdio.h>
/*int TSLN(int a, int b){
	int s=0;
   
	if(a>b){
		return a;
	}else{
		return b;
	}
	return 0;
}*/

int main(){
    int s=0,a,b;
 FILE *f=NULL;
 f =fopen("input.txt","r");
 fscanf(f,"%d%d",&a,&b);
 fclose(f);
    
  if(a>b){
  	s+=a;
  	a-=1;
  }else{
  	s+=b;
  	b-=1;
  }
  if(a>b){
  	s+=a;
  }else{
  	s+=b;
  }
  f =fopen("output.txt","w");
  fprintf(f,"%d",s);
	
}
