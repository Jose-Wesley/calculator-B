# calculator-B
#É uma calculadora básica, ela nos ajuda a entender como funciona as expressões aritméticas in shell-cript

#!/bin/bash
###############FichaTécnica############ #                                     #
#                                     #
# Calculadora                         #
# By: jw #Shell                       #
# In: 17/12/17                        #
#                                     #
#                                     #
# Faz as devidas funcoes de uma       # # calculadora rudimentar, com suas    # # principais operacoes matematicas,   #
# nao liguem!!!                       #
#                                     #
#######################################

sleep 1

echo  "\033[1;36m =+=++=!!!CALCULADORA!!!+=+=+= \033[m"

sleep 1

echo

menu="\033[1;34m \n
 #1) Adicao \n
 #2) Subtracao \n
 #3) Multiplicacao  \n
 #4) Divisao \n
 #5) Exponenciacao \n
 \033[m "
 
echo  $menu


#Aqui inicia a parte das funcoes, ok!


adicao() {

echo "Digite o primeiro numero"
read num1

echo "Digite o segundo numero"
read num2

resultado=$(($num1+$num2))

echo  "\033[1;32m O resultado da soma eh $resultado \033[m"

} #funcao adicao terminada

subtracao() {

echo "Digite o primeiro numero"
read num1

echo "Digite o segundo numero"
read num2 

resultado=$(($num1-$num2))

echo  "\033[1;32m O resultado da subtracao eh $resultado \033[m"

}

#Funcao subtracao terminada

multiplicacao() {

echo "Digite o primeiro numero"
read num1

echo "Digitr o segundo numero"
read num2

resultado=$(($num1×$num2))

echo "\033[1;32m  O resultado da multiplicacao eh $resultado \033[m"

}

#A funcao multiplicacao termina aqui

divisao() {

echo "Digite o primeiro numero"
read num1

echo "Digite o segundo numero"
read num2

resultado=$(($num1/$num2))

echo  "\033[1;32m O resultado da divisao eh $resultado \033[m"

} #aqui acaba a funcao divisao

exponenciacao() {

echo "Digite o primeiro numero"
read num1
echo "Digite o segundo numero"
read num2

resultado=$(($num1**$num2))

echo  " \033[1;32m O resultado da exponenciacao eh $resultado \033[m "

} #Aqui acaba a funcao  exponenciacao


funcao_nada() {


while true [[$opc = $?]]

do

echo  "\n Voce  nao digitou nada"

echo " Digite uma opcao" 

menu="\033[1;34m \n
 #1) Adicao 
 #2) Subtracao 
 #3) Multiplicacao 
 #4) Divisao 
 #5) Exponenciacao
 \033[m "
 
echo "$menu"

read opc

case $opc in

1) adicao ;;
2) subtracao ;;
3) multiplicacao ;;
4) divisao ;;
5) exponenciacao ;;
*) echo "Voce nao dugitou nada" funcao_nada 

esac

done

} #aqui acaba a funcao_nada




#Aqui termina a parte das funcoes, ok!!




echo "O que voce quer fazer?"
read fazer

case $fazer in

1) adicao ;;
2) subtracao ;;
3) multiplicacao ;;
4) divisao ;;
5) exponenciacao ;;
*) echo "Voce nao digitou nada" ;j   funcao_nada 

esac

echo
echo "Godbye...."
echo "Obrigado por usar meu script"

#tenho que criar quatro funcao
