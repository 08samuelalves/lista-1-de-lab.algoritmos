# lista-1-de-lab.algoritmos
Lista 1
Listas de Lab. De Algoritmos lista-1, ponteiros
//QUESTÃO-1//
X= 3;Y=4;P=4;
//QUESTÃO-2//
A) classificado como erro.
B) Por ausência do & no X, para armazenar o endereço de P, portanto deu 
erro.
C) Não foi sucedida por estar faltando o &.
D) #include<stdio.h> 
int main(void) {
int x, *p; x = 100; p = &x;
printf("Valor de p = %p\t Valor de *p = %d", p, *p);
return 0;
}
E) Sim, pois foi adicionado &.
//QUESTÃO-3//
Resposta dada pelo programa é 30;20;10.
//QUESTÃO-4//
#include<stdio.h>// declaração das blibliotecas//
#include<locale.h>
#include<math.h> 
void calcula__hexagono (float l, float *area, float *perimetro);
int main(void){ 
float lado, area, perimetro; 
setlocale(LC_ALL, "Portuguese"); 
printf("Universidade Federal Rural do Semi-Árido\n "); 
printf("disciplina: PEX1243 \n"); 
printf("Aluno: Samuel A. da Cruz"); 
printf("\n\n");
printf("Digite um lado do hexágono: "); //faz solicitação ao usuário dos lados do 
hexágono//
scanf("%f", &lado); 
calcula_hexagono(lado&area, &perimetro); //nessa linha ocorre a chamada da 
função principal no int main//
printf("A area do hexágono=%.2f\nO perimetro=%.2f\nO lado=%.2f
",area,perimetro, lado ); //nessa linha ocorre a exibição do cálculo dos 
lados que foram colocados na função//
return 0; }
void calcula_hexagono(float l, float *area, float *perimetro){ //função que faz o 
cálculo do perímetro e do hexágono//
*area=(3*pow(l,2)*sqrt(3))/2; 
*perimetro=6*l; 
}
//QUESTÃO-5//
#include<stdio.h>// declaração das bibliotecas//
#include<stdlib.h>
#include<locale.h>
#include<math.h>
char situação_aluno(float p1, float p2, float p3, int faltas, int aulas, float 
*media); 
//essa linha é declarado o prottipo da função//
int main(void){
setlocale(LC_ALL, "Portuguese");
float p1, p2, p3, media;
int faltas,aulas;
printf("Universidade Federal Rural do Semi-Árido\n "); 
printf("Diciplina: PEX1243 \n");
printf("Aluna: Samuel A. da Cruz");
printf("\n\n");
printf("Digite a primeira nota: "); //faz a solicitação das notas//
scanf("%f", &p1);
printf("Digite a segunda nota: "); //faz a solicitação das notas//
scanf("%f", &p2); 
printf("Digite a terceira nota: "); //faz a solicitação das notas//
scanf("%f", &p3); 
printf("Digite o total de faltas: "); //faz a solicitação das faltas//
scanf("%d", &faltas); 
printf("Digite o total de aulas: "); //faz a solicitação das aulas//
scanf("%d", &aulas);
char s = situacao(p1, p2, p3, faltas, aulas, &media); // faz a chamada da 
função principal no int main//
printf("Nota 1,2,3=%.2f%.2f.2f\nTotal de aulas=%d\nTotal de 
faltas=%d\nMédia=%.2f", p1,p2,p3,aulas,faltas,media); //nessa linha ocorre a
exibição da media, das falta, das aulas e também da notas//
return(0);}
char situacao(float p1, float p2, float p3, int faltas, int aulas, float *media){ 
//fução que calcula a media 
*media=(p1+p2+p3)/3; 
a=(100*faltas/aulas); 
//nessa linha faz o cálculo das faltas//
if(a<=25 && *media>=6){
//tem por função verificar se a média é >= 6 e exibe caso a afirmação seja 
verdadeira return 'A';
}
else if(a<=25 && *media<6){ 
//verifica se a media é < que 6 e exibe caso a afirmação seja verdadeira 
return'R';
} 
else { // caso nenhuma das afirmações acima seja verdadeira exibe esta return
'F'; }
