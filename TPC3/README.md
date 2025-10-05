import random
lista=[]
continuar=True
while continuar:
    print("MENU PRINCIPAL")
    print("*(1) Criar Lista")
    print("*(2) Ler Lista") 
    print("*(3) Soma")
    print("*(4) Média")
    print("*(5) Maior")
    print("*(6) Menor")
    print("*(7) estaOrdenada por ordem crescente")
    print("*(8) estaOrdenada por ordem decrescente")
    print("*(9) Procura um elemento")
    print("*(0) Sair")
    num=(int(input("Escolha o número da função que quer executar")))
    if num==0:
        print("Aplicação fechada")
        continuar=False
    elif num==1:
        N=10
        lista=[]
        while N>0:
            lista.append(random.randint(1,100))
            N=N-1
        print(lista)
    elif num==2:
        res=[]
        i=0
        N2=int(input("Quantos números quer introduzir na lista?"))
        while i<N2:
            num=int(input(f"Introduza o {i+1}º número"))
            res.append(num)
            i=i+1
        lista=res
        print(lista)
    elif num==3:
        res=0
        for N in lista:
            res=res+N
        print(res)
    elif num==4:
        res=0
        for N in lista:
            res=res+N
            media=res/len(lista)
        print(media)
    elif num==5:
        res=lista[0]
        for N in lista[1:]:
            if N>res:
                res=N
        print(res)
    elif num==6:
        res=lista[0]
        for N in lista[1:]:
            if N<res:
                res=N
        print(res)
    elif num==7:
        anterior=lista[0]
        ordenada=True
        for N in lista[1:]:
            if N<anterior:
                ordenada=False
            anterior=N
        if ordenada:
            print("Sim")
        else:
            print("Não")
    elif num==8:
        anterior=lista[0]
        ordenada=True
        for N in lista[1:]:
            if N>anterior:
                ordenada=False
            anterior=N
        if ordenada:
            print("Sim")
        else:
            print("Não")
    elif num==9:
        procurar=int(input("Introduza o número que quer procurar na lista"))
        i=0
        pos=-1
        for N in lista:
            if N==procurar and pos==-1:
                pos=i
            i=i+1
        print(pos)
