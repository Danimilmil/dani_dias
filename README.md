<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Daniel Dias · Portfólio</title>
<style>
  :root {
    --bg-1: #0b0d12;
    --bg-2: #12151d;
    --bg-3: #1a1f2b;
    --accent: #d4a24e;
    --accent-2: #7ee787;
    --accent-3: #58a6ff;
    --text: #e6e6e6;
    --text-dim: #9aa3b2;
    --border: rgba(212, 162, 78, 0.25);
    --glow: rgba(212, 162, 78, 0.15);
  }

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  html {
    scroll-behavior: smooth;
  }

  body {
    font-family: 'Segoe UI', 'Inter', system-ui, -apple-system, sans-serif;
    background:
      radial-gradient(ellipse at top left, rgba(212, 162, 78, 0.08), transparent 50%),
      radial-gradient(ellipse at bottom right, rgba(88, 166, 255, 0.06), transparent 50%),
      linear-gradient(160deg, var(--bg-1) 0%, var(--bg-2) 50%, var(--bg-3) 100%);
    background-attachment: fixed;
    color: var(--text);
    line-height: 1.7;
    min-height: 100vh;
    padding: 0 20px;
    position: relative;
    overflow-x: hidden;
  }

  /* Linhas panorâmicas decorativas */
  body::before {
    content: "";
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image:
      linear-gradient(rgba(212, 162, 78, 0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(212, 162, 78, 0.03) 1px, transparent 1px);
    background-size: 80px 80px;
    pointer-events: none;
    z-index: -1;
    mask-image: radial-gradient(ellipse at center, black 30%, transparent 80%);
    -webkit-mask-image: radial-gradient(ellipse at center, black 30%, transparent 80%);
  }

  /* Container panorâmico */
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 60px 0 80px;
  }

  /* Cabeçalho */
  .hero {
    text-align: center;
    padding: 40px 30px;
    margin-bottom: 60px;
    border: 1px solid var(--border);
    border-radius: 24px;
    background: linear-gradient(145deg, rgba(26, 31, 43, 0.9), rgba(18, 21, 29, 0.9));
    backdrop-filter: blur(10px);
    box-shadow:
      0 0 60px var(--glow),
      inset 0 1px 0 rgba(255, 255, 255, 0.05);
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 60%;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--accent), transparent);
  }

  .hero::after {
    content: "";
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: conic-gradient(from 0deg, transparent, rgba(212, 162, 78, 0.08), transparent 30%);
    animation: rotate 20s linear infinite;
    pointer-events: none;
  }

  @keyframes rotate {
    to { transform: rotate(360deg); }
  }

  .hero h1 {
    font-size: 3.2rem;
    font-weight: 800;
    letter-spacing: -1px;
    background: linear-gradient(135deg, #fff 0%, var(--accent) 60%, #b8862b 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 12px;
    position: relative;
    z-index: 1;
  }

  .hero h3 {
    font-size: 1rem;
    font-weight: 400;
    color: var(--text-dim);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 28px;
    position: relative;
    z-index: 1;
  }

  .social-links {
    display: flex;
    gap: 14px;
    justify-content: center;
    flex-wrap: wrap;
    position: relative;
    z-index: 1;
  }

  .social-links a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 1px solid var(--border);
    border-radius: 10px;
    background: rgba(11, 13, 18, 0.6);
    color: var(--text);
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 600;
    letter-spacing: 1px;
    transition: all 0.3s ease;
  }

  .social-links a:hover {
    border-color: var(--accent);
    box-shadow: 0 0 20px var(--glow);
    transform: translateY(-3px);
    color: var(--accent);
  }

  .social-links img {
    filter: brightness(0) invert(1);
    transition: filter 0.3s ease;
  }

  .social-links a:hover img {
    filter: brightness(0) invert(0.8) sepia(1) saturate(5) hue-rotate(5deg);
  }

  /* Seções */
  section {
    margin-bottom: 60px;
  }

  section h2 {
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--accent);
    margin-bottom: 24px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
    letter-spacing: 1px;
    text-transform: uppercase;
    position: relative;
  }

  section h2::after {
    content: "";
    position: absolute;
    bottom: -1px;
    left: 0;
    width: 80px;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), transparent);
  }

  /* Sobre mim */
  .about p {
    color: var(--text-dim);
    margin-bottom: 16px;
    font-size: 1.02rem;
  }

  .about strong {
    color: var(--accent);
    font-weight: 600;
  }

  /* Stack */
  .stack-group {
    margin-bottom: 30px;
    padding: 20px 24px;
    background: linear-gradient(145deg, rgba(26, 31, 43, 0.7), rgba(18, 21, 29, 0.7));
    border: 1px solid var(--border);
    border-radius: 14px;
    transition: all 0.3s ease;
  }

  .stack-group:hover {
    border-color: var(--accent);
    box-shadow: 0 0 30px var(--glow);
    transform: translateX(4px);
  }

  .stack-group h3 {
    font-size: 0.9rem;
    color: var(--accent-2);
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 12px;
    font-weight: 600;
  }

  .stack-group p {
    color: var(--text);
    font-size: 1rem;
    margin-top: 10px;
    font-weight: 500;
  }

  .stack-group img {
    margin-bottom: 8px;
  }

  /* Áreas de interesse */
  .interests-table {
    width: 100%;
    border-collapse: separate;
    border-spacing: 12px 0;
  }

  .interests-table td {
    text-align: center;
    padding: 24px 12px;
    background: linear-gradient(145deg, rgba(26, 31, 43, 0.8), rgba(18, 21, 29, 0.8));
    border: 1px solid var(--border);
    border-radius: 14px;
    transition: all 0.3s ease;
    vertical-align: middle;
  }

  .interests-table td:hover {
    border-color: var(--accent);
    box-shadow: 0 0 25px var(--glow);
    transform: translateY(-4px);
  }

  .interests-table td .emoji {
    font-size: 2rem;
    display: block;
    margin-bottom: 10px;
  }

  .interests-table td strong {
    color: var(--accent);
    font-size: 0.9rem;
    letter-spacing: 0.5px;
  }

  /* Tabela de conhecimentos */
  .knowledge-table {
    width: 100%;
    border-collapse: collapse;
    background: linear-gradient(145deg, rgba(26, 31, 43, 0.7), rgba(18, 21, 29, 0.7));
    border: 1px solid var(--border);
    border-radius: 14px;
    overflow: hidden;
  }

  .knowledge-table th,
  .knowledge-table td {
    padding: 14px 20px;
    text-align: left;
    border-bottom: 1px solid rgba(212, 162, 78, 0.1);
  }

  .knowledge-table th {
    background: rgba(212, 162, 78, 0.08);
    color: var(--accent);
    font-weight: 700;
    font-size: 0.85rem;
    text-transform: uppercase;
    letter-spacing: 1.5px;
  }

  .knowledge-table td {
    color: var(--text-dim);
    font-size: 0.95rem;
  }

  .knowledge-table tr:last-child td {
    border-bottom: none;
  }

  .knowledge-table tr:hover td {
    background: rgba(212, 162, 78, 0.04);
    color: var(--text);
  }

  .knowledge-table td:first-child {
    color: var(--accent-2);
    font-weight: 600;
    white-space: nowrap;
  }

  /* Atualmente estudando */
  .roadmap {
    padding: 30px;
    background: linear-gradient(145deg, rgba(26, 31, 43, 0.8), rgba(18, 21, 29, 0.8));
    border: 1px solid var(--border);
    border-radius: 14px;
    text-align: center;
  }

  .roadmap p {
    color: var(--text);
    font-size: 1.1rem;
    font-weight: 600;
    letter-spacing: 1px;
    padding: 8px 0;
  }

  .roadmap .arrow {
    color: var(--accent);
    font-size: 1.4rem;
    display: block;
    margin: 4px 0;
    animation: bounce 2s ease-in-out infinite;
  }

  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(4px); }
  }

  /* Divisores */
  hr {
    border: none;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 50px 0;
  }

  /* Responsivo */
  @media (max-width: 768px) {
    .hero h1 { font-size: 2.2rem; }
    .hero h3 { font-size: 0.8rem; letter-spacing: 1px; }
    .interests-table { border-spacing: 6px 0; }
    .interests-table td { padding: 16px 6px; }
    .interests-table td .emoji { font-size: 1.5rem; }
    .interests-table td strong { font-size: 0.75rem; }
    .knowledge-table th, .knowledge-table td { padding: 10px 12px; font-size: 0.85rem; }
    section h2 { font-size: 1.3rem; }
  }

  @media (max-width: 480px) {
    .interests-table { border-spacing: 3px 0; }
    .interests-table td { padding: 12px 3px; }
    .interests-table td strong { font-size: 0.65rem; }
    .interests-table td .emoji { font-size: 1.2rem; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <div class="hero" align="center">
    <h1>Daniel Dias</h1>
    <h3>Estudante de Informática para Web · Tecnologia · Qualidade · Infraestrutura</h3>
    <div class="social-links">
      <a href="https://github.com/Danimilmil/dani_dias">
        <img src="https://img.shields.io/badge/GitHub-18181B?style=flat-square&logo=github&logoColor=white">
      </a>
      <a href="https://www.linkedin.com/in/daniel-dias-37a639375/">
        <img src="https://img.shields.io/badge/LinkedIn-18181B?style=flat-square&logo=linkedin&logoColor=white">
      </a>
      <a href="https://mail.google.com/mail/?view=cm&fs=1&to=ddias6574@gmail.com">
        <img src="https://img.shields.io/badge/Email-18181B?style=flat-square&logo=gmail&logoColor=white">
      </a>
    </div>
  </div>

  <hr>

  <!-- SOBRE MIM -->
  <section class="about">
    <h2>Sobre mim</h2>
    <p>Sou estudante de <strong>Informática para Web</strong>, interessado em tecnologia, qualidade de software e infraestrutura.</p>
    <p>Meu objetivo é construir uma carreira em TI explorando principalmente <strong>Banco de Dados, QA, DevOps, Computação em Nuvem e Cibersegurança</strong>.</p>
    <p>Tenho interesse em entender não apenas o desenvolvimento de aplicações, mas também os processos, ambientes e tecnologias que tornam sistemas mais <strong>seguros, confiáveis e eficientes</strong>.</p>
    <p>Atualmente, busco minha <strong>primeira oportunidade profissional na área de TI</strong>, enquanto continuo aprimorando meus conhecimentos por meio de estudos e projetos práticos.</p>
  </section>

  <hr>

  <!-- STACK -->
  <section>
    <h2>Stack &amp; Ferramentas</h2>

    <div class="stack-group">
      <h3>Desenvolvimento</h3>
      <p><img src="https://skillicons.dev/icons?i=html,css,js" alt="HTML, CSS, JavaScript"></p>
      <p><strong>HTML · CSS · JavaScript</strong></p>
    </div>

    <div class="stack-group">
      <h3>Mobile</h3>
      <p><img src="https://skillicons.dev/icons?i=react" alt="React Native"></p>
      <p><strong>React Native</strong></p>
    </div>

    <div class="stack-group">
      <h3>Qualidade de Software</h3>
      <p><img src="https://skillicons.dev/icons?i=jest" alt="Jest"></p>
      <p><strong>Jest · Testes automatizados · QA</strong></p>
    </div>

    <div class="stack-group">
      <h3>Banco de Dados</h3>
      <p><img src="https://skillicons.dev/icons?i=mysql" alt="MySQL"></p>
      <p><strong>MySQL · SQL · Modelagem de dados</strong></p>
    </div>

    <div class="stack-group">
      <h3>Versionamento</h3>
      <p><img src="https://skillicons.dev/icons?i=git,github" alt="Git, GitHub"></p>
      <p><strong>Git · GitHub · Controle de versão</strong></p>
    </div>

    <div class="stack-group">
      <h3>Sistemas</h3>
      <p><img src="https://skillicons.dev/icons?i=linux" alt="Linux"></p>
      <p><strong>Linux · Terminal · Linha de comando</strong></p>
    </div>
  </section>

  <hr>

  <!-- ÁREAS DE INTERESSE -->
  <section>
    <h2>Áreas de interesse</h2>
    <table class="interests-table">
      <tr>
        <td width="20%">
          <span class="emoji">🗄️</span>
          <strong>Banco de Dados</strong>
        </td>
        <td width="20%">
          <span class="emoji">🧪</span>
          <strong>QA</strong>
        </td>
        <td width="20%">
          <span class="emoji">⚙️</span>
          <strong>DevOps</strong>
        </td>
        <td width="20%">
          <span class="emoji">☁️</span>
          <strong>Cloud</strong>
        </td>
        <td width="20%">
          <span class="emoji">🔐</span>
          <strong>Cibersegurança</strong>
        </td>
      </tr>
    </table>
  </section>

  <hr>

  <!-- CONHECIMENTOS -->
  <section>
    <h2>Conhecimentos</h2>
    <table class="knowledge-table">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Tecnologias</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Web</td>
          <td>HTML · CSS · JavaScript</td>
        </tr>
        <tr>
          <td>Mobile</td>
          <td>React Native</td>
        </tr>
        <tr>
          <td>Testes</td>
          <td>Jest · Testes automatizados</td>
        </tr>
        <tr>
          <td>Banco de Dados</td>
          <td>MySQL · SQL · Modelagem de dados</td>
        </tr>
        <tr>
          <td>Versionamento</td>
          <td>Git · GitHub</td>
        </tr>
        <tr>
          <td>Sistemas</td>
          <td>Linux · Terminal</td>
        </tr>
      </tbody>
    </table>
  </section>

  <hr>

  <!-- ATUALMENTE ESTUDANDO -->
  <section>
    <h2>Atualmente estudando</h2>
    <div class="roadmap">
      <p>Banco de Dados</p>
      <span class="arrow">↓</span>
      <p>Quality Assurance</p>
      <span class="arrow">↓</span>
      <p>DevOps</p>
      <span class="arrow">↓</span>
      <p>Computação em Nuvem</p>
      <span class="arrow">↓</span>
      <p>Cibersegurança</p>
    </div>
  </section>

</div>
</body>
</html>
