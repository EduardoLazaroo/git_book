# Bloco 20 — Conflitos

## Objetivo

Entender por que conflitos de merge acontecem, aprender a identificar os marcadores visuais de conflito (`<<<<<<<`, `=======`, `>>>>>>>`), resolver a divergência com segurança e finalizar o merge.

## Conceito

O Git é incrivelmente inteligente: se uma pessoa alterar o topo do arquivo e outra alterar o rodapé do mesmo arquivo, o Git junta tudo automaticamente sem reclamar.

Um **conflito (Merge Conflict)** só acontece em uma situação específica:
> Quando duas branches diferentes alteram **a mesma linha** do mesmo arquivo com conteúdos diferentes.

O Git não pode adivinhar qual versão está certa (a do João ou a da Maria?). Em vez de apagar o trabalho de alguém, o Git para tudo, levanta a bandeira amarela e diz: *"Humano, venha aqui e escolha qual versão você quer manter!"*.

Conflitos **não são erros** e não quebram o projeto. Eles fazem parte da rotina de qualquer time e são muito simples de resolver.

## Analogia

Imagine que você e um amigo estão montando uma lista de supermercado. Na linha 5 da folha, você escreveu *"Comprar Sorvete de Chocolate"*. Na mesma linha 5, seu amigo escreveu *"Comprar Sorvete de Flocos"*. Vocês sentam juntos, conversam e decidem: *"Vamos levar o de Flocos!"* ou *"Vamos levar os dois!"*. Resolver um conflito é exatamente essa conversa.

## Na prática

Vamos criar um conflito controlado e resolvê-lo passo a passo em 3 minutos!

### Passo 1: Criar uma branch e alterar uma frase

Estando na `main`, crie uma branch chamada `ajuste-frase`:

```bash
git switch -c ajuste-frase
```

Abra o `index.html`, localize o parágrafo `<p>` dentro da seção `.hero`:

```html
<p>Construa, versione e publique este site passo a passo enquanto aprende a controlar versões como um desenvolvedor profissional.</p>
```

Substitua por:
```html
<p>Versão da Branch: Aprenda Git criando um site do zero absoluto!</p>
```

Salve e faça o commit:

```bash
git add index.html
git commit -m "style: atualiza frase de impacto na branch ajuste-frase"
```

---

### Passo 2: Voltar para a `main` e alterar A MESMA frase de outro jeito

Volte para a `main`:

```bash
git switch main
```

Abra o `index.html` novamente. Repare que a frase antiga está lá. Altere essa MESMA linha para:

```html
<p>Versão da Main: O melhor curso prático de versionamento para novos devs!</p>
```

Salve e comite na `main`:

```bash
git add index.html
git commit -m "style: atualiza frase de impacto direto na main"
```

Agora temos duas versões diferentes competindo exatamente pela mesma linha!

---

### Passo 3: O Conflito em Ação!

Tente juntar a branch na `main`:

```bash
git merge ajuste-frase
```

### O que o Git responde:

```text
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

Não entre em pânico! O Git apenas avisou: `CONFLICT in index.html`.

---

### Passo 4: Como identificar e resolver no editor

Abra o arquivo `index.html` no seu editor (se você estiver usando o VS Code, verá botões coloridos de ajuda).

Procure a linha onde estava o parágrafo. O Git colocou marcadores especiais lá dentro:

```html
<<<<<<< HEAD (Current Change - O que estava na branch atual: main)
<p>Versão da Main: O melhor curso prático de versionamento para novos devs!</p>
=======
<p>Versão da Branch: Aprenda Git criando um site do zero absoluto!</p>
>>>>>>> ajuste-frase (Incoming Change - O que veio da outra branch)
```

#### Para resolver:
1. Decida qual texto fica (ou combine os dois). Vamos ficar com o texto mais legal:
   `<p>Aprenda Git e GitHub na prática construindo um site do zero absoluto!</p>`
2. **Apague manualmente** as linhas com `<<<<<<< HEAD`, `=======` e `>>>>>>> ajuste-frase`.
3. O código final deve ficar limpo, assim:

```html
      <p>Aprenda Git e GitHub na prática construindo um site do zero absoluto!</p>
```

4. Salve o arquivo (`Ctrl + S`).

---

### Passo 5: Concluir o merge

Agora que você resolveu o conflito na mesa de trabalho, avise ao Git que está tudo em paz com o ciclo tradicional:

```bash
git status
```
*(Ele mostrará: `both modified: index.html`).*

Adicione e comite:

```bash
git add index.html
git commit -m "fix: resolve conflito no texto de apresentacao do hero"
```

Pronto! Conflito resolvido com maestria!

---

### Passo 6: Enviar para a nuvem e limpar

```bash
git push
git branch -d ajuste-frase
```

---

## Verificação Rápida

Rode `git status`.  
O terminal devolveu `nothing to commit, working tree clean`? Se sim, você acaba de passar pelo maior medo de muitos programadores experientes e venceu sem nenhuma dificuldade!

> Próximo passo: Vamos explorar as ferramentas visuais do GitHub no [Bloco 21 — GitHub na prática](21-github-na-pratica.md).
