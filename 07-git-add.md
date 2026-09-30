# Bloco 07 — git add

## Objetivo

Compreender o conceito da **Staging Area** (área de preparação) e aprender a utilizar o comando `git add` para selecionar quais arquivos farão parte do próximo registro histórico.

## Conceito

No Git, salvar um trabalho não é um pulo direto do editor de texto para o histórico definitivo. Existe uma etapa intermediária chamada **Staging Area** (Área de Preparação ou Índice).

O fluxo funciona em 3 ambientes:

```text
[ Working Directory ]  ──( git add )──>  [ Staging Area ]  ──( git commit )──>  [ Repositório Local ]
 (Mesa de Trabalho)                      (Caixa de Envio)                        (Álbum Oficial)
```

Por que isso existe? Porque você pode ter alterado 5 arquivos no seu dia, mas querer salvar apenas 2 deles agora com uma mensagem específica e deixar os outros 3 para depois. O `git add` te dá o poder dessa escolha cirúrgica.

## Analogia

Pense que:
1. **Working Directory (Diretório de Trabalho)** é a sua mesa bagunçada de estudos.
2. **Staging Area (Área de Preparação)** é uma caixa de encomenda aberta onde você coloca cuidadosamente apenas os itens que você quer despachar pelo correio hoje.
3. **Commit** é fechar a caixa com fita adesiva, colar a etiqueta com remetente e data, e despachar!

O comando `git add` é o ato de pegar o item da mesa e colocá-lo dentro da caixa.

## Na prática

Atualmente temos dois arquivos no nosso diretório de trabalho: `index.html` e `style.css`.

### Passo 1: Adicionar um arquivo específico

Se quisermos colocar apenas o `index.html` na Staging Area, digitamos o nome exato dele:

```bash
git add index.html
```

Agora, rode o comando do painel para ver o que aconteceu:

```bash
git status
```

**Veja a diferença mágica na tela:**
```text
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	style.css
```

- `index.html` agora está **verde** (Changes to be committed — na Staging Area).
- `style.css` continua **vermelho** (Untracked — ainda na mesa de trabalho).

---

### Passo 2: Adicionar tudo de uma vez com o ponto `.`

E se você alterou 10 arquivos e quer colocar todos eles na caixa de uma vez só? 
O caractere ponto `.` no terminal significa *"o diretório atual e tudo o que está nele"*:

```bash
git add .
```

Agora execute novamente:

```bash
git status
```

**Resultado:**
```text
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   index.html
	new file:   style.css
```

Os dois arquivos agora estão **verdes**, aguardando pacientemente na Staging Area pelo momento do commit.

---

### Curiosidade: E se eu me arrepender e quiser tirar da caixa?

Se você colocou um arquivo na Staging Area por engano, você pode tirá-lo da caixa sem apagar seu código:

```bash
git restore --staged style.css
```
*(Ele volta a ficar vermelho no `git status`, mas seu código continua intacto na mesa).*

Depois de testar, adicione-o de volta com `git add .` para que ambos continuem prontos para a foto!

```bash
git add .
```

---

## Verificação Rápida

Rode:
```bash
git status
```
Confirme se você vê os dois arquivos (`index.html` e `style.css`) listados em verde sob a frase `Changes to be committed`. Se sim, a caixa está pronta para ser lacrada!

> Próximo passo: Vamos eternizar essa primeira versão no [Bloco 08 — Primeiro commit](08-primeiro-commit.md).
