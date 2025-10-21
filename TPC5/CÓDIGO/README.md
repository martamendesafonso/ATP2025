```python

aluno=("nome",id,["notaTPC", "notaProj", "notaTeste"])
turma=[aluno]

def criarTurma ():
    turma=[]
    return turma
    
def inserirAluno(turma):
    nome=input("Insira o nome do aluno")
    id_=int(input("Introduza o id do aluno"))
    notaTPC=float(input("Introduza a nota do TPC do aluno"))
    notaProj=float(input("Introduza a nota do projeto do aluno"))
    notaTeste=float(input("Introduza a nota do teste do aluno"))
    aluno=(nome,id,[notaTPC,notaProj,notaTeste])
    turma.append(aluno)

def listarTurma(turma):
    if not turma:
        print("A turma está vazia!")
        return 
    for aluno in turma:
        nome=aluno[0]
        id_=aluno[1]
        notas=aluno[2]
        print(f"{nome}, {id}, {notas[0]}, {notas[1]}, {notas[2]}")

def consultarAluno(turma):
    if not turma:
        print("A turma está vazia")
        return
    id_procurado=int(input("Introduza o id do aluno que quer procurar:"))
    for aluno in turma:
        if id_procurado==aluno[1]:
            nome,id_, notas=aluno
            print(f"{nome}, {id}, {notas[0]}, {notas[1]}, {notas[2]}")
            break

def guardarTurma(turma, fnome):
    with open(fnome, "w",encoding="utf-8") as f:
        for nome, id_, notas in turma:
            linha=f"{nome}::{id}::{notas[0]}::{notas[1]}::{notas[2]}\n"
            f.write(linha)
    print(f"Turma guardada em '{fnome}'")

def carregarTurma(fnome):
    turma=[]
    with open(fnome, "r",encoding="utf-8") as f:
        for linha in f:
            partes= linha.strip().split("::")
            if len(partes)!=5:
                continue
            nome=partes[0]
            id_=int(partes[1])
            notaTPC=float(partes[2])
            notaProj=float(partes[3])
            notaTeste=float(partes[4])
            aluno=("nome",id_,["notaTPC", "notaProj", "notaTeste"])
            turma.append(aluno)
    return(turma)





