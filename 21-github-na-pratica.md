# Bloco 21 — GitHub na prática

## Objetivo

Navegar pelas principais ferramentas da interface web do GitHub: histórico visual de commits, abas de arquivos, visualização de branches e criação de **Issues** para organizar tarefas.

## Conceito

O GitHub não é apenas um disco rígido na nuvem; ele é uma **plataforma completa de gerenciamento e colaboração**.

Os principais recursos que você usará no GitHub são:
1. **Code (Código)**: Onde ficam os arquivos, as pastas e a visualização do `README.md`.
2. **Commits**: Linha do tempo visual onde é possível clicar em qualquer commit e ver o diff com cores na tela do navegador.
3. **Issues**: Um quadro de tarefas e chamados de erros (*tickets*). É onde os membros da equipe relatam bugs, sugerem novas ideias ou pedem melhorias.
4. **Pull Requests (PRs)**: O local sagrado onde um desenvolvedor pede para outro colega revisar seu código antes de juntar na branch principal.

## Analogia

Pense no GitHub como o escritório virtual da equipe:
- A aba **Code** é o arquivo de documentos da empresa.
- Os **Commits** são as atas de reunião arquivadas.
- As **Issues** são os post-its no quadro Scrum / Kanban com tarefas pendentes.
- Os **Pull Requests** são a mesa de aprovação do chefe antes de lançar o produto no mercado.

## Na prática

Abra o seu repositório `github-academy` no navegador.

### Passo 1: Explorando a aba Code e o Histórico de Commits

1. Na página inicial do seu repositório, clique no botão que mostra o número de commits (ex: **5 commits** ou **6 commits**).
2. Clique em qualquer um dos commits da lista.
3. Observe como o GitHub desenha o `git diff` visualmente:
   - Fundo verde para código adicionado.
   - Fundo vermelho para código removido.
   - Você pode até deixar comentários em uma linha específica clicando no sinal de `+` que aparece ao passar o mouse sobre a linha!

---

### Passo 2: Criando sua primeira Issue (Relato de Tarefa)

Vamos registrar uma tarefa oficial para melhorar o site:

1. No menu superior do repositório, clique na aba **Issues**.
2. Clique no botão verde **New issue**.
3. Preencha os campos:
   - **Title**: `Adicionar links de redes sociais no perfil do desenvolvedor`
   - **Leave a comment**:
     ```markdown
     ### Descrição da Tarefa
     Adicionar links para o LinkedIn e GitHub no card do perfil do aluno em `index.html`.
     
     ### Critérios de Aceitação
     - [ ] Criar ícones ou textos clicáveis
     - [ ] Abrir os links em uma nova aba (`target="_blank"`)
     ```
4. Clique no botão verde **Submit new issue**.

Observe que a sua issue ganhou um número identificador único, como **#1**! No mundo profissional, os desenvolvedores usam esse número em mensagens de commit (ex: `feat: adiciona redes sociais (closes #1)`), e o GitHub fecha a tarefa automaticamente!

---

### Passo 3: Inspecionando o seletor de branches na web

1. Volte para a aba **Code**.
2. No canto superior esquerdo da lista de arquivos, clique no botão onde está escrito **main** com o ícone de bifurcação.
3. Ali você pode ver todas as branches ativas no repositório remoto e até alternar entre elas para visualizar como o código estava em cada galho!

---

## Verificação Rápida

Acesse a aba **Issues** do seu repositório.  
Você vê a sua issue **#1** listada com a etiqueta verde **Open**? Se sim, você já aprendeu a documentar e gerenciar demandas técnicas como um profissional!

> Próximo passo: Agora vamos aprender o recurso mais usado em equipes do mundo inteiro no [Bloco 22 — Pull Request](22-pull-request.md).
