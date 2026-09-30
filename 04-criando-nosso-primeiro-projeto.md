# Bloco 04 — Criando nosso primeiro projeto

## Objetivo

Criar os arquivos iniciais do site **GitHub Academy** em HTML e CSS, testá-lo no navegador e preparar o terreno para iniciarmos o versionamento.

## Conceito

Para aprender Git de verdade, precisamos de arquivos de verdade para alterar, salvar e controlar. Não usaremos comandos Git neste bloco; o foco aqui é criar nosso objeto de estudo: uma página web moderna, leve e funcional.

O projeto contém apenas dois arquivos:
1. `index.html`: Define o conteúdo e a estrutura da página (títulos, textos, cartões e links).
2. `style.css`: Aplica as cores, fontes, espaçamentos e visual moderno (modo escuro profissional).

## Analogia

Antes de aprender a usar uma câmera fotográfica profissional com lentes e tripé, precisamos primeiro montar o cenário que será fotografado. Nosso site é esse cenário.

## Na prática

### Passo 1: Criar a pasta do seu projeto

Abra o terminal e crie uma nova pasta chamada `github-academy` na sua área de trabalho ou pasta de projetos, e entre nela:

```bash
mkdir github-academy
cd github-academy
```

*(Se você já estiver utilizando os arquivos prontos da pasta `projeto/` deste material, basta abrir o terminal diretamente dentro dela).*

---

### Passo 2: Criar o arquivo `index.html`

Crie um arquivo chamado `index.html` dentro da pasta `github-academy` e cole o código completo abaixo:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GitHub Academy — Guia Prático de Git e GitHub</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Cabeçalho Principal -->
  <header class="navbar">
    <div class="container nav-content">
      <div class="logo">
        <span class="logo-icon">🐙</span>
        <span class="logo-text">GitHub <strong>Academy</strong></span>
      </div>
      <nav>
        <ul class="nav-links">
          <li><a href="#sobre">Sobre</a></li>
          <li><a href="#comandos">Comandos</a></li>
          <li><a href="#perfil">Meu Perfil</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Seção Hero / Apresentação -->
  <header class="hero">
    <div class="container hero-content">
      <span class="badge">Curso Técnico • Desenvolvimento de Sistemas</span>
      <h1>Domine o <span>Git</span> e o <span>GitHub</span> na Prática</h1>
      <p>Construa, versione e publique este site passo a passo enquanto aprende a controlar versões como um desenvolvedor profissional.</p>
      <div class="hero-actions">
        <a href="#comandos" class="btn btn-primary">Ver Comandos</a>
        <a href="#sobre" class="btn btn-secondary">Entender Conceitos</a>
      </div>
    </div>
  </header>

  <!-- Conteúdo Principal -->
  <main class="container">
    <!-- Seção Sobre -->
    <section id="sobre" class="section">
      <h2 class="section-title">O que estamos aprendendo?</h2>
      <div class="grid-2">
        <article class="card">
          <div class="card-icon">💻</div>
          <h3>Git: A Máquina do Tempo</h3>
          <p>O Git é um sistema de controle de versão distribuído que roda localmente no seu computador. Ele salva fotografias (commits) de cada evolução do seu projeto, permitindo voltar no tempo caso algo dê errado.</p>
        </article>

        <article class="card">
          <div class="card-icon">☁️</div>
          <h3>GitHub: A Nuvem dos Devs</h3>
          <p>O GitHub é uma plataforma online que hospeda repositórios Git na nuvem. Ele permite compartilhar código, colaborar em equipe e exibir seus projetos para o mundo.</p>
        </article>
      </div>
    </section>

    <!-- Seção Comandos Essenciais -->
    <section id="comandos" class="section">
      <h2 class="section-title">Comandos Essenciais do Dia a Dia</h2>
      <p class="section-desc">Estes são os comandos que você utilizará com mais frequência em sua carreira:</p>

      <div class="grid-3">
        <article class="command-card">
          <code>git status</code>
          <h4>Ver o Estado</h4>
          <p>Mostra quais arquivos foram criados, alterados ou estão prontos para commit.</p>
        </article>

        <article class="command-card">
          <code>git add .</code>
          <h4>Preparar Arquivos</h4>
          <p>Coloca as alterações na Staging Area (área de preparação antes da foto).</p>
        </article>

        <article class="command-card">
          <code>git commit -m "..."</code>
          <h4>Registrar Versão</h4>
          <p>Salva permanentemente a foto atual das alterações com uma mensagem descritiva.</p>
        </article>

        <article class="command-card">
          <code>git push</code>
          <h4>Enviar para a Nuvem</h4>
          <p>Envia os commits locais do seu computador para o repositório no GitHub.</p>
        </article>

        <article class="command-card">
          <code>git pull</code>
          <h4>Puxar Atualizações</h4>
          <p>Baixa alterações do repositório remoto para o seu computador local.</p>
        </article>

        <article class="command-card">
          <code>git branch</code>
          <h4>Gerenciar Ramificações</h4>
          <p>Cria e visualiza ramificações seguras para desenvolver novas funcionalidades.</p>
        </article>
      </div>
    </section>

    <!-- Seção Meu Perfil de Desenvolvedor -->
    <section id="perfil" class="section">
      <h2 class="section-title">Perfil do Desenvolvedor</h2>
      <div class="profile-card">
        <div class="avatar-placeholder">🧑‍💻</div>
        <div class="profile-info">
          <h3>Seu Nome Aqui</h3>
          <p class="role">Estudante de Desenvolvimento de Sistemas</p>
          <p class="bio">Apaixonado por tecnologia, aprendendo controle de versão com Git e GitHub para construir projetos em equipe!</p>
          <div class="tags">
            <span class="tag">HTML5</span>
            <span class="tag">CSS3</span>
            <span class="tag">Git</span>
            <span class="tag">GitHub</span>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- Rodapé -->
  <footer class="footer">
    <div class="container footer-content">
      <p>Construído durante a aula de Git & GitHub — GitHub Academy</p>
      <p class="copyright">Versão 1.0 • Desenvolvido para fins educacionais</p>
    </div>
  </footer>
</body>
</html>
```

---

### Passo 3: Criar o arquivo `style.css`

Na mesma pasta, crie o arquivo `style.css` e cole o código completo abaixo:

```css
:root {
  --bg-primary: #0d1117;
  --bg-secondary: #161b22;
  --bg-tertiary: #21262d;
  --border-color: #30363d;
  --text-main: #c9d1d9;
  --text-muted: #8b949e;
  --text-white: #ffffff;
  --accent-blue: #58a6ff;
  --accent-green: #238636;
  --accent-green-hover: #2ea043;
  --accent-purple: #bc8cff;
  --font-sans: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-mono: 'Fira Code', monospace;
  --transition: all 0.2s ease-in-out;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: var(--bg-primary);
  color: var(--text-main);
  font-family: var(--font-sans);
  line-height: 1.6;
  padding-bottom: 3rem;
}

.container {
  width: 90%;
  max-width: 1000px;
  margin: 0 auto;
}

/* Navbar */
.navbar {
  background-color: rgba(22, 27, 34, 0.9);
  backdrop-filter: blur(8px);
  border-bottom: 1px solid var(--border-color);
  position: sticky;
  top: 0;
  z-index: 100;
  padding: 0.8rem 0;
}

.nav-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 1.2rem;
  color: var(--text-white);
}

.logo strong {
  color: var(--accent-blue);
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 1.5rem;
}

.nav-links a {
  color: var(--text-muted);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
  transition: var(--transition);
}

.nav-links a:hover {
  color: var(--accent-blue);
}

/* Hero */
.hero {
  padding: 4.5rem 0 3.5rem;
  text-align: center;
  border-bottom: 1px solid var(--border-color);
  background: radial-gradient(circle at 50% 20%, rgba(88, 166, 255, 0.08) 0%, transparent 70%);
}

.badge {
  display: inline-block;
  background-color: rgba(88, 166, 255, 0.15);
  color: var(--accent-blue);
  border: 1px solid rgba(88, 166, 255, 0.3);
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  margin-bottom: 1.2rem;
  letter-spacing: 0.5px;
}

.hero h1 {
  font-size: 2.6rem;
  color: var(--text-white);
  line-height: 1.2;
  margin-bottom: 1rem;
}

.hero h1 span {
  color: var(--accent-blue);
}

.hero p {
  font-size: 1.15rem;
  color: var(--text-muted);
  max-width: 650px;
  margin: 0 auto 2rem;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn {
  display: inline-block;
  padding: 0.75rem 1.6rem;
  border-radius: 6px;
  font-size: 0.95rem;
  font-weight: 600;
  text-decoration: none;
  transition: var(--transition);
}

.btn-primary {
  background-color: var(--accent-green);
  color: #ffffff;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.btn-primary:hover {
  background-color: var(--accent-green-hover);
  transform: translateY(-2px);
}

.btn-secondary {
  background-color: var(--bg-tertiary);
  color: var(--text-white);
  border: 1px solid var(--border-color);
}

.btn-secondary:hover {
  background-color: var(--border-color);
  transform: translateY(-2px);
}

/* Seções */
.section {
  padding: 3.5rem 0 1rem;
}

.section-title {
  font-size: 1.8rem;
  color: var(--text-white);
  margin-bottom: 0.5rem;
  text-align: center;
}

.section-desc {
  text-align: center;
  color: var(--text-muted);
  margin-bottom: 2rem;
  font-size: 1rem;
}

/* Grids */
.grid-2 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}

.grid-3 {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.2rem;
}

/* Cards Conceito */
.card {
  background-color: var(--bg-secondary);
  border: 1px solid var(--border-color);
  border-radius: 8px;
  padding: 1.8rem;
  transition: var(--transition);
}

.card:hover {
  border-color: var(--accent-blue);
  transform: translateY(-3px);
}

.card-icon {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.card h3 {
  color: var(--text-white);
  font-size: 1.25rem;
  margin-bottom: 0.7rem;
}

.card p {
  color: var(--text-muted);
  font-size: 0.95rem;
}

/* Cards Comandos */
.command-card {
  background-color: var(--bg-secondary);
  border: 1px solid var(--border-color);
  border-radius: 8px;
  padding: 1.4rem;
  transition: var(--transition);
}

.command-card:hover {
  border-color: var(--accent-purple);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
}

.command-card code {
  display: inline-block;
  background-color: var(--bg-primary);
  border: 1px solid var(--border-color);
  color: var(--accent-blue);
  font-family: var(--font-mono);
  font-size: 0.9rem;
  padding: 0.25rem 0.55rem;
  border-radius: 4px;
  margin-bottom: 0.8rem;
}

.command-card h4 {
  color: var(--text-white);
  font-size: 1.05rem;
  margin-bottom: 0.4rem;
}

.command-card p {
  color: var(--text-muted);
  font-size: 0.88rem;
}

/* Perfil do Aluno */
.profile-card {
  background-color: var(--bg-secondary);
  border: 1px solid var(--border-color);
  border-radius: 10px;
  padding: 2rem;
  display: flex;
  align-items: center;
  gap: 1.8rem;
  margin-top: 1.5rem;
}

.avatar-placeholder {
  font-size: 3.5rem;
  background-color: var(--bg-tertiary);
  width: 90px;
  height: 90px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 2px solid var(--accent-blue);
  flex-shrink: 0;
}

.profile-info h3 {
  color: var(--text-white);
  font-size: 1.4rem;
}

.profile-info .role {
  color: var(--accent-blue);
  font-weight: 500;
  font-size: 0.95rem;
  margin-bottom: 0.5rem;
}

.profile-info .bio {
  color: var(--text-muted);
  font-size: 0.95rem;
  margin-bottom: 1rem;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  background-color: var(--bg-tertiary);
  color: var(--text-main);
  border: 1px solid var(--border-color);
  padding: 0.2rem 0.6rem;
  border-radius: 4px;
  font-size: 0.8rem;
  font-family: var(--font-mono);
}

/* Rodapé */
.footer {
  margin-top: 4rem;
  border-top: 1px solid var(--border-color);
  padding-top: 2rem;
  text-align: center;
  color: var(--text-muted);
  font-size: 0.9rem;
}

.footer .copyright {
  margin-top: 0.4rem;
  font-size: 0.8rem;
}

/* Responsividade simples */
@media (max-width: 600px) {
  .hero h1 {
    font-size: 2rem;
  }
  .profile-card {
    flex-direction: column;
    text-align: center;
  }
}
```

---

## Verificação Rápida

1. Dê um duplo clique no arquivo `index.html` ou abra-o com seu navegador favorito (Chrome, Firefox, Edge).
2. O site deve carregar com um visual escuro moderno, botões interativos e cartões bem alinhados.
3. Se o visual estiver bonito e legível, seu projeto base está 100% pronto para receber o Git!

> Próximo passo: Vamos transformar essa pasta comum em um repositório Git no [Bloco 05 — git init](05-git-init.md).
