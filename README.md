<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Daniel Dias · 先生 · Portfólio</title>
<style>
  :root {
    --bg-deep: #0d0a0a;
    --bg-1: #1a1210;
    --bg-2: #241814;
    --bg-3: #2e1e18;
    --torii: #b8302a;
    --torii-light: #e04a3a;
    --gold: #c9a04e;
    --gold-light: #e8c777;
    --washi: #f2e8d5;
    --text: #ede4d3;
    --text-dim: #b0a08a;
    --border: rgba(201, 160, 78, 0.28);
    --glow: rgba(184, 48, 42, 0.25);
    --glow-gold: rgba(201, 160, 78, 0.18);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body {
    font-family: 'Yu Mincho', 'Hiragino Mincho ProN', 'Georgia', serif;
    background:
      radial-gradient(ellipse at top, rgba(184, 48, 42, 0.14), transparent 55%),
      radial-gradient(ellipse at bottom right, rgba(201, 160, 78, 0.08), transparent 50%),
      linear-gradient(165deg, var(--bg-deep) 0%, var(--bg-1) 35%, var(--bg-2) 70%, var(--bg-3) 100%);
    background-attachment: fixed;
    color: var(--text);
    line-height: 1.75;
    min-height: 100vh;
    padding: 0 20px;
    position: relative;
    overflow-x: hidden;
  }

  /* Textura de papel washi + linhas panorâmicas */
  body::before {
    content: "";
    position: fixed;
    inset: 0;
    background-image:
      repeating-linear-gradient(0deg, rgba(201, 160, 78, 0.025) 0px, rgba(201, 160, 78, 0.025) 1px, transparent 1px, transparent 3px),
      linear-gradient(rgba(201, 160, 78, 0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(201, 160, 78, 0.04) 1px, transparent 1px);
    background-size: 100% 3px, 90px 90px, 90px 90px;
    pointer-events: none;
    z-index: -1;
    mask-image: radial-gradient(ellipse at center, black 25%, transparent 85%);
    -webkit-mask-image: radial-gradient(ellipse at center, black 25%, transparent 85%);
  }

  /* Círculo ensō decorativo */
  body::after {
    content: "";
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 900px;
    height: 900px;
    border: 1px solid rgba(184, 48, 42, 0.06);
    border-radius: 50%;
    box-shadow: 0 0 120px rgba(184, 48, 42, 0.05) inset;
    pointer-events: none;
    z-index: -1;
    animation: breathe 8s ease-in-out infinite;
  }

  @keyframes breathe {
    0%, 100% { transform: translate(-50%, -50%) scale(1); opacity: 0.8; }
    50% { transform: translate(-50%, -50%) scale(1.04); opacity: 1; }
  }

  .container {
    max-width: 1080px;
    margin: 0 auto;
    padding: 60px 0 90px;
  }

  /* HERO */
  .hero {
    text-align: center;
    padding: 50px 30px 40px;
    margin-bottom: 55px;
    border: 1px solid var(--border);
    border-radius: 4px;
    background: linear-gradient(150deg, rgba(36, 24, 20, 0.92), rgba(13, 10, 10, 0.92));
    box-shadow:
      0 0 70px var(--glow),
      0 0 140px var(--glow-gold),
      inset 0 0 40px rgba(184, 48, 42, 0.06);
    position: relative;
    overflow: hidden;
  }

  /* Faixa torii superior */
  .hero::before {
    content: "";
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 4px;
    background: linear-gradient(90deg, transparent, var(--torii) 20%, var(--torii-light) 50%, var(--torii) 80%, transparent);
    box-shadow: 0 0 20px var(--torii);
  }

  /* Kanji decorativo de fundo */
  .hero .kanji-bg {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 22rem;
    font-weight: 900;
    color: rgba(184, 48, 42, 0.05);
    font-family: 'Yu Mincho', serif;
    line-height: 1;
    pointer-events: none;
    user-select: none;
    z-index: 0;
  }

  .hero > * { position: relative; z-index: 1; }

  .hero .seal {
    display: inline-block;
    width: 54px;
    height: 54px;
    line-height: 54px;
    border-radius: 50%;
    background: var(--torii);
    color: var(--washi);
    font-size: 1.4rem;
    font-weight: 700;
    font-family: 'Yu Mincho', serif;
    margin-bottom: 18px;
    box-shadow: 0 0 24px var(--glow), inset 0 0 12px rgba(0,0,0,0.4);
    transform: rotate(-6deg);
  }

  .hero h1 {
    font-size: 3.2rem;
    font-weight: 800;
    letter-spacing: 2px;
    background: linear-gradient(135deg, var(--washi) 0%, var(--gold-light) 50%, var(--gold) 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 10px;
    font-family: 'Yu Mincho', 'Georgia', serif;
  }

  .hero .jp-name {
    font-size: 1rem;
    color: var(--torii-light);
    letter-spacing: 8px;
    margin-bottom: 14px;
    font-family: 'Yu Mincho', serif;
  }

  .hero h3 {
    font-size: 0.95rem;
    font-weight: 400;
    color: var(--text-dim);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 28px;
    font-family: 'Segoe UI', sans-serif;
  }

  .social-links {
    display: flex;
    gap: 14px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .social-links a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 1px solid var(--border);
    border-radius: 3px;
    background: rgba(13, 10, 10, 0.7);
    color: var(--text);
    text-decoration: none;
    font-size: 0.85rem;
    font-weight: 600;
    letter-spacing: 1px;
    font-family: 'Segoe UI', sans-serif;
    transition: all 0.35s ease;
    position: relative;
    overflow: hidden;
  }

  .social-links a::before {
    content: "";
    position: absolute;
    top: 0; left: -100%;
    width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(184, 48, 42, 0.3), transparent);
    transition: left 0.5s ease;
  }

  .social-links a:hover::before { left: 100%; }

  .social-links a:hover {
    border-color: var(--torii-light);
    box-shadow: 0 0 22px var(--glow);
    transform: translateY(-3px);
    color: var(--gold-light);
  }

  .social-links img { filter: brightness(0) invert(1); transition: filter 0.3s; }
  .social-links a:hover img { filter: brightness(0) invert(0.85) sepia(1) saturate(4) hue-rotate(340deg); }

  /* SEÇÕES */
  section { margin-bottom: 55px; }

  section h2 {
    font-size: 1.45rem;
    font-weight: 700;
    color: var(--gold-light);
    margin-bottom: 26px;
    padding: 0 0 14px 18px;
    letter-spacing: 3px;
    text-transform: uppercase;
    position: relative;
    font-family: 'Yu Mincho', 'Segoe UI', serif;
    border-left: 3px solid var(--torii);
  }

  section h2::after {
    content: "";
    position: absolute;
    bottom: 0; left: 0;
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  section h2 .kanji {
    color: var(--torii-light);
    font-size: 0.85rem;
    margin-left: 12px;
    letter-spacing: 2px;
    opacity: 0.8;
  }

  /* SOBRE */
  .about p { color: var(--text-dim); margin-bottom: 16px; font-size: 1.02rem; }
  .about strong { color: var(--gold-light); font-weight: 600; }

  /* BLOCO ÚNICO DE TECNOLOGIAS */
  .tech-block {
    padding: 34px 30px;
    background:
      linear-gradient(150deg, rgba(36, 24, 20, 0.85), rgba(13, 10, 10, 0.85));
    border: 1px solid var(--border);
    border-radius: 4px;
    position: relative;
    box-shadow: inset 0 0 50px rgba(184, 48, 42, 0.05), 0 0 40px rgba(0,0,0,0.4);
  }

  .tech-block::before,
  .tech-block::after {
    content: "";
    position: absolute;
    width: 22px; height: 22px;
    border: 2px solid var(--torii);
    opacity: 0.7;
  }
  .tech-block::before { top: -1px; left: -1px; border-right: none; border-bottom: none; }
  .tech-block::after  { bottom: -1px; right: -1px; border-left: none; border-top: none; }

  .tech-item {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 16px 8px;
    border-bottom: 1px dashed rgba(201, 160, 78, 0.15);
    transition: all 0.3s ease;
  }

  .tech-item:last-child { border-bottom: none; }

  .tech-item:hover {
    padding-left: 18px;
    background: linear-gradient(90deg, rgba(184, 48, 42, 0.08), transparent);
  }

  .tech-item .label {
    flex: 0 0 190px;
    display: flex;
    align-items: center;
    gap: 10px;
    font-family: 'Segoe UI', sans-serif;
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    color: var(--torii-light);
  }

  .tech-item .label .jp {
    font-family: 'Yu Mincho', serif;
    font-size: 1.1rem;
    color: var(--gold);
    opacity: 0.85;
    min-width: 28px;
  }

  .tech-item .icons {
    flex: 1;
    display: flex;
    align-items: center;
    gap: 12px;
    flex-wrap: wrap;
  }

  .tech-item .icons img {
    transition: transform 0.3s ease, filter 0.3s ease;
    filter: drop-shadow(0 0 4px rgba(201, 160, 78, 0.15));
  }

  .tech-item:hover .icons img {
    transform: translateY(-3px) scale(1.08);
    filter: drop-shadow(0 0 8px rgba(201, 160, 78, 0.5));
  }

  .tech-item .desc {
    color: var(--text);
    font-size: 0.92rem;
    font-weight: 500;
    font-family: 'Segoe UI', sans-serif;
    margin-left: auto;
    opacity: 0.85;
  }

  /* ÁREAS DE INTERESSE */
  .interests-table {
    width: 100%;
    border-collapse: separate;
    border-spacing: 10px 0;
  }

  .interests-table td {
    text-align: center;
    padding: 26px 12px;
    background: linear-gradient(155deg, rgba(36, 24, 20, 0.85), rgba(13, 10, 10, 0.85));
    border: 1px solid var(--border);
    border-radius: 4px;
    transition: all 0.35s ease;
    vertical-align: middle;
    position: relative;
    overflow: hidden;
  }

  .interests-table td::before {
    content: "";
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--torii), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }

  .interests-table td:hover::before { opacity: 1; }

  .interests-table td:hover {
    border-color: var(--torii-light);
    box-shadow: 0 0 28px var(--glow);
    transform: translateY(-5px);
  }

  .interests-table td .emoji {
    font-size: 2rem;
    display: block;
    margin-bottom: 10px;
  }

  .interests-table td strong {
    color: var(--gold-light);
    font-size: 0.88rem;
    letter-spacing: 0.5px;
    font-family: 'Segoe UI', sans-serif;
  }

  .interests-table td .jp-sub {
    display: block;
    font-family: 'Yu Mincho', serif;
    font-size: 0.72rem;
    color: var(--text-dim);
    margin-top: 4px;
    letter-spacing: 1px;
  }

  /* TABELA DE CONHECIMENTOS */
  .knowledge-table {
    width: 100%;
    border-collapse: collapse;
    background: linear-gradient(150deg, rgba(36, 24, 20, 0.85), rgba(13, 10, 10, 0.85));
    border: 1px solid var(--border);
    border-radius: 4px;
    overflow: hidden;
    font-family: 'Segoe UI', sans-serif;
  }

  .knowledge-table th,
  .knowledge-table td {
    padding: 14px 20px;
    text-align: left;
    border-bottom: 1px solid rgba(201, 160, 78, 0.1);
  }

  .knowledge-table th {
    background: rgba(184, 48, 42, 0.12);
    color: var(--gold-light);
    font-weight: 700;
    font-size: 0.82rem;
    text-transform: uppercase;
    letter-spacing: 2px;
  }

  .knowledge-table td { color: var(--text-dim); font-size: 0.93rem; }
  .knowledge-table tr:last-child td { border-bottom: none; }
  .knowledge-table tr:hover td { background: rgba(184, 48, 42, 0.05); color: var(--text); }
  .knowledge-table td:first-child { color: var(--torii-light); font-weight: 600; white-space: nowrap; }

  /* ROADMAP */
  .roadmap {
    padding: 34px 30px;
    background: linear-gradient(150deg, rgba(36, 24, 20, 0.85), rgba(13, 10, 10, 0.85));
    border: 1px solid var(--border);
    border-radius: 4px;
    text-align: center;
    position: relative;
  }

  .roadmap p {
    color: var(--text);
    font-size: 1.08rem;
    font-weight: 600;
    letter-spacing: 2px;
    padding: 8px 0;
    font-family: 'Yu Mincho', 'Segoe UI', serif;
  }

  .roadmap .arrow {
    color: var(--torii-light);
    font-size: 1.3rem;
    display: block;
    margin: 2px 0;
    animation: bounce 2.2s ease-in-out infinite;
  }

  @keyframes bounce {
    0%, 100% { transform: translateY(0); opacity: 0.6; }
    50% { transform: translateY(4px); opacity: 1; }
  }

  /* DIVISORES */
  hr {
    border: none;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 45px 0;
    position: relative;
  }

  hr::after {
    content: "❀";
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: var(--torii);
    font-size: 0.85rem;
    background: var(--bg-1);
    padding: 0 12px;
    opacity: 0.7;
  }

  /* RESPONSIVO */
  @media (max-width: 768px) {
    .hero h1 { font-size: 2.2rem; }
    .hero h3 { font-size: 0.78rem; letter-spacing: 1px; }
    .hero .kanji-bg { font-size: 14rem; }
    .tech-item { flex-direction: column; align-items: flex-start; gap: 10px; }
    .tech-item .label { flex: none; }
    .tech-item .desc { margin-left: 0; }
    .interests-table { border-spacing: 5px 0; }
    .interests-table td { padding: 16px 6px; }
    .interests-table td .emoji { font-size: 1.5rem; }
    .interests-table td strong { font-size: 0.75rem; }
    .knowledge-table th, .knowledge-table td { padding: 10px 12px; font-size: 0.85rem; }
    section h2 { font-size: 1.15rem; letter-spacing: 2px; }
  }

  @media (max-width: 480px) {
    .interests-table { border-spacing: 3px 0; }
    .interests-table td { padding: 12px 3px; }
    .interests-table td strong { font-size: 0.65rem; }
    .interests-table td .jp-sub { display: none; }
    .interests-table td .emoji { font-size: 1.2rem; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <div class="hero" align="center">
    <div class="kanji-bg">先</div>
    <div class="seal">先</div>
    <h1>Daniel Dias</h1>
    <div class="jp-name">ダニエル・ディアス</div>
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
    <h2>Sobre mim <span class="kanji">自己紹介</span></h2>
    <p>Sou estudante de <strong>Informática para Web</strong>, interessado em tecnologia, qualidade de software e infraestrutura.</p>
    <p>Meu objetivo é construir uma carreira em TI explorando principalmente <strong>Banco de Dados, QA, DevOps, Computação em Nuvem e Cibersegurança</strong>.</p>
    <p>Tenho interesse em entender não apenas o desenvolvimento de aplicações, mas também os processos, ambientes e tecnologias que tornam sistemas mais <strong>seguros, confiáveis e eficientes</strong>.</p>
    <p>Atualmente, busco minha <strong>primeira oportunidade profissional na área de TI</strong>, enquanto continuo aprimorando meus conhecimentos por meio de estudos e projetos práticos.</p>
  </section>

  <hr>

  <!-- BLOCO ÚNICO DE TECNOLOGIAS -->
  <section>
    <h2>Stack &amp; Ferramentas <span class="kanji">技術</span></h2>

    <div class="tech-block">

      <div class="tech-item">
        <div class="label"><span class="jp">開</span> Desenvolvimento</div>
        <div class="icons">
          <img src="https://skillicons.dev/icons?i=html" alt="HTML">
          <img src="https://skillicons.dev/icons?i=css" alt="CSS">
          <img src="https://skillicons.dev/icons?i=js" alt="JavaScript">
        </div>
        <div class="desc">HTML · CSS · JavaScript</div>
      </div>

      <div class="tech-item">
        <div class="label"><span class="jp">携</span> Mobile</div>
        <div class="icons">
          <img src="https://skillicons.dev/icons?i=react" alt="React Native">
        </div>
        <div class="desc">React Native</div>
      </div>

      <div class="tech-item">
        <div class="label"><span class="jp">質</span> Qualidade</div>
        <div class="icons">
          <img src="https://skillicons.dev/icons?i=jest" alt="Jest">
        </div>
        <div class="desc">Jest · Testes automatizados · QA</div>
      </div>

      <div class="tech-item">
        <div class="label"><span class="jp">庫</span> Banco de Dados</div>
        <div class="icons">
          <img src="https://skillicons.dev/icons?i=mysql" alt="MySQL">
        </div>
        <div class="desc">MySQL · SQL · Modelagem de dados</div>
      </div>

      <div class="tech-item">
        <div class="label"><span class="jp">版</span> Versionamento</div>
        <div class="icons">
          <img src="https://skillicons.dev/icons?i=git" alt="Git">
          <img src="https://skillicons.dev/icons?i=github" alt="GitHub">
        </div>
        <div class="desc">Git · GitHub · Controle de versão</div>
      </div>

      <div class="tech-item">
        <div class="label"><span class="jp">系</span> Sistemas</div>
        <div class="icons">
          <img src="https://skillicons.dev/icons?i=linux" alt="Linux">
        </div>
        <div class="desc">Linux · Terminal · Linha de comando</div>
      </div>

    </div>
  </section>

  <hr>

  <!-- ÁREAS DE INTERESSE -->
  <section>
    <h2>Áreas de interesse <span class="kanji">興味</span></h2>
    <table class="interests-table">
      <tr>
        <td width="20%">
          <span class="emoji">🗄️</span>
          <strong>Banco de Dados</strong>
          <span class="jp-sub">データベース</span>
        </td>
        <td width="20%">
          <span class="emoji">🧪</span>
          <strong>QA</strong>
          <span class="jp-sub">品質保証</span>
        </td>
        <td width="20%">
          <span class="emoji">⚙️</span>
          <strong>DevOps</strong>
          <span class="jp-sub">開発運用</span>
        </td>
        <td width="20%">
          <span class="emoji">☁️</span>
          <strong>Cloud</strong>
          <span class="jp-sub">クラウド</span>
        </td>
        <td width="20%">
          <span class="emoji">🔐</span>
          <strong>Cibersegurança</strong>
          <span class="jp-sub">サイバー安全</span>
        </td>
      </tr>
    </table>
  </section>

  <hr>

  <!-- CONHECIMENTOS -->
  <section>
    <h2>Conhecimentos <span class="kanji">知識</span></h2>
    <table class="knowledge-table">
      <thead>
        <tr><th>Categoria</th><th>Tecnologias</th></tr>
      </thead>
      <tbody>
        <tr><td>Web</td><td>HTML · CSS · JavaScript</td></tr>
        <tr><td>Mobile</td><td>React Native</td></tr>
        <tr><td>Testes</td><td>Jest · Testes automatizados</td></tr>
        <tr><td>Banco de Dados</td><td>MySQL · SQL · Modelagem de dados</td></tr>
        <tr><td>Versionamento</td><td>Git · GitHub</td></tr>
        <tr><td>Sistemas</td><td>Linux · Terminal</td></tr>
      </tbody>
    </table>
  </section>

  <hr>

  <!-- ATUALMENTE ESTUDANDO -->
  <section>
    <h2>Atualmente estudando <span class="kanji">勉強中</span></h2>
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
