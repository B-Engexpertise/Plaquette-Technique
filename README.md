<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="description" content="B-Engineering – Bureau d'études structures à Dakar. Calculs béton armé, acier, génie civil, conformité Eurocodes et exigences clients. Expertise terrain France & Sénégal.">
<title>B-Engineering — Expertise en Calculs de Structures | Dakar</title>
<style>
  :root {
    --navy: #0a0f1e;
    --navy2: #0e1628;
    --navy3: #111d35;
    --orange: #e8621a;
    --orange2: #f07833;
    --electric: #1a9de8;
    --electric2: #3ab5f5;
    --white: #f0f4ff;
    --grey: #bdd2f0;
    --border: rgba(26,157,232,0.22);
    --grid: rgba(26,157,232,0.07);
    --transition: all 0.3s cubic-bezier(0.2, 0.9, 0.4, 1.1);
  }
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
  body { font-family: 'DM Sans', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif; background: var(--navy); color: var(--white); overflow-x: hidden; line-height: 1.6; font-size: 16px; }
  @font-face { font-family: 'Bebas Neue'; font-style: normal; font-weight: 400; src: local('Bebas Neue'), url('https://fonts.gstatic.com/s/bebasneue/v9/JTUSjIg69CK48gW7PXooxW5rygbi49c.woff2') format('woff2'); font-display: swap; }
  @font-face { font-family: 'DM Sans'; font-style: normal; font-weight: 300 700; src: local('DM Sans'), url('https://fonts.gstatic.com/s/dmsans/v11/rP2Hp2ywxg089UriCZOIHQ.woff2') format('woff2'); font-display: swap; }
  @font-face { font-family: 'JetBrains Mono'; font-style: normal; font-weight: 400 700; src: local('JetBrains Mono'), url('https://fonts.gstatic.com/s/jetbrainsmono/v13/tDbY2o-flEEny0FZhsfKu5WU4zr3E_BX0PnT8RD8yKxTN1OVgaY.woff2') format('woff2'); font-display: swap; }

  .bg-grid { position: fixed; inset: 0; z-index: 0; pointer-events: none; background-image: linear-gradient(var(--grid) 1px, transparent 1px), linear-gradient(90deg, var(--grid) 1px, transparent 1px); background-size: 60px 60px; }
  .bg-noise { position: fixed; inset: 0; z-index: 0; pointer-events: none; opacity: 0.02; background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)'/%3E%3C/svg%3E"); background-repeat: repeat; background-size: 180px; }
  section, footer { position: relative; z-index: 2; }

  body:not(.touch-device) { cursor: none; }
  .cursor-dot, .cursor-ring { display: none; }
  body:not(.touch-device) .cursor-dot, body:not(.touch-device) .cursor-ring { display: block; }
  .cursor-dot { width: 8px; height: 8px; background: var(--orange); border-radius: 50%; position: fixed; pointer-events: none; z-index: 9999; transform: translate(-50%,-50%); mix-blend-mode: screen; }
  .cursor-ring { width: 34px; height: 34px; border: 1.5px solid var(--electric); border-radius: 50%; position: fixed; pointer-events: none; z-index: 9998; transform: translate(-50%,-50%); transition: width 0.2s, height 0.2s, border-color 0.2s; opacity: 0.75; }
  .reveal { opacity: 0; transform: translateY(28px); transition: opacity 0.7s ease, transform 0.7s cubic-bezier(0.2, 0.9, 0.3, 1.1); will-change: opacity, transform; }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .btn { display: inline-flex; align-items: center; gap: 0.6rem; padding: 0.85rem 2rem; font-family: 'DM Sans', sans-serif; font-size: 12px; font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase; text-decoration: none; border: none; background: none; transition: var(--transition); cursor: pointer; }
  .btn-primary { background: var(--orange); color: #fff; clip-path: polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 8px 100%, 0 calc(100% - 8px)); }
  .btn-primary:hover { background: var(--orange2); transform: translateY(-2px); box-shadow: 0 8px 24px rgba(232,98,26,0.35); }
  .btn-outline { background: transparent; color: var(--electric2); border: 1px solid var(--electric); clip-path: polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 8px 100%, 0 calc(100% - 8px)); }
  .btn-outline:hover { background: rgba(26,157,232,0.12); transform: translateY(-2px); }
  .divider { height: 1px; background: linear-gradient(to right, transparent, var(--border), transparent); margin: 0 5vw; position: relative; z-index: 1; }
  .hero { min-height: 100vh; display: flex; flex-direction: column; justify-content: center; padding: 10vh 5vw 8vh; position: relative; }
  .hero::before { content: ''; position: absolute; right: -15vw; top: -10vh; width: 80vw; height: 70vh; background: radial-gradient(ellipse, rgba(232,98,26,0.1) 0%, rgba(26,157,232,0.05) 50%, transparent 80%); pointer-events: none; }
  .hero-tag { font-family: 'JetBrains Mono', monospace; font-size: 10px; letter-spacing: 0.25em; color: var(--electric2); text-transform: uppercase; margin-bottom: 2rem; display: flex; flex-wrap: wrap; align-items: center; gap: 1rem; }
  .hero-tag .dot { width: 5px; height: 5px; background: var(--orange); border-radius: 50%; display: inline-block; animation: blink 1.4s infinite; }
  .hero-logo { font-family: 'Bebas Neue', sans-serif; font-size: clamp(58px, 13vw, 150px); line-height: 1.1; }
  .hero-logo .orange-b { color: var(--orange); }
  .hero-logo .main-line { font-size: clamp(58px, 13vw, 150px); font-family: 'Bebas Neue', sans-serif; display: block; }
  .hero-logo .sub-line { font-size: clamp(16px, 3.5vw, 36px); font-family: 'DM Sans', sans-serif; font-weight: 300; letter-spacing: 0.1em; color: var(--grey); margin-top: 0.5rem; }
  .hero-sub { font-size: clamp(15px, 4vw, 21px); font-weight: 400; color: var(--white); opacity: 0.85; margin-top: 1.8rem; max-width: 580px; line-height: 1.65; }
  .hero-cta { margin-top: 2.5rem; display: flex; gap: 1rem; flex-wrap: wrap; }
  .hero-metrics { margin-top: 4rem; display: flex; gap: 2rem; flex-wrap: wrap; }
  .metric-num { font-family: 'Bebas Neue', sans-serif; font-size: 40px; color: var(--white); line-height: 1; }
  .metric-num span { color: var(--orange); font-size: 28px; }
  .metric-label { font-family: 'JetBrains Mono', monospace; font-size: 9px; letter-spacing: 0.15em; color: var(--grey); text-transform: uppercase; margin-top: 5px; }
  .section-label { font-family: 'JetBrains Mono', monospace; font-size: 11px; letter-spacing: 0.3em; color: var(--electric2); text-transform: uppercase; display: flex; align-items: center; gap: 0.8rem; margin-bottom: 1rem; }
  .section-label::before { content: ''; width: 28px; height: 1px; background: var(--electric); }
  .section-title { font-family: 'Bebas Neue', sans-serif; font-size: clamp(34px, 8vw, 72px); line-height: 1.05; }
  .about { padding: 8vh 5vw; display: grid; grid-template-columns: 1fr; gap: 3rem; align-items: center; }
  @media (min-width: 800px) { .about { grid-template-columns: 1fr 1fr; gap: 4rem; } }
  .about-visual { position: relative; min-height: 380px; display: flex; justify-content: center; align-items: center; }
  .blueprint-box { position: absolute; border: 1px solid var(--border); background: var(--navy2); opacity: 0.7; }
  .bb1 { width: 220px; height: 280px; top: 0; left: 0; }
  .bb2 { width: 170px; height: 170px; bottom: 0; right: 0; border-color: rgba(232,98,26,0.3); }
  .about-card { position: relative; padding: 1.5rem; background: linear-gradient(145deg, var(--navy3), var(--navy2)); border: 1px solid var(--border); width: 260px; z-index: 3; margin: 0 auto; }
  .about-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(to right, var(--orange), var(--electric)); }
  .ac-label { font-family: 'JetBrains Mono', monospace; font-size: 9px; letter-spacing: 0.3em; color: var(--orange); margin-bottom: 0.7rem; }
  .ac-title { font-family: 'Bebas Neue', sans-serif; font-size: 28px; line-height: 1; margin-bottom: 0.5rem; }
  .ac-desc { font-size: 11px; color: var(--grey); }
  .about-text p { color: var(--grey); line-height: 1.75; font-size: 16px; font-weight: 400; margin-bottom: 1.2rem; }
  .norms { display: flex; gap: 0.8rem; flex-wrap: wrap; margin-top: 1.5rem; }
  .norm-badge { padding: 0.3rem 0.8rem; font-family: 'JetBrains Mono', monospace; font-size: 10px; letter-spacing: 0.05em; border: 1px solid var(--border); color: var(--electric2); background: rgba(26,157,232,0.02); }
  .services { padding: 8vh 5vw; background: var(--navy2); }
  .services-header { display: flex; justify-content: space-between; align-items: flex-end; flex-wrap: wrap; margin-bottom: 3rem; gap: 1rem; }
  .services-num { font-family: 'Bebas Neue', sans-serif; font-size: 80px; color: rgba(255,255,255,0.03); line-height: 1; }
  .services-grid { display: grid; grid-template-columns: 1fr; gap: 2px; background: var(--border); }
  @media (min-width: 640px) { .services-grid { grid-template-columns: repeat(2, 1fr); } }
  @media (min-width: 1024px) { .services-grid { grid-template-columns: repeat(3, 1fr); } }
  .service-card { background: var(--navy); padding: 2rem; transition: var(--transition); cursor: pointer; }
  .service-card:hover { background: var(--navy3); transform: translateY(-3px); }
  .service-icon svg { width: 30px; height: 30px; stroke: var(--electric2); stroke-width: 1.4; margin-bottom: 1rem; }
  .service-num { font-family: 'JetBrains Mono', monospace; font-size: 9px; color: var(--orange); letter-spacing: 0.2em; margin-bottom: 0.5rem; }
  .service-title { font-family: 'Bebas Neue', sans-serif; font-size: 28px; margin-bottom: 0.8rem; }
  .service-desc { font-size: 14px; color: var(--grey); line-height: 1.75; font-weight: 400; }
  .service-tags { margin-top: 1.2rem; display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .stag { font-family: 'JetBrains Mono', monospace; font-size: 8px; padding: 3px 8px; background: rgba(26,157,232,0.1); border: 1px solid rgba(26,157,232,0.2); color: var(--electric2); text-transform: uppercase; }
  .methodology { padding: 8vh 5vw; }
  .meth-header { display: grid; grid-template-columns: 1fr; gap: 1.5rem; margin-bottom: 3rem; }
  @media (min-width: 800px) { .meth-header { grid-template-columns: 1fr 1fr; align-items: end; gap: 2rem; } }
  .meth-desc { color: var(--grey); line-height: 1.7; font-size: 14px; }
  .steps { display: grid; grid-template-columns: 1fr; gap: 1rem; }
  @media (min-width: 640px) { .steps { grid-template-columns: repeat(2, 1fr); } }
  @media (min-width: 1024px) { .steps { grid-template-columns: repeat(4, 1fr); gap: 1.5rem; } }
  .step { background: var(--navy2); padding: 1.6rem; transition: var(--transition); }
  .step:hover { transform: translateY(-3px); background: var(--navy3); }
  .step-num { width: 44px; height: 44px; border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; font-family: 'Bebas Neue', sans-serif; font-size: 20px; color: var(--orange); margin-bottom: 1rem; background: var(--navy); }
  .step-title { font-weight: 700; font-size: 16px; margin-bottom: 0.5rem; }
  .step-desc { font-size: 13px; color: var(--grey); line-height: 1.65; }
  .software { padding: 8vh 5vw; background: var(--navy3); }
  .sw-grid { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 2rem; }
  .sw-item { flex: 1 1 170px; padding: 1.2rem; background: var(--navy); border: 1px solid var(--border); transition: var(--transition); display: flex; align-items: center; gap: 1rem; }
  .sw-item:hover { border-color: var(--electric); transform: translateY(-2px); background: var(--navy2); }
  .sw-icon svg { width: 26px; height: 26px; fill: var(--electric2); stroke: none; }
  .sw-name { font-weight: 600; font-size: 14px; }
  .team { padding: 8vh 5vw; display: grid; grid-template-columns: 1fr; gap: 2.5rem; }
  @media (min-width: 800px) { .team { grid-template-columns: 1fr 1fr; gap: 4rem; } }
  .team-grid { display: flex; flex-direction: column; gap: 1.5rem; }
  .team-card { padding: 1.5rem; background: var(--navy2); border: 1px solid var(--border); display: grid; grid-template-columns: 52px 1fr; gap: 1rem; transition: var(--transition); }
  .team-card:hover { border-color: var(--orange); transform: translateX(4px); }
  .team-avatar { width: 52px; height: 52px; background: linear-gradient(135deg, var(--orange), var(--electric)); display: flex; align-items: center; justify-content: center; font-family: 'Bebas Neue', sans-serif; font-size: 20px; color: white; }
  .team-name { font-weight: 700; font-size: 16px; }
  .team-title { font-family: 'JetBrains Mono', monospace; font-size: 10px; letter-spacing: 0.12em; color: var(--orange); margin-bottom: 0.4rem; }
  .team-desc { font-size: 13px; color: var(--grey); line-height: 1.6; }
  .contact { padding: 8vh 5vw; background: var(--navy2); }
  .contact-inner { display: grid; grid-template-columns: 1fr; gap: 2.5rem; }
  @media (min-width: 800px) { .contact-inner { grid-template-columns: 1.2fr 1fr; gap: 4rem; } }
  .contact-info { margin-top: 2rem; display: flex; flex-direction: column; gap: 1rem; }
  .ci-item { display: flex; align-items: center; gap: 1rem; padding: 0.8rem; background: var(--navy); border: 1px solid var(--border); }
  .ci-icon { width: 36px; height: 36px; border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; color: var(--orange); flex-shrink: 0; }
  .ci-label { font-family: 'JetBrains Mono', monospace; font-size: 9px; letter-spacing: 0.2em; color: var(--grey); text-transform: uppercase; }
  .ci-value { font-size: 14px; color: var(--white); font-weight: 600; word-break: break-word; }
  .form-group { margin-bottom: 1.2rem; }
  .form-group label { display: block; font-family: 'JetBrains Mono', monospace; font-size: 9px; letter-spacing: 0.2em; color: var(--electric2); margin-bottom: 0.4rem; }
  .form-group input, .form-group textarea, .form-group select { width: 100%; padding: 0.7rem 1rem; background: var(--navy); border: 1px solid var(--border); color: var(--white); font-family: 'DM Sans', sans-serif; font-size: 13px; outline: none; transition: border 0.2s; }
  .form-group input:focus, .form-group textarea:focus, .form-group select:focus { border-color: var(--electric); background: var(--navy3); }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  footer { padding: 2rem 5vw; border-top: 1px solid var(--border); display: flex; flex-direction: column; gap: 1rem; align-items: center; text-align: center; }
  @media (min-width: 640px) { footer { flex-direction: row; justify-content: space-between; text-align: left; } }
  .footer-logo { font-family: 'Bebas Neue', sans-serif; font-size: 28px; }
  .footer-logo span { color: var(--orange); }
  .footer-copy { font-family: 'JetBrains Mono', monospace; font-size: 9px; color: var(--grey); letter-spacing: 0.1em; }
  .footer-links { display: flex; gap: 1.2rem; }
  .footer-links a { font-family: 'JetBrains Mono', monospace; font-size: 9px; letter-spacing: 0.1em; color: var(--grey); text-decoration: none; transition: color 0.2s; }
  .footer-links a:hover { color: var(--orange); }
  @keyframes blink { 0%,100%{ opacity:1; } 50%{ opacity:0.3; } }

  /* ══ Print pages: invisible on screen ══ */
  .print-pages { display: none !important; }

  /* ════════════════════════════════════════════
     PRINT MEDIA QUERY
  ════════════════════════════════════════════ */
  @media print {
    @page { size: A4 landscape; margin: 0; }

    *, *::before, *::after {
      -webkit-print-color-adjust: exact !important;
      print-color-adjust: exact !important;
      color-adjust: exact !important;
    }

    body { background: #ffffff !important; margin: 0; padding: 0; }
    .bg-grid, .bg-noise, .cursor-dot, .cursor-ring,
    main > section, main > .divider, footer { display: none !important; }
    .print-pages { display: block !important; }

    /* Each page exactly fills A4 landscape */
    .p-page {
      width: 297mm;
      height: 210mm;
      overflow: hidden;
      position: relative;
      page-break-after: always;
      break-after: page;
      display: flex;
    }
    .p-page:last-child { page-break-after: avoid; break-after: avoid; }

    /* ─── PAGE FOOTER STRIP (all pages) ─── */
    .p-foot {
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 8mm;
      background: #0a0f1e;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 10mm;
      z-index: 10;
    }
    .p-foot-brand { font-family: 'Bebas Neue', sans-serif; font-size: 10.5pt; color: rgba(240,244,255,0.45); }
    .p-foot-brand span { color: #e8621a; }
    .p-foot-info { font-family: 'JetBrains Mono', monospace; font-size: 5.5pt; color: rgba(160,187,223,0.45); letter-spacing: 0.1em; }
    .p-foot-pg { font-family: 'JetBrains Mono', monospace; font-size: 7pt; color: rgba(160,187,223,0.45); letter-spacing: 0.12em; }

    /* ════════════════
       PAGE 1: COVER + ABOUT
    ════════════════ */
    .p1 { flex-direction: row; background: #ffffff; }

    .p1-left {
      width: 107mm;
      flex-shrink: 0;
      background: #0a0f1e;
      display: flex;
      flex-direction: column;
      position: relative;
    }
    .p1-top-bar {
      height: 5mm;
      background: linear-gradient(to right, #e8621a, #1a9de8);
      flex-shrink: 0;
    }
    .p1-left-body {
      flex: 1;
      padding: 11mm 12mm 18mm;
      display: flex;
      flex-direction: column;
    }
    .p1-eyebrow {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6.5pt;
      color: #3ab5f5;
      letter-spacing: 0.28em;
      text-transform: uppercase;
      margin-bottom: 5mm;
    }
    .p1-logo-main {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 46pt;
      line-height: 0.95;
      color: #f0f4ff;
      margin-bottom: 2mm;
    }
    .p1-logo-main .ob { color: #e8621a; }
    .p1-logo-sub {
      font-family: 'DM Sans', sans-serif;
      font-size: 9.5pt;
      font-weight: 300;
      letter-spacing: 0.18em;
      color: rgba(160,187,223,0.7);
      margin-bottom: 7mm;
      text-transform: uppercase;
    }
    .p1-rule { height: 1px; background: linear-gradient(to right, #e8621a 30%, transparent); margin-bottom: 6mm; }
    .p1-pitch {
      font-family: 'DM Sans', sans-serif;
      font-size: 9pt;
      font-weight: 300;
      color: #a0bbdf;
      line-height: 1.65;
      margin-bottom: 8mm;
    }
    .p1-rule2 { height: 1px; background: rgba(26,157,232,0.25); margin-bottom: 7mm; }
    .p1-kpi-list { display: flex; flex-direction: column; gap: 5mm; flex: 1; }
    .p1-kpi-num {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 30pt;
      color: #f0f4ff;
      line-height: 1;
    }
    .p1-kpi-num .acc { color: #e8621a; font-size: 22pt; }
    .p1-kpi-lbl {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6.5pt;
      color: rgba(160,187,223,0.6);
      letter-spacing: 0.15em;
      text-transform: uppercase;
      margin-top: 1mm;
    }
    .p1-left-tag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6pt;
      color: rgba(160,187,223,0.3);
      letter-spacing: 0.12em;
      text-transform: uppercase;
      padding-top: 5mm;
      border-top: 1px solid rgba(26,157,232,0.12);
    }

    .p1-right {
      flex: 1;
      display: flex;
      flex-direction: column;
      background: #ffffff;
      padding: 0;
    }
    .p1-right-top-bar {
      height: 5mm;
      background: #f0f6ff;
      flex-shrink: 0;
    }
    .p1-right-body {
      flex: 1;
      padding: 10mm 12mm 18mm;
      display: flex;
      flex-direction: column;
    }
    .p1-stag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6.5pt;
      color: #1a9de8;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      display: flex;
      align-items: center;
      gap: 5mm;
      margin-bottom: 4mm;
    }
    .p1-stag::before { content: ''; width: 8mm; height: 1px; background: #1a9de8; flex-shrink: 0; }
    .p1-rtitle {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 30pt;
      line-height: 1.05;
      color: #0a0f1e;
      margin-bottom: 5mm;
    }
    .p1-rtitle .hl { color: #e8621a; }
    .p1-rtext {
      font-family: 'DM Sans', sans-serif;
      font-size: 9pt;
      font-weight: 300;
      color: #374151;
      line-height: 1.65;
      margin-bottom: 3.5mm;
    }
    .p1-badges {
      display: flex;
      gap: 3mm;
      flex-wrap: wrap;
      margin-top: 4.5mm;
      margin-bottom: 5mm;
    }
    .p1-badge-item {
      padding: 2mm 5mm;
      font-family: 'JetBrains Mono', monospace;
      font-size: 7pt;
      letter-spacing: 0.08em;
      border: 1px solid #1a9de8;
      color: #1a9de8;
      background: #e8f4fd;
    }
    .p1-bottom-card {
      margin-top: auto;
      background: #0a0f1e;
      padding: 6mm 8mm;
      display: flex;
      align-items: center;
      gap: 6mm;
      position: relative;
    }
    .p1-bottom-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
      background: linear-gradient(to right, #e8621a, #1a9de8);
    }
    .p1-card-big {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 38pt;
      color: rgba(240,244,255,0.06);
      line-height: 1;
      flex-shrink: 0;
    }
    .p1-card-t {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 14pt;
      color: #f0f4ff;
      line-height: 1.1;
    }
    .p1-card-s {
      font-family: 'DM Sans', sans-serif;
      font-size: 7.5pt;
      color: #a0bbdf;
      margin-top: 1.5mm;
    }

    /* ════════════════
       PAGE 2: SERVICES
    ════════════════ */
    .p2 { flex-direction: column; background: #f2f6fb; }
    .p2-head {
      height: 20mm;
      background: #0a0f1e;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 12mm;
      flex-shrink: 0;
      position: relative;
    }
    .p2-head::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(to right, #e8621a, #f07833, #1a9de8, #3ab5f5, #1a9de8);
    }
    .p2-head-left {}
    .p2-head-tag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6.5pt;
      color: #3ab5f5;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      margin-bottom: 1.5mm;
    }
    .p2-head-h {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 20pt;
      color: #f0f4ff;
      letter-spacing: 0.02em;
      line-height: 1;
    }
    .p2-head-h .oa { color: #e8621a; }
    .p2-head-right {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 12pt;
      color: rgba(240,244,255,0.12);
      letter-spacing: 0.05em;
    }
    .p2-head-right span { color: #e8621a; opacity: 1; }

    .p2-grid-wrap {
      flex: 1;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: repeat(2, 1fr);
      gap: 2px;
      background: #c5d2e0;
      padding-bottom: 8mm;
    }
    .p2c {
      background: #ffffff;
      padding: 7mm 8mm 6mm 10mm;
      display: flex;
      flex-direction: column;
      position: relative;
      overflow: hidden;
    }
    .p2c::before {
      content: '';
      position: absolute;
      left: 0; top: 0; bottom: 0;
      width: 3.5px;
    }
    .p2c:nth-child(odd)::before { background: #e8621a; }
    .p2c:nth-child(even)::before { background: #1a9de8; }
    .p2c-ghost {
      position: absolute;
      right: 2mm;
      bottom: -3mm;
      font-family: 'Bebas Neue', sans-serif;
      font-size: 52pt;
      color: rgba(10,15,30,0.045);
      line-height: 1;
      pointer-events: none;
    }
    .p2c-num {
      font-family: 'JetBrains Mono', monospace;
      font-size: 7pt;
      color: #e8621a;
      letter-spacing: 0.22em;
      margin-bottom: 2mm;
    }
    .p2c:nth-child(even) .p2c-num { color: #1a9de8; }
    .p2c-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 15.5pt;
      color: #0a0f1e;
      line-height: 1.1;
      margin-bottom: 2.5mm;
    }
    .p2c-desc {
      font-family: 'DM Sans', sans-serif;
      font-size: 8.5pt;
      color: #4b5563;
      line-height: 1.55;
      font-weight: 300;
      flex: 1;
    }
    .p2c-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 2mm;
      margin-top: 3.5mm;
    }
    .p2c-tag {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6pt;
      padding: 1.5mm 3.5mm;
      background: #e8f4fd;
      border: 1px solid #93c5fd;
      color: #1d4ed8;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }
    .p2c:nth-child(odd) .p2c-tag { background: #fff3ed; border-color: #fed7aa; color: #c2410c; }
    .p2c-ico {
      width: 6.5mm;
      height: 6.5mm;
      margin-bottom: 2.5mm;
    }
    .p2c-ico svg { width: 100%; height: 100%; fill: none; stroke: #1a9de8; stroke-width: 1.5; }
    .p2c:nth-child(odd) .p2c-ico svg { stroke: #e8621a; }

    /* ════════════════
       PAGE 3: MÉTHODE + ÉQUIPE + CONTACT
    ════════════════ */
    .p3 { flex-direction: column; background: #ffffff; }
    .p3-head {
      height: 17mm;
      background: #0e1628;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 12mm;
      flex-shrink: 0;
      position: relative;
    }
    .p3-head::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(to right, #1a9de8, #3ab5f5, #e8621a, #3ab5f5, #1a9de8);
    }
    .p3-head-h {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 16pt;
      color: #f0f4ff;
      letter-spacing: 0.04em;
    }
    .p3-head-h span { color: #e8621a; }
    .p3-head-r {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6.5pt;
      color: rgba(160,187,223,0.4);
      letter-spacing: 0.15em;
    }

    .p3-body {
      flex: 1;
      display: grid;
      grid-template-columns: 1fr 1fr;
      padding-bottom: 8mm;
    }

    /* Left col */
    .p3-left {
      border-right: 1.5px solid #e5eaf2;
      display: flex;
      flex-direction: column;
      background: #f7fafd;
    }
    .p3-meth-wrap {
      flex: 1;
      padding: 7mm 10mm 5mm;
    }
    .p3-slabel {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6.5pt;
      color: #1a9de8;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      display: flex;
      align-items: center;
      gap: 4mm;
      margin-bottom: 3mm;
    }
    .p3-slabel::before { content: ''; width: 7mm; height: 1px; background: #1a9de8; flex-shrink: 0; }
    .p3-stitle {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 20pt;
      color: #0a0f1e;
      line-height: 1.05;
      margin-bottom: 5mm;
    }
    .p3-stitle .b1 { color: #1a9de8; }
    .p3-stitle .b2 { color: #e8621a; }
    .p3-4steps {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3mm;
    }
    .p3s {
      background: #ffffff;
      border: 1px solid #dde6f0;
      padding: 4mm 5mm;
      position: relative;
    }
    .p3s::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2.5px;
    }
    .p3s:nth-child(1)::before, .p3s:nth-child(4)::before { background: #e8621a; }
    .p3s:nth-child(2)::before, .p3s:nth-child(3)::before { background: #1a9de8; }
    .p3s-n {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 20pt;
      line-height: 1;
      margin-bottom: 1.5mm;
    }
    .p3s:nth-child(1) .p3s-n, .p3s:nth-child(4) .p3s-n { color: #e8621a; }
    .p3s:nth-child(2) .p3s-n, .p3s:nth-child(3) .p3s-n { color: #1a9de8; }
    .p3s-t { font-family: 'DM Sans', sans-serif; font-size: 8.5pt; font-weight: 700; color: #0a0f1e; margin-bottom: 1.5mm; }
    .p3s-d { font-family: 'DM Sans', sans-serif; font-size: 7.5pt; color: #4b5563; line-height: 1.5; }

    /* Software dark strip */
    .p3-sw-strip {
      background: #0a0f1e;
      padding: 4mm 10mm;
      display: flex;
      align-items: center;
      gap: 5mm;
      border-top: 1px solid #1d2b4a;
    }
    .p3-sw-ttl {
      font-family: 'JetBrains Mono', monospace;
      font-size: 6pt;
      color: #3ab5f5;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      white-space: nowrap;
      flex-shrink: 0;
    }
    .p3-sw-sep { width: 1px; height: 7mm; background: rgba(26,157,232,0.3); flex-shrink: 0; }
    .p3-sw-list { display: flex; gap: 3.5mm; flex-wrap: wrap; }
    .p3-sw-pill {
      font-family: 'DM Sans', sans-serif;
      font-size: 7.5pt;
      font-weight: 600;
      color: #e2e8f0;
      padding: 1.5mm 3.5mm;
      border: 1px solid rgba(26,157,232,0.3);
      background: rgba(26,157,232,0.1);
    }

    /* Right col */
    .p3-right {
      display: flex;
      flex-direction: column;
      background: #ffffff;
    }
    .p3-team-wrap {
      flex: 1;
      padding: 7mm 10mm 5mm;
      border-bottom: 1.5px solid #e5eaf2;
    }
    .p3-team-cards {
      display: flex;
      flex-direction: column;
      gap: 3mm;
      margin-top: 4mm;
    }
    .p3-tc {
      display: flex;
      gap: 4mm;
      align-items: flex-start;
      padding: 4mm 5mm 4mm 4mm;
      border: 1px solid #e5eaf2;
      background: #f7fafd;
      position: relative;
    }
    .p3-tc::before {
      content: '';
      position: absolute;
      left: 0; top: 0; bottom: 0;
      width: 3px;
      background: linear-gradient(to bottom, #e8621a, #1a9de8);
    }
    .p3-av {
      width: 11mm;
      height: 11mm;
      background: linear-gradient(135deg, #e8621a, #1a9de8);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Bebas Neue', sans-serif;
      font-size: 12pt;
      color: white;
      flex-shrink: 0;
    }
    .p3-tc-role { font-family: 'JetBrains Mono', monospace; font-size: 6pt; color: #e8621a; letter-spacing: 0.1em; text-transform: uppercase; }
    .p3-tc-name { font-family: 'DM Sans', sans-serif; font-size: 9pt; font-weight: 700; color: #0a0f1e; margin-bottom: 1.5mm; }
    .p3-tc-desc { font-family: 'DM Sans', sans-serif; font-size: 7.5pt; color: #4b5563; line-height: 1.5; }

    .p3-contact-wrap {
      padding: 5mm 10mm 5mm;
      background: #f7fafd;
    }
    .p3-ci-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2.5mm;
      margin-top: 3.5mm;
    }
    .p3ci {
      display: flex;
      align-items: center;
      gap: 3mm;
      padding: 2.5mm 3.5mm;
      background: #ffffff;
      border: 1px solid #e2e8f0;
      border-left: 3px solid #1a9de8;
    }
    .p3ci:nth-child(1) { border-left-color: #e8621a; }
    .p3ci:nth-child(2) { border-left-color: #3ab5f5; }
    .p3ci-last { grid-column: 1 / -1; border-left-color: #6366f1 !important; }
    .p3ci-ico { font-size: 9pt; flex-shrink: 0; }
    .p3ci-lbl { font-family: 'JetBrains Mono', monospace; font-size: 5.5pt; color: #9ca3af; letter-spacing: 0.15em; text-transform: uppercase; }
    .p3ci-val { font-family: 'DM Sans', sans-serif; font-size: 8pt; font-weight: 600; color: #0a0f1e; }
  }
</style>
</head>
<body>

<div class="cursor-dot" id="cursorDot"></div>
<div class="cursor-ring" id="cursorRing"></div>
<div class="bg-grid"></div>
<div class="bg-noise"></div>

<main>
  <!-- ════ WEB SECTIONS ════ -->
  <section class="hero" aria-label="Présentation B-Engineering">
    <div class="hero-tag"><span><span class="dot"></span> Bureau d'études · Dakar, Sénégal</span></div>
    <div class="hero-logo">
      <div class="main-line"><span class="orange-b">B</span>-Engineering <span style="font-size:0.5em;letter-spacing:0;">(</span><span class="orange-b">B</span><span style="font-size:0.5em;">-Eng</span><span style="font-size:0.5em;">)</span></div>
      <div class="sub-line">INGÉNIERIE STRUCTURALE</div>
    </div>
    <p class="hero-sub"><strong>Calculs de structures</strong> de précision pour bâtiments et infrastructures.<br>Béton armé · Acier · Génie civil — Conformité Eurocodes et exigences clients.</p>
    <div class="hero-cta"><a href="#contact" class="btn btn-primary">Nous contacter</a><a href="#services" class="btn btn-outline">Nos prestations</a></div>
    <div class="hero-metrics">
      <div class="metric"><div class="metric-num">2<span>+</span></div><div class="metric-label">Continents d'expérience</div></div>
      <div class="metric"><div class="metric-num">100<span>%</span></div><div class="metric-label">Conformité réglementaire</div></div>
      <div class="metric"><div class="metric-num">5M<span>₣</span></div><div class="metric-label">Capital CFA</div></div>
    </div>
  </section>
  <div class="divider"></div>
  <section class="about" id="about">
    <div class="about-visual"><div class="blueprint-box bb1"></div><div class="blueprint-box bb2"></div><div class="about-card"><div class="ac-label">// À propos</div><div class="ac-title">Ingénierie<br>de haut niveau</div><div class="ac-desc">Expertise terrain France & Sénégal.</div></div></div>
    <div class="about-text">
      <div class="section-label reveal">À propos de B-Engineering</div>
      <h2 class="section-title reveal">Une ingénierie<br>dédiée aux<br><span style="color:var(--orange)">structures</span></h2>
      <p class="reveal"><strong>B-Engineering</strong> est un bureau d'études techniques basé à Dakar, porté par une ambition claire : offrir une ingénierie de structures de haut niveau au Sénégal.</p>
      <p class="reveal">Jeune par son immatriculation, B-Engineering s'appuie sur des fondateurs au parcours d'excellence : formation entre l'École Supérieure Polytechnique de Dakar, l'Université Cheikh Anta Diop et l'École Centrale de Lyon, complétée par une expérience terrain solide en France et au Sénégal.</p>
      <div class="norms reveal"><span class="norm-badge">Eurocodes</span><span class="norm-badge">RCC-CW</span><span class="norm-badge">RCC-M</span></div>
    </div>
  </section>
  <div class="divider"></div>
  <section class="services" id="services">
    <div class="services-header"><div><div class="section-label reveal">Ce que nous faisons</div><h2 class="section-title reveal">Nos<br><span style="color:var(--orange)">prestations</span></h2></div><div class="services-num reveal">06</div></div>
    <div class="services-grid">
      <div class="service-card reveal"><div class="service-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><rect x="3" y="3" width="18" height="18" rx="1"/><line x1="3" y1="9" x2="21" y2="9"/><line x1="9" y1="3" x2="9" y2="21"/></svg></div><div class="service-num">01 —</div><div class="service-title">Calculs de Structures</div><div class="service-desc">Modélisation 3D éléments finis, dimensionnement multi-matériaux, notes de calcul détaillées.</div><div class="service-tags"><span class="stag">Béton Armé</span><span class="stag">Acier</span><span class="stag">EF 3D</span></div></div>
      <div class="service-card reveal"><div class="service-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M2 20h20M4 20V10l8-8 8 8v10"/><path d="M10 20v-6h4v6"/></svg></div><div class="service-num">02 —</div><div class="service-title">Études Techniques</div><div class="service-desc">APS, APD, DCE, plans de ferraillage et charpente avec traçabilité rigoureuse.</div><div class="service-tags"><span class="stag">APS/APD</span><span class="stag">Ferraillage</span></div></div>
      <div class="service-card reveal"><div class="service-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><circle cx="12" cy="12" r="10"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg></div><div class="service-num">03 —</div><div class="service-title">Expertise & Diagnostic</div><div class="service-desc">Diagnostic d'ouvrages, expertise structurelle, contrôle de conformité.</div><div class="service-tags"><span class="stag">Diagnostic</span><span class="stag">Conformité</span></div></div>
      <div class="service-card reveal"><div class="service-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg></div><div class="service-num">04 —</div><div class="service-title">Ouvrages Béton Armé</div><div class="service-desc">Fondations, poteaux, poutres, dalles, voiles, réservoirs spéciaux.</div><div class="service-tags"><span class="stag">Bâtiments résidentiels</span><span class="stag">Ouvrages industriels</span></div></div>
      <div class="service-card reveal"><div class="service-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><polyline points="4 12 12 4 20 12"/><line x1="12" y1="4" x2="12" y2="20"/><line x1="2" y1="20" x2="22" y2="20"/></svg></div><div class="service-num">05 —</div><div class="service-title">Structures Métalliques</div><div class="service-desc">Charpentes, halles industrielles, passerelles, assemblages complexes.</div><div class="service-tags"><span class="stag">Charpentes</span><span class="stag">Assemblages</span></div></div>
      <div class="service-card reveal"><div class="service-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div><div class="service-num">06 —</div><div class="service-title">Génie Civil & Infra</div><div class="service-desc">Ouvrages d'art, infrastructures routières, approche adaptée au contexte local.</div><div class="service-tags"><span class="stag">Ponts</span><span class="stag">Routes</span></div></div>
    </div>
  </section>
  <div class="divider"></div>
  <section class="methodology" id="methodology">
    <div class="meth-header"><div><div class="section-label reveal">Comment nous travaillons</div><h2 class="section-title reveal">Notre <span style="color:var(--electric2)">méthodo</span><span style="color:var(--orange)">logie</span></h2></div><p class="meth-desc reveal">Processus structuré en quatre phases garantissant rigueur et conformité.</p></div>
    <div class="steps"><div class="step reveal"><div class="step-num">01</div><div class="step-title">Analyse & Hypothèses</div><div class="step-desc">Recueil données architecturales, géotechniques, charges environnementales.</div></div><div class="step reveal"><div class="step-num">02</div><div class="step-title">Modélisation & Calculs</div><div class="step-desc">Modèle numérique 3D, vérifications réglementaires, optimisation sections.</div></div><div class="step reveal"><div class="step-num">03</div><div class="step-title">Rapport & Plans</div><div class="step-desc">Note de calcul, plans d'exécution et détails d'armatures.</div></div><div class="step reveal"><div class="step-num">04</div><div class="step-title">Accompagnement</div><div class="step-desc">Assistance technique au chantier, contrôle de conformité.</div></div></div>
  </section>
  <div class="divider"></div>
  <section class="software" id="software">
    <div><div class="section-label reveal">Outils & Logiciels</div><h2 class="section-title reveal">Simulation <span style="color:var(--electric2)">avancée</span></h2></div>
    <div class="sw-grid">
      <div class="sw-item reveal"><div class="sw-icon"><svg viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg></div><div><div class="sw-name">Robot Structural</div></div></div>
      <div class="sw-item reveal"><div class="sw-icon"><svg viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2"/><line x1="8" y1="21" x2="16" y2="21"/></svg></div><div><div class="sw-name">RSTAB / RFEM</div></div></div>
      <div class="sw-item reveal"><div class="sw-icon"><svg viewBox="0 0 24 24"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"/></svg></div><div><div class="sw-name">Autocad / Archicad / Revit</div></div></div>
      <div class="sw-item reveal"><div class="sw-icon"><svg viewBox="0 0 24 24"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/></svg></div><div><div class="sw-name">Graitec Advance</div></div></div>
    </div>
  </section>
  <div class="divider"></div>
  <section class="team" id="team">
    <div><div class="section-label reveal">Notre équipe</div><h2 class="section-title reveal">Des experts<br><span style="color:var(--orange)">engagés</span></h2><p class="reveal" style="margin-top:1.5rem;color:var(--grey);">L'équipe dirigeante combine expertise en génie civil, modélisation BIM et expérience terrain France & Sénégal.</p><div class="reveal" style="margin-top:2rem;padding:1.2rem;border:1px solid var(--border);background:var(--navy2);"><div style="font-family:'JetBrains Mono';font-size:9px;color:var(--orange);">// Réseau de partenaires</div><p style="font-size:12px;color:var(--grey);margin-top:0.5rem;">B-Engineering s'appuie sur un réseau de partenaires géotechniciens et formateurs qualifiés.</p></div></div>
    <div class="team-grid"><div class="team-card reveal"><div class="team-avatar">AB</div><div><div class="team-name">M. Alassane BOUSSO</div><div class="team-title">Gérant — Fondateur</div><div class="team-desc">Ingénieur génie civil, spécialiste en <strong>calcul de structures et pilotage de conception en génie civil</strong>. Expérience terrain en France et au Sénégal, orientée ouvrages industriels, barrages et structures nucléaires.</div></div></div><div class="team-card reveal"><div class="team-avatar">HS</div><div><div class="team-name">M. Hamidou SY</div><div class="team-title">Co-Gérant — Fondateur</div><div class="team-desc">Ingénieur bâtiment, expert en <strong>conception et calcul de bâtiments résidentiels, matériaux en terre</strong> et modélisation BIM pour une coordination multidisciplinaire optimale.</div></div></div></div>
  </section>
  <div class="divider"></div>
  <section class="contact" id="contact">
    <div class="contact-inner">
      <div><div class="section-label reveal">Travaillons ensemble</div><h2 class="section-title reveal">Démarrons<br>votre <span style="color:var(--orange)">projet</span></h2><p class="reveal">Maîtres d'ouvrage, architectes, entreprises — B-Engineering est votre partenaire technique.</p>
      <div class="contact-info reveal"><div class="ci-item"><div class="ci-icon">✉️</div><div><div class="ci-label">Email</div><div class="ci-value">contact@b-engexpertise.com</div></div></div><div class="ci-item"><div class="ci-icon">📞</div><div><div class="ci-label">Téléphone (Sénégal)</div><div class="ci-value">+221 77 842 52 51</div></div></div><div class="ci-item"><div class="ci-icon">📞</div><div><div class="ci-label">Téléphone (France)</div><div class="ci-value">+33 7 62 71 51 09</div></div></div><div class="ci-item"><div class="ci-icon">🌍</div><div><div class="ci-label">Site web</div><div class="ci-value">www.b-engexpertise.com</div></div></div><div class="ci-item"><div class="ci-icon">📍</div><div><div class="ci-label">Adresse</div><div class="ci-value">Parcelles Assainies 5085 — Dakar, Sénégal</div></div></div></div></div>
      <form class="contact-form reveal" action="#" method="post" novalidate><div class="form-row"><div class="form-group"><label for="prenom">Prénom</label><input type="text" id="prenom" name="prenom" placeholder="Votre prénom"></div><div class="form-group"><label for="nom">Nom</label><input type="text" id="nom" name="nom" placeholder="Votre nom"></div></div><div class="form-group"><label for="email">Email</label><input type="email" id="email" name="email" placeholder="votre@email.com"></div><div class="form-group"><label for="projet">Type de projet</label><select id="projet" name="projet"><option value="">Sélectionner un domaine</option><option>Bâtiment résidentiel</option><option>Bâtiment industriel</option><option>Infrastructure / Génie civil</option><option>Diagnostic / Expertise</option></select></div><div class="form-group"><label for="message">Description du projet</label><textarea id="message" name="message" rows="3" placeholder="Décrivez brièvement votre projet..."></textarea></div><button type="submit" class="btn btn-primary" style="width:100%;justify-content:center;">Envoyer la demande</button></form>
    </div>
  </section>
</main>

<footer><div class="footer-logo"><span>B</span>-Engineering</div><div class="footer-copy">© 2023 B-Engineering · SARL capital 5 000 000 F CFA<br>Calculs structures — Conformité — Performance</div><div class="footer-links"><a href="#services">Services</a><a href="#methodology">Méthode</a><a href="#team">Équipe</a><a href="#contact">Contact</a></div></footer>

<!-- ════════════════════════════════════════════════════════════
     PRINT PAGES — hidden on screen, shown only when printing
════════════════════════════════════════════════════════════ -->
<div class="print-pages">

  <!-- ═══ PAGE 1 : COVER + ABOUT ═══ -->
  <div class="p-page p1">
    <!-- Left dark panel -->
    <div class="p1-left">
      <div class="p1-top-bar"></div>
      <div class="p1-left-body">
        <div class="p1-eyebrow">Bureau d'études · Dakar, Sénégal</div>
        <div class="p1-logo-main"><span class="ob">B</span>-Eng<br>ineering</div>
        <div class="p1-logo-sub">Ingénierie Structurale</div>
        <div class="p1-rule"></div>
        <div class="p1-pitch">Calculs de structures de précision pour bâtiments et infrastructures. Béton armé · Acier · Génie civil — Conformité Eurocodes.</div>
        <div class="p1-rule2"></div>
        <div class="p1-kpi-list">
          <div><div class="p1-kpi-num">2<span class="acc">+</span></div><div class="p1-kpi-lbl">Continents d'expérience</div></div>
          <div><div class="p1-kpi-num">100<span class="acc">%</span></div><div class="p1-kpi-lbl">Conformité réglementaire</div></div>
          <div><div class="p1-kpi-num">5M<span class="acc">₣</span></div><div class="p1-kpi-lbl">Capital CFA</div></div>
        </div>
        <div class="p1-left-tag">SARL · RC Dakar · Fondé 2023</div>
      </div>
    </div>
    <!-- Right content panel -->
    <div class="p1-right">
      <div class="p1-right-top-bar"></div>
      <div class="p1-right-body">
        <div class="p1-stag">À propos de B-Engineering</div>
        <div class="p1-rtitle">Une ingénierie<br>dédiée aux <span class="hl">structures</span></div>
        <div class="p1-rtext"><strong>B-Engineering</strong> est un bureau d'études techniques basé à Dakar, porté par une ambition claire : offrir une ingénierie de structures de haut niveau au Sénégal.</div>
        <div class="p1-rtext">Jeune par son immatriculation, B-Engineering s'appuie sur des fondateurs au parcours d'excellence : formation entre l'École Supérieure Polytechnique de Dakar, l'Université Cheikh Anta Diop et l'École Centrale de Lyon, complétée par une expérience terrain solide acquise en France et au Sénégal.</div>
        <div class="p1-rtext">Notre bureau maîtrise l'ensemble des phases d'une étude structurale, de la conception préliminaire à l'assistance chantier, en pleine conformité avec les référentiels normatifs en vigueur et les exigences spécifiques de chaque client.</div>
        <div class="p1-badges">
          <span class="p1-badge-item">Eurocodes</span>
          <span class="p1-badge-item">RCC-CW</span>
          <span class="p1-badge-item">RCC-M</span>
        </div>
        <div class="p1-bottom-card">
          <div class="p1-card-big">B</div>
          <div>
            <div class="p1-card-t">Ingénierie de haut niveau</div>
            <div class="p1-card-s">Expertise terrain France & Sénégal — au service de vos projets</div>
          </div>
        </div>
      </div>
    </div>
    <div class="p-foot">
      <div class="p-foot-brand"><span>B</span>-Engineering</div>
      <div class="p-foot-info">contact@b-engexpertise.com · +221 77 842 52 51 · www.b-engexpertise.com</div>
      <div class="p-foot-pg">01 / 03</div>
    </div>
  </div>

  <!-- ═══ PAGE 2 : SERVICES ═══ -->
  <div class="p-page p2">
    <div class="p2-head">
      <div class="p2-head-left">
        <div class="p2-head-tag">Ce que nous faisons</div>
        <div class="p2-head-h">Nos <span class="oa">Prestations</span></div>
      </div>
      <div class="p2-head-right"><span>B</span>-Engineering · Bureau d'études structures · Dakar</div>
    </div>
    <div class="p2-grid-wrap">
      <div class="p2c">
        <div class="p2c-ico"><svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="1"/><line x1="3" y1="9" x2="21" y2="9"/><line x1="9" y1="3" x2="9" y2="21"/></svg></div>
        <div class="p2c-num">01 ——</div>
        <div class="p2c-title">Calculs de Structures</div>
        <div class="p2c-desc">Modélisation 3D éléments finis, dimensionnement multi-matériaux et rédaction de notes de calcul détaillées conformes aux normes en vigueur.</div>
        <div class="p2c-tags"><span class="p2c-tag">Béton Armé</span><span class="p2c-tag">Acier</span><span class="p2c-tag">EF 3D</span></div>
        <div class="p2c-ghost">01</div>
      </div>
      <div class="p2c">
        <div class="p2c-ico"><svg viewBox="0 0 24 24"><path d="M2 20h20M4 20V10l8-8 8 8v10"/><path d="M10 20v-6h4v6"/></svg></div>
        <div class="p2c-num">02 ——</div>
        <div class="p2c-title">Études Techniques</div>
        <div class="p2c-desc">Avant-projets sommaires et détaillés (APS/APD), dossiers de consultation des entreprises (DCE), plans de ferraillage et charpente.</div>
        <div class="p2c-tags"><span class="p2c-tag">APS/APD</span><span class="p2c-tag">Ferraillage</span><span class="p2c-tag">DCE</span></div>
        <div class="p2c-ghost">02</div>
      </div>
      <div class="p2c">
        <div class="p2c-ico"><svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg></div>
        <div class="p2c-num">03 ——</div>
        <div class="p2c-title">Expertise & Diagnostic</div>
        <div class="p2c-desc">Diagnostic structurel d'ouvrages existants, expertise après sinistres, contrôle de conformité et recommandations de renforcement.</div>
        <div class="p2c-tags"><span class="p2c-tag">Diagnostic</span><span class="p2c-tag">Conformité</span></div>
        <div class="p2c-ghost">03</div>
      </div>
      <div class="p2c">
        <div class="p2c-ico"><svg viewBox="0 0 24 24"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg></div>
        <div class="p2c-num">04 ——</div>
        <div class="p2c-title">Ouvrages Béton Armé</div>
        <div class="p2c-desc">Conception et calcul de fondations, poteaux, poutres, dalles, voiles de contreventement et réservoirs. Résidentiels, tertiaires et industriels.</div>
        <div class="p2c-tags"><span class="p2c-tag">Résidentiel</span><span class="p2c-tag">Industriel</span></div>
        <div class="p2c-ghost">04</div>
      </div>
      <div class="p2c">
        <div class="p2c-ico"><svg viewBox="0 0 24 24"><polyline points="4 12 12 4 20 12"/><line x1="12" y1="4" x2="12" y2="20"/><line x1="2" y1="20" x2="22" y2="20"/></svg></div>
        <div class="p2c-num">05 ——</div>
        <div class="p2c-title">Structures Métalliques</div>
        <div class="p2c-desc">Calcul et dimensionnement de charpentes, halles industrielles, passerelles et assemblages complexes boulonnés ou soudés.</div>
        <div class="p2c-tags"><span class="p2c-tag">Charpentes</span><span class="p2c-tag">Assemblages</span></div>
        <div class="p2c-ghost">05</div>
      </div>
      <div class="p2c">
        <div class="p2c-ico"><svg viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div>
        <div class="p2c-num">06 ——</div>
        <div class="p2c-title">Génie Civil & Infra</div>
        <div class="p2c-desc">Ouvrages d'art, infrastructures routières et hydrauliques, approche adaptée aux spécificités du contexte local ouest-africain.</div>
        <div class="p2c-tags"><span class="p2c-tag">Ponts</span><span class="p2c-tag">Routes</span></div>
        <div class="p2c-ghost">06</div>
      </div>
    </div>
    <div class="p-foot">
      <div class="p-foot-brand"><span>B</span>-Engineering</div>
      <div class="p-foot-info">contact@b-engexpertise.com · +221 77 842 52 51 · www.b-engexpertise.com</div>
      <div class="p-foot-pg">02 / 03</div>
    </div>
  </div>

  <!-- ═══ PAGE 3 : MÉTHODE + ÉQUIPE + CONTACT ═══ -->
  <div class="p-page p3">
    <div class="p3-head">
      <div class="p3-head-h">Méthodologie · Équipe · <span>Contact</span></div>
      <div class="p3-head-r">B-Engineering · Dakar · 2023</div>
    </div>
    <div class="p3-body">
      <!-- Left: Methodology + Software -->
      <div class="p3-left">
        <div class="p3-meth-wrap">
          <div class="p3-slabel">Comment nous travaillons</div>
          <div class="p3-stitle">Notre <span class="b1">méthodo</span><span class="b2">logie</span></div>
          <div class="p3-4steps">
            <div class="p3s"><div class="p3s-n">01</div><div class="p3s-t">Analyse & Hypothèses</div><div class="p3s-d">Recueil des données architecturales, géotechniques et des charges environnementales.</div></div>
            <div class="p3s"><div class="p3s-n">02</div><div class="p3s-t">Modélisation & Calculs</div><div class="p3s-d">Modèle numérique 3D, vérifications réglementaires et optimisation des sections.</div></div>
            <div class="p3s"><div class="p3s-n">03</div><div class="p3s-t">Rapport & Plans</div><div class="p3s-d">Note de calcul complète, plans d'exécution et détails d'armatures.</div></div>
            <div class="p3s"><div class="p3s-n">04</div><div class="p3s-t">Accompagnement</div><div class="p3s-d">Assistance technique au chantier et contrôle de conformité des ouvrages.</div></div>
          </div>
        </div>
        <div class="p3-sw-strip">
          <div class="p3-sw-ttl">Logiciels</div>
          <div class="p3-sw-sep"></div>
          <div class="p3-sw-list">
            <div class="p3-sw-pill">Robot Structural</div>
            <div class="p3-sw-pill">RSTAB / RFEM</div>
            <div class="p3-sw-pill">AutoCAD · Revit · Archicad</div>
            <div class="p3-sw-pill">Graitec Advance</div>
          </div>
        </div>
      </div>
      <!-- Right: Team + Contact -->
      <div class="p3-right">
        <div class="p3-team-wrap">
          <div class="p3-slabel">Notre équipe</div>
          <div class="p3-stitle">Des experts <span class="b2">engagés</span></div>
          <div class="p3-team-cards">
            <div class="p3-tc">
              <div class="p3-av">AB</div>
              <div>
                <div class="p3-tc-role">Gérant — Fondateur</div>
                <div class="p3-tc-name">M. Alassane BOUSSO</div>
                <div class="p3-tc-desc">Ingénieur génie civil, spécialiste en calcul de structures et pilotage de conception. Expérience France & Sénégal, orientée ouvrages industriels, barrages et structures nucléaires.</div>
              </div>
            </div>
            <div class="p3-tc">
              <div class="p3-av">HS</div>
              <div>
                <div class="p3-tc-role">Co-Gérant — Fondateur</div>
                <div class="p3-tc-name">M. Hamidou SY</div>
                <div class="p3-tc-desc">Ingénieur bâtiment, expert en conception de bâtiments résidentiels, matériaux en terre et modélisation BIM pour une coordination multidisciplinaire optimale.</div>
              </div>
            </div>
          </div>
        </div>
        <div class="p3-contact-wrap">
          <div class="p3-slabel">Travaillons ensemble</div>
          <div class="p3-ci-grid">
            <div class="p3ci"><div class="p3ci-ico">✉️</div><div><div class="p3ci-lbl">Email</div><div class="p3ci-val">contact@b-engexpertise.com</div></div></div>
            <div class="p3ci"><div class="p3ci-ico">🌍</div><div><div class="p3ci-lbl">Site web</div><div class="p3ci-val">www.b-engexpertise.com</div></div></div>
            <div class="p3ci"><div class="p3ci-ico">📞</div><div><div class="p3ci-lbl">Sénégal</div><div class="p3ci-val">+221 77 842 52 51</div></div></div>
            <div class="p3ci"><div class="p3ci-ico">📞</div><div><div class="p3ci-lbl">France</div><div class="p3ci-val">+33 7 62 71 51 09</div></div></div>
            <div class="p3ci p3ci-last"><div class="p3ci-ico">📍</div><div><div class="p3ci-lbl">Adresse</div><div class="p3ci-val">Parcelles Assainies 5085 — Dakar, Sénégal</div></div></div>
          </div>
        </div>
      </div>
    </div>
    <div class="p-foot">
      <div class="p-foot-brand"><span>B</span>-Engineering</div>
      <div class="p-foot-info">SARL au capital de 5 000 000 F CFA · Calculs structures — Conformité — Performance</div>
      <div class="p-foot-pg">03 / 03</div>
    </div>
  </div>

</div><!-- end .print-pages -->

<script>
(function(){
  const isTouch = ('ontouchstart' in window)||(navigator.maxTouchPoints>0);
  if(isTouch) document.body.classList.add('touch-device');
  if(!isTouch){
    const dot=document.getElementById('cursorDot'), ring=document.getElementById('cursorRing');
    let mx=0,my=0,rx=0,ry=0;
    document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;});
    (function anim(){dot.style.left=mx+'px';dot.style.top=my+'px';rx+=(mx-rx)*.12;ry+=(my-ry)*.12;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(anim);})();
    document.querySelectorAll('a,button,.service-card,.team-card,.sw-item,.btn').forEach(el=>{
      el.addEventListener('mouseenter',()=>{ring.style.width='54px';ring.style.height='54px';ring.style.borderColor='var(--orange)';dot.style.opacity='0';});
      el.addEventListener('mouseleave',()=>{ring.style.width='34px';ring.style.height='34px';ring.style.borderColor='var(--electric)';dot.style.opacity='1';});
    });
  }
  // Reveal on scroll
  const reveals = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver(entries=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('visible'); } });
  },{threshold:0.12});
  reveals.forEach(el=>io.observe(el));
})();
</script>
</body>
</html>
[Plaquette_Officiel_B-Eng.html](https://github.com/user-attachments/files/26240995/Plaquette_Officiel_B-Eng.html)
