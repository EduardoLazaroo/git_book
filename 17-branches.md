# Bloco 17 — Branches

## Objetivo

Compreender o conceito de **branches** (ramificações), aprender a listar, criar e alternar entre branches usando os comandos modernos `git branch` e `git switch`.

## Conceito

Até aqui, trabalhamos o tempo todo em uma única linha reta chamada `main`. Em projetos reais e empresas sérias, **quase ninguém programa diretamente na `main`**!

Por que? Porque a `main` é a linha de produção estável: é o código que os clientes reais estão usando no site. Se você cometer um erro de digitação na `main`, o site oficial sai do ar.

Uma **branch** é uma linha do tempo paralela e independente. Nela, você pode:
- Experimentar ideias loucas.
- Criar novas telas e funcionalidades (*feature branches*).
- Quebrar e consertar o código sem afetar em nada a branch `main`.

Se der tudo certo, você une a branch à `main` mais tarde (com o *merge*). Se der tudo errado, você simplesmente descarta a branch sem qualquer prejuízo ao projeto principal.

### Comandos Modernos vs Comandos Antigos

O Git atualizou seus comandos para ficarem mais intuitivos:
- Modo moderno (recomendado): `git switch <nome-da-branch>` (serve exclusivamente para trocar de galho).
- Modo antigo (ainda muito visto em tutoriais na internet): `git checkout <nome-da-branch>`.

## Analogia

Imagine uma árvore genealógica ou o multiverso dos filmes:
A `main` é o universo principal. Criar uma branch é abrir um portal para uma dimensão paralela: você pode transformar o céu em verde e os carros em barcos. Nada disso afeta as pessoas no universo principal até que você decida fundir as realidades.

## Na prática

Abra seu terminal na pasta do projeto.

### Passo 1: Listar as branches existentes

Digite o comando:

```bash
git branch
```

**Resultado:**
```text
* main
```
O asterisco verde `*` indica em qual branch você está com a cabeça (*HEAD*) apontada no momento.

---

### Passo 2: Criar uma nova branch

Vamos criar uma branch para desenvolver uma funcionalidade de teste:

```bash
git branch teste-ideias
```

Agora liste as branches novamente:

```bash
git branch
```

**Resultado:**
```text
* main
  teste-ideias
```
Agora temos duas branches! Porém, repare que o asterisco `*` continua na `main`. Apenas criamos o novo caminho, mas ainda não entramos nele.

---

### Passo 3: Mudar para a nova branch (`git switch`)

Para entrar na branch recém-criada, use:

```bash
git switch teste-ideias
```

**O que o Git responde:**
```text
Switched to branch 'teste-ideias'
```

Rode `git branch` novamente:
```text
  main
* teste-ideias
```
Agora a sua cabeça de trabalho está no universo paralelo `teste-ideias`!

---

### Passo 4: O atalho que todo desenvolvedor usa no dia a dia

Existe um atalho incrível para **criar e já entrar** na nova branch com um único comando usando a flag `-c` (de *create*):

```bash
git switch -c feature/nova-secao
```

O Git criará a branch `feature/nova-secao` e já mudará você para ela imediatamente!

---

### Passo 5: Voltando para a `main` e deletando a branch de teste

Para voltar para a branch principal:

```bash
git switch main
```

E para apagar a branch `teste-ideias` que criamos apenas para treino:

```bash
git branch -d teste-ideias
```
*(O parâmetro `-d` significa **delete**).*

---

## Verificação Rápida

Rode `git branch`.  
Você deve ver a branch `main` com o asterisco `*` e a branch `feature/nova-secao` na lista. Se sim, o conceito de mundos paralelos está dominado!

> Próximo passo: Vamos construir uma funcionalidade real em uma branch no [Bloco 18 — Criando uma funcionalidade em uma branch](18-criando-uma-funcionalidade-em-uma-branch.md).
