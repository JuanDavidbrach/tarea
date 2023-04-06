#include<stdio.h>
int matriz1[10][10], f,c,f2,c2,matriz2[10][10],matriz[10][10]];
int main(){
    //Filas Matriz 1
    printf("ingrese el numero de filas de la matriz 1 :");
    scanf("%i",&f);
    // Columnas de matriz 1
	printf("Ingrese numero de columnas de la matriz 1: ");
	scanf("%i", &c);

    for(int i=0;i<f;i++){
        for(int j=0;j<c;j++){
            printf("Ingrese un numero en [%i] [%i]: \n",i+1,j+1);
			scanf("%i", &matriz1[i][j]);
        }
    }

    do{ //Ciclo repetitivo para asegurar que se cumpla la norma de la multiplicacion de matrices
   
    // Filas de matriz 2
	printf("\nIngrese el numero de filas de la matriz 2: ");
	scanf("%i",&f2);
	// Columnas de matriz 2
	printf("\nIngrese el numero de columnas de la matriz 2: ");
	scanf("%i",&c2);
    if(c != f2){
        printf("las columnas de la primera matriz deben coincidir con las filas de las segunda matriz para poder multiplicar");
    }
    }while(c != f2);

    for(int i=0; i<f2; i++){ //Llenando la matriz 2
		for(int j=0; j<c2; j++){
			printf("Ingrese un numero en [%i] [%i]: \n",i+1,j+1);
			scanf("%i",&matriz2[i][j]);
         }
     }
     //haciendo la matriz producto
     for(int i=0;i<f;i++){
        for(int j=0;j<c2;j++){
           for(int z=0;z<c;z++){
            matriz[i][j]=matriz[i][j]+matriz1[i][z]*matriz2[z][j];
           }
        }
     }
	printf("Matriz multiplicada:\n");

		for(int i=0; i<f; i++){ //Mostrando la matriz producto
		    for(int j=0; j<c2; j++){
			printf("[%i]",matriz[i][j]);
		}
		printf("\n");
	}

     
    volver 0;
}
