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
![url do repositório no GitHub](assets/img-5.png)

## 5. Conectar o Repositório Local ao GitHub

### 5.1 Criar Token no GitHub
Acesse as configurações do usuário no Github;
No menu da esquerda, escolha a opção “< > Developer Settings”;
Em “Personal access tokens”, selecione a opção “Fine-grained tokens”;
Clique no botão "Generate new token";
### Exemplo:
![em "Developer Settings", acesso a área "Fine-grained tokens" em “Personal access tokens”](assets/img-6.png)
Preencha os dados do projeto, sendo que é importante manter o "Expiration" como "No expiration".
Além disso, em "Repository Access" marque a opção "Only select repositories" e selecione o repositório desejado, neste caso é o "meu-projeto".
### Exemplo:
![dados do projeto preenchidos no token](assets/img-7.png)  
!["Only select repositores" selecionado](assets/img-8.png)  
![repositorio "meu-projeto" selecionado](assets/img-9.png)

Em “Permissions”, “Repository permissions”, selecione a opção “access: Read and Write” na opção “Contents”.

![Access de "contents" definido como "Read and write"](assets/img-10.png)

Por fim, clique em “Generate Token”.

![token para o repositório "meu-projeto" gerado](assets/img-11.png)

### 5.2 Conctar Repositório
Caso a branch seja "master" renomeie para "main":
```bash
git branch -m master main
```
Adicione o remoto:
```bash
git remote add origin https://github.com/seu-usuario/meu-projeto.git
```
Atenção: o passo 5.1 é essencial para realizar a autenticação, pois é necessário o Token de acesso para realizar qualquer comunicação com o Repositório Remoto.
Envie para o GitHub:
```bash
git push -u origin main
```
Neste momento você será direcionado para fazer login. Selecione a opção "token" e cole o "token" gerado no passo 5.1.
### Exemplo:
![renomeia branch para "main"](assets/img-12.png)  
![início da conexão com repositório remoto](assets/img-13.png)  
![tela de Sign in](assets/img-14.png)  
![tela de Sign in com token](assets/img-15.png)  
![processo de conexão completo](assets/img-16.png)  

## 6. Criar e Trabalhar em uma Nova Branch
Crie a nova branch:
```bash
git checkout -b feature/nova-funcionalidade
```
Crie o arquivo de funcionalidade:
```bash
echo "Nova funcionalidade em desenvolvimento" > nova-funcionalidade.txt
```
Adicione e comnit:
```bash
git add nova-funcionalidade.txt
git commit -m "Adiciona nova funcionalidade"
```
Envie a branch:
```bash
git push -u origin feature/nova-funcionalidade
```
### Exemplo:
![criação da branch, novo arquivo, commit e push](assets/img-17.png)

## 7. Fazer Merge da Branch na Main
Volte para main:
```bash
git checkout main
```
Atualize a main:
```bash
git pull origin main
```
Mescle:
```bash
git merge feature/nova-funcionalidade
```
Envie:
```bash
git push origin main
```
### Exemplo:
![git merge + push final](assets/img-18.png)

## 8. Conteúdo extra: criação deste tutorial
Crie e adicione um texto qualquer ao arquivo do tutorial:
```bash
echo "Laboratorio Prático - Git e Github" > laboratorio.md
```
Utilizando o editor de texto que preferir, escreva o conteúdo do tutorial utilizando a linguagem Markdown.
Crie a pasta assets e adicione os prints capturados.
Adicione os arquivos ao stage:
```bash
git add assets
git add laboratorio.md
```
Faça o commit com uma mensagem descritiva:
```bash
git commit -m "Adiciona tutorial em Markdown com imagens do processo"
```
Envie para o repositório remoto:
```bash
git push origin main
```
### Exemplo:
![criação do documento "laboratorio.md"](assets/img-19.png)
![Visual Studio Code com folder "meu-projeto" aberto](assets/img-22.png)
![Adiciona pasta assets ao git](assets/img-20.png)
![Adição dos arquivos ao git e push final](assets/img-21.png)
