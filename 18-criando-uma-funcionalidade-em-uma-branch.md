# Bloco 18 — Criando uma funcionalidade em uma branch

## Objetivo

Desenvolver uma nova seção no site dentro de uma branch dedicada chamada `feature/curiosidades`, comitar as alterações e comprovar que a branch `main` continua totalmente isolada e intacta.

## Conceito

No desenvolvimento de software profissional, toda nova tarefa recebe uma branch com um prefixo semântico, como `feature/nome-da-tarefa` (ou `fix/nome-do-bug`).

O grande poder das branches é o **isolamento total**:
Enquanto você estiver trabalhando na branch `feature/curiosidades`, os arquivos da branch `main` permanecem congelados no tempo. Se alguém abrir a `main`, verá o site exatamente como era antes.

Você só verá a novidade quando estiver posicionado dentro da branch da funcionalidade.

## Analogia

Pense em um rascunho em papel vegetal transparente sobre um mapa original: você pode desenhar novas estradas e prédios no papel transparente o quanto quiser; o mapa original embaixo continua 100% limpo e protegido.

## Na prática

Vamos criar uma seção de curiosidades incríveis sobre o Git no nosso site.

### Passo 1: Criar e entrar na branch da funcionalidade

Abra o terminal e execute:

```bash
git switch -c feature/curiosidades
```

Confirme com `git branch` que você está com o `*` em `feature/curiosidades`.

---

### Passo 2: Adicionar a seção de curiosidades no `index.html`

Abra o arquivo `index.html` no seu editor.

Logo após o fechamento da seção de comandos (`</section>`), adicione a nova seção completa abaixo:

```html
    <!-- Seção Curiosidades sobre Git -->
    <section id="curiosidades" class="section">
      <h2 class="section-title">Curiosidades do Mundo Git</h2>
      <div class="grid-2">
        <article class="card">
          <div class="card-icon">⚡</div>
          <h3>Criado em apenas 10 dias!</h3>
          <p>Linus Torvalds, o mesmo criador do sistema operacional Linux, criou a primeira versão funcional do Git em apenas cerca de 10 dias em abril de 2005.</p>
        </article>

        <article class="card">
          <div class="card-icon">💡</div>
          <h3>O significado do nome "Git"</h3>
          <p>Em gíria britânica antiga, "git" significa alguém desagradável ou teimoso. O próprio Linus brincou dizendo: <em>"Eu dou aos meus projetos nomes em homenagem a mim mesmo: primeiro Linux, depois Git!"</em></p>
        </article>
      </div>
    </section>
```

Salve o arquivo (`Ctrl + S`).

---

### Passo 3: Registrar o commit na branch

No terminal, confira com `git status`, prepare e faça o commit:

```bash
git status
git add index.html
git commit -m "feat: adiciona secao com curiosidades historicas sobre o Git"
```

---

### Passo 4: O Momento "AHA!" — A Mágica do Isolamento

Agora preste muita atenção na tela do seu editor de código (VS Code) e faça este teste:

Volte para a branch `main`:

```bash
git switch main
```

**Olhe para o seu editor agora mesmo!**
A seção de curiosidades **desapareceu** do arquivo `index.html`! Se você recarregar o navegador, ela não existe lá. O site voltou ao estado original seguro da `main`.

Agora volte para a branch da funcionalidade:

```bash
git switch feature/curiosidades
```

**Olhe novamente para o editor!**
A seção de curiosidades reapareceu instantaneamente como mágica! O Git trocou os arquivos no seu disco rígido em frações de milissegundo.

---

## Verificação Rápida

Alterne entre as branches mais uma vez observando o arquivo `index.html` aberto:
- `git switch main` (o código novo some).
- `git switch feature/curiosidades` (o código novo reaparece).

Essa é a prova visual definitiva de que branches são linhas temporais independentes e seguras!

> Próximo passo: Agora que a funcionalidade foi testada e aprovada, vamos juntá-la à linha principal no [Bloco 19 — Merge](19-merge.md).
