# Bloco 15 — git clone

## Objetivo

Aprender a clonar (baixar) um repositório existente do GitHub para qualquer computador através do comando `git clone`.

## Conceito

Quando você entra para trabalhar em uma empresa de tecnologia ou vai contribuir em um projeto de código aberto, você não começa o repositório do zero com `git init`. O projeto já existe na nuvem!

O comando `git clone` faz o seguinte de forma totalmente automatizada:
1. Cria uma pasta no seu computador com o nome do projeto.
2. Inicializa o Git localmente (`git init` embutido).
3. Configura o endereço remoto `origin` apontando para o repositório correto.
4. Baixa **todos** os arquivos, todas as branches e **todo o histórico de commits** já feito desde o primeiro dia de vida do projeto.

## Analogia

Fazer um `git clone` é como tirar uma cópia xerox idêntica de uma enciclopédia inteira guardada na biblioteca central: você ganha um exemplar perfeito para ler e rabiscar na sua casa, sem estragar o livro original da biblioteca.

## Na prática

Vamos simular uma situação real: você acabou de chegar no laboratório da escola ou comprou um computador novo e precisa continuar o projeto.

### Passo 1: Ir para uma pasta temporária

Abra uma nova janela de terminal e vá para uma pasta diferente (por exemplo, sua pasta de `Downloads` ou área de trabalho):

```bash
cd ~/Downloads
```
*(ou qualquer outra pasta fora da sua pasta atual `github-academy`)*

---

### Passo 2: Copiar o endereço do repositório no GitHub

1. Abra seu repositório no GitHub pelo navegador.
2. Clique no botão verde **Code**.
3. Na aba **HTTPS**, clique no ícone de dois quadradinhos para copiar o link:
   `https://github.com/SEU-USUARIO/github-academy.git`

---

### Passo 3: Executar o comando `git clone`

Digite no terminal:

```bash
git clone https://github.com/SEU-USUARIO/github-academy.git
```

### O que o Git responde:

```text
Cloning into 'github-academy'...
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 12 (delta 2), reused 12 (delta 2), pack-reused 0
Receiving objects: 100% (12/12), done.
```

---

### Passo 4: Entrar na pasta clonada e inspecionar

Entre na pasta que acabou de ser criada pelo clone:

```bash
cd github-academy
```

Agora liste o histórico de commits:

```bash
git log --oneline
```

**Repare na mágica:** todos os seus commits anteriores feitos no outro local estão aí, intactos, com as mesmas mensagens e autores!

E o endereço remoto? Confira com:

```bash
git remote -v
```

O `origin` já veio configurado automaticamente. Não precisa rodar `git init` nem `git remote add`. O `git clone` fez tudo por você!

---

## Verificação Rápida

Após terminar os testes na pasta clonada, volte para o terminal da sua pasta de trabalho original do curso (`github-academy`). Se quiser apagar a pasta clonada de testes dos Downloads para não ocupar espaço, pode apagar sem medo: o repositório oficial continua seguro no GitHub!

> Próximo passo: E quando um colega de equipe subir código novo e você precisar atualizar o seu computador? Vamos aprender no [Bloco 16 — git pull](16-git-pull.md).
