# calculadora-de-matriz
# include <stdio.h>
# include<stdlib.h>
# include <time.h>
# include <windows.h>
int mat1[3][3]={};
int mat2[3][3]={};
int mar[3][3]={};
int r,c,j,i,m;
int ik;
void imprimemat1();
void imprimemat2();
void imprimemar();
int main(){
	int ip;
	do{
	printf("Opciones \n");
	printf("1)Asigna valores a las matriz 1\n");
	printf("2)Asigna valores a las matriz 2\n");
	printf("3)Multiplicar \n");
	printf("4)Suma\n");
	printf("5)Resta Matriz1-Matriz2 \n");
	printf("6)Resta Matriz2-Matriz1 \n");
	printf("7)Salir\n");
	scanf("%d",&ip);
	switch(ip){
		case 1 :
		system("cls");	
		printf("Asigna valores a las matriz 1\n");
		m=0;
			while(m<9){
		         for(r=0;r<3;r++){   
	               for(c=0;c<3;c++){
	  	              printf(" mat1 \n");
	  	              for(i=0;i<3;i++){
		                 for(j=0;j<3;j++){
		                 printf(" %d",mat1[i][j]);
			             }
		                 printf("\n");
			            }
		             scanf("%d",&mat1[r][c]);
	  	             m++;
	  	             system("cls");
		 	        }	
                }        
            }
		imprimemat1();
		break;
		case 2 :
		system("cls");	
		printf("Asigna valores a las matriz 2\n");
		m=0;
		while(m<9){
		         for(r=0;r<3;r++){   
	               for(c=0;c<3;c++){
	  	              printf(" mat2 \n");
	  	              for(i=0;i<3;i++){
		                 for(j=0;j<3;j++){
		                 printf(" %d",mat2[i][j]);
			             }
		                 printf("\n");
			            }
		             scanf("%d",&mat2[r][c]);
	  	             m++;
	  	             system("cls");
		 	        }	
                }        
            }
        imprimemat2();
		break;
		case 3 :
		system("cls");	
		printf("Multiplicar\n");
		 for(r=0;r<3;r++){ 
	        for(c=0;c<3;c++){
	  	    ik=mat1[r][c]*mat2[r][c];
	  	     mar[r][c]=ik;}
         }
         
         imprimemat1();
         imprimemat2();
         imprimemar();
		break;	
		case 4 :
		system("cls");	
		printf("Suma\n");
		for(r=0;r<3;r++){ 
	        for(c=0;c<3;c++){
	  	    ik=mat1[r][c]+mat2[r][c];
	  	     mar[r][c]=ik;}
         }
         
         imprimemat1();
         imprimemat2();
         imprimemar();
		break;	
		case 5 :
		printf("resta\n");
		for(r=0;r<3;r++){ 
	        for(c=0;c<3;c++){
	  	    ik=mat1[r][c]-mat2[r][c];
	  	     mar[r][c]=ik;}
         }
         system("cls");
         imprimemat1();
         imprimemat2();
         imprimemar();
		break;	
		case 6 :
		printf("resta\n");
		for(r=0;r<3;r++){ 
	        for(c=0;c<3;c++){
	  	    ik=mat2[r][c]-mat1[r][c];
	  	     mar[r][c]=ik;}
         }
         system("cls");
         imprimemat1();
         imprimemat2();
         imprimemar();
		break;	
		case 7 :
		printf("Salir\n");
		break;
		default:
		printf("Ese numero no es opcion\n");
	}	
		
	}
	while(ip 	!=7);
	
return 0;	
}


void imprimemat1(){
printf("matriz 1\n");
printf("\n");
       for(r=0;r<3;r++){
		    for(c=0;c<3;c++){
		     printf(" %d",mat1[r][c]);}
		     printf("\n");}
printf("\n");
	
}


void imprimemat2(){
printf("matriz 2\n");
printf("\n");
       for(r=0;r<3;r++){
		    for(c=0;c<3;c++){
		     printf(" %d",mat2[r][c]);}
		     printf("\n");}
printf("\n");	
}


void imprimemar(){
printf("matriz 3\n");	
printf("\n");
 
for(r=0;r<3;r++){
for(c=0;c<3;c++){
printf(" %d",mar[r][c]);}
printf("\n");}
printf("\n");	
}
