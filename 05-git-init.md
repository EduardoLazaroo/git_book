# Bloco 05 — git init

## Objetivo

Inicializar o Git na pasta do seu projeto, transformando-a em um repositório local e entendendo o papel crucial da pasta oculta `.git`.

## Conceito

Qualquer pasta no seu computador é apenas uma pasta comum até você rodar o comando `git init`.

Quando você executa esse comando:
1. O Git cria uma pasta oculta chamada `.git` dentro do seu diretório.
2. Essa pasta `.git` é o cérebro do repositório: ela guarda todo o histórico de versões, commits, configurações e ramificações.
3. **Regra de ouro**: Nunca edite, renomeie ou apague nada dentro da pasta `.git` manualmente! Deixe que apenas os comandos do Git mexam nela.

Se você deletar a pasta `.git`, a sua pasta volta a ser uma pasta comum e todo o histórico de versões é perdido.

## Analogia

Imagine que sua pasta é um diário em branco. O comando `git init` é como colocar um cadeado inteligente e abrir a primeira folha de registro na contracapa do diário. A partir deste segundo, todas as anotações futuras serão monitoradas.

## Na prática

Abra o terminal **dentro da pasta do seu projeto** (onde estão os arquivos `index.html` e `style.css`).

### Passo 1: Inicializar o repositório

Digite o comando:

```bash
git init
```

### O que o Git responde?

O terminal exibirá uma mensagem parecida com:

```text
Initialized empty Git repository in C:/.../github-academy/.git/
```

Pronto! Sua pasta comum agora é oficialmente um **Repositório Git Local**.

---

### Passo 2: Ver a pasta oculta `.git`

Por ser oculta, ela não aparece na listagem comum do Windows. Para provar que ela existe, digite no terminal:

No PowerShell / Git Bash:
```bash
ls -Force
```
*(ou `dir /a` no Prompt de Comando do Windows, ou `ls -la` no Git Bash)*

Você verá a pasta `.git` listada junto aos seus arquivos `index.html` e `style.css`.

---

### Passo 3: Fazer nossa primeira checagem com `git status`

Logo após inicializar, sempre chamamos o comando de status para ver como o Git enxerga nosso projeto:

```bash
git status
```

O Git responderá:

```text
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	index.html
	style.css

nothing added to commit but untracked files present (use "git add" to track)
```

Observe a expressão **"Untracked files"** (Arquivos não rastreados). O Git está dizendo: *"Ei, eu vi que esses dois arquivos existem aqui, mas você ainda não me pediu para rastrear o histórico deles!"*.

---

## Verificação Rápida

Responda mentalmente:
1. Se você quiser parar de usar Git em um projeto e deixá-lo como uma pasta comum, o que você faria? *(Bastaria apagar a pasta oculta `.git`).*
2. Você deve abrir a pasta `.git` no VS Code para editar arquivos de código? *(Não! Nunca mexemos manualmente lá dentro).*

> Próximo passo: Vamos dissecar em detalhes tudo o que o Git nos conta no [Bloco 06 — git status](06-git-status.md).
