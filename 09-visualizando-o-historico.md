# Bloco 09 — Visualizando o histórico

## Objetivo

Aprender a consultar a linha do tempo do projeto através dos comandos `git log` e `git log --oneline`, entendendo o que é o Hash SHA e como navegar pelo histórico.

## Conceito

O comando `git log` é o explorador do tempo do Git. Ele lista todos os commits já realizados em ordem cronológica inversa (do mais recente para o mais antigo).

Em cada entrada do histórico, você enxerga:
1. **O Commit Hash**: Uma sequência criptográfica única gerada por um algoritmo matemático (SHA-1). É a impressão digital daquele momento. Dois commits nunca terão o mesmo hash no universo.
2. **Autor**: Nome e e-mail de quem comitou.
3. **Data**: Dia, mês, ano e segundo em que o commit foi gerado.
4. **Mensagem**: A descrição digitada no parâmetro `-m`.

## Analogia

O `git log` é como rolar o feed de uma rede social pessoal do seu código ou folhear um diário de bordo de uma nave estelar: cada post é uma missão cumprida com data, hora, autor e legenda explicativa.

## Na prática

Execute os comandos abaixo no seu terminal:

### Passo 1: O log detalhado

Digite:

```bash
git log
```

**O que você verá:**
```text
commit 4f82a1b5c92d84719e84610283c47e8b919248a1 (HEAD -> main)
Author: Maria Silva <maria.silva@email.com>
Date:   Wed Sep 30 10:00:00 2026 -0300

    feat: cria estrutura inicial do site GitHub Academy
```

*(Se a lista de commits for grande e o terminal exibir dois pontos `:` na parte inferior, use a tecla `Enter` ou setas para rolar e pressione a tecla `q` para sair).*

---

### Passo 2: O log resumido e elegante (`--oneline`)

No dia a dia, quando um projeto tem centenas de commits, o `git log` normal ocupa muita tela. Os programadores costumam usar a flag `--oneline`:

```bash
git log --oneline
```

**Resultado:**
```text
4f82a1b (HEAD -> main) feat: cria estrutura inicial do site GitHub Academy
```

Veja como fica compacto: apenas os primeiros 7 caracteres do Hash e a mensagem do commit em uma única linha!

---

### Passo 3: Curiosidade sobre o Hash SHA-1

Por que o Git usa códigos estranhos como `4f82a1b...` em vez de simplesmente numerar os commits como `1`, `2`, `3`?

> **A resposta de gênio**: Porque o Git é distribuído! Imagine se 10 programadores estivessem trabalhando desconectados em suas casas. Se o Git usasse números sequenciais, todos eles criariam o "commit 4" ao mesmo tempo, e na hora de juntar os trabalhos haveria uma colisão terrível. Com o hash criptográfico calculado a partir do conteúdo do arquivo, da data e do autor, cada commit tem um identificador único absoluto!

---

## Verificação Rápida

Teste rodar mais uma variação muito útil:
```bash
git log -n 1
```
O parâmetro `-n 1` limita a exibição aos últimos `1` commits. Útil quando você quer relembrar apenas a última coisa que acabou de fazer!

> Próximo passo: Vamos fazer uma alteração e ver exatamente o que mudou linha por linha no [Bloco 10 — git diff](10-git-diff.md).
