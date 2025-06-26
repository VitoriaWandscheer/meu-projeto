# Laboratório Prático - Git e Github
## 1. Configuração Inicial do Git
Antes de começar, configure seu nome e e-mail no Git:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@example.com"
```
### Exemplo:
![configuração do nome e email](assets/img-1.png)

## 2. Criar um Repositório Local
Crie uma pasta e entre nela:
```bash
mkdir meu-projeto
cd meu-projeto
```
Inicialize o repositório Git:
```bash
git init
```
### Exemplo:
![criação da pasta e git init](assets/img-2.png)
## 3. Adicionar Arquivos e Fazer Commit
Crie o README.md:
```bash
echo "# Meu Projeto" > README.md
```
Verifique o status:
```bash
git status
```
Adicione o arquivo ao stage:
```bash
git commit -m "Primeiro commit: adiciona README.md"
```
### Exemplo:
![criação do README e commit inicial](assets/img-3.png)
## 4. Criar um Repositório no GitHub
### 4.1 Vá até github.com
### 4.2 Clique em "New repository"
### 4.3 Preencha os dados:
Nome: meu-projeto
Visibilidade: Público
Não selecione nenhuma opção adicional (README, .gitignore etc.)
Depois de criar, copie a URL gerada.
### Exemplo:
![criação do repositório no GitHub](assets/img-4.png)
![criação do repositório no GitHub](assets/img-5.png)
