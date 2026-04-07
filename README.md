<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Contabilidade Especialista em Clínicas Médicas | Jardel Queiroz</title>
<meta name="description" content="Se você é médico e seu contador não é especialista na área da saúde, você provavelmente está queimando dinheiro com impostos.">

<!-- Preload crítico -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>
  /* ===== RESET & BASE ===== */
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --gold: #C9A84C;
    --gold-light: #E8C97A;
    --gold-dark: #9A7B35;
    --gold-glow: rgba(201,168,76,0.18);
    --black: #0A0A0A;
    --black-2: #111111;
    --black-3: #1A1A1A;
    --black-4: #222222;
    --white: #F5F0E8;
    --white-dim: rgba(245,240,232,0.7);
    --white-faint: rgba(245,240,232,0.12);
    --font-display: 'Cormorant Garamond', Georgia, serif;
    --font-body: 'Outfit', sans-serif;
    --transition: 0.35s cubic-bezier(0.4,0,0.2,1);
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--black);
    color: var(--white);
    font-family: var(--font-body);
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ===== GRAIN OVERLAY ===== */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.5;
  }

  /* ===== TYPOGRAPHY ===== */
  h1, h2, h3, h4 { font-family: var(--font-display); font-weight: 600; line-height: 1.2; }

  /* ===== GOLD DIVIDER ===== */
  .gold-line {
    display: block;
    width: 60px;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    margin: 0 auto 2rem;
  }

  /* ===== ANIMATIONS ===== */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(28px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  @keyframes shimmer {
    0%   { background-position: -200% center; }
    100% { background-position: 200% center; }
  }
  @keyframes pulse-gold {
    0%, 100% { box-shadow: 0 0 0 0 rgba(201,168,76,0.4); }
    50%       { box-shadow: 0 0 0 14px rgba(201,168,76,0); }
  }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50%       { transform: translateY(-8px); }
  }
  @keyframes borderGlow {
    0%, 100% { border-color: var(--gold-dark); }
    50%       { border-color: var(--gold-light); }
  }

  .fade-up {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  /* ===== GOLD BUTTON ===== */
  .btn-gold {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: linear-gradient(135deg, var(--gold-dark), var(--gold), var(--gold-light), var(--gold));
    background-size: 300% 300%;
    color: var(--black);
    font-family: var(--font-body);
    font-weight: 600;
    font-size: 1rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    padding: 1rem 2.4rem;
    border: none;
    cursor: pointer;
    text-decoration: none;
    transition: var(--transition);
    animation: shimmer 4s linear infinite, pulse-gold 2.5s ease-in-out infinite;
    clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%);
  }
  .btn-gold:hover {
    transform: translateY(-2px) scale(1.02);
    filter: brightness(1.1);
  }

  /* ===== NAVBAR ===== */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 1rem 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(10,10,10,0.92);
    backdrop-filter: blur(14px);
    border-bottom: 1px solid rgba(201,168,76,0.15);
  }
  .nav-logo {
    font-family: var(--font-display);
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--gold);
    letter-spacing: 0.04em;
  }
  .nav-cta {
    font-size: 0.78rem;
    padding: 0.6rem 1.4rem;
  }

  /* ===== HERO ===== */
  #hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 8rem 1.5rem 5rem;
    position: relative;
    overflow: hidden;
  }
  #hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 50% 0%, rgba(201,168,76,0.08) 0%, transparent 70%),
      radial-gradient(ellipse 60% 40% at 80% 80%, rgba(201,168,76,0.05) 0%, transparent 60%);
    pointer-events: none;
  }

  .hero-eyebrow {
    font-family: var(--font-body);
    font-size: 0.82rem;
    font-weight: 500;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.5rem;
    animation: fadeUp 0.6s ease both;
  }
  .hero-eyebrow span {
    display: inline-block;
    animation: float 3s ease-in-out infinite;
  }

  .hero-headline {
    font-size: clamp(2rem, 5vw, 3.8rem);
    font-weight: 700;
    max-width: 860px;
    margin: 0 auto 1.5rem;
    animation: fadeUp 0.7s 0.1s ease both;
    line-height: 1.15;
  }
  .hero-headline em {
    font-style: normal;
    background: linear-gradient(90deg, var(--gold-dark), var(--gold-light), var(--gold));
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: shimmer 4s linear infinite;
  }

  .hero-sub {
    font-size: clamp(1rem, 2vw, 1.2rem);
    color: var(--white-dim);
    max-width: 680px;
    margin: 0 auto 2.5rem;
    animation: fadeUp 0.7s 0.2s ease both;
  }

  /* ===== VIDEO SECTION ===== */
  #video-section {
    padding: 2rem 1.5rem 5rem;
    text-align: center;
    position: relative;
  }
  .video-wrapper {
    max-width: 820px;
    margin: 0 auto;
    position: relative;
    border: 1px solid rgba(201,168,76,0.3);
    background: var(--black-3);
    animation: borderGlow 4s ease-in-out infinite;
  }
  .video-wrapper::before {
    content: '';
    position: absolute;
    inset: -1px;
    background: linear-gradient(135deg, var(--gold-dark), transparent, var(--gold-dark));
    z-index: -1;
    opacity: 0.4;
  }
  .video-placeholder {
    width: 100%;
    aspect-ratio: 16/9;
    background: var(--black-4);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    color: var(--white-dim);
    cursor: pointer;
    position: relative;
    overflow: hidden;
  }
  .video-placeholder iframe {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    border: none;
  }
  .video-placeholder .play-icon {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: var(--gold);
    display: flex;
    align-items: center;
    justify-content: center;
    animation: pulse-gold 2s ease-in-out infinite;
    flex-shrink: 0;
  }
  .play-icon svg { fill: var(--black); width: 28px; margin-left: 4px; }
  .video-label {
    font-family: var(--font-body);
    font-size: 0.85rem;
    letter-spacing: 0.12em;
    color: var(--gold);
    text-transform: uppercase;
  }

  /* ===== SECTION BASE ===== */
  section { padding: 5rem 1.5rem; }
  .container { max-width: 900px; margin: 0 auto; }

  /* ===== EMOTION SECTION ===== */
  #emotion {
    background: linear-gradient(180deg, var(--black) 0%, var(--black-2) 100%);
    text-align: center;
  }
  .emotion-card {
    background: var(--black-3);
    border: 1px solid rgba(201,168,76,0.2);
    padding: 3rem 2.5rem;
    position: relative;
    overflow: hidden;
  }
  .emotion-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
  }
  .emotion-card blockquote {
    font-family: var(--font-display);
    font-size: clamp(1.4rem, 3vw, 2.1rem);
    font-weight: 500;
    font-style: italic;
    color: var(--white);
    margin-bottom: 1.5rem;
    line-height: 1.45;
  }
  .emotion-card blockquote strong {
    color: var(--gold);
    font-style: normal;
  }
  .emotion-body {
    font-size: 1.05rem;
    color: var(--white-dim);
    max-width: 700px;
    margin: 0 auto;
  }

  /* ===== LOGIC SECTION ===== */
  #logic { background: var(--black-2); }
  .logic-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1.5rem;
    margin-top: 2.5rem;
  }
  .logic-card {
    background: var(--black-3);
    border: 1px solid rgba(201,168,76,0.15);
    padding: 2rem 1.8rem;
    transition: var(--transition);
    position: relative;
  }
  .logic-card:hover {
    border-color: var(--gold);
    transform: translateY(-4px);
    background: var(--black-4);
  }
  .logic-card .stat {
    font-family: var(--font-display);
    font-size: 3rem;
    font-weight: 700;
    color: var(--gold);
    line-height: 1;
    margin-bottom: 0.5rem;
  }
  .logic-card .stat-label {
    font-size: 0.9rem;
    color: var(--white-dim);
    font-weight: 400;
  }
  .logic-card .stat-desc {
    margin-top: 0.75rem;
    font-size: 0.95rem;
    color: var(--white);
    border-top: 1px solid rgba(201,168,76,0.12);
    padding-top: 0.75rem;
  }

  /* ===== CHART ===== */
  .chart-container {
    margin: 3rem auto 0;
    max-width: 700px;
  }
  .chart-title {
    text-align: center;
    font-family: var(--font-body);
    font-size: 0.85rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.5rem;
  }
  .bar-chart {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  .bar-row { display: flex; align-items: center; gap: 1rem; }
  .bar-label {
    font-size: 0.85rem;
    color: var(--white-dim);
    min-width: 120px;
    text-align: right;
  }
  .bar-track {
    flex: 1;
    height: 32px;
    background: var(--black-4);
    border: 1px solid rgba(201,168,76,0.1);
    position: relative;
    overflow: hidden;
  }
  .bar-fill {
    height: 100%;
    display: flex;
    align-items: center;
    padding-left: 0.75rem;
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--black);
    width: 0%;
    transition: width 1.6s cubic-bezier(0.4,0,0.2,1);
  }
  .bar-fill.bad  { background: linear-gradient(90deg, #7B3030, #C04040); color: #fff; }
  .bar-fill.good { background: linear-gradient(90deg, var(--gold-dark), var(--gold)); }

  /* ===== RATIONAL SECTION ===== */
  #rational {
    background: var(--black);
    border-top: 1px solid rgba(201,168,76,0.1);
    border-bottom: 1px solid rgba(201,168,76,0.1);
  }
  .steps {
    display: flex;
    flex-direction: column;
    gap: 0;
    margin-top: 2.5rem;
  }
  .step {
    display: grid;
    grid-template-columns: 56px 1fr;
    gap: 1.5rem;
    padding: 2rem 0;
    border-bottom: 1px solid rgba(201,168,76,0.1);
    align-items: start;
    transition: var(--transition);
  }
  .step:hover { background: var(--white-faint); padding-left: 1rem; padding-right: 1rem; margin: 0 -1rem; }
  .step-num {
    width: 56px; height: 56px;
    border: 1px solid var(--gold);
    display: flex; align-items: center; justify-content: center;
    font-family: var(--font-display);
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--gold);
    flex-shrink: 0;
  }
  .step-content h4 {
    font-family: var(--font-display);
    font-size: 1.3rem;
    color: var(--gold-light);
    margin-bottom: 0.4rem;
  }
  .step-content p { font-size: 0.95rem; color: var(--white-dim); }

  /* ===== FAQ ===== */
  #faq { background: var(--black-2); }
  .faq-list { margin-top: 2.5rem; display: flex; flex-direction: column; gap: 1rem; }
  .faq-item {
    border: 1px solid rgba(201,168,76,0.15);
    background: var(--black-3);
    overflow: hidden;
    transition: var(--transition);
  }
  .faq-item:hover { border-color: rgba(201,168,76,0.4); }
  .faq-q {
    width: 100%;
    text-align: left;
    background: none;
    border: none;
    color: var(--white);
    font-family: var(--font-body);
    font-size: 1rem;
    font-weight: 500;
    padding: 1.3rem 1.5rem;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    transition: color var(--transition);
  }
  .faq-q:hover { color: var(--gold); }
  .faq-q .icon {
    width: 22px; height: 22px;
    border: 1px solid var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
    transition: transform var(--transition);
    color: var(--gold);
    font-size: 1rem;
    line-height: 1;
  }
  .faq-item.open .faq-q .icon { transform: rotate(45deg); }
  .faq-a {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.45s ease, padding 0.3s ease;
    font-size: 0.95rem;
    color: var(--white-dim);
    padding: 0 1.5rem;
  }
  .faq-item.open .faq-a { max-height: 300px; padding: 0 1.5rem 1.3rem; }

  /* ===== SECTION HEADINGS ===== */
  .section-tag {
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 500;
    margin-bottom: 0.75rem;
  }
  .section-h2 {
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    margin-bottom: 1rem;
  }
  .section-lead {
    font-size: 1.05rem;
    color: var(--white-dim);
    max-width: 660px;
  }

  /* ===== CTA SECTION ===== */
  #cta {
    background: linear-gradient(180deg, var(--black-2) 0%, var(--black) 100%);
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  #cta::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 60% 50% at 50% 50%, rgba(201,168,76,0.07) 0%, transparent 70%);
    pointer-events: none;
  }
  .cta-box {
    background: var(--black-3);
    border: 1px solid rgba(201,168,76,0.3);
    padding: 3.5rem 2.5rem;
    max-width: 700px;
    margin: 0 auto;
    position: relative;
  }
  .cta-box::before, .cta-box::after {
    content: '';
    position: absolute;
    width: 40px; height: 40px;
  }
  .cta-box::before { top: -1px; left: -1px; border-top: 2px solid var(--gold); border-left: 2px solid var(--gold); }
  .cta-box::after  { bottom: -1px; right: -1px; border-bottom: 2px solid var(--gold); border-right: 2px solid var(--gold); }

  .form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-top: 2rem;
    text-align: left;
  }
  .form-group { display: flex; flex-direction: column; gap: 0.4rem; }
  .form-group.full { grid-column: 1 / -1; }
  .form-group label {
    font-size: 0.78rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 500;
  }
  .form-group input,
  .form-group select {
    background: var(--black-4);
    border: 1px solid rgba(201,168,76,0.25);
    color: var(--white);
    font-family: var(--font-body);
    font-size: 0.95rem;
    padding: 0.85rem 1rem;
    outline: none;
    transition: border-color var(--transition);
    -webkit-appearance: none;
    appearance: none;
    width: 100%;
  }
  .form-group input:focus,
  .form-group select:focus { border-color: var(--gold); }
  .form-group select option { background: var(--black-4); }

  .form-submit {
    margin-top: 1.5rem;
    width: 100%;
    justify-content: center;
    font-size: 1.05rem;
    padding: 1.2rem 2rem;
    clip-path: none;
  }

  .form-privacy {
    margin-top: 1rem;
    font-size: 0.78rem;
    color: rgba(245,240,232,0.35);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.4rem;
  }

  /* ===== SUCCESS MESSAGE ===== */
  .success-msg {
    display: none;
    text-align: center;
    padding: 2rem;
  }
  .success-msg .check {
    width: 64px; height: 64px;
    border-radius: 50%;
    background: var(--gold);
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 1rem;
    font-size: 1.8rem;
    color: var(--black);
  }
  .success-msg h3 {
    font-family: var(--font-display);
    font-size: 1.8rem;
    color: var(--gold);
    margin-bottom: 0.5rem;
  }
  .success-msg p { color: var(--white-dim); }

  /* ===== FOOTER ===== */
  footer {
    background: var(--black);
    border-top: 1px solid rgba(201,168,76,0.12);
    padding: 2rem 1.5rem;
    text-align: center;
  }
  footer p { font-size: 0.8rem; color: rgba(245,240,232,0.3); }
  footer a { color: var(--gold); text-decoration: none; }

  /* ===== FLOATING CTA ===== */
  .floating-cta {
    position: fixed;
    bottom: 1.5rem;
    right: 1.5rem;
    z-index: 200;
    transform: translateY(80px);
    opacity: 0;
    transition: var(--transition);
  }
  .floating-cta.show { transform: translateY(0); opacity: 1; }

  /* ===== MOBILE ===== */
  @media (max-width: 600px) {
    .form-grid { grid-template-columns: 1fr; }
    .form-group.full { grid-column: 1; }
    nav .nav-cta { display: none; }
    .bar-label { min-width: 80px; font-size: 0.75rem; }
    .step { grid-template-columns: 44px 1fr; }
  }

  /* ===== LOADING STATE ===== */
  .btn-gold.loading {
    opacity: 0.7;
    pointer-events: none;
  }
  .btn-gold.loading::after {
    content: '';
    width: 16px; height: 16px;
    border: 2px solid var(--black);
    border-top-color: transparent;
    border-radius: 50%;
    animation: spin 0.7s linear infinite;
  }
  @keyframes spin { to { transform: rotate(360deg); } }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="nav-logo">Q&M Contabilidade</span>
  <a href="#cta" class="btn-gold nav-cta">Diagnóstico Gratuito →</a>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-eyebrow">
    <span>▼ Assista o vídeo abaixo</span>
  </div>

  <h1 class="hero-headline">
    Se você é médico e seu contador<br>não é especialista na área da saúde,<br>
    você provavelmente está
    <em>queimando dinheiro com impostos.</em>
  </h1>

  <p class="hero-sub">
    Nem sempre o Simples Nacional é o melhor regime para clínicas médicas. Essa escolha errada pode fazer você pagar <strong>muito mais imposto do que realmente precisa</strong>, e a maioria dos médicos nem sabe disso.
  </p>

  <a href="#cta" class="btn-gold">Quero parar de perder dinheiro →</a>
</section>

<!-- VIDEO -->
<section id="video-section">
  <div class="video-wrapper fade-up">
    <div class="video-placeholder" id="videoPlaceholder">
      <!-- Cole aqui o iframe do seu vídeo (YouTube, Vimeo, Panda, etc.) -->
      <!-- Exemplo: <iframe src="https://www.youtube.com/embed/SEU_ID_AQUI" allowfullscreen></iframe> -->
      <div class="play-icon">
        <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
      </div>
      <p class="video-label">Assista antes de sair desta página</p>
      <p style="font-size:0.82rem;color:rgba(245,240,232,0.3);margin-top:0.5rem;">⚙️ Cole o link do seu vídeo no código-fonte nesta seção</p>
    </div>
  </div>
</section>

<!-- EMOTION -->
<section id="emotion">
  <div class="container fade-up">
    <span class="gold-line"></span>
    <div class="emotion-card">
      <blockquote>
        "Você passou anos estudando medicina, abriu sua clínica, trabalha 12 horas por dia,<br>
        e parte do que você ganha vai embora <strong>sem necessidade</strong>."
      </blockquote>
      <p class="emotion-body">
        Imagina descobrir, após anos pagando impostos a mais, que existia um caminho legal e legítimo para pagar menos, e ninguém te contou.
        Não por má-fé, mas porque seu contador simplesmente <strong>não conhece a legislação específica da área médica</strong>.
        Isso acontece todos os dias com médicos em todo o Brasil.
        <br><br>
        A sensação de que algo está errado nas suas finanças, mas você não sabe exatamente o quê, isso tem nome: é falta de especialização contábil na área da saúde.
      </p>
    </div>
    <br>
    <a href="#cta" class="btn-gold">Quero uma análise do meu caso →</a>
  </div>
</section>

<!-- LOGIC -->
<section id="logic">
  <div class="container">
    <div class="fade-up">
      <p class="section-tag">Os números não mentem</p>
      <h2 class="section-h2">Por que o regime tributário errado custa tanto?</h2>
      <p class="section-lead">
        A legislação brasileira oferece regimes tributários distintos para pessoas jurídicas. Para clínicas e médicos PJ, a escolha correta pode representar uma diferença expressiva no bolso, todo mês.
      </p>
    </div>

    <div class="logic-grid fade-up">
      <div class="logic-card">
        <div class="stat">19%</div>
        <div class="stat-label">Simples Nacional só é vantajoso para empresa com faturamento baixo</div>
        <p class="stat-desc">Empresas no Simples Nacional podem pagar até 19% do faturamento total, não se leva em consideração as diversas despesas do seu consultório.</p>
      </div>
      <div class="logic-card">
        <div class="stat">7,93%</div>
        <div class="stat-label">Alíquota máxima para médicos com benefícios fiscais</div>
        <p class="stat-desc">Com planejamento correto, é possível organizar a empresa para aproveitar ao máximo os benefícios fiscais previstos em lei para a área da saúde.</p>
      </div>
      <div class="logic-card">
        <div class="stat">R$ 0</div>
        <div class="stat-label">Custo para descobrir quanto você está perdendo</div>
        <p class="stat-desc">Um diagnóstico tributário gratuito pode revelar em minutos se você está no regime ideal. Sem compromisso, sem letra miúda.</p>
      </div>
    </div>

    <!-- BAR CHART -->
    <div class="chart-container fade-up">
      <p class="chart-title">Comparativo de carga tributária estimada, Clínica médica faturando R$ 30k/mês</p>
      <div class="bar-chart">
        <div class="bar-row">
          <span class="bar-label">Pessoa Física (PF)</span>
          <div class="bar-track">
            <div class="bar-fill bad" data-width="90">Até 33% efetivo</div>
          </div>
        </div>
        <div class="bar-row">
          <span class="bar-label">Simples Nacional</span>
          <div class="bar-track">
            <div class="bar-fill good" data-width="60">Até 19,5% efetivo</div>
          </div>
        </div>
        <div class="bar-row">
          <span class="bar-label">Lucro Presumido</span>
          <div class="bar-track">
            <div class="bar-fill good" data-width="34">7,93% com a estratégia certa</div>
          </div>
        </div>
      </div>
      <p style="font-size:0.72rem;color:rgba(245,240,232,0.28);text-align:center;margin-top:1rem;">*Valores baseado em informações de mercado. O resultado real depende de análise individual.</p>
    </div>

    <div style="text-align:center;margin-top:3rem;" class="fade-up">
      <a href="#cta" class="btn-gold">Quero descobrir meu regime ideal →</a>
    </div>
  </div>
</section>

<!-- RATIONAL -->
<section id="rational">
  <div class="container">
    <div class="fade-up">
      <p class="section-tag">Como funciona</p>
      <h2 class="section-h2">Em 3 passos, você para de pagar mais do que deve</h2>
      <p class="section-lead">
        Não é magia. É conhecimento técnico aplicado à realidade de quem vive a medicina. O processo é simples, rápido e sem burocracia.
      </p>
    </div>

    <div class="steps fade-up">
      <div class="step">
        <div class="step-num">01</div>
        <div class="step-content">
          <h4>Diagnóstico Tributário Gratuito</h4>
          <p>Você preenche o formulário abaixo com dados básicos da sua clínica. Em até 48h, fazemos uma análise completa do seu cenário fiscal atual e identificamos oportunidades de economia.</p>
        </div>
      </div>
      <div class="step">
        <div class="step-num">02</div>
        <div class="step-content">
          <h4>Apresentação do Relatório de Economia</h4>
          <p>Apresentamos um relatório claro mostrando exatamente quanto você pode economizar ao migrar para o regime tributário adequado. Números reais, sem promessas vagas.</p>
        </div>
      </div>
      <div class="step">
        <div class="step-num">03</div>
        <div class="step-content">
          <h4>Transição Segura e Gestão Contínua</h4>
          <p>Caso faça sentido para você, assumimos toda a contabilidade da sua clínica: folha de pagamento, obrigações fiscais, planejamento tributário anual e suporte especializado todo mês.</p>
        </div>
      </div>
    </div>

    <div style="text-align:center;margin-top:3rem;" class="fade-up">
      <a href="#cta" class="btn-gold">Começar meu diagnóstico gratuito →</a>
    </div>
  </div>
</section>

<!-- FAQ -->
<section id="faq">
  <div class="container">
    <div class="fade-up">
      <p class="section-tag">Perguntas frequentes</p>
      <h2 class="section-h2">Respondendo suas dúvidas</h2>
    </div>

    <div class="faq-list fade-up">
      <div class="faq-item">
        <button class="faq-q">
          O Simples Nacional nunca é vantajoso para médicos?
          <span class="icon">+</span>
        </button>
        <div class="faq-a">
          <p>Não é uma regra universal. Para clínicas com faturamento muito baixo ou que estão começando, o Simples pode ser vantajoso. O ponto é: só um contador especialista na área da saúde consegue simular com precisão qual regime é o melhor para o seu perfil específico. Muitos médicos ficam no Simples por comodidade ou desconhecimento, e pagam mais do que deveriam.</p>
        </div>
      </div>
      <div class="faq-item">
        <button class="faq-q">
          Mudar de regime tributário no meio do ano é possível?
          <span class="icon">+</span>
        </button>
        <div class="faq-a">
          <p>A troca de regime e feita durante o ano. Com o diagnóstico antecipado é definida a melhor estratégia econômica: quanto antes você identificar que está no regime errado, mais rápido começa a economizar. Fazemos todo o planejamento e a transição de forma segura.</p>
        </div>
      </div>
      <div class="faq-item">
        <button class="faq-q">
          Isso é legal? Tenho medo de ter problemas com o Fisco.
          <span class="icon">+</span>
        </button>
        <div class="faq-a">
          <p>100% legal. Chamamos de Planejamento Tributário, e é um direito garantido pela legislação brasileira. Não falamos de sonegação; falamos de usar corretamente o que a lei permite. A escolha do regime tributário adequado, a utilização de deduções legais e a organização societária correta são práticas totalmente lícitas e recomendadas.</p>
        </div>
      </div>
      <div class="faq-item">
        <button class="faq-q">
          Quanto tempo para ter o primeiro resultado?
          <span class="icon">+</span>
        </button>
        <div class="faq-a">
          <p>Nosso trabalho é confirmado em números reais, e com um modelo ja validado de estratégia tributária, nós podemos replicar o que já funciona com nossos clientes e ajustar com base em qualquer consultório do país. O resultado já aparece no mês seguinte a implementação da estratégia e a apuração mensal.</p>
        </div>
      </div>
      <div class="faq-item">
        <button class="faq-q">
          O diagnóstico é realmente gratuito? Qual o compromisso?
          <span class="icon">+</span>
        </button>
        <div class="faq-a">
          <p>Sim, é gratuito e sem compromisso. Você preenche o formulário, recebemos suas informações, fazemos a análise e apresentamos os resultados. Só avançamos para uma proposta de serviço se você quiser. Nosso objetivo é que você tome a melhor decisão, mesmo que seja continuar com quem já tem.</p>
        </div>
      </div>
    </div>

    <!-- REAFIRMAÇÃO -->
    <div class="emotion-card" style="margin-top:3rem;" class="fade-up">
      <blockquote style="font-size:clamp(1.2rem,2.5vw,1.7rem);">
        "Cada mês que passa sem a contabilidade certa<br>
        é dinheiro que não volta."
      </blockquote>
      <p class="emotion-body">
        Médicos que trabalham com contadores especializados em saúde economizam, em média, entre <strong style="color:var(--gold)">R$ 5.000 a R$ 20.000 por mês</strong> em impostos, dependendo do faturamento e do regime atual.
        Isso é uma viagem internacional, a expansão da sua clínica, ou simplesmente a sua tranquilidade financeira.
      </p>
    </div>
  </div>
</section>

<!-- CTA FORM -->
<section id="cta">
  <div class="container fade-up">
    <p class="section-tag">Diagnóstico Gratuito</p>
    <h2 class="section-h2">Descubra agora quanto você pode economizar</h2>
    <p class="section-lead" style="margin:0 auto 2.5rem;">
      Preencha o formulário abaixo. Nossa equipe entra em contato em até 24h com uma análise personalizada da sua situação tributária.
    </p>

    <div class="cta-box">
      <div id="formWrapper">
        <form id="leadForm" novalidate>
          <div class="form-grid">
            <div class="form-group">
              <label for="nome">Nome completo *</label>
              <input type="text" id="nome" name="nome" placeholder="Dr. João Silva" required>
            </div>
            <div class="form-group">
              <label for="cnpj">CNPJ da clínica *</label>
              <input type="text" id="cnpj" name="cnpj" placeholder="00.000.000/0001-00" maxlength="18" required>
            </div>
            <div class="form-group">
              <label for="faturamento">Faturamento mensal *</label>
              <select id="faturamento" name="faturamento" required>
                <option value="">Selecione</option>
                <option value="Até R$ 10.000">Até R$ 10.000</option>
                <option value="R$ 10.001 a R$ 30.000">R$ 10.001 a R$ 30.000</option>
                <option value="R$ 30.001 a R$ 80.000">R$ 30.001 a R$ 80.000</option>
                <option value="R$ 80.001 a R$ 200.000">R$ 80.001 a R$ 200.000</option>
                <option value="Acima de R$ 200.000">Acima de R$ 200.000</option>
              </select>
            </div>
            <div class="form-group">
              <label for="regime">Regime tributário atual *</label>
              <select id="regime" name="regime" required>
                <option value="">Selecione</option>
                <option value="Simples Nacional">Simples Nacional</option>
                <option value="Lucro Presumido">Lucro Presumido</option>
                <option value="Lucro Real">Lucro Real</option>
                <option value="Não sei">Não sei informar</option>
              </select>
            </div>
            <div class="form-group">
              <label for="email">E-mail *</label>
              <input type="email" id="email" name="email" placeholder="seuemail@clinica.com.br" required>
            </div>
            <div class="form-group">
              <label for="whatsapp">WhatsApp *</label>
              <input type="tel" id="whatsapp" name="whatsapp" placeholder="(81) 99999-9999" maxlength="15" required>
            </div>
          </div>

          <button type="submit" class="btn-gold form-submit" id="submitBtn">
            <span id="btnText">Quero meu diagnóstico gratuito →</span>
          </button>

          <p class="form-privacy">
            🔒 Seus dados são sigilosos e não serão compartilhados com terceiros.
          </p>
        </form>
      </div>

      <div class="success-msg" id="successMsg">
        <div class="check">✓</div>
        <h3>Recebemos seus dados!</h3>
        <p>Nossa equipe entrará em contato em até 24h com a análise personalizada da sua situação tributária. Fique de olho no seu WhatsApp e e-mail.</p>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p style="color:var(--gold);font-family:var(--font-display);font-size:1.1rem;margin-bottom:0.5rem;">Q&M Contabilidade</p>
  <p>Especialistas em contabilidade para médicos e clínicas de saúde.</p>
  <p style="margin-top:0.5rem;">contabilidade.qem@gmail.com</p>
  <p style="margin-top:1rem;">© 2026 Q&M Contabilidade. Todos os direitos reservados.</p>
</footer>

<!-- FLOATING CTA -->
<div class="floating-cta" id="floatingCta">
  <a href="#cta" class="btn-gold" style="font-size:0.82rem;padding:0.75rem 1.4rem;">
    📋 Diagnóstico grátis
  </a>
</div>

<script>
  // ===== INTERSECTION OBSERVER (fade-up) =====
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) { e.target.classList.add('visible'); }
    });
  }, { threshold: 0.12 });
  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // ===== BAR CHART ANIMATION =====
  const chartObserver = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.bar-fill').forEach(bar => {
          bar.style.width = bar.dataset.width + '%';
        });
        chartObserver.unobserve(e.target);
      }
    });
  }, { threshold: 0.3 });
  const chart = document.querySelector('.bar-chart');
  if (chart) chartObserver.observe(chart);

  // ===== FAQ =====
  document.querySelectorAll('.faq-q').forEach(btn => {
    btn.addEventListener('click', () => {
      const item = btn.closest('.faq-item');
      const isOpen = item.classList.contains('open');
      document.querySelectorAll('.faq-item.open').forEach(i => i.classList.remove('open'));
      if (!isOpen) item.classList.add('open');
    });
  });

  // ===== FLOATING CTA =====
  const floatingCta = document.getElementById('floatingCta');
  window.addEventListener('scroll', () => {
    floatingCta.classList.toggle('show', window.scrollY > 500);
  });

  // ===== MASK CNPJ =====
  document.getElementById('cnpj').addEventListener('input', function () {
    let v = this.value.replace(/\D/g, '').substring(0, 14);
    v = v.replace(/^(\d{2})(\d)/, '$1.$2');
    v = v.replace(/^(\d{2})\.(\d{3})(\d)/, '$1.$2.$3');
    v = v.replace(/\.(\d{3})(\d)/, '.$1/$2');
    v = v.replace(/(\d{4})(\d)/, '$1-$2');
    this.value = v;
  });

  // ===== MASK WHATSAPP =====
  document.getElementById('whatsapp').addEventListener('input', function () {
    let v = this.value.replace(/\D/g, '').substring(0, 11);
    if (v.length > 6) v = '(' + v.substring(0,2) + ') ' + v.substring(2,7) + '-' + v.substring(7);
    else if (v.length > 2) v = '(' + v.substring(0,2) + ') ' + v.substring(2);
    else if (v.length > 0) v = '(' + v;
    this.value = v;
  });

  // ===== FORM SUBMIT =====
  document.getElementById('leadForm').addEventListener('submit', async function (e) {
    e.preventDefault();
    const btn = document.getElementById('submitBtn');
    const btnText = document.getElementById('btnText');

    // Validação simples
    const fields = ['nome','cnpj','faturamento','regime','email','whatsapp'];
    let valid = true;
    fields.forEach(f => {
      const el = document.getElementById(f);
      if (!el.value.trim()) { el.style.borderColor = '#C04040'; valid = false; }
      else el.style.borderColor = '';
    });
    if (!valid) return;

    btn.classList.add('loading');
    btnText.textContent = 'Enviando...';

    const payload = {
      nome: document.getElementById('nome').value,
      cnpj: document.getElementById('cnpj').value,
      faturamento: document.getElementById('faturamento').value,
      regime: document.getElementById('regime').value,
      email: document.getElementById('email').value,
      whatsapp: document.getElementById('whatsapp').value,
      data: new Date().toLocaleString('pt-BR')
    };

    // ─── ENVIO VIA FORMSPREE ───────────────────────────────────────────────
    // 1. Acesse https://formspree.io e crie uma conta gratuita
    // 2. Crie um novo form e substitua "SEU_ID_FORMSPREE" pelo ID gerado
    // 3. Configure o e-mail de destino como contabilidade.qem@gmail.com
    // ─────────────────────────────────────────────────────────────────────
    try {
      const res = await fetch('https://formspree.io/f/mwvwylpn', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json', 'Accept': 'application/json' },
        body: JSON.stringify(payload)
      });

      if (res.ok) {
        document.getElementById('formWrapper').style.display = 'none';
        document.getElementById('successMsg').style.display = 'block';
        // Scroll suave para a mensagem de sucesso
        document.getElementById('successMsg').scrollIntoView({ behavior: 'smooth', block: 'center' });
      } else {
        throw new Error('Erro no envio');
      }
    } catch (err) {
      // Fallback: abre o cliente de e-mail com os dados
      const body = encodeURIComponent(
        `Novo lead - Diagnóstico Gratuito\n\n` +
        `Nome: ${payload.nome}\nCNPJ: ${payload.cnpj}\nFaturamento: ${payload.faturamento}\n` +
        `Regime: ${payload.regime}\nE-mail: ${payload.email}\nWhatsApp: ${payload.whatsapp}\n` +
        `Data: ${payload.data}`
      );
      window.location.href = `mailto:contabilidade.qem@gmail.com?subject=Novo%20Lead%20-%20Diagn%C3%B3stico%20Gratuito&body=${body}`;
      document.getElementById('formWrapper').style.display = 'none';
      document.getElementById('successMsg').style.display = 'block';
    }

    btn.classList.remove('loading');
  });
</script>
</body>
</html>
