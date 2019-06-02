
#20190524.ipynb
lst_n   = []
lst_s   = []
lst_tx  = []
  
while True:
  nome = input("qual o seu nome: ")
  if nome == "FIM" :
    break
   
  else: 
    lst_n.append(nome)
    salario = int(input ("informe  seu salario: "))  
    lst_s.append(salario)
  
    if salario <= 1000:
      tx = 0
      lst_tx.append(tx)
    
    elif 1000< salario and salario <= 3000:
      tx = (salario * 0.15)
      lst_tx.append(tx)
  
    else:
      tx = (salario * 0.20)
      lst_tx.append(tx)
       
    
print(lst_n, lst_s, lst_tx)

   
  
  

---------------------------------------------------------------------------

#20190517_1P.ipynb  graficos
#01
import numpy             as np  # gerador de dados
import matplotlib.pyplot as plt #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)
y = x**2

papel, caneta = plt.subplots()
caneta.plot(x,y)



#02
import numpy             as np  # gerador de dados
import matplotlib.pyplot as plt #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)
y = np.sin(x +(2 * np.pi * x))

papel, caneta = plt.subplots()
caneta.plot(x, y)



#03
import numpy             as np           # gerador de dados
import matplotlib.pyplot as plt          #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)        # geracao de dados (vetor)
y = np.cos ((np.pi / 6)+ (4 * np.pi * x))#implementar funcao

#plotagem do grafico
papel, caneta = plt.subplots ()          #criando os objetos para plotagem
caneta.plot(x, y)                        #plotando o grafico



#04
import numpy             as np           # gerador de dados
import matplotlib.pyplot as plt          #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)        # geracao de dados (vetor)
y = []                                   #implementar funcao
for  v in x:
  if v <= 1:
    y.append(1- v)
  if v > 1:
    y.append(v**2)
    
#plotagem do grafico
papel, caneta = plt.subplots ()          #criando os objetos para plotagem
caneta.plot(x, y)                        #plotando o grafico



#05
import numpy             as np           # gerador de dados
import matplotlib.pyplot as plt          #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)        # geracao de dados (vetor)
y = -(x-1)- (x+1)                                    #implementar funcao
    
#plotagem do grafico
papel, caneta = plt.subplots ()          #criando os objetos para plotagem
caneta.plot(x, y)                        #plotando o grafico



#06
import numpy             as np           # gerador de dados
import matplotlib.pyplot as plt          #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)        # geracao de dados (vetor)
y = -(x** 3 - 2.5 *x)                                   #implementar funcao
    
#plotagem do grafico
papel, caneta = plt.subplots ()          #criando os objetos para plotagem
caneta.plot(x, y)                        #plotando o grafico



#07 dever
import numpy             as np           # gerador de dados
import matplotlib.pyplot as plt          #plotagem do grafico

x = np.arange(-10.0, 10.0, 0.001)        # geracao de dados (vetor)
y = []                                   #implementar funcao
for v in x:
  if v <= -2:
    y.append(-2*v-1)
  if -2 <v and v < 1: 
    y.append (3)
  if 1 <= v:
    y.append (2*v+1)
#plotagem do grafico
papel, caneta = plt.subplots()          #criando os objetos para plotagem
caneta.plot(x, y)                        #plotando o grafico
plt.show


--------------------------------------------------------------------------

#aula/20190506.ipynb
lst = []
lst.append(1)
lst.append('joao')
print(lst)
print(len (lst))
lst.append('maria')
print(len(lst))
#   deletar um elemento
#del lst [0]
#print (lst)
#   atualizar posicao
lst [-1]= 'pedro'
print (lst)

#$###
copo = lst[-1]
#print(copo)
lst[-1]= "pedraooo"
lst.append(copo)
print (lst)


#import numpy as np
lst = list(np.arange(0.0,10,0.001))
#print(len(lst))
#print(lst)
for i in lst:
  print (i)
--------------------------------------------------------------------------
#aula/20190507.ipynb
#lst1, lst2 = [1,2,3,4,5,6],['a',1,'jose', 'livro,3.4']
lst1 = [1,2,3,4,5,6]
print ('valor maximo'max(lst1))
print ('valor minimo'min(lst1))

nome = "Jose Maria"
lst = list(nome.upper())
print (nome)
print (lst)
print ("Numoro de ocorrencias da letra A eh:", lst.count ('A'))

lst = list("maria")
lst_val = list (range(5))
print (lst_val)
print (lst)

lst_val.extend(lst)
print (lst_val)

#lst_val.remove("m")
#print(lst_val)
print (lst_val.index('m'))
-----------------------------------------------------------------------------
#20190514.ipynb
import matplotlib
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(-4.0, 4.0, 0.001)
y = 1 / (1+np.exp(-x))


fig, ax = plt.subplots()

ax.plot(x,y,'--b')
ax.grid()

import matplotlib
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(-4.0, 4.0, 0.001)
y = (np.exp(x)- np.exp(-x))/(np.exp(x) + np.exp(-x))

fig, ax = plt.subplots()

ax.plot(x,y,'--b')
ax.grid()
-----------------------------------------------------------------------------
def mensagem_ola():
  print ("ola mundo")
  print("tudo bem com voce?")
  
def avalia_idade():
  idade = int(input("qual a sua idade"))
  if idade >18:
    print ("voce tem mais que 18")
  else:
    print("voce nao tem mais que 18")
    
mensagem_ola()
avalia_idade()

import numpy as np
def f01(x):
  return ((-2*x)-1) 
print(f01(-1))

def f02(x):
  return (2*x)+1

def f00(x):
  if x<= -2:
    return f01(x)
  if -2 < x and x < 1:
    return 3
  if 1<= x:
    return f02(x)
    
x = np.arange(-10,10,0.001)
y =[]
for v in x:
  y.append(f00(v))

print(len(x))
print(len(x))
-----------------------------------------------------------------------------
#monte um laço que some os elementos de uma lista com 30 elementos contando em paços de dois (codigo e fluxo)
qtd = 0
for i in range (qtd,30,2): 
  qtd += i
print(qtd)

#monte uma lista com nomes informados pelo usuario.para parar p processo 
de inclusas dos nomes o usuario deve digitar a palavra "fim"
#depois deve ser impresso a relação dos nomes seguida com o tamanho(nmr 
de letras) de cada um deles (codigo e fluxo) 
lista = []
nome = ""

while nome.upper() != 'FIM':
  nome = input ("informe um nome: ")
  lista.append(nome)
  
print ('foram informados {} nome(s)' .format(len(lista)))
for n in lista:
  print ('nome informado {} com {} letra(s)' .format(n, len(n)))
print ("fim")

------------------------------------------------------------------------------
#exemplo 1
qtd = 10
for i in range (qtd,0,-1):  
    print (i)
print ("sai do loop")   
#exemplo 2
qtd = 10
while qtd != 0 :
  qtd -= 1  
  print (qtd) 
print ("sai do loop") 

# emeplo lista (numpy,scipt, matplotlib)
lst_a = []
lst_b = [1, 2, 3, 'casa', True, False, 1.25]
print (lst_b)
print (lst_b[3])

print (lst_b[len(lst_b)-1])
print (lst_b[-1])
------------------------------------------------------------------------------
#projeto1
def falar_ola (nome):
    print ("entrando na funcao falar_ola")
    print("ola",nome)
    print ("saindo da funcao falar_ola")
falar_ola ("tereza") 

idade = 12

if idade <20:
    print ('idade menor que 20')
    print ('blabla')
    nome = input ('qual o seu nome: ')
    if nome.upper()== "MARIA":
        falar_ola (nome)
else:
    print ('entao voce eh maio que 20')
print ("fim") 

#cenario 1
idade = int(input("qual a sua idade: "))
if idade > 18:
  print("você é maior de idade")
------------------------------------------------------------------------------

#cenario 2
idade = int(input("qual a sua idade: "))
if idade > 18:
  print("você é maior de idade")
else:
  print ("você tem menos de 18 anos")
#cenario 3
cdd = input ("Você mora em Guaxupé?(sim;nao) ")
if cdd == "sim":
  idade = int(input ("qual a sua idade? "))
  if idade > 18:
    print ("feliz morador de Guaxupé com mais de 18 anos.")
else:
  print ("Que pena, Guaxupé é uma cidade linda.")
  

#cenário 4 
cdd = input("Você mora em Guaxupé?(sim;nao) ")
if cdd     == "sim":
  idade = int(input ("qual a sua idade? "))
  if idade > 18:
    print  ("feliz morador de Guaxupé com mais de 18 anos.")
  else:
    print  ("Mais um infante morador de guaxupé")
elif cdd   == "nao":
  print    ("Que pena, Guaxupé é uma cidade linda.")
  mrd   = input ("voce tem interesse em de se mudar para Guaxupé? 
(sim;nao)")
  if mrd   == "sim":
    print  ("Que bom, será muito bem vindo a Guaxupé")
  elif mrd == "nao":
    print  ("OK, também fico feliz em sabem que és feliz onde moras")
# cenário 5
total = 0
while True:
  valor = int(input("informe valor: "))
  if valor == 0 :
    print ("total da soma {} ".format(total))
    break
  elif valor > 0 and valor < 10:
    total += valor # total = total + valor
  else:
    print ("valor informado esta incoreto, favor informar um valor 
valido. ")

#cenario 6
total = 0
lista = [] 
while True:
  valor = int(input("informe valor: "))
  if valor == 0 :
    print ("total da soma {}. numero de elementos {}, e lista de 
elementos {} ".format(total,len(lista),lista))
    break
  elif valor > 0 and valor < 10:
    total += valor # total = total + valor
    lista.append(valor)
  else:
    print ("valor informado esta incoreto, favor informar um valor 
valido. ")
------------------------------------------------------------------------------

valor     = int(input("Informe valor...: "))  
if valor <= 80: 
  print ("valor menor ou igual a 80")
  
else:
  print ("valor maior que 80")
print   ("fim")

val_inicio = int(input('informe valor de inicio......: ')) 
val_fim    = int(input('informe o valor de termino...: ')) 
operacao   = input    ('informe operacao a ser executada [A]dicao ou 
[S]ubtracao...: ')
passo      = int(input('informe valor do passo...: ')) 
  
  
while True:  
  if operacao == 'A':
    val_inicio = val_inicio + passo
    print (val_inicio)
    if val_inicio > val_fim:      
      print ("valor alem")  
      break
    
  elif operacao == 'S':
    val_inicio  = val_inicio - passo    
    print (val_inicio)   
    if val_inicio < val_fim:      
      print ("valor alem")
      break
      
  else:   
    print ('Operacao informada nao existe')
    break
    
 
  
  if val_inicio == val_fim:      
    print ("fim")
    break
------------------------------------------------------------------------------
#aula_20190308
#programa exemplo da aula
#variaveis globais (podem ir no começo)
soma_dentro = 0
soma_fora   = 0
qtd_passos  = 0

qtd_passos = int(input ("informe numero de passos "))

for v in range(qtd_passos):
  
  valor = int(input("informe o valor"))
  
  if valor in range(10,20):
    soma_dentro +=1
  else :
    soma_fora   += 1
print ("valor total de valores dentro da faixa foi de", soma_dentro)
print ("valor total de valores fora da faixa foi de ", soma_fora)
print ("grã finale")

#programa DEVER da aula

soma_dentro = 0

qtd_passos  = 0

qtd_passos = int(input ("informe numero de passos "))

for v in range(qtd_passos):
  
  valor = int(input("informe o valor"))
  
  if valor in range(10,20):
    soma_dentro +=1
  
print ("valor total de valores dentro da faixa foi de", soma_dentro)

#demorei pra raciocinar e fiquei putoquando descobri!
#apenas subtrairqtd_passos -  soma_dentro
print ("valor total de valores fora da faixa foi de ", qtd_passos -  
soma_dentro)
print ("grã finale")
------------------------------------------------------------------------------
#anotacoes
for v in range(5) :
  print (v)

#numeros quebrado poe float ex: 1.5

#numero inteiro poe int ex: 5

#selecao_de_uma_faixa(periodo)_de_numeros

if int (nome)in range (1,100):

#lista_de_nomes_barrados
if nome in ["exemplo1","exemplo2","exemplo3"]:
------------------------------------------------------------------------------
#Aula1oP_20190225.ipynb
a = 10
b = 20

if a>b :
  print ("a maior que b")
else:
  print ("a nao eh maior que b")
  
print (">-< fim da aplicacao")

while a < b:
  print (a)
  a += 1
print (">-< fim da aplicacao")
------------------------------------------------------------------------------
#Untitled1.ipynb
print ("Hello world")

nome  = input ("Qual o seu nome?")
idade = input ("Qual a sua idade?")

if int(idade) >= 18:
  print ("Voce é maior de idade,vamos continuar")
else:
  print ("Sinto muito mas voce nao tem idade o suficiente")
  
print ("Obrigado,é só isso!")
print (">-< fim")
------------------------------------------------------------------------------
#1P_Comp_20190222.ipynb
#print ("qual é a sua idade?")
idade = input ("qual é a sua idade?")
if int(idade) >= 18:
  nome = input (" qual o seu nome?")
  if nome =='felipe':
    print ("Deu mal")
  else:
    print(nome)
else:
  print ("deixa quieto")
  
print ("..fim.")
 
------------------------------------------------------------------------------

#Codigo da aula 2019-02-15
#Curso de Ciencias da Computacao 1o periodo de 2019

#cria uma variavel do tipo string
nome_da_gato = "dueo"

#cria as varias booleanas para os testes logicis
sera_que_pergunto = False
shipo = True

#Aqui vou testar minha coragem
if sera_que_pergunto:
  
  nome_da_gato = input("qual eh seu nome ")
  
  #aqui teste o clima
  if shipo:
      print(nome_da_gato)
  else:
    print("deu mal")

  
else:
  print("moio o encontro")
  
print("fim da aplicacao")
