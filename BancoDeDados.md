# 🌐 Desafio DIO - Configuração de Instância de Banco de Dados no Azure

Este repositório faz parte do **Desafio de Projeto da DIO**, cujo objetivo é praticar a configuração de uma instância de **Banco de Dados na plataforma Microsoft Azure** e documentar todo o processo de forma clara e estruturada.  

---

## 🎯 Objetivos de Aprendizagem
Ao concluir este desafio, você será capaz de:
- Aplicar os conceitos aprendidos em um ambiente prático;
- Documentar processos técnicos de forma organizada;
- Utilizar o GitHub como ferramenta para compartilhar documentação técnica.

---

## 📝 Conteúdo do Repositório
- `README.md` → Documentação principal com resumos e anotações.  
- `/images` (opcional) → Capturas de tela do processo no portal Azure.  
- Outros arquivos adicionais que servirem como apoio.  

---

## 🚀 Passo a Passo Resumido
### 1. Criar Recurso de Banco de Dados no Azure
1. Acesse o [Portal do Azure](https://portal.azure.com).  
2. Clique em **Criar um recurso** → **Banco de Dados SQL**.  
3. Preencha os detalhes básicos:  
   - Nome do servidor  
   - Usuário administrador  
   - Região e versão do SQL  
4. Configure autenticação e regras de firewall para acesso remoto.  
5. Revise e crie a instância.  

### 2. Conectar-se ao Banco de Dados
- Utilize **Azure Data Studio** ou **SQL Server Management Studio (SSMS)**.  
- Conecte usando o **nome do servidor**, **usuário administrador** e **senha** definidos.  

### 3. Criar Tabelas e Consultas
- Após conexão, você pode rodar comandos SQL como:  
```sql
CREATE DATABASE DIO_DB;
GO
USE DIO_DB;
CREATE TABLE Alunos (
    Id INT PRIMARY KEY IDENTITY,
    Nome NVARCHAR(100),
    Curso NVARCHAR(50),
    DataCadastro DATETIME DEFAULT GETDATE()
);

📁 dio-azure-database
 ┣ 📂 images
 ┃ ┗ 📜 screenshot1.png
 ┣ 📜 README.md
 ┗ 📜 dicas.md



👉 Esse modelo já atende os critérios do desafio (documentação clara, README detalhado, passo a passo e espaço para imagens).  


---

## Sugestões de Capturas de Tela

1. **01-criacao-recurso.png**  
   Tela inicial ao clicar em **Criar recurso → Banco de Dados SQL**.  

2. **02-detalhes-banco.png**  
   Formulário preenchido com **nome do banco, servidor, usuário administrador e região**.  

3. **03-configuracao-firewall.png**  
   Configuração das **regras de firewall** permitindo seu IP local.  

4. **04-revisao-e-criacao.png**  
   Tela de **revisão final** antes de clicar em **Criar**.  

5. **05-instancia-criada.png**  
   Confirmação da criação da instância e botão **Ir para o recurso**.  

6. **06-conexao-azure-data-studio.png**  
   Conexão ao banco de dados usando **Azure Data Studio** ou **SSMS**.  

---

## Dicas de Organização
- Nomeie os arquivos em **ordem numérica** para facilitar a leitura.  
- Use nomes **curtos e descritivos** (evite `Screenshot_001.png`).  
- No `README.md`, insira os prints quando explicar cada etapa:  

Exemplo:  
```markdown
### Criando o Banco de Dados
Na tela de criação do recurso, preencha as informações conforme mostrado abaixo:  

![Criação do Recurso](./images/01-criacao-recurso.png)




















