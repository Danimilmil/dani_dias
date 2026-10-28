/* ==========================================================================
   PERFIL DANIEL DIAS — Tema "Dojo Digital"
   Estética: japonesa minimalista · Panorâmica · Intuitiva
   ========================================================================== */

:root {
  /* Paleta principal */
  --bg-deep:      #0f0e0d;
  --bg-panel:     #1a1816;
  --bg-soft:      #24201d;
  --ink:          #f2ece3;
  --ink-muted:    #b8b0a4;
  --ink-faint:    #7a7267;

  /* Cores de acento (inspiradas no vermelho torii + dourado) */
  --accent-red:   #b8302a;
  --accent-red-2: #d94a3d;
  --accent-gold:  #d9a441;
  --accent-green: #6c8c5a;

  /* Bordas e sombras */
  --line:         rgba(217, 164, 65, 0.18);
  --line-strong:  rgba(217, 164, 65, 0.35);
  --glow-red:     0 0 24px rgba(184, 48, 42, 0.35);
  --glow-gold:    0 0 24px rgba(217, 164, 65, 0.28);

  /* Tipografia */
  --font-serif:   "Shippori Mincho", "Noto Serif JP", "Georgia", serif;
  --font-sans:    "Inter", "Noto Sans JP", system-ui, -apple-system, sans-serif;
  --font-mono:    "JetBrains Mono", "Fira Code", monospace;

  /* Espaçamento */
  --space-xs: 0.5rem;
  --space-sm: 1rem;
  --space-md: 2rem;
  --space-lg: 3.5rem;
  --space-xl: 5rem;
}

/* --------------------------------------------------------------------------
   Reset suave
   -------------------------------------------------------------------------- */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* --------------------------------------------------------------------------
   Corpo — fundo panorâmico com gradiente sutil e textura
   -------------------------------------------------------------------------- */
body {
  font-family: var(--font-sans);
  color: var(--ink);
  background: var(--bg-deep);
  background-image:
    radial-gradient(ellipse at 20% 0%, rgba(184, 48, 42, 0.10), transparent 55%),
    radial-gradient(ellipse at 80% 100%, rgba(217, 164, 65, 0.08), transparent 55%),
    linear-gradient(180deg, #0f0e0d 0%, #14110f 50%, #0f0e0d 100%);
  line-height: 1.7;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  min-height: 100vh;
  padding: 0;
  margin: 0;
}

/* --------------------------------------------------------------------------
   Container principal — largura panorâmica e respiro
   -------------------------------------------------------------------------- */
.markdown-body,
body > div,
main {
  max-width: 1080px;
  margin: 0 auto;
  padding: var(--space-lg) clamp(1rem, 4vw, 3rem);
}

/* --------------------------------------------------------------------------
   Cabeçalho central (div align="center")
   -------------------------------------------------------------------------- */
.markdown-body > div[align="center"],
div[align="center"] {
  text-align: center;
  padding: var(--space-lg) 0 var(--space-md);
  position: relative;
}

/* Ornamento superior — linha dupla com kanji central */
div[align="center"]::before {
  content: "道";
  display: block;
  font-family: var(--font-serif);
  font-size: 1.4rem;
  color: var(--accent-gold);
  letter-spacing: 0.6em;
  margin-bottom: var(--space-sm);
  opacity: 0.85;
}

/* H1 — Nome principal */
h1 {
  font-family: var(--font-serif);
  font-size: clamp(2.4rem, 6vw, 4rem);
  font-weight: 700;
  letter-spacing: 0.04em;
  line-height: 1.1;
  background: linear-gradient(135deg, var(--ink) 0%, var(--accent-gold) 100%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: var(--space-xs);
  position: relative;
}

/* Título japonês (h3) */
h3 {
  font-family: var(--font-serif);
  font-size: clamp(1.1rem, 2.2vw, 1.5rem);
  font-weight: 400;
  color: var(--accent-red-2);
  letter-spacing: 0.3em;
  margin: var(--space-xs) 0 var(--space-sm);
  text-transform: none;
}

/* Parágrafo de subtítulo (bold) */
div[align="center"] > p > strong {
  display: inline-block;
  font-family: var(--font-mono);
  font-size: 0.85rem;
  font-weight: 500;
  color: var(--ink-muted);
  letter-spacing: 0.08em;
  padding: 0.4rem 1.2rem;
  border: 1px solid var(--line);
  border-radius: 999px;
  background: rgba(26, 24, 22, 0.6);
}

/* Badges de contato */
div[align="center"] p a img {
  transition: transform 0.25s ease, filter 0.25s ease;
  margin: 0 0.25rem;
}

div[align="center"] p a:hover img {
  transform: translateY(-3px) scale(1.05);
  filter: drop-shadow(0 0 12px rgba(217, 164, 65, 0.5));
}

/* Citação principal (nanakorobi yaoki) */
blockquote {
  margin: var(--space-md) auto var(--space-sm);
  padding: var(--space-sm) var(--space-md);
  max-width: 640px;
  border-left: 3px solid var(--accent-red);
  border-right: 3px solid var(--accent-red);
  background: linear-gradient(90deg,
    transparent 0%,
    rgba(184, 48, 42, 0.08) 50%,
    transparent 100%);
  font-family: var(--font-serif);
  font-size: 1.15rem;
  color: var(--ink);
  text-align: center;
  border-radius: 6px;
  position: relative;
}

blockquote::before,
blockquote::after {
  content: "";
  position: absolute;
  width: 8px;
  height: 8px;
  background: var(--accent-gold);
  transform: rotate(45deg);
  top: 50%;
  margin-top: -4px;
}
blockquote::before { left: -5px; }
blockquote::after  { right: -5px; }

blockquote em {
  display: block;
  font-style: normal;
  font-size: 0.9rem;
  color: var(--ink-muted);
  margin-top: 0.4rem;
  letter-spacing: 0.04em;
}

/* --------------------------------------------------------------------------
   Linhas divisórias (--- → hr)
   -------------------------------------------------------------------------- */
hr {
  border: none;
  height: 1px;
  background: linear-gradient(90deg,
    transparent 0%,
    var(--line-strong) 50%,
    transparent 100%);
  margin: var(--space-lg) 0;
  position: relative;
}

hr::after {
  content: "◆";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: var(--accent-gold);
  background: var(--bg-deep);
  padding: 0 0.8rem;
  font-size: 0.7rem;
  letter-spacing: 0;
}

/* --------------------------------------------------------------------------
   Cabeçalhos de seção (h2) — com numeração kanji
   -------------------------------------------------------------------------- */
h2 {
  font-family: var(--font-serif);
  font-size: clamp(1.3rem, 3vw, 1.8rem);
  font-weight: 600;
  color: var(--ink);
  letter-spacing: 0.06em;
  margin-bottom: var(--space-md);
  padding-bottom: var(--space-xs);
  border-bottom: 1px solid var(--line);
  display: flex;
  align-items: center;
  gap: 0.6rem;
}

h2::before {
  content: "";
  width: 6px;
  height: 1.5rem;
  background: linear-gradient(180deg, var(--accent-red) 0%, var(--accent-gold) 100%);
  border-radius: 2px;
  box-shadow: var(--glow-red);
}

/* Parágrafos de conteúdo */
p {
  color: var(--ink-muted);
  margin-bottom: var(--space-sm);
  font-size: 1rem;
  max-width: 75ch;
}

p strong {
  color: var(--accent-gold);
  font-weight: 600;
}

/* --------------------------------------------------------------------------
   TABELAS — estilo panorâmico de "dojo"
   -------------------------------------------------------------------------- */
table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  margin: var(--space-md) 0;
  background: var(--bg-panel);
  border: 1px solid var(--line);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.35);
}

table thead {
  background: linear-gradient(180deg, var(--bg-soft) 0%, var(--bg-panel) 100%);
}

table th {
  font-family: var(--font-serif);
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--accent-gold);
  text-align: left;
  padding: var(--space-sm) var(--space-md);
  border-bottom: 1px solid var(--line-strong);
  letter-spacing: 0.04em;
}

table td {
  padding: var(--space-sm) var(--space-md);
  color: var(--ink-muted);
  font-size: 0.95rem;
  border-bottom: 1px solid rgba(217, 164, 65, 0.08);
  vertical-align: middle;
}

table tr:last-child td {
  border-bottom: none;
}

table tr:hover td {
  background: rgba(184, 48, 42, 0.06);
  color: var(--ink);
  transition: background 0.2s ease, color 0.2s ease;
}

table strong {
  color: var(--ink);
  font-weight: 600;
}

/* Ícones (skillicons) alinhados */
table img {
  display: inline-block;
  vertical-align: middle;
  height: 32px;
  margin-right: 4px;
}

/* --------------------------------------------------------------------------
   TABELA DE ÁREAS DE INTERESSE — cards panorâmicos
   -------------------------------------------------------------------------- */
table td[align="center"] {
  padding: var(--space-md) var(--space-sm);
  text-align: center;
  font-size: 1.6rem;
  line-height: 1.4;
  border-right: 1px solid rgba(217, 164, 65, 0.08);
  transition: transform 0.25s ease, background 0.25s ease;
}

table td[align="center"]:last-child {
  border-right: none;
}

table td[align="center"]:hover {
  background: linear-gradient(180deg,
    rgba(184, 48, 42, 0.08) 0%,
    rgba(217, 164, 65, 0.05) 100%);
  transform: translateY(-2px);
}

table td[align="center"] strong {
  display: block;
  font-family: var(--font-serif);
  font-size: 1rem;
  color: var(--ink);
  margin-top: 0.5rem;
  letter-spacing: 0.02em;
}

table td[align="center"] sub {
  display: block;
  font-family: var(--font-serif);
  font-size: 0.75rem;
  color: var(--accent-red-2);
  letter-spacing: 0.15em;
  margin-top: 0.2rem;
  bottom: 0;
}

/* --------------------------------------------------------------------------
   BLOCO DE CÓDIGO — trilha de estudo (fluxo vertical)
   -------------------------------------------------------------------------- */
pre,
code {
  font-family: var(--font-mono);
  font-size: 0.9rem;
}

pre {
  background: linear-gradient(180deg, var(--bg-panel) 0%, var(--bg-deep) 100%);
  border: 1px solid var(--line);
  border-left: 4px solid var(--accent-red);
  border-radius: 10px;
  padding: var(--space-md);
  overflow-x: auto;
  margin: var(--space-md) 0;
  position: relative;
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.4);
}

pre::before {
  content: "▸ trilha";
  position: absolute;
  top: 0.6rem;
  right: 1rem;
  font-size: 0.65rem;
  color: var(--accent-gold);
  letter-spacing: 0.2em;
  text-transform: uppercase;
  opacity: 0.7;
}

pre code {
  color: var(--accent-gold);
  line-height: 1.9;
  display: block;
  white-space: pre;
}

/* --------------------------------------------------------------------------
   Citação final (一日一歩)
   -------------------------------------------------------------------------- */
div[align="center"] h3:last-of-type,
div[align="center"] em:last-of-type {
  color: var(--accent-gold);
}

/* Contador de visitas */
div[align="center"] img[alt*="Visitas"],
div[align="center"] img[src*="komarev"] {
  margin-top: var(--space-md);
  border-radius: 6px;
  filter: brightness(0.95) contrast(1.05);
}

/* --------------------------------------------------------------------------
   Links
   -------------------------------------------------------------------------- */
a {
  color: var(--accent-gold);
  text-decoration: none;
  transition: color 0.2s ease, text-shadow 0.2s ease;
}

a:hover {
  color: var(--accent-red-2);
  text-shadow: 0 0 12px rgba(184, 48, 42, 0.5);
}

/* --------------------------------------------------------------------------
   Responsividade — mobile primeiro
   -------------------------------------------------------------------------- */
@media (max-width: 768px) {
  .markdown-body,
  body > div,
  main {
    padding: var(--space-md) var(--space-sm);
  }

  h1 {
    font-size: 2.2rem;
  }

  h2 {
    font-size: 1.2rem;
  }

  blockquote {
    font-size: 1rem;
    padding: var(--space-sm);
  }

  table {
    font-size: 0.85rem;
  }

  table th,
  table td {
    padding: 0.6rem 0.8rem;
  }

  /* Em mobile, tabela de áreas vira grade */
  table td[align="center"] {
    padding: var(--space-sm) 0.4rem;
    font-size: 1.3rem;
  }

  table td[align="center"] strong {
    font-size: 0.8rem;
  }
}

@media (max-width: 480px) {
  h1 {
    font-size: 1.8rem;
  }

  div[align="center"]::before {
    font-size: 1rem;
    letter-spacing: 0.4em;
  }

  /* Oculta sub-rótulos em telas muito pequenas */
  table td[align="center"] sub {
    display: none;
  }
}

/* --------------------------------------------------------------------------
   Acessibilidade — preferência por menos movimento
   -------------------------------------------------------------------------- */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    transition: none !important;
    animation: none !important;
  }
}

/* Foco visível para navegação por teclado */
a:focus-visible,
button:focus-visible {
  outline: 2px solid var(--accent-gold);
  outline-offset: 3px;
  border-radius: 4px;
}

/* --------------------------------------------------------------------------
   Scrollbar personalizada (WebKit)
   -------------------------------------------------------------------------- */
::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}
::-webkit-scrollbar-track {
  background: var(--bg-deep);
}
::-webkit-scrollbar-thumb {
  background: linear-gradient(180deg, var(--accent-red) 0%, var(--accent-gold) 100%);
  border-radius: 6px;
  border: 2px solid var(--bg-deep);
}
::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(180deg, var(--accent-red-2) 0%, var(--accent-gold) 100%);
}
