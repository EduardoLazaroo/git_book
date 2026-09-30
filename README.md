# GitHub Academy: Guia do Curso

Bem-vindo(a)! Este material foi feito para o seu primeiro contato com Git e GitHub. Você não precisa decorar comandos: precisa entender o que está acontecendo, praticar com calma e conferir o resultado a cada etapa.

## O que vamos construir

Você vai usar o projeto **GitHub Academy**, um site simples em HTML e CSS, como laboratório. Enquanto faz pequenas alterações no site, aprenderá a registrar versões, recuperar o histórico e publicar seu trabalho no GitHub.

Ao final, você conseguirá explicar e executar o ciclo básico:

```text
alterar arquivos -> conferir -> preparar -> registrar -> enviar
```

Em comandos, esse ciclo será:

```bash
git status
git add .
git commit -m "mensagem clara"
git push
```

Não se preocupe: cada comando será apresentado no momento certo. Por enquanto, guarde a ideia principal: o Git acompanha as mudanças do seu projeto; o GitHub guarda uma cópia dele na internet.

## Antes de começar

Você precisa de:

- Um computador com Git instalado.
- Um editor de código, como o VS Code.
- Um terminal aberto dentro da pasta deste material.
- A pasta `projeto/`, que contém os arquivos `index.html` e `style.css` usados nas práticas.

Não encontrou o Git ou não sabe abrir o terminal? Sem problema. O [Bloco 02](02-instalacao-e-ambiente.md) explica isso passo a passo.

## Como estudar

Em cada bloco, siga sempre esta ordem:

1. Leia o objetivo e a explicação curta.
2. Faça somente o passo indicado, sem pular adiante.
3. Digite o comando no terminal. Evite copiar e colar para se acostumar com a escrita.
4. Compare o resultado com a seção de verificação.
5. Encontrou uma mensagem diferente? Leia-a com calma. Mensagens do Git quase sempre dizem o que fazer em seguida.

Erros fazem parte da prática. Antes de tentar outro comando, use `git status`: ele é o painel que mostra onde você está.

## Mapa dos blocos

| Bloco | Tema | O que você vai fazer |
| :---: | :--- | :--- |
| **01** | [O que é Git?](01-o-que-e-git.md) | Entender o problema do "trabalho_final_v2_agora_vai.zip" |
| **02** | [Instalação e Ambiente](02-instalacao-e-ambiente.md) | Verificar o terminal e instalar o Git no computador |
| **03** | [Configurando o Git](03-configurando-o-git.md) | Informar nome e e-mail ao Git |
| **04** | [Criando o Projeto](04-criando-nosso-primeiro-projeto.md) | Montar a estrutura do site GitHub Academy |
| **05** | [`git init`](05-git-init.md) | Transformar uma pasta em repositório local |
| **06** | [`git status`](06-git-status.md) | Ler o painel de controle do Git |
| **07** | [`git add`](07-git-add.md) | Preparar alterações para o próximo registro |
| **08** | [Primeiro Commit](08-primeiro-commit.md) | Registrar a primeira versão do projeto |
| **09** | [`git log`](09-visualizando-o-historico.md) | Consultar a linha do tempo dos commits |
| **10** | [`git diff`](10-git-diff.md) | Ver exatamente o que mudou |
| **11** | [Criando conta no GitHub](11-criando-o-github.md) | Criar seu espaço na nuvem |
| **12** | [`git remote`](12-git-remote.md) | Conectar o repositório local ao GitHub |
| **13** | [Primeiro `git push`](13-primeiro-git-push.md) | Enviar o código para a nuvem |
| **14** | [Ciclo Essencial Dev](14-alteracao-commit-push.md) | Praticar: alterar, conferir, preparar, registrar e enviar |
| **15** | [`git clone`](15-git-clone.md) | Baixar uma cópia de um projeto do GitHub |
| **16** | [`git pull`](16-git-pull.md) | Atualizar a cópia local com mudanças da nuvem |
| **17** | [Branches](17-branches.md) | Entender linhas paralelas de trabalho |
| **18** | [Criando uma funcionalidade](18-criando-uma-funcionalidade-em-uma-branch.md) | Trabalhar em uma branch sem mexer na `main` |
| **19** | [`git merge`](19-merge.md) | Unir a funcionalidade à linha principal |
| **20** | [Conflitos](20-conflitos.md) | Resolver edições na mesma linha |
| **21** | [GitHub na Prática](21-github-na-pratica.md) | Navegar por Issues e histórico no GitHub |
| **22** | [Pull Requests](22-pull-request.md) | Propor alterações para revisão |
| **23** | [Desafio Final](23-desafio-final.md) | Executar o fluxo completo sem cola |

## Onde ficam os arquivos

```text
git_book/
├── README.md                              <- Você está aqui
├── 01-o-que-e-git.md
├── 02-instalacao-e-ambiente.md
├── 03-configurando-o-git.md
├── 04-criando-nosso-primeiro-projeto.md
├── ... (até o bloco 23)
└── projeto/
    ├── index.html                         <- Página do laboratório
    └── style.css                          <- Estilos da página
```

---

> Comece pelo [Bloco 01: O que é Git?](01-o-que-e-git.md). Ao terminar cada bloco, volte aqui para localizar o próximo.
