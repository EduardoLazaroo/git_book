# Bloco 02 — Instalação e ambiente

## Objetivo

Verificar se o Git está instalado no seu computador, entender o que é o terminal de comandos e deixar seu ambiente pronto para os próximos blocos.

## Conceito

O Git é operado primariamente pelo **terminal** (também chamado de prompt de comando, console ou CLI — *Command Line Interface*). 

Em vez de clicar com o mouse em janelas coloridas, nós conversamos com o sistema operacional digitando instruções de texto diretas. Isso torna o trabalho muito mais rápido, preciso e compatível com servidores em nuvem.

No Windows, você pode usar:
- **Git Bash** (recomendado — emula o ambiente Linux no Windows)
- **PowerShell** (nativo do Windows)
- **Prompt de Comando (CMD)**
- **Terminal integrado do VS Code** (o mais prático no dia a dia)

## Analogia

Usar interface gráfica (cliques com mouse) é como apontar para itens em um cardápio com fotos: fácil, mas limitado ao que está desenhado.

Usar o terminal é como pedir diretamente ao chef da cozinha personalizando cada ingrediente: você tem controle total e imediato com comandos precisos.

## Na prática

### Passo 1: Abrir o terminal

No Windows:
1. Pressione as teclas `Win + R` no teclado.
2. Digite `powershell` ou `cmd` e pressione `Enter`.
3. Ou, se estiver no VS Code, abra o menu superior: **Terminal → New Terminal** (ou o atalho `Ctrl + '`).

Para as próximas aulas, prefira o terminal integrado do VS Code. Ele abrirá na pasta que está sendo exibida no editor. Sempre confira a linha antes do cursor: ela mostra em qual pasta o comando será executado.

### Passo 2: Verificando a instalação

Digite o comando abaixo e tecle `Enter`:

```bash
git --version
```

### O que esperar da tela?

- **Cenário de Sucesso**: O terminal retornará algo como:
  ```text
  git version 2.45.2.windows.1
  ```
  *(O número exato da versão pode variar, o importante é exibir "git version")*.

- **Cenário de Erro**: O terminal exibirá uma mensagem como:
  ```text
  'git' não é reconhecido como um comando interno ou externo...
  ```
  Se isso acontecer, o Git ainda não está instalado no seu computador.

### Passo 3: Instalando o Git (caso não esteja instalado)

1. Acesse o site oficial: [git-scm.com/downloads](https://git-scm.com/downloads).
2. Baixe o instalador para **Windows** (Standalone Installer 64-bit).
3. Execute o instalador baixado.
4. **Dica de ouro**: Durante a instalação, pode avançar clicando em **Next** em todas as opções padrão. As opções padrão já são ideais para iniciantes.
5. Quando concluir, **feche todos os terminais abertos** e abra um novo terminal.
6. Digite novamente:
   ```bash
   git --version
   ```

---

## Verificação Rápida

Execute novamente:

```bash
git --version
```

Se a resposta começar com `git version`, o Git está pronto. Você já concluiu o que precisava neste bloco.

> Próximo passo: identifique você no Git no [Bloco 03: Configurando o Git](03-configurando-o-git.md).
