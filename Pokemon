#include<stdio.h>
#include<string.h>
#include<time.h>
#include<locale.h>

//Estrutura
struct pokemon {
    char nomepoke[50];
    int evolui;
    int evolucao;
    int numpok;
}pikachu;

//Função Principal
int main(){
setlocale(LC_ALL, "Portuguese");
int e,i,num, chave, r;
char resp;
FILE *TrabalhoPokemonB;
TrabalhoPokemonB = fopen("TrabalhoPokemonBin.txt", "wb");

	printf("Informe quantos Pokemons que gostaria de Cadastrar:");
	scanf("%d", &e);
struct pokemon vetor[e];
//Laço de Repetição
do {
	while (getchar() != '\n');
	for (i=0; i<e;i++) {
   		printf("Informe o Nome do Pokemon:", i+1);
		fgets(vetor[i].nomepoke,50,stdin);
    	strtok(vetor[i].nomepoke, "\n");
   		printf("Informe o Número do Pokémon na Pokedex: ", i+1);
		scanf("%d",&vetor[i].numpok);
		num = vetor[i].numpok;
   		printf("Informe se o Pokémon evoluiu (1-Sim/0-Não):", i+1);
		scanf("%d",&vetor[i].evolui);
		if (vetor[i].evolui==0) {
			printf("\nESSE POKéMON NÃO TEM EVOLUÇÃO!");
			getchar();
		}
		else {
			printf("Quantas evoluções o Pokémon tem?", i+1);
			scanf("%d",&vetor[i].evolucao);
			getchar();
			}
		printf("\n---------Saída de Dados---------\n");
	    if (vetor[i].evolui == 1) {
				 printf("\nIdentificador:%d\nPokémon:%s\nNúmero:#%d\nEvoluções:%d\n", i, vetor[i].nomepoke, vetor[i].numpok, vetor[i].evolucao);
				}
				 else {
			 		  printf("\nIdentificador:%d\nPokémon:%s\nNúmero:#%d\nEvoluções:Nenhuma.\n", i, vetor[i].nomepoke, vetor[i].numpok);
				 }
		}
     }while (resp == 's');
     printf("\nDeseja procurar os pokémons cadastrados (1-Sim/0-Não): ");
     scanf("%d",&r);
     if (r == 1) {
     	printf("\nDigite o identificador do pokémon que deseja encontrar:");
     	scanf("%d",&chave);
     	i = chave;
     	while (getchar()!= '\n'); 
    		if (chave == i) {
        	     printf("\nIdentificador:%d\nPokemon:%s\nNumero:#%d\nEvolucoes:%d\n", i, vetor[i].nomepoke, vetor[i].numpok, vetor[i].evolucao);
       		 }
          	   else{
               		 printf("POKEMON NAO ENCONTRADO!");
            	 }
     }
     	else {
     		printf("\nSem busca na Pokedex!\n")	;
     	}
		  fflush(stdin);
    	fwrite(&vetor[i], sizeof(vetor[i]), 1, TrabalhoPokemonB);
    	}
    	printf("\n--------------------------\n");
		printf("-----FIM DO PROGRAMA!-----\n");
		printf("\n--------------------------\n"); 
	return 0;
}
