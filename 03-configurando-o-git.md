# Bloco 03 — Configurando o Git

## Objetivo

Configurar seu nome e e-mail no Git globalmente, garantindo que todos os seus futuros commits sejam devidamente assinados com a sua autoria.

## Conceito

Sempre que você salva uma versão do seu código no Git, essa versão carrega um selo de autoria imutável: **quem fez a alteração** e **qual é o e-mail de contato do autor**.

Se você não configurar seu nome e e-mail, o Git reclamará ou usará o nome de usuário genérico do Windows (ex: `user@DESKTOP-XYZ`), o que fica feio no histórico e impede que o GitHub associe seus commits à sua conta.

A opção `--global` significa que você só precisa fazer isso **uma única vez** por computador. Todos os seus projetos usarão essa configuração.

## Analogia

Pense em assinar uma prova escolar ou um contrato oficial. Antes de entregar a folha, você preenche seu nome e RG no cabeçalho. No Git, configurar `user.name` e `user.email` é como carimbar sua assinatura em cada página do projeto.

## Na prática

Abra seu terminal e execute os passos abaixo.

### Passo 1: Configurar seu nome completo

Substitua `"Seu Nome Completo"` pelo seu nome real entre aspas duplas:

```bash
git config --global user.name "Maria Silva"
```

### Passo 2: Configurar seu e-mail

Substitua `"seuemail@exemplo.com"` pelo seu e-mail (de preferência o mesmo e-mail que você usa ou usará no GitHub):

```bash
git config --global user.email "maria.silva@email.com"
```

### Passo 3: Definir o nome padrão da branch principal para `main`

Por padrão histórico, o Git criava a branch com o nome antigo `master`. Hoje em dia, o padrão universal da indústria e do GitHub é `main`. Vamos padronizar:

```bash
git config --global init.defaultBranch main
```

### Passo 4: Conferir as configurações ativas

Para ter certeza de que o Git salvou suas preferências, consulte cada informação separadamente:

```bash
git config --global user.name
git config --global user.email
git config --global init.defaultBranch
```

O terminal deve mostrar, em linhas separadas, algo parecido com:

```text
user.name=Maria Silva
user.email=maria.silva@email.com
init.defaultbranch=main
```

---

## Verificação Rápida

Teste consultar apenas o seu nome cadastrado digitando:

```bash
git config user.name
```

E o seu e-mail:

```bash
git config user.email
```

Se o terminal respondeu exatamente o que você digitou, a sua identidade de desenvolvedor está pronta!

> Próximo passo: crie o projeto web que iremos versionar no [Bloco 04: Criando nosso primeiro projeto](04-criando-nosso-primeiro-projeto.md).
