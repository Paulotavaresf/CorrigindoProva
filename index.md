Algoritmo "CorrigindoProva"
Var
   gab: vetor[1..5] de caractere
   prova: vetor[1..5] de caractere
   nome:vetor[1..3] de caractere
   nota:vetor[1..3] de real
   a:inteiro
   s,m:real
Procedimento CadastroGabarito()
var
   c:inteiro
Inicio
     escreval("Passo 1 - Cadastro de Gabarito")
     escreval("------------------------------")
     Para c<- 1 ate 5 faca
          escreva("Questao ",c,": ")
          leia(gab[c])
     Fimpara
Fimprocedimento

Funcao cadastraprova():real
var
   c:inteiro
   notafinal:real
inicio
      notaFinal<-0
      escreval("RESPOSTAS DADAS")
      para c<-1 ate 5 faca
         escreva("Questao ",c,": ")
         leia(prova[c])
         se (maiusc(prova[c]) = maiusc(gab[c])) entao
           notaFinal <- notaFinal + 2
         Fimse
      FimPara
      retorne notaFinal
Fimfuncao
inicio
     CadastroGabarito()
     Para a <- 1 ate 3 faca
          Limpatela
          escreval("--------------------")
          escreval("ALUNO ",a)
          escreval("--------------------")
          escreva("Nome: ")
          leia(nome[a])
          nota[a]<-Cadastraprova()
          s<-s+nota[a]
     FimPara
     Limpatela
     escreval("NOTAS FINAIS")
     escreval("--------------------")
     para a <- 1 ate 3 faca
          escreval(nome[a]:10,nota[a]:4:1)
     fimpara
     m<-s/3
     escreval("--------------------")
     escreval("Media da Turma: ",M:4:1)
Fimalgoritmo