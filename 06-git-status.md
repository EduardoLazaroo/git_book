# Bloco 06 — git status

## Objetivo

Aprender a usar e interpretar as mensagens do comando `git status`, o comando mais importante e frequente do seu dia a dia como desenvolvedor.

## Conceito

O `git status` é o seu painel de instrumentos. Ele nunca altera nenhum arquivo e nunca quebra nada. Você pode executá-lo a qualquer momento, centenas de vezes por dia, sem medo.

Ele responde quatro perguntas vitais:
1. Em qual **branch** (ramificação) estou agora?
2. Existem arquivos novos que o Git ainda não conhece (**Untracked**)?
3. Existem arquivos conhecidos que foram modificados (**Modified**)?
4. Existem arquivos preparados prontos para serem salvos na próxima foto (**Staged**)?
5. O projeto está 100% em dia e sem pendências (**working tree clean**)?

## Analogia

Pense no painel do carro ou na tela de notificações do seu celular. Antes de acelerar na estrada, você olha o painel para conferir o nível de combustível, a velocidade e se as portas estão fechadas. O `git status` é esse velocímetro e medidor de bordo do seu código.

## Na prática

Vamos simular e observar os principais estados que o Git mostra na tela.

### Estado 1: Arquivos Não Rastreados (Untracked)

Execute agora no terminal:

```bash
git status
```

**O que o Git mostra:**
```text
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	index.html
	style.css
```
*(Geralmente em cor **vermelha** no terminal).*  
**Significado**: Os arquivos foram criados na pasta de trabalho, mas o Git ainda não tem autorização para incluir no próximo registro histórico.

---

### Estado 2: Entendendo as cores do terminal

O terminal moderno do Git usa cores para facilitar a sua vida:

| Cor no Terminal | O que significa? | Próxima ação recomendada |
| :--- | :--- | :--- |
| **Vermelho** | Arquivo alterado ou novo que **NÃO** está na esteira de foto | Usar `git add` se quiser incluir |
| **Verde** | Arquivo preparado (**Staged**) pronto para a foto | Usar `git commit` para registrar |
| **Sem cores / Mensagem limpa** | Nada pendente (**working tree clean**) | Continuar trabalhando ou enviar (`push`) |

---

### Passo Prático: Criando um arquivo temporário para observar

Digite no terminal para criar um arquivo de rascunho de teste:

```bash
echo "Meu rascunho de anotações" > rascunho.txt
```

Agora chame o status:

```bash
git status
```

Veja que `rascunho.txt` apareceu imediatamente listado entre os arquivos vermelhos não rastreados!

Agora vamos apagar esse arquivo de teste para não poluir nosso site:

No Windows PowerShell:
```bash
Remove-Item rascunho.txt
```
*(ou `del rascunho.txt` no CMD, ou `rm rascunho.txt` no Git Bash)*

Rode `git status` novamente e veja que `rascunho.txt` sumiu do radar sem deixar rastro.

---

## Verificação Rápida

Memorize esta regra de ouro:
> **"Na dúvida, rode `git status`."**  
> Antes de fazer commit: rode `git status`.  
> Depois de fazer commit: rode `git status`.  
> Antes de mudar de branch: rode `git status`.

Se você seguir esse hábito, você quase nunca cometerá erros com Git!

> Próximo passo: Vamos aprender a selecionar o que entra na próxima foto no [Bloco 07 — git add](07-git-add.md).
