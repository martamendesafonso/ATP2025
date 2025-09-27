```phyton
primeiro=input("Escolha se quer jogar primeiro: s ou n")
fósforos=21
while fósforos>0:
    if primeiro =="s":
        jogador=int(input("Introduza o número entre 1 e 4 que deseja subtrair:"))
        fósforos-=jogador
        print(f"Fósforos restantes:{fósforos}")
        if fósforos==0:
            print("Perdeu!")
            break

        if fósforos%5==0:
            computador=1
        else:
            computador=fósforos%5
        print(f"O computador tira {computador} fósforos")
        fósforos-=computador
        print(f"Fósforos restantes:{fósforos}")
        if fósforos==0:
            print("Ganhaste!")
            break
    else:
        if fósforos%5==0:
            computador=1
        else:
            computador=fósforos%5
        print(f"O computador tira {computador} fósforos")
        fósforos-=computador
        print(f"Fósforos restantes:{fósforos}")
        if fósforos==0:
            print("Ganhaste!")
            break
            
        jogador=int(input("Introduza o número entre 1 e 4 que deseja subtrair:"))
        fósforos-=jogador
        print(f"Fósforos restantes:{fósforos}")
        if fósforos==0:
            print("Perdeu!")
            break
    




