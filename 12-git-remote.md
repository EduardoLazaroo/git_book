# Bloco 12 — git remote

## Objetivo

Conectar o seu repositório local do computador ao repositório remoto criado no GitHub utilizando o comando `git remote`.

## Conceito

O seu Git local não sabe por telepatia para onde enviar o seu código na internet. Você precisa dizer a ele: *"Git, o endereço da nuvem deste projeto é esta URL aqui"*.

Para isso usamos o comando:
```bash
git remote add origin <URL-DO-GITHUB>
```

### O que significa a palavra "origin"?

`origin` é simplesmente o **apelido padrão** (alias) que a comunidade Git dá para o servidor remoto principal. Em vez de você ter que digitar a URL inteira `https://github.com/fulano/projeto-super-longo-123.git` toda vez que for enviar um código, você digita apenas o apelido: `origin`.

Você poderia chamar de `meu-github` ou `nuvem`? Sim! Mas 99,9% das empresas e projetos no mundo usam a palavra `origin`.

## Analogia

Pense no aplicativo de contatos do seu celular. Quando você cadastra o número de telefone da sua mãe, você não fica discando `11 98765-4321` de cabeça toda vez. Você salva o apelido `"Mãe"`. No Git, `origin` é o apelido do número de telefone do GitHub.

## Na prática

Abra o terminal na pasta do seu projeto `github-academy`.

### Passo 1: Adicionar o endereço remoto

Copie a URL HTTPS do seu repositório criado no GitHub e execute o comando abaixo (substitua pelo seu usuário real):

```bash
git remote add origin https://github.com/SEU-USUARIO/github-academy.git
```

*(Se o terminal não der nenhuma mensagem de erro e apenas voltar para a linha de comando, deu tudo certo! No terminal, silêncio significa sucesso).*

---

### Passo 2: Verificar a conexão (`git remote -v`)

Para confirmar que o apelido `origin` foi salvo com o endereço certo, digite:

```bash
git remote -v
```
*(O parâmetro `-v` significa **verbose**, ou seja, detalhado).*

**O que o Git responde:**
```text
origin  https://github.com/SEU-USUARIO/github-academy.git (fetch)
origin  https://github.com/SEU-USUARIO/github-academy.git (push)
```

Observe que ele criou dois canais de comunicação com o mesmo apelido:
- `(fetch)`: canal de onde seu computador vai buscar atualizações que vierem da nuvem.
- `(push)`: canal para onde seu computador vai empurrar as suas alterações para a nuvem.

---

### Dica de ouro: Errei a URL digitada, como corrijo?

Se você digitou a URL com alguma letra errada, não se desespere! Basta atualizar o apelido com o comando `set-url`:

```bash
git remote set-url origin https://github.com/SEU-USUARIO-CORRETO/github-academy.git
```

---

## Verificação Rápida

Rode no terminal:
```bash
git remote
```
Ele deve devolver apenas a palavra `origin`. Se devolver, a sua ponte entre a terra e a nuvem está construída!

> Próximo passo: É hora de decolar! Vamos mandar os arquivos para a nuvem no [Bloco 13 — Primeiro git push](13-primeiro-git-push.md).
