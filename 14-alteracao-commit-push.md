# Bloco 14 — Alteração → commit → push

## Objetivo

Consolidar o ciclo de vida essencial que você repetirá todos os dias ao longo de toda a sua carreira como programador: **Modificar → Status → Add → Commit → Push**.

## Conceito

Na vida real de uma equipe de tecnologia, o trabalho nunca é um único evento. Ele é um ciclo contínuo de pequenas melhorias frequentes. 

O fluxo padrão do desenvolvedor é:

```text
 1. Fazer alterações no código (VS Code)
       │
 2. git status (verificar o que mudou)
       │
 3. git add . (colocar na esteira de envio)
       │
 4. git commit -m "..." (registrar a foto com mensagem)
       │
 5. git push (sincronizar com a nuvem)
```

Seguir esse ciclo frequentemente garante que você nunca perca mais de 1 ou 2 horas de trabalho se qualquer imprevisto acontecer.

## Analogia

Pense em um escritor escrevendo um livro:
1. Ele redige um parágrafo novo.
2. Revisa a frase.
3. Coloca o parágrafo no manuscrito.
4. Salva a versão no diário.
5. Envia uma cópia do capítulo para a editora na nuvem.

## Na prática

Vamos adicionar um novo cartão na seção de comandos do nosso site para incluir o `git diff` que aprendemos no Bloco 10.

### Passo 1: Fazer a alteração no `index.html`

Abra o arquivo `index.html` no seu editor. 

Na seção `<section id="comandos">`, dentro de `<div class="grid-3">`, adicione este novo cartão logo após o cartão do `git pull`:

```html
        <article class="command-card">
          <code>git diff</code>
          <h4>Ver Diferenças</h4>
          <p>Exibe linha por linha o que foi modificado nos arquivos antes do commit.</p>
        </article>
```

Salve o arquivo (`Ctrl + S`).

---

### Passo 2: Executar o ciclo passo a passo

Abra seu terminal e execute a sequência com atenção:

#### 1. Verificar o status
```bash
git status
```
*Observe `index.html` em vermelho indicando que foi modificado.*

#### 2. Preparar a alteração
```bash
git add .
```

#### 3. Salvar o commit com mensagem profissional
```bash
git commit -m "feat: adiciona card explicativo do comando git diff na pagina"
```

#### 4. Enviar para a nuvem
Como já usamos `-u origin main` no bloco anterior, agora basta digitar apenas:

```bash
git push
```

**Veja a resposta imediata:**
```text
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 432 bytes | 432.00 KiB/s, done.
To https://github.com/SEU-USUARIO/github-academy.git
   4f82a1b..98a12bc  main -> main
```

---

### Passo 3: Conferir o GitHub no navegador

1. Atualize a página do seu repositório no GitHub (`F5`).
2. Veja o contador de commits subir para **3 commits**.
3. Abra o arquivo `index.html` direto pela interface do GitHub e veja seu novo card do `git diff` lá dentro!

---

## Verificação Rápida

Recite em voz alta sem olhar para a tela os 4 comandos do ciclo essencial do desenvolvedor:
1. `git status`
2. `git add .`
3. `git commit -m "..."`
4. `git push`

Se você memorizou essa sequência, você já sabe fazer 70% das tarefas operacionais diárias de um desenvolvedor iniciante!

> Próximo passo: E se você trocou de computador ou entrou em uma nova empresa? Vamos aprender a baixar projetos no [Bloco 15 — git clone](15-git-clone.md).
