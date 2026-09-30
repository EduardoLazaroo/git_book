# Bloco 23 — Desafio final

## Objetivo

Testar e comprovar sua autonomia prática executando o ciclo completo de um desenvolvedor júnior sem comandos pré-prontos: ramificação, desenvolvimento, versionamento, publicação, Pull Request e sincronização.

## Conceito

Na vida profissional, ninguém estará ao seu lado ditando comando por comando. Você receberá uma demanda de negócio e precisará aplicar as boas práticas aprendidas por conta própria.

Este desafio final é o teste de graduação da **GitHub Academy**: se você conseguir concluí-lo sozinho, você estará 100% apto a trabalhar com Git e GitHub em qualquer empresa ou projeto acadêmico.

## Analogia

Pense no teste prático de direção da autoescola: o examinador apenas senta ao seu lado e diz: *"Faça a baliza e dirija até o semáforo"*. Você já sabe onde fica a embreagem, o freio e as setas; agora é a sua hora de conduzir sozinho com calma e maestria.

## Na prática

### O Desafio: Implementar a Seção "Dicas de Ouro do Git"

Sua missão é adicionar uma nova seção no site `github-academy` contendo 3 dicas práticas para iniciantes, seguindo rigorosamente o fluxo de trabalho de engenharia de software.

---

### As Regras do Jogo (O que você deve fazer):

1. **Partir da base correta**:
   - Certifique-se de estar na branch `main` e de que ela está 100% atualizada com o GitHub.
2. **Criar uma nova branch**:
   - Crie uma branch chamada `feature/dicas-de-ouro` e mude para ela.
3. **Desenvolver o código**:
   - No arquivo `index.html`, crie uma nova seção antes do rodapé com o `id="dicas"`.
   - Adicione 3 cards com dicas úteis que você aprendeu no curso. Exemplos de dicas:
     - *Dica 1: Commits pequenos e frequentes são melhores que um commit gigante no final da semana.*
     - *Dica 2: Sempre rode `git status` antes de adicionar arquivos.*
     - *Dica 3: Nunca edite a pasta oculta `.git` manualmente.*
4. **Testar visualmente**:
   - Abra o `index.html` no navegador e certifique-se de que a página está bonita e sem erros de formatação.
5. **Versionar com commits semânticos**:
   - Verifique os arquivos alterados com o comando de status.
   - Coloque os arquivos na Staging Area.
   - Faça o commit utilizando uma mensagem clara com o prefixo `feat:`.
6. **Enviar para a nuvem**:
   - Envie a sua branch nova para o GitHub configurando o upstream.
7. **Abrir e finalizar o Pull Request**:
   - Acesse o GitHub no navegador.
   - Abra o Pull Request para mesclar `feature/dicas-de-ouro` dentro da `main`.
   - Descreva brevemente o que foi feito.
   - Analise os arquivos alterados na aba de revisão.
   - Faça o **Merge pull request** e confirme.
8. **Finalizar no computador**:
   - Volte para o terminal do seu computador.
   - Troque para a branch `main`.
   - Puxe as atualizações mais recentes da nuvem.
   - Delete a branch local `feature/dicas-de-ouro`.

---

## Tabela de Dicas (Consulte apenas em caso de emergência!)

<details>
<summary>💡 Clique aqui se você travar em algum comando</summary>

- Para garantir que está na main: `git switch main`
- Para criar a branch: `git switch -c feature/dicas-de-ouro`
- Para ver o que mudou: `git status` e `git diff`
- Para preparar os arquivos: `git add index.html`
- Para comitar: `git commit -m "feat: ..."`
- Para enviar a branch: `git push -u origin feature/dicas-de-ouro`
- Para atualizar a main local após o merge no GitHub: `git switch main` e depois `git pull`
- Para apagar a branch local: `git branch -d feature/dicas-de-ouro`
</details>

---

## Checklist de Autoavaliação do Desenvolvedor

Marque os itens que você conseguiu realizar com sucesso:

- [ ] Criei a branch sem mexer direto na `main`.
- [ ] O código HTML ficou bem formatado e agradável no navegador.
- [ ] Minha mensagem de commit seguiu um padrão semântico profissional.
- [ ] A branch apareceu corretamente no GitHub.
- [ ] Abri o Pull Request com título e descrição adequados.
- [ ] Fiz o merge pelo GitHub sem nenhum conflito.
- [ ] Executei o `git pull` na máquina e vi a seção nova carregada na `main` local.
- [ ] O comando `git branch` mostra apenas a `main` limpa e sem galhos órfãos.

---

## 🏆 Parabéns, Desenvolvedor!

Se você completou este percurso do Bloco 00 ao Bloco 23:
Você não apenas decorou comandos soltos do Git; você aprendeu a **mentalidade profissional de controle de versão e colaboração em equipe**. 

Mantenha esse repositório no seu perfil do GitHub, fixe-o na página inicial do seu perfil e compartilhe com seus professores, colegas e recrutadores como prova do seu aprendizado prático!
