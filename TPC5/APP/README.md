```python
from tpc5 import(criarTurma, inserirAluno,listarTurma,consultarAluno,guardarTurma,carregarTurma)
def menu():
    turma = []
    while True:
        print("\nMenu:")
        print("1: Criar uma turma")
        print("2: Inserir um aluno na turma")
        print("3: Listar a turma")
        print("4: Consultar um aluno por id")
        print("5: Guardar a turma em ficheiro")
        print("6: Carregar uma turma dum ficheiro")
        print("0: Sair da aplicação")
        op = input("Opção: ").strip()

        if op=="1":
            turma=criarTurma()
        elif op=="2":
            inserirAluno(turma)
        elif op=="3":
            listarTurma(turma)
        elif op=="4":
            consultarAluno(turma)
        elif op=="5":
            fn=input("Nome do ficheiro:").strip()
            guardarTurma(turma,fn)
        elif op=="6":
            fn=input("Nome do ficheiro a carregar:").strip()
            turma=carregarTurma(fn)
            print("Turma carregada!")
        elif op=="0":
            print("Aplicação fechada")
            break
        else:
            print("Opção inválida")
if __name__=="__main__":
    menu()
