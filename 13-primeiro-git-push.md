# Bloco 13 — Primeiro git push

## Objetivo

Enviar pela primeira vez os commits salvos no seu computador para o repositório no GitHub usando o comando `git push`.

## Conceito

O comando `git push` (empurrar) faz o upload dos seus commits locais para o servidor remoto.

```text
  [ SEU COMPUTADOR ]
   (Repositório Local)
          │
          │  git push
          ▼
     [ GITHUB ]
   (Repositório Remoto)
```

Até você rodar o `git push`, todo o seu trabalho só existe no seu computador. Quando você executa o push, todos os arquivos, pastas, histórico de commits e mensagens são replicados na nuvem.

### O que significa `git push -u origin main`?

- `git push`: Ação de empurrar/fazer upload.
- `-u`: Abreviação de *upstream*. Ele diz ao Git: *"Ligue a minha branch local `main` diretamente à branch `main` do `origin`"*. Nas próximas vezes, você poderá digitar apenas `git push` seco!
- `origin`: O apelido da nuvem que você configurou no Bloco 12.
- `main`: O nome da ramificação principal que você quer enviar.

## Analogia

Pense em um foguete de carga:
Você passou o dia inteiro empacotando caixas no galpão (trabalho local). O `git push` é acionar os motores do foguete e disparar a carga até a estação espacial orbital (o GitHub).

## Na prática

Abra o terminal na pasta do seu projeto.

### Passo 1: Garantir que a branch se chama `main`

Para ter certeza absoluta de que a ramificação principal está com o nome moderno `main`:

```bash
git branch -M main
```
*(O parâmetro `-M` força a renomeação da branch atual para `main`).*

---

### Passo 2: O Grande Envio (`git push`)

Execute o comando:

```bash
git push -u origin main
```

### O que vai acontecer na primeira vez?

1. Uma janela do seu navegador ou um pop-up de login do **GitHub / Git Credential Manager** se abrirá automaticamente.
2. Clique no botão verde: **Sign in with your browser** (ou autorize a conexão).
3. O terminal receberá a autorização de segurança e iniciará a transferência.

### Saída de Sucesso no Terminal:

```text
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (7/7), 2.80 KiB | 2.80 MiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/SEU-USUARIO/github-academy.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

---

### Passo 3: Ver seu código ao vivo no GitHub!

1. Volte ao seu navegador de internet na página do seu repositório no GitHub.
2. Pressione a tecla **F5** (atualizar página).
3. **Mágica pura!** Aquela tela em branco de instruções sumiu. No lugar dela, agora aparecem:
   - Os arquivos `index.html` e `style.css`.
   - A contagem de **2 commits**.
   - A mensagem do último commit que você fez.
   - O autor com sua foto de perfil do GitHub!

---

## Verificação Rápida

No site do GitHub, clique no link **2 commits** (logo acima da lista de arquivos).  
Você verá a linha do tempo idêntica àquela que você consultou no terminal com o comando `git log` no Bloco 09! O terminal e a nuvem agora são um só.

> Próximo passo: Vamos exercitar o ciclo diário de todo programador no [Bloco 14 — Alteração → commit → push](14-alteracao-commit-push.md).
