/* ==========================================================================
   PERFIL DANIEL DIAS — Tema "NEON CYBERPUNK EDITORIAL"
   Estética: vibrante · magazine digital · grid assimétrico
   ========================================================================== */

:root {
  /* Fundo — claro com "punch" neon */
  --bg:            #f5f2ff;
  --bg-alt:        #ece6ff;
  --surface:       #ffffff;
  --surface-2:     #faf7ff;

  /* Tinta */
  --ink:           #0d0620;
  --ink-soft:      #3a2f5c;
  --ink-muted:     #6b5f8a;
  --ink-faint:     #a99fc4;

  /* Neon palette */
  --neon-pink:     #ff2e88;
  --neon-cyan:     #00d4ff;
  --neon-lime:     #b5ff2e;
  --neon-violet:   #7c3aed;
  --neon-orange:   #ff6b1a;

  /* Gradientes */
  --grad-hero:     linear-gradient(135deg, #ff2e88 0%, #7c3aed 50%, #00d4ff 100%);
  --grad-hot:      linear-gradient(90deg, #ff2e88, #ff6b1a);
  --grad-cool:     linear-gradient(90deg, #00d4ff, #7c3aed);
  --grad-lime:     linear-gradient(135deg, #b5ff2e 0%, #00d4ff 100%);

  /* Sombras */
  --shadow-sm:     0 2px 8px rgba(13, 6, 32, 0.06);
  --shadow-md:     0 8px 32px rgba(13, 6, 32, 0.10);
  --shadow-lg:     0 20px 60px rgba(124, 58, 237, 0.18);
  --shadow-glow:   0 0 32px rgba(255, 46, 136, 0.35);

  /* Tipografia */
  --font-display:  "Space Grotesk", "Clash Display", "Archivo Black", sans-serif;
  --font-body:     "Inter", "DM Sans", system-ui, sans-serif;
  --font-mono:     "IBM Plex Mono", "Space Mono", monospace;

  /* Espaço */
  --s1: 0.5rem;
  --s2: 1rem;
  --s3: 1.5rem;
  --s4: 2.5rem;
  --s5: 4rem;
  --s6: 6rem;

  /* Radius */
  --r-sm: 10px;
  --r-md: 18px;
  --r-lg: 28px;
  --r-pill: 999px;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* --------------------------------------------------------------------------
   Body — fundo claro com grid de pontos sutil e "blobs" neon
   -------------------------------------------------------------------------- */
body {
  font-family: var(--font-body);
  color: var(--ink);
  background-color: var(--bg);
  background-image:
    radial-gradient(circle at 12% 8%,  rgba(255, 46, 136, 0.18), transparent 42%),
    radial-gradient(circle at 88% 12%, rgba(0, 212, 255, 0.16),  transparent 40%),
    radial-gradient(circle at 50% 95%, rgba(181, 255, 46, 0.12), transparent 45%),
    radial-gradient(rgba(13, 6, 32, 0.06) 1px, transparent 1px);
  background-size: auto, auto, auto, 22px 22px;
  background-attachment: fixed;
  line-height: 1.65;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  min-height: 100vh;
}

/* --------------------------------------------------------------------------
   Container panorâmico
   -------------------------------------------------------------------------- */
.markdown-body,
body > div,
main {
  max-width: 1160px;
  margin: 0 auto;
  padding: var(--s5) clamp(1.25rem, 4vw, 3rem);
}

/* --------------------------------------------------------------------------
   HEADER (div align="center")
   -------------------------------------------------------------------------- */
div[align="center"] {
  text-align: center;
  padding: var(--s4) 0 var(--s5);
  position: relative;
}

/* Selo "STUDENT / DEV" no topo */
div[align="center"]::before {
  content: "◦ PROFILE / 2025 ◦";
  display: inline-block;
  font-family: var(--font-mono);
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.3em;
  color: var(--neon-violet);
  background: var(--surface);
  padding: 0.5rem 1.2rem;
  border-radius: var(--r-pill);
  border: 1px solid rgba(124, 58, 237, 0.25);
  box-shadow: var(--shadow-sm);
  margin-bottom: var(--s3);
}

/* H1 — display neon com gradiente */
h1 {
  font-family: var(--font-display);
  font-size: clamp(2.8rem, 8vw, 5.5rem);
  font-weight: 800;
  line-height: 0.95;
  letter-spacing: -0.03em;
  background: var(--grad-hero);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: var(--s2);
  filter: drop-shadow(0 4px 24px rgba(255, 46, 136, 0.25));
}

/* Subtítulo japonês */
div[align="center"] h3 {
  font-family: var(--font-display);
  font-size: clamp(1.1rem, 2.5vw, 1.6rem);
  font-weight: 500;
  color: var(--ink-muted);
  letter-spacing: 0.5em;
  text-transform: uppercase;
  margin-bottom: var(--s3);
}

/* Tagline */
div[align="center"] > p > strong {
  display: inline-block;
  font-family: var(--font-mono);
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--ink);
  background: var(--surface);
  padding: 0.6rem 1.4rem;
  border-radius: var(--r-pill);
  border: 2px solid var(--ink);
  box-shadow: 4px 4px 0 var(--neon-pink);
  letter-spacing: 0.02em;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

div[align="center"] > p > strong:hover {
  transform: translate(-2px, -2px);
  box-shadow: 6px 6px 0 var(--neon-cyan);
}

/* Badges — estilo "chunky" */
div[align="center"] p a img {
  margin: 0.3rem 0.25rem;
  transition: transform 0.2s ease, filter 0.2s ease;
  border-radius: 8px;
}

div[align="center"] p a:hover img {
  transform: translateY(-4px) rotate(-2deg);
  filter: drop-shadow(0 8px 16px rgba(255, 46, 136, 0.4));
}

/* Blockquote (nanakorobi) — cartão editorial */
blockquote {
  margin: var(--s4) auto var(--s2);
  max-width: 720px;
  padding: var(--s3) var(--s4);
  background: var(--surface);
  border: 3px solid var(--ink);
  border-radius: var(--r-lg);
  box-shadow: 8px 8px 0 var(--neon-violet), 16px 16px 0 rgba(0, 212, 255, 0.3);
  font-family: var(--font-display);
  font-size: clamp(1.1rem, 2.4vw, 1.4rem);
  font-weight: 600;
  color: var(--ink);
  text-align: center;
  position: relative;
  transform: rotate(-0.6deg);
  transition: transform 0.3s ease;
}

blockquote:hover {
  transform: rotate(0deg) scale(1.01);
}

blockquote::before {
  content: "❝";
  position: absolute;
  top: -1.5rem;
  left: 2rem;
  font-size: 4rem;
  color: var(--neon-pink);
  line-height: 1;
}

blockquote em {
  display: block;
  font-family: var(--font-mono);
  font-style: normal;
  font-size: 0.85rem;
  font-weight: 400;
  color: var(--ink-muted);
  margin-top: var(--s1);
  letter-spacing: 0.05em;
}

/* --------------------------------------------------------------------------
   Divisórias — barras neon
   -------------------------------------------------------------------------- */
hr {
  border: none;
  height: 3px;
  background: var(--grad-hot);
  border-radius: var(--r-pill);
  margin: var(--s5) 0;
  width: 100%;
  max-width: 120px;
  margin-left: auto;
  margin-right: auto;
  box-shadow: 0 0 20px rgba(255, 46, 136, 0.5);
}

/* --------------------------------------------------------------------------
   H2 — display com número neon em bloco
   -------------------------------------------------------------------------- */
h2 {
  font-family: var(--font-display);
  font-size: clamp(1.6rem, 4vw, 2.4rem);
  font-weight: 800;
  letter-spacing: -0.02em;
  color: var(--ink);
  margin-bottom: var(--s4);
  line-height: 1.1;
  display: flex;
  align-items: center;
  gap: var(--s2);
}

h2::before {
  content: "";
  width: 12px;
  height: 2.4rem;
  background: var(--grad-hero);
  border-radius: 4px;
  box-shadow: 0 0 20px rgba(255, 46, 136, 0.5);
  flex-shrink: 0;
}

/* Parágrafos */
p {
  color: var(--ink-soft);
  max-width: 72ch;
  margin-bottom: var(--s2);
  font-size: 1.02rem;
}

p strong {
  color: var(--neon-violet);
  font-weight: 700;
  background: linear-gradient(180deg, transparent 65%, rgba(181, 255, 46, 0.5) 65%);
  padding: 0 2px;
}

/* --------------------------------------------------------------------------
   TABELAS — cards flutuantes com cantos coloridos
   -------------------------------------------------------------------------- */
table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  margin: var(--s4) 0;
  background: var(--surface);
  border-radius: var(--r-lg);
  overflow: hidden;
  box-shadow: var(--shadow-md);
  border: 1px solid rgba(13, 6, 32, 0.06);
}

table th {
  font-family: var(--font-display);
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--ink);
  background: var(--bg-alt);
  text-align: left;
  padding: var(--s2) var(--s3);
  border-bottom: 2px solid var(--ink);
}

table td {
  padding: var(--s2) var(--s3);
  color: var(--ink-soft);
  font-size: 0.97rem;
  border-bottom: 1px solid rgba(13, 6, 32, 0.06);
  vertical-align: middle;
}

table tr:last-child td {
  border-bottom: none;
}

table tr {
  transition: background 0.2s ease;
}

table tr:hover td {
  background: var(--surface-2);
}

table strong {
  color: var(--ink);
  font-weight: 700;
}

table img {
  height: 32px;
  vertical-align: middle;
  margin-right: 4px;
  transition: transform 0.2s ease;
}

table tr:hover img {
  transform: scale(1.1);
}

/* --------------------------------------------------------------------------
   TABELA DE ÁREAS — cards neon interativos
   -------------------------------------------------------------------------- */
table td[align="center"] {
  padding: var(--s4) var(--s2);
  text-align: center;
  font-size: 2rem;
  line-height: 1.3;
  transition: all 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
  cursor: default;
  position: relative;
}

table td[align="center"]:nth-child(1):hover { background: linear-gradient(180deg, transparent, rgba(255, 46, 136, 0.15)); }
table td[align="center"]:nth-child(2):hover { background: linear-gradient(180deg, transparent, rgba(0, 212, 255, 0.15)); }
table td[align="center"]:nth-child(3):hover { background: linear-gradient(180deg, transparent, rgba(181, 255, 46, 0.20)); }
table td[align="center"]:nth-child(4):hover { background: linear-gradient(180deg, transparent, rgba(124, 58, 237, 0.15)); }
table td[align="center"]:nth-child(5):hover { background: linear-gradient(180deg, transparent, rgba(255, 107, 26, 0.15)); }

table td[align="center"] strong {
  display: block;
  font-family: var(--font-display);
  font-size: 0.95rem;
  font-weight: 700;
  color: var(--ink);
  margin-top: var(--s1);
  letter-spacing: -0.01em;
}

table td[align="center"] sub {
  display: block;
  font-family: var(--font-mono);
  font-size: 0.7rem;
  color: var(--ink-faint);
  letter-spacing: 0.1em;
  margin-top: 2px;
  bottom: 0;
  text-transform: uppercase;
}

/* --------------------------------------------------------------------------
   BLOCO DE CÓDIGO — terminal "editorial"
   -------------------------------------------------------------------------- */
pre {
  font-family: var(--font-mono);
  font-size: 0.9rem;
  background: #0d0620;
  color: var(--neon-lime);
  border-radius: var(--r-md);
  padding: var(--s3) var(--s4);
  margin: var(--s4) 0;
  overflow-x: auto;
  position: relative;
  box-shadow: var(--shadow-lg), inset 0 0 60px rgba(0, 212, 255, 0.08);
  border: 1px solid rgba(0, 212, 255, 0.2);
  line-height: 2;
}

/* Barra de "window controls" */
pre::before {
  content: "● ● ●";
  display: block;
  color: var(--neon-pink);
  font-size: 0.7rem;
  letter-spacing: 0.5em;
  margin-bottom: var(--s2);
  opacity: 0.9;
}

pre code {
  color: inherit;
  background: transparent;
  padding: 0;
  white-space: pre;
  display: block;
}

code {
  font-family: var(--font-mono);
  background: rgba(124, 58, 237, 0.1);
  color: var(--neon-violet);
  padding: 0.15em 0.45em;
  border-radius: 6px;
  font-size: 0.9em;
}

/* --------------------------------------------------------------------------
   Contador de visitas
   -------------------------------------------------------------------------- */
div[align="center"] img[src*="komarev"] {
  margin-top: var(--s4);
  border-radius: var(--r-pill);
  box-shadow: var(--shadow-sm);
  filter: saturate(1.2);
}

/* --------------------------------------------------------------------------
   Links
   -------------------------------------------------------------------------- */
a {
  color: var(--neon-violet);
  text-decoration: none;
  font-weight: 600;
  position: relative;
  transition: color 0.2s ease;
}

a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -2px;
  width: 100%;
  height: 2px;
  background: var(--grad-hot);
  transform: scaleX(0);
  transform-origin: right;
  transition: transform 0.3s ease;
}

a:hover {
  color: var(--neon-pink);
}

a:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

/* --------------------------------------------------------------------------
   Bloco final (一日一歩)
   -------------------------------------------------------------------------- */
div[align="center"] h3:last-of-type {
  font-family: var(--font-display);
  font-size: clamp(1.4rem, 3vw, 2rem);
  color: var(--ink);
  letter-spacing: 0.2em;
  margin-top: var(--s4);
}

div[align="center"] em:last-of-type {
  font-family: var(--font-mono);
  color: var(--ink-muted);
  font-size: 0.85rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

/* --------------------------------------------------------------------------
   Responsivo
   -------------------------------------------------------------------------- */
@media (max-width: 820px) {
  .markdown-body,
  body > div,
  main {
    padding: var(--s4) var(--s2);
  }

  h1 {
    font-size: clamp(2rem, 9vw, 3rem);
  }

  blockquote {
    padding: var(--s2) var(--s3);
    box-shadow: 6px 6px 0 var(--neon-violet), 10px 10px 0 rgba(0, 212, 255, 0.3);
  }

  table th,
  table td {
    padding: 0.75rem 0.9rem;
    font-size: 0.88rem;
  }

  table td[align="center"] {
    padding: var(--s3) 0.5rem;
    font-size: 1.5rem;
  }

  table td[align="center"] strong {
    font-size: 0.8rem;
  }
}

@media (max-width: 520px) {
  h2 {
    flex-direction: column;
    align-items: flex-start;
    gap: var(--s1);
  }

  h2::before {
    width: 40px;
    height: 6px;
  }

  blockquote::before {
    font-size: 2.5rem;
    top: -0.8rem;
    left: 1rem;
  }

  table td[align="center"] sub {
    display: none;
  }

  /* Áreas em mobile: empilha em grid 2 colunas */
  table td[align="center"] {
    display: inline-block;
    width: 48%;
    margin: 1%;
    border-radius: var(--r-md);
    background: var(--surface-2);
  }
}

/* --------------------------------------------------------------------------
   Acessibilidade
   -------------------------------------------------------------------------- */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    transition: none !important;
    animation: none !important;
  }
}

a:focus-visible,
button:focus-visible {
  outline: 3px solid var(--neon-cyan);
  outline-offset: 3px;
  border-radius: 4px;
}

/* Scrollbar — trilho claro, polegar neon */
::-webkit-scrollbar {
  width: 12px;
}
::-webkit-scrollbar-track {
  background: var(--bg-alt);
}
::-webkit-scrollbar-thumb {
  background: var(--grad-hero);
  border-radius: var(--r-pill);
  border: 3px solid var(--bg-alt);
}
::-webkit-scrollbar-thumb:hover {
  background: var(--grad-hot);
}
