<h1 align=center>GitHub - Guia de Utilização</h1>
<div align=center>
  <img width="720" height="352" alt="git" src="https://github.com/user-attachments/assets/09ebe036-0126-455f-88e2-4b853132c7de" />
</div>
<div align=center>
  Versão: Julho/2024 - 73710
</div>

## 📌 Introdução

Este passo a passo é destinado ao desenvolvimento em **Linux** e apresenta os principais comandos para autenticação, criação de repositórios e gerenciamento de branches no Git e GitHub.

---

# 🔐 Autenticação no GitHub

Execute:

```bash
gh auth login
```

Este comando faz a autenticação da sua conta no GitHub.

Você pode utilizar:

- HTTPS
- SSH

Basta seguir as instruções exibidas na tela. Será gerado um código e um link para confirmar sua identidade no GitHub. Após a confirmação, você poderá utilizar o Git normalmente em seu sistema.

## Exemplo

```text
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations on this host? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: 116D-2U92
Press Enter to open github.com in your browser...

xdg-open: no method available for opening 'https://github.com/login/device'

✓ Logged in as "USUARIO_GITHUB"
```

---

# 🚀 Criando um Projeto Remoto

Crie uma pasta para o projeto e entre nela.

## Inicializando o repositório

```bash
git init
```

Inicializa um novo repositório Git dentro da pasta do projeto.

---

## Criando o README

```bash
touch README.md
```

Cria o arquivo README.


---

## Adicionando arquivos

```bash
git add README.md
```

Adiciona o arquivo à área de preparação (staging).

Para adicionar todos os arquivos da pasta atual:

```bash
git add .
```

---

## Verificando alterações

```bash
git status
```

Mostra os arquivos modificados e o que será enviado no próximo commit.

---

## Criando um commit

```bash
git commit -m "Mensagem de versionamento"
```

Registra as alterações realizadas no projeto.

---

## Desfazendo alterações

```bash
git restore ARQUIVO_OU_PASTA
```

Cancela alterações em arquivos ou pastas antes do commit.

---

## Renomeando a branch principal

```bash
git branch -M main
```

Renomeia a branch atual para `main`.

---

## Criando o repositório no GitHub

Crie um repositório com o mesmo nome da pasta do projeto.

Em seguida, associe o repositório local ao remoto:

```bash
git remote add origin https://repositorioCriado.git
```

---

## Enviando o projeto para o GitHub

```bash
git push -u origin main
```

Envia os commits locais para o repositório remoto.

---

# 🌿 Trabalhando com Branches

## O que é uma branch?

Uma branch é uma cópia do projeto principal. Ela permite desenvolver novas funcionalidades sem alterar o código estável.

Após os testes e validações, as alterações podem ser incorporadas ao código principal.

---

## Criando uma nova branch

```bash
git checkout -b nome-da-branch
```

Cria uma nova branch e muda para ela automaticamente.

Exemplo:

```bash
git checkout -b feature/login
```

---

## Verificando a branch atual

```bash
git branch
```

Mostra todas as branches e destaca a branch atual.

---

## Mudando para outra branch

```bash
git checkout nome-da-branch
```

Exemplo:

```bash
git checkout feature/login
```

---

## Enviando uma branch para o GitHub

```bash
git push -u origin nome-da-branch
```

Este comando deve ser executado sempre que uma nova branch for criada.

---

## Mesclando alterações com a branch principal

Volte para a branch principal:

```bash
git checkout main
```

Faça a junção das alterações:

```bash
git merge nome-da-branch
```

Assim, as mudanças desenvolvidas na branch secundária serão incorporadas ao código principal.

---

## Atualizando o GitHub com as alterações

```bash
git push origin main
```

Envia as atualizações da branch principal para o repositório remoto.

---

# 📚 Principais Comandos

| Comando | Descrição |
|-----------|-----------|
| `gh auth login` | Autentica no GitHub |
| `git init` | Inicializa um repositório |
| `git add .` | Adiciona todos os arquivos |
| `git status` | Mostra o estado do projeto |
| `git commit -m "mensagem"` | Cria um commit |
| `git restore arquivo` | Desfaz alterações |
| `git branch -M main` | Renomeia a branch para main |
| `git remote add origin URL` | Vincula ao repositório remoto |
| `git push -u origin main` | Envia para o GitHub |
| `git checkout -b branch` | Cria uma nova branch |
| `git checkout branch` | Alterna entre branches |
| `git merge branch` | Junta alterações de outra branch |
| `git push origin main` | Atualiza o repositório remoto |

---

## ✅ Fluxo Básico

```text
Criar pasta
    ↓
git init
    ↓
Criar arquivos
    ↓
git add .
    ↓
git commit -m "Descrição"
    ↓
git push origin main
```

---

**Autor:** 73710  
**Versão:** Julho/2024
