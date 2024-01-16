 lista2=[]
numericos2=[]
#DEFINE SE O VALOR É PAR
def func(n1):
  lista1=[]
  if n1 % 2 ==0 :
    t= f'{n1}: é par'
    #SALVA O VALOR NA LISTA1
    lista1.append(t)
 
#DFINE SE O VALOR É IMPAR
  if n1 %2 != 0:
    j= f'{n1}: é Impar'
    #SALVA O VALOR NA LISTA1
    lista1.append(j)

#DEFINE SE O VALOR É POSITIVO
  if n1 > 0:
    t=f'{n1}: é Positivo'
    #SALVA O VALOR NA LISTA1
    lista1.append(t)

#DEFINE SE O VALOR É NEGATIVO  
  if n1 < 0:
    h=f'{n1}: é Negativo'
    #SALVA O VALOR NA LISTA1
    lista1.append(h)
  #SALVA O VALOR NA LISTA2(GLOBAL)
  lista2.append(lista1)

def func_2():
  while True:
    n1=int(input('Digite Um Valor: '))#RECEBE O VALOR DIGITADO PELO O USUARIO
    numericos2.append(n1)#SALVA O VALOR DIGITADO NA LISTA NUMERICOS2(GLOBAL)
    func(n1)
    print(lista2)    
    resp=input('Quer Continuar?: ').lower().strip()#SE USUARIO DESEJA CONTINUAR
    match resp:
      case 's':
        continue
      case 'n':
        break
      case _:
        continue
func_2() 
print()
r=sum(numericos2)# sOMA DOS VALORES LISTA NUMERICOS2(GLOBAL)
print()
print('\033[32m========== Soma Dos Valores Digitados ==========\033[0m')
print()
if r %2 ==0 and r > 0:
  print(f'A Soma Do Valor: {r} é Um Valor Par e Positivo.')
if r %2 !=0 and r > 0:
  print(f'A Soma Do Valor: {r} é Um Valor Impar e Positivo.')
if r %2 ==0 and r < 0:
  print(f'A Soma Do Valor: {r} é Um Valor Par e Negativo.')
if r %2 !=0 and r < 0:
  print(f'A Soma Do Valor: {r} é Um Valor Impar e Negativo.')
