<style>
  /* ==========================================================================
     PERFIL — NEON CYBERPUNK EDITORIAL (Adaptado para GitHub)
     ========================================================================== */

  .cyber-profile {
    font-family: "Inter", "DM Sans", system-ui, sans-serif;
    color: #0d0620;
    background-color: #f5f2ff;
    background-image: 
      radial-gradient(circle at 12% 8%, rgba(255, 46, 136, 0.15), transparent 40%),
      radial-gradient(circle at 88% 12%, rgba(0, 212, 255, 0.15), transparent 40%),
      radial-gradient(circle at 50% 95%, rgba(181, 255, 46, 0.1), transparent 40%),
      radial-gradient(rgba(13, 6, 32, 0.08) 1px, transparent 1px);
    background-size: auto, auto, auto, 20px 20px;
    padding: 3rem 2rem;
    border-radius: 20px;
    margin: 1rem 0;
  }

  /* Tipografia */
  .cyber-profile h1 {
    font-family: "Space Grotesk", "Archivo Black", sans-serif;
    font-size: clamp(2.5rem, 6vw, 4rem);
    font-weight: 800;
    line-height: 1;
    background: linear-gradient(135deg, #ff2e88 0%, #7c3aed 50%, #00d4ff 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 0.5rem;
    filter: drop-shadow(0 4px 20px rgba(255, 46, 136, 0.2));
  }

  .cyber-profile h2 {
    font-family: "Space Grotesk", sans-serif;
    font-size: 1.8rem;
    font-weight: 800;
    color: #0d0620;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    border-bottom: none;
    margin-top: 2rem;
  }

  .cyber-profile h2::before {
    content: "";
    width: 10px;
    height: 1.8rem;
    background: linear-gradient(135deg, #ff2e88 0%, #00d4ff 100%);
    border-radius: 4px;
  }

  .cyber-profile h3 {
    font-family: "Space Grotesk", sans-serif;
    color: #6b5f8a;
    letter-spacing: 0.3em;
    text-transform: uppercase;
  }

  /* Tagline */
  .cyber-profile strong {
    color: #7c3aed;
  }

  /* Cartão de Citação (Blockquote) */
  .cyber-profile blockquote {
    background: #ffffff;
    border: 3px solid #0d0620;
    border-radius: 16px;
    box-shadow: 6px 6px 0 #7c3aed, 10px 10px 0 rgba(0, 212, 255, 0.3);
    padding: 1.5rem;
    margin: 2rem auto;
    max-width: 600px;
    transform: rotate(-0.5deg);
    transition: transform 0.3s ease;
    color: #0d0620;
  }

  .cyber-profile blockquote:hover {
    transform: rotate(0deg) scale(1.02);
  }

  /* Divisórias */
  .cyber-profile hr {
    height: 3px;
    background: linear-gradient(90deg, #ff2e88, #00d4ff);
    border: none;
    border-radius: 10px;
    margin: 3rem auto;
    max-width: 150px;
    box-shadow: 0 0 15px rgba(255, 46, 136, 0.4);
  }

  /* Tabelas Estilo Card */
  .cyber-profile table {
    background: #ffffff;
    border-radius: 16px;
    box-shadow: 0 8px 30px rgba(13, 6, 32, 0.08);
    border: 1px solid rgba(13, 6, 32, 0.05);
    width: 100%;
    overflow: hidden;
    border-collapse: separate;
    border-spacing: 0;
    margin: 1.5rem 0;
  }

  .cyber-profile th {
    background: #ece6ff;
    color: #0d0620;
    text-transform: uppercase;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    padding: 1rem;
    text-align: left;
    border-bottom: 2px solid #0d0620;
  }

  .cyber-profile td {
    padding: 1rem;
    border-bottom: 1px solid rgba(13, 6, 32, 0.05);
    color: #3a2f5c;
  }

  .cyber-profile tr:hover td {
    background: #faf7ff;
  }

  /* Terminal (Bloco de Código) */
  .cyber-profile pre {
    background: #0d0620;
    color: #b5ff2e;
    border-radius: 12px;
    padding: 1.5rem;
    box-shadow: inset 0 0 50px rgba(0, 212, 255, 0.1);
    border: 1px solid rgba(0, 212, 255, 0.2);
    overflow-x: auto;
  }

  .cyber-profile code {
    font-family: "IBM Plex Mono", monospace;
  }
</style>

<!-- INÍCIO DO CONTEÚDO DO PERFIL -->
<div class="cyber-profile" align="center">

  <h1>Daniel Dias</h1>
  
  <h3>ダニエル・ディアス</h3>

  <p><strong>Estudante de Informática para Web · Tecnologia · Qualidade · Infraestrutura</strong></p>

  <p>
    <a href="https://github.com/Danimilmil/dani_dias"><img src="https://img.shields.io/badge/GitHub-18181B?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
    <a href="https://www.linkedin.com/in/daniel-dias-37a639375/"><img src="https://img.shields.io/badge/LinkedIn-18181B?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
    <a href="mailto:ddias6574@gmail.com"><img src="https://img.shields.io/badge/Email-18181B?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  </p>

  <blockquote>
    <strong>「七転び八起き」</strong><br>
    <em>Nanakorobi yaoki — cair sete vezes, levantar oito.</em>
  </blockquote>

  <hr>

  <h2>Sobre mim · 自己紹介</h2>

  <p align="left">Sou estudante de <strong>Informática para Web</strong>, interessado em tecnologia, qualidade de software e infraestrutura.</p>

  <p align="left">Meu objetivo é construir uma carreira em TI explorando principalmente <strong>Banco de Dados, QA, DevOps, Computação em Nuvem e Cibersegurança</strong>.</p>

  <p align="left">Tenho interesse em entender não apenas o desenvolvimento de aplicações, mas também os processos, ambientes e tecnologias que tornam os sistemas mais <strong>seguros, confiáveis e eficientes</strong>.</p>

  <p align="left">Atualmente, busco minha <strong>primeira oportunidade profissional na área de TI</strong>, enquanto continuo aprimorando meus conhecimentos por meio de estudos e projetos práticos.</p>

  <hr>

  <h2>Stack & Ferramentas · 技術</h2>

  <table align="center">
    <tr>
      <td align="left"><strong>開 Desenvolvimento</strong></td>
      <td align="center"><img src="https://skillicons.dev/icons?i=html,css,js" alt="HTML, CSS e JavaScript" /></td>
      <td align="left">HTML · CSS · JavaScript</td>
    </tr>
    <tr>
      <td align="left"><strong>携 Mobile</strong></td>
      <td align="center"><img src="https://skillicons.dev/icons?i=react" alt="React Native" /></td>
      <td align="left">React Native</td>
    </tr>
    <tr>
      <td align="left"><strong>質 Qualidade</strong></td>
      <td align="center"><img src="https://skillicons.dev/icons?i=jest" alt="Jest" /></td>
      <td align="left">Jest · Testes automatizados · QA</td>
    </tr>
    <tr>
      <td align="left"><strong>庫 Banco de Dados</strong></td>
      <td align="center"><img src="https://skillicons.dev/icons?i=mysql" alt="MySQL" /></td>
      <td align="left">MySQL · SQL · Modelagem de dados</td>
    </tr>
    <tr>
      <td align="left"><strong>版 Versionamento</strong></td>
      <td align="center"><img src="https://skillicons.dev/icons?i=git,github" alt="Git e GitHub" /></td>
      <td align="left">Git · GitHub · Controle de versão</td>
    </tr>
    <tr>
      <td align="left"><strong>系 Sistemas</strong></td>
      <td align="center"><img src="https://skillicons.dev/icons?i=linux" alt="Linux" /></td>
      <td align="left">Linux · Terminal · Linha de comando</td>
    </tr>
  </table>

  <hr>

  <h2>Áreas de interesse · 興味</h2>

  <table align="center">
    <tr>
      <td align="center">
        🗄️<br><strong>Banco de Dados</strong><br><sub>データベース</sub>
      </td>
      <td align="center">
        🧪<br><strong>QA</strong><br><sub>品質保証</sub>
      </td>
      <td align="center">
        ⚙️<br><strong>DevOps</strong><br><sub>開発運用</sub>
      </td>
      <td align="center">
        ☁️<br><strong>Cloud</strong><br><sub>クラウド</sub>
      </td>
      <td align="center">
        🔐<br><strong>Cibersegurança</strong><br><sub>サイバー安全</sub>
      </td>
    </tr>
  </table>

  <hr>

  <h2>Conhecimentos · 知識</h2>

  <table align="center">
    <thead>
      <tr>
        <th>Categoria</th>
        <th>Tecnologias</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Web</strong></td>
        <td>HTML · CSS · JavaScript</td>
      </tr>
      <tr>
        <td><strong>Mobile</strong></td>
        <td>React Native</td>
      </tr>
      <tr>
        <td><strong>Testes</strong></td>
        <td>Jest · Testes automatizados</td>
      </tr>
      <tr>
        <td><strong>Banco de Dados</strong></td>
        <td>MySQL · SQL · Modelagem de dados</td>
      </tr>
      <tr>
        <td><strong>Versionamento</strong></td>
        <td>Git · GitHub</td>
      </tr>
      <tr>
        <td><strong>Sistemas</strong></td>
        <td>Linux · Terminal</td>
      </tr>
    </tbody>
  </table>

  <hr>

  <h2>Atualmente estudando · 勉強中</h2>

  <pre><code>Banco de Dados
      ↓
Quality Assurance
      ↓
DevOps
      ↓
Computação em Nuvem
      ↓
Cibersegurança</code></pre>

  <hr>

  <h3>「一日一歩」</h3>
  <p><em>Ichinichi ippo — um passo por dia.</em></p>

  <p>
    <img src="https://komarev.com/ghpvc/?username=Danimilmil&style=flat-square&color=b8302a&label=VISITAS+AO+DOJO" alt="Visitas ao perfil" />
  </p>

</div>
<!-- FIM DO CONTEÚDO DO PERFIL -->
