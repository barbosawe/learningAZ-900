# 🚀 Desafio de Projeto - DIO

Este repositório foi criado para a entrega do **Desafio de Projeto da DIO**.  
O objetivo é demonstrar os conceitos aprendidos até aqui, organizar o material e publicar no GitHub como parte do meu portfólio.

---

## 📌 Estrutura do Projeto

- `README.md` → Documentação do projeto e instruções.  
- `src/` → Diretório com os arquivos de código ou scripts.  
- `assets/` → Imagens, diagramas ou documentos de apoio.  
- `projeto.sql` → Arquivo de banco de dados (se aplicável).  

---

## 📖 Passo a Passo Realizado

1. Criei um repositório público no **GitHub**.  
2. Estruturei o projeto com pastas organizadas (`src`, `assets`).  
3. Documentei todo o processo neste `README.md`.  
4. Adicionei links úteis e referências.  
5. Fiz o versionamento e publiquei no GitHub.  

---

## 🔗 Links Úteis

- [Digital Innovation One (DIO)](https://www.dio.me/)  
- [Como Entregar Seu Desafio de Projeto - DIO](https://web.dio.me/course/como-entregar-o-seu-desafio-de-projeto/learning/25f5ac52-9c7e-47b6-9f63-3dbb02a3a482)  
- [Guia Básico de Markdown](https://www.markdownguide.org/basic-syntax/)  
- [Documentação Git](https://git-scm.com/doc)  
- [Documentação GitHub](https://docs.github.com/pt)  

---

## 💡 Como Executar (se tiver código)

```bash
# Clone este repositório
git clone https://github.com/SEU-USUARIO/meu-desafio-dio.git

# Entre na pasta
cd meu-desafio-dio

# Execute o arquivo (se houver)
python src/app.py
---


import json
import os

# Arquivo onde as tarefas serão armazenadas
ARQUIVO = "tarefas.json"

# Função para carregar tarefas existentes
def carregar_tarefas():
    if os.path.exists(ARQUIVO):
        with open(ARQUIVO, "r", encoding="utf-8") as f:
            return json.load(f)
    return []

# Função para salvar tarefas
def salvar_tarefas(tarefas):
    with open(ARQUIVO, "w", encoding="utf-8") as f:
        json.dump(tarefas, f, indent=4, ensure_ascii=False)

# Função para listar tarefas
def listar_tarefas(tarefas):
    if not tarefas:
        print("\n Nenhuma tarefa cadastrada.\n")
    else:
        print("\n Lista de Tarefas:")
        for i, tarefa in enumerate(tarefas, start=1):
            print(f"{i}. {tarefa}")
        print()

# Função para adicionar nova tarefa
def adicionar_tarefa(tarefas):
    nova = input("Digite a nova tarefa: ")
    tarefas.append(nova)
    salvar_tarefas(tarefas)
    print(" Tarefa adicionada com sucesso!\n")

# Função para remover tarefa
def remover_tarefa(tarefas):
    listar_tarefas(tarefas)
    try:
        indice = int(input("Digite o número da tarefa a remover: "))
        if 1 <= indice <= len(tarefas):
            removida = tarefas.pop(indice - 1)
            salvar_tarefas(tarefas)
            print(f" Tarefa '{removida}' removida.\n")
        else:
            print(" Número inválido.\n")
    except ValueError:
        print(" Entrada inválida.\n")

# Menu principal
def main():
    tarefas = carregar_tarefas()

    while True:
        print("=== Gerenciador de Tarefas ===")
        print("1. Listar tarefas")
        print("2. Adicionar tarefa")
        print("3. Remover tarefa")
        print("4. Sair")
        
        opcao = input("Escolha uma opção: ")

        if opcao == "1":
            listar_tarefas(tarefas)
        elif opcao == "2":
            adicionar_tarefa(tarefas)
        elif opcao == "3":
            remover_tarefa(tarefas)
        elif opcao == "4":
            print(" Saindo... Até logo!")
            break
        else:
            print(" Opção inválida.\n")

if __name__ == "__main__":
    main()

