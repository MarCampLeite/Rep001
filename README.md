# Rep001

Programa "SobreTestePHD"

Sorteia três conjuntos de assuntos acadêmicos, tirados de quatro, com cinco itens cada, para teste de admissão de professor titular em universidade.

Autor: Mário Leite<br>
E-mail: marleite[at]gmail.com

<hr>

```c
#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <time.h>
int main() {
  int i, j;
  char *Assuntos[][5] = {
  //Assuntos de Matemática
  {"Topologia Algebrica","Teoria de Homotopia","Sistemas Dinamicos","Teoria de Aneis",
    "Trigonometria Transcendental"},
  //Assuntos de Física
  {"Relatividade Geral","Particulas Elementares","Teoria de Campo","Teoria das Cordas",
    "Mecanica Quantica"},
  //Assuntos de Português
  {"O Portugues do Brasil","Filologia Portuguesa","Latim Avancado","Lexico e Morfologia", 
   "Gramaticos Brasileiros"},
  //Assuntos de Informática
  {"Redes de Alta Velocidade","Sistema Distribuidos","Assembly III","IA em Jogos", 
   "Renderizacao em Tempo Real"}
  };
  srand(time(NULL));  //cria nova sequência de valores aleatórios
  for(i=1; i<=3; i++){
     printf("\nPonto composto por:\n");
     printf("%s, ", Assuntos[0][rand() % 5]);
     //Gera as três "cestas" de assuntos 
     for(j=1; j<=3; j++)
        printf("%s, ", Assuntos[j][rand() % 5]);
     printf("e %s\n\n", Assuntos[2][rand() % 7]);  
  }
  printf("\n");
  getch();
  return 0;
}
```
