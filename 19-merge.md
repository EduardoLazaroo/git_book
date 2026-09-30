# Bloco 19 — Merge

## Objetivo

Aprender a unir o histórico e o código de uma branch de funcionalidade à branch principal utilizando o comando `git merge`.

## Conceito

O **Merge** (mesclar ou fundir) é a operação que traz as alterações desenvolvidas em um galho secundário para dentro da branch de destino.

```text
main:        ●───●───────────────────────● (merge commit)
                  \                     /
feature:           ●──────●────────────●
```

### Regra de Ouro do Merge: "Para onde eu quero levar o código?"

A dúvida número um de todo estudante iniciante é: *"Onde eu devo estar quando rodar o `git merge`?"*

Memorize a regra:
> **Você sempre se posiciona na branch que vai RECEBER o código.**

Se você quer levar o código da `feature/curiosidades` para dentro da `main`:
1. Primeiro você vai para a `main`: `git switch main`
2. Depois você puxa a feature para dentro dela: `git merge feature/curiosidades`

## Analogia

Pense em um afluente encontrando o rio principal. O rio Amazonas continua correndo em frente; o afluente deságua nele, misturando suas águas. Após a confluência, o rio principal agora carrega todas as águas trazidas pelo afluente.

## Na prática

Abra o terminal na pasta do projeto.

### Passo 1: Posicionar-se na branch de destino (`main`)

Antes de qualquer coisa, confirme que você está na `main`:

```bash
git switch main
```

Confira com `git branch` (o asterisco deve estar na `main`).

---

### Passo 2: Executar o merge

Agora execute a fusão trazendo a branch `feature/curiosidades`:

```bash
git merge feature/curiosidades
```

### O que o Git responde:

```text
Updating c4d5e6f..e8f9a0b
Fast-forward
 index.html | 17 +++++++++++++++++
 1 file changed, 17 insertions(+)
```

Observe a expressão **Fast-forward**:  
Como a `main` não havia recebido nenhum outro commit diferente enquanto você trabalhava na feature, o Git simplesmente "avançou a fita" da `main` até a ponta da feature de forma instantânea e limpa!

---

### Passo 3: Conferir o resultado no navegador

Abra o arquivo `index.html` no seu navegador e aperte `F5`.  
A seção de **Curiosidades do Mundo Git** agora faz parte oficialmente da versão principal do site!

Confira também o histórico no terminal:

```bash
git log --oneline
```

O commit feito na branch da feature agora faz parte da linha do tempo da `main`.

---

### Passo 4: Atualizar a nuvem (`git push`)

O merge foi feito localmente no seu computador. Para que o GitHub também receba essa novidade:

```bash
git push
```

---

### Passo 5: Limpeza de boas práticas (Deletar a branch concluída)

Uma vez que a funcionalidade foi mesclada com sucesso na `main`, a branch `feature/curiosidades` já cumpriu sua missão. É uma boa prática deletá-la para manter o repositório limpo:

```bash
git branch -d feature/curiosidades
```

---

## Verificação Rápida

Rode `git branch`.  
Você verá que apenas a branch `main` existe agora, mas todo o código da seção de curiosidades continua são e salvo dentro dela!

> Próximo passo: E quando duas pessoas mexem na mesma linha do mesmo arquivo ao mesmo tempo? Vamos perder o medo de conflitos no [Bloco 20 — Conflitos](20-conflitos.md).
