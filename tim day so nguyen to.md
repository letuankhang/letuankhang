#include <stdio.h>
#include <math.h>

int KTSNT(int n){
	int flag = 1;
	if(n<2){
	   flag =0;
	}
	for(int i=2;i<=sqrt(n);i++){
		if(n%i==0){
			flag=0;
			break;
		}
	}
	return flag;
}
int main(){
	int a,b,n,i;
	FILE*f=NULL;
	f =fopen("input.txt","r");
	fscanf(f,"%d%d",&a,&b);
    fclose(f);
//	scanf("%d",&a);
  //  scanf("%d",&b);
	//printf("%d",KTSNT(6));
	f =fopen("output.txt","w");
	
	for(i=a;i<=b;i++){
		if(KTSNT(i)){
			fprintf(f,"%3d",i);
		}
		
		
	}	
	fclose(f);
	return 0;
}
