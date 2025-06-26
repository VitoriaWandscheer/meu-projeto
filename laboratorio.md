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
## 5. Conectar o Repositório Local ao GitHub
### 5.1 Criar Token no GitHub
Acesse as configurações do usuário no Github;
No menu da esquerda, escolha a opção “< > Developer Settings”;
Em “Personal access tokens”, selecione a opção “Fine-grained tokens”;
Clique no botão "Generate new token";
### Exemplo:
![seleção da opção "Developer Settings"](assets/img-6.png)
![acesso a área "Fine-grained tokens" em “Personal access tokens”](assets/img-7.png)
Preencha os dados do projeto, sendo que é importante manter o "Expiration" como "No expiration".
Além disso, em "Repository Access" marque a opção "Only select repositories" e selecione o repositório desejado, neste caso é o "meu-projeto".
### Exemplo:
![seleção da opção "Developer Settings"](assets/img-8.png)
![acesso a área "Fine-grained tokens" em “Personal access tokens”](assets/img-9.png)
Em “Permissions”, “Repository permissions”, selecione a opção “access: Read and Write” na opção “Contents”.
![acesso a área "Fine-grained tokens" em “Personal access tokens”](assets/img-10.png)
Por fim, clique em “Generate Token”.
![acesso a área "Fine-grained tokens" em “Personal access tokens”](assets/img-11.png)
### 5.2 Conctar Repositório
Adicione o remoto:
```bash
git remote add origin https://github.com/seu-usuario/meu-projeto.git
```
Atenção: o passo 5.1 é essencial para realizar a autenticação, pois é necessário o Token de acesso para realizar qualquer comunicação com o Repositório Remoto.
Envie para o GitHub:
```bash
git push -u origin main
```
### Exemplo:
![seleção da opção "Developer Settings"](assets/img-12.png)
![acesso a área "Fine-grained tokens" em “Personal access tokens”](assets/img-13.png)
