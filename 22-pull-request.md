# Bloco 22 — Pull Request

## Objetivo

Compreender o fluxo de trabalho colaborativo de maior prestígio na indústria de tecnologia: criar uma branch, enviar à nuvem, abrir um **Pull Request (PR)**, inspecionar a revisão de código (*code review*) e realizar o merge pela interface web do GitHub.

## Conceito

Em empresas e grandes projetos, nenhum desenvolvedor (nem mesmo o dono da empresa) faz merge direto no terminal para a `main`. Tudo passa por um **Pull Request**.

O fluxo oficial é:

```text
 1. Criar branch local (feature/minha-tarefa)
        │
 2. Fazer alterações e commits locais
        │
 3. Enviar a branch para o GitHub (git push -u origin feature/...)
        │
 4. Abrir um Pull Request no site do GitHub
        │
 5. Outros programadores revisam o código (Code Review)
        │
 6. Clicar no botão verde "Merge pull request" no GitHub
        │
 7. Atualizar a main no computador (git switch main && git pull)
```

Um Pull Request significa literalmente: *"Colegas, terminei esta funcionalidade nesta branch separada. Peço (Request) que vocês puxem (Pull) e revisem meu código para integrarmos à branch principal!"*.

## Analogia

Pense em um jornalista enviando uma reportagem para o editor-chefe do jornal: o repórter escreve o texto em uma folha separada (branch) e coloca na mesa do editor (Pull Request). O editor lê, aponta correções ou elogia (revisão) e, quando aprovado, autoriza a impressão na primeira página do jornal (merge).

## Na prática

Vamos resolver exatamente a Issue #1 criada no bloco anterior através de um Pull Request impecável!

### Passo 1: Criar a branch local

Abra o terminal na pasta do projeto e certifique-se de partir da `main`:

```bash
git switch main
git switch -c feature/redes-sociais
```

---

### Passo 2: Implementar a melhoria no `index.html`

Abra o arquivo `index.html`. Na seção `#perfil`, dentro de `.profile-info`, logo após a `div` com classe `.tags`, adicione uma linha de links para as redes:

```html
          <div class="social-links" style="margin-top: 1rem;">
            <a href="https://github.com" target="_blank" class="btn btn-secondary" style="padding: 0.4rem 0.8rem; font-size: 0.85rem;">GitHub</a>
            <a href="https://linkedin.com" target="_blank" class="btn btn-secondary" style="padding: 0.4rem 0.8rem; font-size: 0.85rem;">LinkedIn</a>
          </div>
```

Salve o arquivo (`Ctrl + S`).

---

### Passo 3: Comitar e enviar a branch para o GitHub

No terminal:

```bash
git add index.html
git commit -m "feat: adiciona botoes de redes sociais no perfil (closes #1)"
```

Agora envie essa branch nova para o GitHub:

```bash
git push -u origin feature/redes-sociais
```

---

### Passo 4: Abrir o Pull Request no GitHub

1. Vá para a página do seu repositório no navegador.
2. O GitHub é tão inteligente que exibirá um aviso amarelo destacado no topo da página:
   **"feature/redes-sociais had recent pushes... Compare & pull request"**.
3. Clique no botão verde **Compare & pull request**.
4. Veja que ele já preenche o título a partir da mensagem do seu commit.
5. Na descrição, escreva:
   ```markdown
   Este PR adiciona botões de redes sociais ao card de perfil do desenvolvedor, resolvendo a Issue #1.
   ```
6. Clique no botão verde **Create pull request**.

Parabéns! Seu primeiro Pull Request está oficialmente aberto!

---

### Passo 5: Analisar a aba "Files changed" e Aprovar o Merge

1. No topo da página do seu PR, clique na aba **Files changed** (Arquivos alterados).
2. Veja o diff completo das linhas que você adicionou. É assim que os líderes técnicos avaliam o trabalho de novos devs.
3. Volte para a aba **Conversation**.
4. Role até o final da página e clique no botão verde **Merge pull request**.
5. Clique em **Confirm merge**.
6. Uma mensagem roxa aparecerá: **Merged**! E se você quiser, pode clicar no botão cinza **Delete branch** no GitHub.

---

### Passo 6: Sincronizar o seu computador com o merge feito no GitHub

O merge aconteceu na nuvem. Agora seu computador precisa receber essa versão final atualizada da `main`.

No seu terminal local:

```bash
git switch main
git pull
```

E delete a branch local que já foi mesclada:

```bash
git branch -d feature/redes-sociais
```

Pronto! Se você olhar a aba **Issues** no GitHub agora, verá que a Issue #1 foi fechada automaticamente graças à mágica da palavra-chave `closes #1` no commit!

---

## Verificação Rápida

Abra o arquivo `index.html` local no seu navegador na branch `main`.  
Os botões de GitHub e LinkedIn estão visíveis? Se sim, você acabou de executar o fluxo de trabalho real utilizado por Google, Meta, Microsoft e startups do mundo inteiro!

> Próximo passo: É hora de testar sua autonomia e provar que você é um mestre no [Bloco 23 — Desafio final](23-desafio-final.md).
