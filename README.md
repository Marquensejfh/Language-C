# Language-C
 a couple codes I made for college in C / Um conjunto de coisas que fiz para a faculdade em C

Estes projetos foram criados usando: - [Codeblocks](https://www.codeblocks.org)

# Codigo de media de 10 notas:

Bibliotecas:

#include<stdio.h>  
#include <stdlib.h> 


float media (int n, float *vnotas);   // Declaração da função que calcula a média

int main (void)
{
  float vnotas[10];           // Vetor para armazenar 10 notas
  
  float media_notas; 
  
  int i;                      // Variável de controle para o loop
  

  // Loop para ler as 10 notas do usuário
  
   for (i = 0; i < 10; i++){
  
    printf("Digite os valores das notas: ");
    scanf("%f", &vnotas[i]);
  }

  
  
  media_notas = media(10, vnotas); // Chama a função media para calcular a média das notas

  printf("\nMedia = %.1f \n", media_notas);

  system("pause"); // Pausa o sistema (usado em Windows para manter a janela aberta)
  
  return 0; // Retorna 0 indicando que o programa terminou com sucesso
}

// Função que calcula a média das notas

float media (int n, float *vnotas)
{
  int i; // Variável de controle para o loop
  
  float m = 0, soma = 0; // Variáveis para armazenar a soma das notas e a média

  // Loop para somar todas as notas
  
  for (i = 0; i < n; i++)
  
    soma = soma + vnotas[i];

  // Calcula a média
  
  m = soma / n;

  return m;// Retorna a média calculada
}


float media (int n, float *vnotas)

{
  int i;
  
  float m = 0, soma = 0;


  for (i = 0; i < n; i++)
  
    soma = soma + vnotas[i];


  m = soma / n;


  return m;
}


# Calcular Media dos valores dentro do Array

Enunciado:

1- Defina o array de números reais (float) com os seguintes valores: 5.5, 10.5, 15.5, 20.5. (feito)

2- Crie a função:   void calcularMedia(float *array, int tamanho, float *media).

Esta função recebe um array de números reais,  seu tamanho (que será 4 neste caso, porém deve ser utilizado o comando “sizeof(array) / sizeof(array[0]);”
para obter o tamanho de forma calculada), e um ponteiro para armazenar a média dos valores. Utilize ponteiros para percorrer o array e calcular a média
dos valores.

3-No programa principal, chame a função calcularMedia com o array definido e exiba a média calculada.


Codigo: 

#include <stdio.h>

#include <stdlib.h>


float array[] = {5.5, 10.5, 15.5, 20.5};

float x = 0;

int tamanho;


void calcularMedia(float *array, int tamanho, float *media){

int i = 0;

float soma = 0;

for (i = 0; i <  tamanho; i++) {

    soma=soma+array[i];
    }
    x = soma/tamanho;
    *media = x;


}

void main(){


tamanho = sizeof(array) / sizeof(array[0]);

calcularMedia();

printf("Media Calculada: %.2f \n",&x);

}














