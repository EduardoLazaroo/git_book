# Bloco 10 — git diff

## Objetivo

Compreender como inspecionar alterações linha por linha com o comando `git diff` antes de adicioná-las e comitá-las no projeto.

## Conceito

O comando `git diff` mostra a diferença exata entre o código salvo no seu último commit e as alterações que estão na sua mesa de trabalho no momento.

Ele utiliza uma convenção visual muito clara:
- Linhas vermelhas antecedidas por um sinal de menos (`-`): código que foi **removido ou substituído**.
- Linhas verdes antecedidas por um sinal de mais (`+`): código que foi **acrescentado ou atualizado**.

Esse comando é o seu raio-X: ele impede que você envie alterações esquecidas ou erros de digitação por distração.

## Analogia

Pense na brincadeira do "jogo dos 7 erros" ou no recurso de comparação de documentos de texto: o `git diff` coloca a folha antiga e a folha nova lado a lado na luz e destaca com marca-texto colorido exatamente onde a ponta da caneta mudou de lugar.

## Na prática

Vamos personalizar a seção de perfil do nosso site com os seus dados reais!

### Passo 1: Fazer uma alteração real no arquivo `index.html`

Abra o arquivo `index.html` no seu editor (VS Code, Bloco de Notas ou qualquer outro).

Procure pelas linhas onde está a seção `Perfil do Desenvolvedor`:

```html
<div class="profile-info">
  <h3>Seu Nome Aqui</h3>
  <p class="role">Estudante de Desenvolvimento de Sistemas</p>
  <p class="bio">Apaixonado por tecnologia, aprendendo controle de versão com Git e GitHub para construir projetos em equipe!</p>
```

Substitua `"Seu Nome Aqui"` pelo seu próprio nome. Por exemplo:
```html
  <h3>Lucas Oliveira</h3>
```
E salve o arquivo (`Ctrl + S`).

---

### Passo 2: Executar o `git diff` no terminal

Agora abra o terminal e digite:

```bash
git diff
```

**Olhe a saída incrível do Git:**
```diff
diff --git a/index.html b/index.html
index 72bc194..823fa10 100644
--- a/index.html
+++ b/index.html
@@ -95,7 +95,7 @@
         <div class="avatar-placeholder">🧑‍💻</div>
         <div class="profile-info">
-          <h3>Seu Nome Aqui</h3>
+          <h3>Lucas Oliveira</h3>
           <p class="role">Estudante de Desenvolvimento de Sistemas</p>
```

Veja com precisão cirúrgica:
- Em **vermelho** com `-`: `<h3>Seu Nome Aqui</h3>`
- Em **verde** com `+`: `<h3>Lucas Oliveira</h3>`

Nenhum arquivo secreto foi mexido, nenhuma outra linha foi afetada.

---

### Passo 3: Conferir com `git status`

Rode:

```bash
git status
```

**Resultado:**
```text
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   index.html
```

Veja a nova palavra-chave: `modified: index.html` (Modificado).

---

### Passo 4: Registrar essa alteração com o ciclo completo

Agora que você conferiu o que mudou com `git diff` e sabe que está tudo correto, execute o ciclo de registro:

```bash
git add index.html
git commit -m "feat: personaliza nome do autor no perfil do site"
```

Confire no histórico com o `--oneline`:

```bash
git log --oneline
```

Agora você tem **dois commits** impecáveis no seu histórico!

---

## Verificação Rápida

Se você rodar `git diff` agora que o commit foi feito, o que deve aparecer na tela?  
*(Teste no terminal! Não aparece nada, porque não há nenhuma alteração na mesa de trabalho em relação ao último commit salvo).*

> Próximo passo: É hora de nos conectarmos ao mundo! Vamos criar nossa conta e repositório no [Bloco 11 — Criando o GitHub](11-criando-o-github.md).
