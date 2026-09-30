# Bloco 16 — git pull

## Objetivo

Compreender a necessidade de manter seu repositório local atualizado com o servidor remoto e aprender a puxar alterações usando o comando `git pull`.

## Conceito

Em equipes de desenvolvimento de software, vários programadores enviam códigos novos para o GitHub ao longo do dia.

Se você tentar enviar (`git push`) uma alteração enquanto seu computador local estiver desatualizado em relação ao que está no GitHub, o Git **rejeitará o seu envio** por segurança para não apagar o trabalho do seu colega.

A solução é o comando `git pull` (puxar): ele baixa os commits mais recentes do GitHub e os mescla automaticamente no seu computador local.

```text
  [ SEU COMPUTADOR ]
   (Repositório Local)
          ▲
          │  git pull
          │
     [ GITHUB ]
   (Repositório Remoto)
```

## Analogia

Imagine que você e um colega estão escrevendo um documento compartilhado. Antes de você começar a escrever o capítulo 3 hoje de manhã, você clica em *"Atualizar"* no aplicativo para ver o que seu colega escreveu na madrugada passada. O `git pull` é essa xícara de café da manhã que sincroniza as novidades.

## Na prática

Vamos simular perfeitamente o trabalho de um colega criando um arquivo `README.md` diretamente pela interface web do GitHub!

### Passo 1: Simular a alteração de um colega no GitHub

1. Abra a página do seu repositório `github-academy` no navegador.
2. Logo abaixo do título do repositório, clique no botão **Add file** e selecione **Create new file**.
3. No campo do nome do arquivo, digite: `README.md`.
4. No campo de texto do arquivo, cole o seguinte conteúdo:
   ```markdown
   # GitHub Academy 🐙
   
   Projeto prático construído durante o curso de Git e GitHub.
   
   ## Tecnologias
   - HTML5
   - CSS3
   - Git & GitHub
   ```
5. Role até o final da página e clique no botão verde **Commit changes...**.
6. Uma janelinha abrirá com a mensagem padrão *"Create README.md"*. Clique em **Commit changes**.

Pronto! Na nuvem (GitHub), seu projeto agora tem um arquivo a mais que o seu computador ainda não tem!

---

### Passo 2: Tentar encontrar o arquivo no seu computador

Abra o terminal na pasta local do seu projeto (`github-academy`).

Verifique os arquivos da sua pasta:

No PowerShell:
```bash
ls
```
*(ou `dir` no CMD)*

Cadê o arquivo `README.md`? **Ele não está aí!** O seu computador está desatualizado.

---

### Passo 3: Puxar a atualização com `git pull`

Digite no terminal:

```bash
git pull
```

### O que o Git responde:

```text
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 850 bytes | 425.00 KiB/s, done.
From https://github.com/SEU-USUARIO/github-academy
   98a12bc..c4d5e6f  main       -> origin/main
Updating 98a12bc..c4d5e6f
Fast-forward
 README.md | 7 +++++++
 1 file changed, 7 insertions(+)
 create mode 100644 README.md
```

---

### Passo 4: Conferir a sincronização

Liste os arquivos no seu computador agora:

```bash
ls
```

O arquivo `README.md` agora está no seu disco local! 

E se você rodar:

```bash
git log --oneline
```

O commit feito pelo navegador do GitHub agora aparece no histórico do seu terminal local. Computador e nuvem estão perfeitamente alinhados!

---

## Verificação Rápida

Qual é a boa prática recomendada antes de começar a programar no início do seu dia de trabalho em uma empresa?  
*(Resposta: Sempre abrir o terminal e rodar um `git pull` para começar o dia com o código mais atualizado do time).*

> Próximo passo: Chega de mexer direto na linha principal! Vamos aprender a trabalhar com segurança no [Bloco 17 — Branches](17-branches.md).
