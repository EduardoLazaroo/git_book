# Bloco 08 — Primeiro commit

## Objetivo

Realizar o primeiro commit do projeto, gravando permanentemente a primeira versão oficial da história do site com uma mensagem clara e padronizada.

## Conceito

Um **commit** é o registro definitivo de um conjunto de alterações no histórico do Git.

Cada commit contém:
- Uma fotografia (*snapshot*) exata de todos os arquivos naquele instante.
- A autoria (seu nome e e-mail configurados no Bloco 03).
- Data e hora exatas.
- Um identificador único chamado **Hash SHA-1** (uma sequência de 40 letras e números, como `a1b2c3d...`).
- Uma **mensagem de commit**, explicando o motivo daquela alteração.

### Como escrever boas mensagens de commit?

A mensagem do commit é a documentação viva do projeto. No futuro, você e seus colegas lerão essas mensagens para entender por que algo mudou.

| Mensagens Ruins ❌ | Por que é ruim? | Mensagens Boas ✅ | Por que é boa? |
| :--- | :--- | :--- | :--- |
| `alterações` | Não explica o que foi feito | `feat: adiciona página inicial e estilos base` | Explica a novidade adicionada |
| `arrumando coisas` | Vago e sem contexto | `fix: corrige alinhamento do menu mobile` | Informa o erro exato corrigido |
| `asdasdasd` | Falta de profissionalismo | `docs: atualiza instruções de instalação` | Usa convenção clara e objetiva |
| `versao final agora vai` | Gera confusão no time | `style: altera paleta de cores para tema escuro` | Diz o que foi mudado visualmente |

> **Dica de mercado**: O prefixo `feat:` (funcionalidade nova), `fix:` (correção de bug) ou `docs:` (documentação) faz parte de um padrão mundial chamado *Conventional Commits*, muito valorizado em entrevistas de emprego!

## Analogia

Fazer um commit é como tirar uma fotografia oficial em alta resolução da sua turma no último dia de aula e colar no álbum da escola com uma legenda: *"Formatura da turma de 2026"*. A foto nunca mais muda; ela fica guardada para sempre no álbum de memórias do projeto.

## Na prática

Verifique se seus arquivos ainda estão preparados (em verde) com `git status`:

```bash
git status
```

Se estiver tudo verde, vamos disparar o primeiro commit com o parâmetro `-m` (que significa *message*, mensagem):

### Passo 1: Executar o commit

Digite o comando:

```bash
git commit -m "feat: cria estrutura inicial do site GitHub Academy"
```

### O que o Git responde?

O terminal exibirá algo parecido com:

```text
[main (root-commit) 4f82a1b] feat: cria estrutura inicial do site GitHub Academy
 2 files changed, 276 insertions(+)
 create mode 100644 index.html
 create mode 100644 style.css
```

Repare nos detalhes da resposta:
- `root-commit`: Informa que este é o **primeiro commit de toda a história** deste repositório!
- `4f82a1b`: É o início do código de identificação único (o Hash) da sua foto.
- `2 files changed, 276 insertions(+)`: O Git calculou que 2 arquivos foram salvos com 276 linhas de código.

---

### Passo 2: Ver o estado após o commit

Execute agora:

```bash
git status
```

**Resultado:**
```text
On branch main
nothing to commit, working tree clean
```

Essa é a frase mais relaxante do mundo da programação: **"nothing to commit, working tree clean"**! Significa que tudo o que estava na mesa de trabalho já foi fotografado e guardado com segurança no álbum.

---

## Verificação Rápida

Responda mentalmente:
1. O comando `git commit` sem arquivos preparados na Staging Area funciona? *(Não, você precisa fazer `git add` antes).*
2. Por que mensagens como "teste" ou "alterado" devem ser evitadas? *(Porque em um time ou daqui a 6 meses você não saberá o que aquele commit realmente fez).*

> Próximo passo: Vamos abrir o álbum e ver o nosso histórico no [Bloco 09 — Visualizando o histórico](09-visualizando-o-historico.md).
