# Bloco 11 — Criando o GitHub

## Objetivo

Compreender o que é um repositório remoto, como funciona a sincronização entre o seu computador local e o GitHub, e criar seu primeiro repositório remoto na plataforma.

## Conceito

Até agora, todo o seu trabalho esteve trancado dentro do disco rígido do seu próprio computador (no **repositório local**). Se o seu computador quebrar hoje ou cair água no teclado, seu código se perde.

O **GitHub** resolve isso funcionando como um **repositório remoto**: uma cópia espelhada e segura do seu projeto hospedada em servidores em nuvem.

Além de backup em tempo real, o GitHub é a maior rede social de programadores do mundo: é onde recrutadores olham seu portfólio e onde você colabora com colegas de equipe no mesmo projeto.

## Analogia

O repositório local no seu computador é como o arquivo de texto salvo no pendrive de bolso.

O GitHub é o Google Drive ou Dropbox: uma pasta sincronizada na nuvem acessível de qualquer computador do mundo, compartilhável através de um link público.

## Na prática

Vamos criar o nosso repositório remoto no GitHub.

### Passo 1: Criar sua conta gratuita (se ainda não tiver)

1. Acesse: [github.com](https://github.com).
2. Clique em **Sign up** e siga o cadastro com seu melhor e-mail (use o mesmo e-mail configurado no Bloco 03).
3. Confirme o código de verificação recebido por e-mail e faça login.

---

### Passo 2: Criar um Novo Repositório no GitHub

1. No canto superior direito da tela inicial do GitHub, clique no ícone **`+`** e selecione **New repository** (ou acesse diretamente [github.com/new](https://github.com/new)).
2. Preencha os seguintes campos com atenção:
   - **Repository name**: digite exatamente `github-academy`.
   - **Description** (opcional): `Projeto prático desenvolvido no curso de Git e GitHub`.
   - **Public / Private**: Escolha **Public** (para que você possa exibir aos seus professores e futuros recrutadores).
   - ⚠️ **MUITO IMPORTANTE (A pegadinha dos iniciantes)**:
     - **NÃO** marque a opção *"Add a README file"*.
     - **NÃO** marque *"Add .gitignore"*.
     - **NÃO** escolha licença (*Choose a license*).
     - Deixe essas 3 caixas **desmarcadas**! Como já temos arquivos criados no nosso computador, queremos um repositório remoto completamente em branco.
3. Clique no botão verde **Create repository**.

---

### Passo 3: A tela de orientações do GitHub

Assim que você clica em *Create repository*, o GitHub exibe uma tela com links e comandos prontos.

Repare na URL do seu repositório no formato HTTPS:
```text
https://github.com/SEU-USUARIO/github-academy.git
```

Guarde essa URL! Ela é a ponte que conectará o seu computador à nuvem no próximo bloco.

---

## Verificação Rápida

Confira na página aberta do GitHub se o título do repositório exibe:  
`seu-usuario / github-academy` com o símbolo de cadeado aberto (Public). Se sim, sua garagem na nuvem está aberta e pronta para receber o código!

> Próximo passo: Vamos amarrar o seu computador ao GitHub no [Bloco 12 — git remote](12-git-remote.md).
