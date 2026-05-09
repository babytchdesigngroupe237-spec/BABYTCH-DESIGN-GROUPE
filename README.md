<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<meta name="description" content="Babytch Design Groupe – Spécialiste en aménagement intérieur, carrelage, peinture, faux-plafonds, caméras de sécurité et climatisation à Abidjan et au Cameroun."/>
<meta name="keywords" content="aménagement intérieur Abidjan, carrelage Cameroun, peinture intérieure, placoplatre Abidjan, caméra sécurité Cameroun, climatisation Abidjan"/>
<title>Babytch Design Groupe | Aménagement Intérieur – Abidjan & Cameroun</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=Jost:wght@200;300;400;500;600;700&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
<style>
:root {
  --navy: #0e1628;
  --navy-mid: #162035;
  --navy-light: #1e2d4a;
  --gold: #c9a24b;
  --gold-light: #e4c07a;
  --gold-dark: #9e7a2e;
  --cream: #f8f4ec;
  --cream-dark: #ede8dd;
  --white: #ffffff;
  --text-light: #c8cdd8;
  --text-mid: #8892a4;
  --font-display: 'Cormorant Garamond', Georgia, serif;
  --font-body: 'Jost', sans-serif;
  --transition: 0.45s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; font-size: 16px; }

body {
  font-family: var(--font-body);
  background: var(--navy);
  color: var(--white);
  overflow-x: hidden;
  cursor: none;
}

/* CUSTOM CURSOR */
.cursor {
  position: fixed; width: 10px; height: 10px;
  background: var(--gold); border-radius: 50%;
  pointer-events: none; z-index: 9999;
  transform: translate(-50%, -50%);
  transition: transform 0.1s, width 0.3s, height 0.3s, background 0.3s;
}
.cursor-ring {
  position: fixed; width: 36px; height: 36px;
  border: 1.5px solid var(--gold); border-radius: 50%;
  pointer-events: none; z-index: 9998;
  transform: translate(-50%, -50%);
  transition: transform 0.25s ease, width 0.3s, height 0.3s;
  opacity: 0.6;
}
.cursor.hovered { width: 16px; height: 16px; background: var(--gold-light); }
.cursor-ring.hovered { width: 56px; height: 56px; opacity: 0.3; }

/* NOISE TEXTURE OVERLAY */
body::before {
  content: '';
  position: fixed; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.035'/%3E%3C/svg%3E");
  pointer-events: none; z-index: 1000; opacity: 0.4;
}

/* ===== NAVBAR ===== */
nav {
  position: fixed; top: 0; left: 0; right: 0;
  z-index: 900;
  padding: 0 5%;
  display: flex; align-items: center; justify-content: space-between;
  height: 72px;
  transition: var(--transition);
}
nav.scrolled {
  background: rgba(14, 22, 40, 0.97);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(201, 162, 75, 0.15);
  height: 60px;
}
.nav-logo {
  display: flex; align-items: center; gap: 12px;
  text-decoration: none;
}
.logo-icon {
  width: 40px; height: 40px;
  border: 2px solid var(--gold);
  display: flex; align-items: center; justify-content: center;
  font-family: var(--font-display); font-size: 20px;
  color: var(--gold); font-weight: 700;
  position: relative; overflow: hidden;
}
.logo-icon::before {
  content: ''; position: absolute; inset: -1px;
  background: linear-gradient(135deg, var(--gold) 0%, transparent 50%);
  opacity: 0.12;
}
.logo-text {
  display: flex; flex-direction: column; line-height: 1;
}
.logo-name {
  font-family: var(--font-display); font-size: 18px;
  font-weight: 600; color: var(--white); letter-spacing: 0.02em;
}
.logo-tagline {
  font-size: 9px; letter-spacing: 0.25em;
  color: var(--gold); text-transform: uppercase; font-weight: 400;
}
.nav-links {
  display: flex; gap: 40px; list-style: none;
}
.nav-links a {
  font-size: 11px; letter-spacing: 0.18em; text-transform: uppercase;
  color: var(--text-light); text-decoration: none; font-weight: 500;
  position: relative; padding-bottom: 4px;
  transition: color 0.3s;
}
.nav-links a::after {
  content: ''; position: absolute; bottom: 0; left: 0;
  width: 0; height: 1px; background: var(--gold);
  transition: width 0.35s ease;
}
.nav-links a:hover { color: var(--gold); }
.nav-links a:hover::after { width: 100%; }
.nav-cta {
  padding: 10px 24px; border: 1px solid var(--gold);
  color: var(--gold); font-size: 10px; letter-spacing: 0.18em;
  text-transform: uppercase; text-decoration: none; font-weight: 500;
  transition: var(--transition); position: relative; overflow: hidden;
}
.nav-cta::before {
  content: ''; position: absolute; inset: 0;
  background: var(--gold); transform: translateX(-100%);
  transition: transform 0.35s ease;
}
.nav-cta:hover { color: var(--navy); }
.nav-cta:hover::before { transform: translateX(0); }
.nav-cta span { position: relative; z-index: 1; }
.hamburger {
  display: none; flex-direction: column; gap: 5px;
  cursor: pointer; padding: 4px;
}
.hamburger span {
  display: block; width: 24px; height: 1.5px;
  background: var(--gold); transition: var(--transition);
}
.mobile-menu {
  display: none; position: fixed; inset: 0;
  background: var(--navy); z-index: 800;
  flex-direction: column; align-items: center; justify-content: center;
  gap: 36px;
}
.mobile-menu.open { display: flex; }
.mobile-menu a {
  font-family: var(--font-display); font-size: 36px;
  color: var(--white); text-decoration: none; font-weight: 300;
  letter-spacing: 0.04em; transition: color 0.3s;
}
.mobile-menu a:hover { color: var(--gold); }

/* ===== HERO ===== */
#hero {
  min-height: 100vh;
  display: flex; align-items: center;
  position: relative; overflow: hidden;
  padding: 0 5%;
}
.hero-bg {
  position: absolute; inset: 0;
  background: 
    radial-gradient(ellipse 80% 60% at 60% 50%, rgba(201,162,75,0.07) 0%, transparent 70%),
    linear-gradient(160deg, #0e1628 0%, #162035 50%, #0e1628 100%);
}
.hero-grid-lines {
  position: absolute; inset: 0;
  background-image: 
    linear-gradient(rgba(201,162,75,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(201,162,75,0.04) 1px, transparent 1px);
  background-size: 80px 80px;
}
.hero-orb {
  position: absolute; right: 5%; top: 50%;
  transform: translateY(-50%);
  width: min(55vw, 700px); aspect-ratio: 1;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(201,162,75,0.12) 0%, rgba(201,162,75,0.04) 40%, transparent 70%);
  animation: pulse 6s ease-in-out infinite;
}
.hero-orb::before {
  content: ''; position: absolute; inset: 40px;
  border-radius: 50%; border: 1px solid rgba(201,162,75,0.15);
  animation: rotate 20s linear infinite;
}
.hero-orb::after {
  content: ''; position: absolute; inset: 100px;
  border-radius: 50%; border: 1px solid rgba(201,162,75,0.08);
  animation: rotate 30s linear infinite reverse;
}
@keyframes pulse { 0%,100%{opacity:0.6; transform:translateY(-50%) scale(1)} 50%{opacity:1; transform:translateY(-50%) scale(1.04)} }
@keyframes rotate { from{transform:rotate(0deg)} to{transform:rotate(360deg)} }

.hero-content {
  position: relative; z-index: 2;
  max-width: 660px;
}
.hero-badge {
  display: inline-flex; align-items: center; gap: 10px;
  border: 1px solid rgba(201,162,75,0.3);
  padding: 8px 20px; margin-bottom: 40px;
  font-size: 10px; letter-spacing: 0.25em; text-transform: uppercase;
  color: var(--gold); font-weight: 500;
  opacity: 0; animation: fadeUp 0.8s 0.2s ease forwards;
}
.hero-badge::before { content: ''; width: 20px; height: 1px; background: var(--gold); }
.hero-badge::after { content: ''; width: 20px; height: 1px; background: var(--gold); }

.hero-title {
  font-family: var(--font-display);
  font-size: clamp(52px, 7vw, 96px);
  font-weight: 300; line-height: 1.0;
  letter-spacing: -0.01em;
  margin-bottom: 28px;
  opacity: 0; animation: fadeUp 0.9s 0.4s ease forwards;
}
.hero-title em {
  font-style: italic; color: var(--gold);
  font-weight: 300;
}
.hero-title strong { font-weight: 600; }

.hero-sub {
  font-size: 14px; font-weight: 300; line-height: 1.85;
  color: var(--text-light); max-width: 500px; margin-bottom: 52px;
  opacity: 0; animation: fadeUp 0.9s 0.6s ease forwards;
}
.hero-actions {
  display: flex; gap: 20px; flex-wrap: wrap;
  opacity: 0; animation: fadeUp 0.9s 0.8s ease forwards;
}
.btn-primary {
  display: inline-flex; align-items: center; gap: 12px;
  padding: 16px 36px; background: var(--gold);
  color: var(--navy); font-size: 11px; letter-spacing: 0.18em;
  text-transform: uppercase; text-decoration: none; font-weight: 600;
  transition: var(--transition); position: relative; overflow: hidden;
}
.btn-primary::before {
  content: ''; position: absolute; inset: 0;
  background: var(--gold-light); transform: scaleX(0); transform-origin: right;
  transition: transform 0.35s ease;
}
.btn-primary:hover { color: var(--navy); }
.btn-primary:hover::before { transform: scaleX(1); transform-origin: left; }
.btn-primary span, .btn-primary i { position: relative; z-index: 1; }

.btn-outline {
  display: inline-flex; align-items: center; gap: 12px;
  padding: 15px 36px; border: 1px solid rgba(255,255,255,0.2);
  color: var(--white); font-size: 11px; letter-spacing: 0.18em;
  text-transform: uppercase; text-decoration: none; font-weight: 400;
  transition: var(--transition);
}
.btn-outline:hover { border-color: var(--gold); color: var(--gold); }

.hero-scroll {
  position: absolute; bottom: 40px; left: 50%; transform: translateX(-50%);
  display: flex; flex-direction: column; align-items: center; gap: 8px;
  font-size: 9px; letter-spacing: 0.25em; text-transform: uppercase;
  color: var(--text-mid); z-index: 2;
  opacity: 0; animation: fadeUp 1s 1.4s ease forwards;
}
.scroll-line {
  width: 1px; height: 50px;
  background: linear-gradient(to bottom, var(--gold), transparent);
  animation: scrollDown 1.8s ease-in-out infinite;
}
@keyframes scrollDown {
  0% { transform: scaleY(0); transform-origin: top; }
  50% { transform: scaleY(1); transform-origin: top; }
  51% { transform-origin: bottom; }
  100% { transform: scaleY(0); transform-origin: bottom; }
}

.hero-stats {
  position: absolute; bottom: 40px; right: 5%;
  display: flex; gap: 48px; z-index: 2;
  opacity: 0; animation: fadeUp 1s 1s ease forwards;
}
.stat-item { text-align: right; }
.stat-num {
  font-family: var(--font-display); font-size: 40px;
  font-weight: 300; color: var(--gold); line-height: 1;
}
.stat-label {
  font-size: 9px; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--text-mid); margin-top: 4px;
}

@keyframes fadeUp { from{opacity:0;transform:translateY(30px)} to{opacity:1;transform:translateY(0)} }

/* ===== MARQUEE BAND ===== */
.marquee-band {
  border-top: 1px solid rgba(201,162,75,0.2);
  border-bottom: 1px solid rgba(201,162,75,0.2);
  background: rgba(201,162,75,0.04);
  overflow: hidden; padding: 14px 0;
}
.marquee-track {
  display: flex; gap: 0; white-space: nowrap;
  animation: marquee 30s linear infinite;
}
.marquee-item {
  display: inline-flex; align-items: center; gap: 20px;
  padding: 0 32px; font-size: 10px; letter-spacing: 0.22em;
  text-transform: uppercase; color: var(--text-mid); font-weight: 400;
}
.marquee-dot { width: 4px; height: 4px; border-radius: 50%; background: var(--gold); flex-shrink: 0; }
@keyframes marquee { from{transform:translateX(0)} to{transform:translateX(-50%)} }

/* ===== SECTIONS COMMON ===== */
section { padding: 120px 5%; position: relative; }
.section-label {
  display: inline-flex; align-items: center; gap: 16px;
  font-size: 9px; letter-spacing: 0.3em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 20px; font-weight: 500;
}
.section-label::before { content: ''; width: 32px; height: 1px; background: var(--gold); }
.section-title {
  font-family: var(--font-display);
  font-size: clamp(36px, 4.5vw, 64px);
  font-weight: 300; line-height: 1.1;
  margin-bottom: 24px;
}
.section-title em { font-style: italic; color: var(--gold); }
.section-intro {
  font-size: 14px; font-weight: 300; line-height: 1.9;
  color: var(--text-light); max-width: 560px;
}
.reveal { opacity: 0; transform: translateY(40px); transition: opacity 0.8s ease, transform 0.8s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }

/* ===== ABOUT ===== */
#about { background: var(--navy-mid); }
.about-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 80px; align-items: center; margin-top: 72px;
}
.about-visual {
  position: relative; aspect-ratio: 4/5; overflow: hidden;
}
.about-img-placeholder {
  width: 100%; height: 100%;
  background: linear-gradient(135deg, var(--navy-light) 0%, #243355 100%);
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  gap: 16px; position: relative; overflow: hidden;
}
.about-img-placeholder::before {
  content: ''; position: absolute; inset: 0;
  background: 
    repeating-linear-gradient(45deg, rgba(201,162,75,0.03) 0, rgba(201,162,75,0.03) 1px, transparent 0, transparent 50%);
  background-size: 20px 20px;
}
.about-img-icon { font-size: 64px; color: var(--gold); opacity: 0.4; position: relative; }
.about-img-text { font-size: 11px; letter-spacing: 0.2em; color: var(--text-mid); text-transform: uppercase; }
.about-corner {
  position: absolute; width: 50px; height: 50px;
  border-color: var(--gold); border-style: solid; opacity: 0.5;
}
.about-corner.tl { top: 20px; left: 20px; border-width: 2px 0 0 2px; }
.about-corner.br { bottom: 20px; right: 20px; border-width: 0 2px 2px 0; }
.about-badge {
  position: absolute; bottom: -20px; right: -20px;
  width: 140px; height: 140px; border-radius: 50%;
  background: var(--gold); display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  font-family: var(--font-display);
}
.about-badge-num { font-size: 40px; font-weight: 600; color: var(--navy); line-height: 1; }
.about-badge-text { font-size: 9px; letter-spacing: 0.1em; color: var(--navy); text-transform: uppercase; text-align: center; line-height: 1.4; }

.about-content { padding-left: 20px; }
.about-values {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 20px; margin-top: 40px;
}
.value-card {
  padding: 24px; border: 1px solid rgba(201,162,75,0.12);
  background: rgba(201,162,75,0.02); transition: var(--transition);
}
.value-card:hover { border-color: rgba(201,162,75,0.35); background: rgba(201,162,75,0.05); }
.value-icon { font-size: 24px; color: var(--gold); margin-bottom: 12px; }
.value-title { font-size: 13px; font-weight: 600; letter-spacing: 0.05em; margin-bottom: 6px; }
.value-desc { font-size: 12px; color: var(--text-mid); line-height: 1.7; }

.about-flags {
  display: flex; gap: 20px; margin-top: 36px; flex-wrap: wrap;
}
.flag-tag {
  display: flex; align-items: center; gap: 8px;
  padding: 8px 16px; border: 1px solid rgba(201,162,75,0.25);
  font-size: 11px; letter-spacing: 0.08em; color: var(--text-light);
}
.flag-emoji { font-size: 18px; }

/* ===== SERVICES ===== */
#services { background: var(--navy); }
.services-header { display: flex; align-items: flex-end; justify-content: space-between; gap: 40px; }
.services-grid {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 1px; background: rgba(201,162,75,0.1);
  margin-top: 64px; border: 1px solid rgba(201,162,75,0.1);
}
.service-card {
  background: var(--navy);
  padding: 48px 36px;
  transition: var(--transition); position: relative;
  overflow: hidden; cursor: pointer;
}
.service-card::before {
  content: ''; position: absolute; inset: 0;
  background: linear-gradient(135deg, rgba(201,162,75,0.06) 0%, transparent 60%);
  opacity: 0; transition: opacity 0.4s;
}
.service-card::after {
  content: ''; position: absolute; bottom: 0; left: 0; right: 0;
  height: 2px; background: var(--gold);
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.4s ease;
}
.service-card:hover::before { opacity: 1; }
.service-card:hover::after { transform: scaleX(1); }
.service-card:hover { transform: translateY(-4px); }

.service-num {
  font-family: var(--font-display); font-size: 64px;
  font-weight: 300; color: rgba(201,162,75,0.08);
  line-height: 1; margin-bottom: 16px;
  transition: color 0.4s;
}
.service-card:hover .service-num { color: rgba(201,162,75,0.18); }
.service-icon {
  font-size: 28px; color: var(--gold); margin-bottom: 20px;
  display: block;
}
.service-name {
  font-family: var(--font-display); font-size: 22px;
  font-weight: 400; margin-bottom: 14px; line-height: 1.2;
}
.service-desc {
  font-size: 12px; line-height: 1.85; color: var(--text-mid);
  margin-bottom: 24px;
}
.service-items {
  list-style: none; display: flex; flex-direction: column; gap: 6px;
}
.service-items li {
  font-size: 11px; color: var(--text-mid); display: flex; align-items: center; gap: 10px;
}
.service-items li::before {
  content: '—'; color: var(--gold); font-weight: 300; flex-shrink: 0;
}

/* ===== PORTFOLIO ===== */
#portfolio { background: var(--navy-mid); }
.portfolio-filters {
  display: flex; gap: 4px; flex-wrap: wrap;
  margin-top: 52px; margin-bottom: 48px;
}
.filter-btn {
  padding: 9px 22px; border: 1px solid rgba(255,255,255,0.1);
  background: transparent; color: var(--text-mid);
  font-family: var(--font-body); font-size: 10px; letter-spacing: 0.18em;
  text-transform: uppercase; cursor: pointer; transition: var(--transition);
  font-weight: 500;
}
.filter-btn:hover, .filter-btn.active {
  background: var(--gold); border-color: var(--gold);
  color: var(--navy);
}
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto;
  gap: 16px;
}
.portfolio-item {
  position: relative; overflow: hidden;
  background: var(--navy-light);
  cursor: pointer;
  transition: var(--transition);
}
.portfolio-item:nth-child(1) { grid-column: span 2; aspect-ratio: 16/9; }
.portfolio-item:nth-child(2) { aspect-ratio: 9/10; }
.portfolio-item:nth-child(3) { aspect-ratio: 9/10; }
.portfolio-item:nth-child(4) { aspect-ratio: 16/9; grid-column: span 2; }
.portfolio-item:nth-child(5) { aspect-ratio: 4/5; }
.portfolio-item:nth-child(6) { aspect-ratio: 4/5; }

.portfolio-placeholder {
  width: 100%; height: 100%;
  background: linear-gradient(135deg, var(--navy-light), #1a2a45);
  display: flex; flex-direction: column;
  align-items: center; justify-content: center; gap: 12px;
  transition: var(--transition); position: relative;
}
.portfolio-placeholder::after {
  content: ''; position: absolute; inset: 0;
  background: 
    repeating-linear-gradient(135deg, rgba(201,162,75,0.02) 0, rgba(201,162,75,0.02) 1px, transparent 0, transparent 50%);
  background-size: 15px 15px;
}
.portfolio-icon { font-size: 36px; color: var(--gold); opacity: 0.3; }
.portfolio-label { font-size: 10px; letter-spacing: 0.2em; color: var(--text-mid); text-transform: uppercase; }

.portfolio-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(to top, rgba(14,22,40,0.95) 0%, rgba(14,22,40,0.4) 60%, transparent 100%);
  display: flex; flex-direction: column; justify-content: flex-end;
  padding: 28px; opacity: 0; transition: opacity 0.4s;
}
.portfolio-item:hover .portfolio-overlay { opacity: 1; }
.portfolio-item:hover .portfolio-placeholder { transform: scale(1.04); }
.po-tag {
  font-size: 9px; letter-spacing: 0.22em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 6px;
}
.po-title { font-family: var(--font-display); font-size: 20px; font-weight: 300; }
.po-loc { font-size: 11px; color: var(--text-mid); margin-top: 4px; }

/* ===== PROCESS ===== */
#process { background: var(--navy); }
.process-steps {
  display: grid; grid-template-columns: repeat(4, 1fr);
  gap: 0; margin-top: 72px; position: relative;
}
.process-steps::before {
  content: ''; position: absolute;
  top: 36px; left: calc(12.5%); right: calc(12.5%);
  height: 1px; background: linear-gradient(90deg, var(--gold) 0%, rgba(201,162,75,0.2) 100%);
  z-index: 0;
}
.process-step {
  padding: 0 24px; text-align: center; position: relative; z-index: 1;
}
.step-num {
  width: 72px; height: 72px; border: 1px solid var(--gold);
  border-radius: 50%; display: flex; align-items: center; justify-content: center;
  font-family: var(--font-display); font-size: 28px; color: var(--gold);
  font-weight: 300; margin: 0 auto 28px;
  background: var(--navy); transition: var(--transition);
}
.process-step:hover .step-num {
  background: var(--gold); color: var(--navy);
}
.step-title { font-family: var(--font-display); font-size: 20px; margin-bottom: 12px; font-weight: 400; }
.step-desc { font-size: 12px; color: var(--text-mid); line-height: 1.8; }

/* ===== TESTIMONIALS ===== */
#testimonials { background: var(--navy-mid); overflow: hidden; }
.testi-track-wrapper { overflow: hidden; margin-top: 64px; }
.testi-track {
  display: flex; gap: 24px;
  animation: slideTesti 25s linear infinite;
}
.testi-track:hover { animation-play-state: paused; }
@keyframes slideTesti { from{transform:translateX(0)} to{transform:translateX(-50%)} }
.testi-card {
  flex-shrink: 0; width: 380px;
  border: 1px solid rgba(201,162,75,0.15);
  padding: 40px; position: relative;
  background: rgba(201,162,75,0.02);
  transition: var(--transition);
}
.testi-card:hover { border-color: rgba(201,162,75,0.35); }
.testi-quote {
  font-family: var(--font-display); font-size: 80px;
  color: var(--gold); opacity: 0.12; line-height: 0.8;
  position: absolute; top: 20px; left: 28px;
}
.testi-text {
  font-family: var(--font-display); font-size: 16px; font-style: italic;
  line-height: 1.75; color: var(--cream-dark); margin-bottom: 28px;
  position: relative; z-index: 1;
}
.testi-author { display: flex; align-items: center; gap: 14px; }
.testi-avatar {
  width: 44px; height: 44px; border-radius: 50%;
  background: linear-gradient(135deg, var(--gold-dark), var(--gold));
  display: flex; align-items: center; justify-content: center;
  font-family: var(--font-display); font-size: 18px; color: var(--navy); font-weight: 600;
}
.testi-name { font-weight: 600; font-size: 13px; }
.testi-loc { font-size: 11px; color: var(--text-mid); }
.testi-stars { color: var(--gold); font-size: 11px; letter-spacing: 2px; margin-top: 2px; }

/* ===== WHY US ===== */
#why { background: var(--navy); }
.why-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 80px; margin-top: 72px; align-items: center;
}
.why-list { display: flex; flex-direction: column; gap: 0; }
.why-item {
  display: flex; gap: 24px; padding: 28px 0;
  border-bottom: 1px solid rgba(201,162,75,0.08);
  transition: var(--transition); cursor: default;
}
.why-item:hover { padding-left: 12px; }
.why-item-icon {
  flex-shrink: 0; width: 52px; height: 52px;
  border: 1px solid rgba(201,162,75,0.25);
  display: flex; align-items: center; justify-content: center;
  font-size: 20px; color: var(--gold); transition: var(--transition);
}
.why-item:hover .why-item-icon {
  background: var(--gold); color: var(--navy);
}
.why-item-text {}
.why-item-title { font-size: 15px; font-weight: 600; margin-bottom: 6px; }
.why-item-desc { font-size: 12px; color: var(--text-mid); line-height: 1.8; }

.why-visual {
  position: relative;
}
.why-big-stat {
  display: flex; flex-direction: column; align-items: center;
  text-align: center; padding: 60px;
  border: 1px solid rgba(201,162,75,0.15);
  background: linear-gradient(135deg, rgba(201,162,75,0.04), transparent);
}
.why-big-num {
  font-family: var(--font-display); font-size: 100px;
  font-weight: 300; color: var(--gold); line-height: 1;
}
.why-big-label { font-size: 11px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--text-mid); margin-top: 8px; }
.why-mini-stats {
  display: grid; grid-template-columns: 1fr 1fr; gap: 1px;
  background: rgba(201,162,75,0.1); margin-top: 16px;
}
.mini-stat {
  background: var(--navy); padding: 24px;
  text-align: center;
}
.mini-num {
  font-family: var(--font-display); font-size: 36px;
  color: var(--gold); font-weight: 300; line-height: 1;
}
.mini-label { font-size: 10px; color: var(--text-mid); letter-spacing: 0.15em; text-transform: uppercase; margin-top: 4px; }

/* ===== CTA BAND ===== */
.cta-band {
  padding: 100px 5%;
  background: 
    linear-gradient(135deg, rgba(201,162,75,0.12) 0%, rgba(201,162,75,0.03) 100%),
    var(--navy-light);
  border-top: 1px solid rgba(201,162,75,0.2);
  border-bottom: 1px solid rgba(201,162,75,0.2);
  text-align: center; position: relative; overflow: hidden;
}
.cta-band::before {
  content: ''; position: absolute;
  top: -100px; left: 50%; transform: translateX(-50%);
  width: 600px; height: 600px; border-radius: 50%;
  background: radial-gradient(circle, rgba(201,162,75,0.08) 0%, transparent 70%);
  pointer-events: none;
}
.cta-band .section-title { max-width: 700px; margin: 0 auto 16px; }
.cta-sub { font-size: 14px; color: var(--text-light); margin-bottom: 48px; font-weight: 300; }
.cta-actions { display: flex; gap: 20px; justify-content: center; flex-wrap: wrap; }

/* ===== CONTACT ===== */
#contact { background: var(--navy-mid); }
.contact-grid {
  display: grid; grid-template-columns: 1fr 1.2fr;
  gap: 80px; margin-top: 72px;
}
.contact-info {}
.contact-info .section-intro { margin-bottom: 48px; }
.contact-items { display: flex; flex-direction: column; gap: 32px; }
.contact-item { display: flex; gap: 20px; align-items: flex-start; }
.contact-item-icon {
  width: 48px; height: 48px; border: 1px solid rgba(201,162,75,0.25);
  display: flex; align-items: center; justify-content: center;
  font-size: 18px; color: var(--gold); flex-shrink: 0;
}
.contact-item-label { font-size: 9px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--gold); margin-bottom: 6px; }
.contact-item-val { font-size: 14px; color: var(--white); font-weight: 400; }
.contact-item-val a { color: var(--white); text-decoration: none; transition: color 0.3s; }
.contact-item-val a:hover { color: var(--gold); }

.contact-zones { display: flex; gap: 16px; margin-top: 48px; flex-wrap: wrap; }
.zone-pill {
  padding: 10px 20px; border: 1px solid rgba(201,162,75,0.25);
  font-size: 11px; letter-spacing: 0.1em; color: var(--text-light);
  display: flex; align-items: center; gap: 8px;
}

.contact-form {}
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
.form-group { display: flex; flex-direction: column; gap: 8px; margin-bottom: 16px; }
.form-group label { font-size: 9px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--gold); }
.form-group input,
.form-group select,
.form-group textarea {
  background: rgba(201,162,75,0.03); border: 1px solid rgba(201,162,75,0.15);
  color: var(--white); font-family: var(--font-body); font-size: 13px;
  padding: 14px 18px; outline: none; transition: border-color 0.3s;
  width: 100%;
}
.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus { border-color: var(--gold); }
.form-group input::placeholder,
.form-group textarea::placeholder { color: var(--text-mid); font-size: 12px; }
.form-group select option { background: var(--navy-mid); }
.form-group textarea { resize: vertical; min-height: 130px; }
.form-submit {
  width: 100%; padding: 18px;
  background: var(--gold); color: var(--navy);
  border: none; font-family: var(--font-body); font-size: 11px;
  letter-spacing: 0.22em; text-transform: uppercase; font-weight: 600;
  cursor: pointer; transition: var(--transition);
}
.form-submit:hover { background: var(--gold-light); }
.form-note { font-size: 11px; color: var(--text-mid); margin-top: 12px; }
.form-success {
  display: none; padding: 24px; border: 1px solid var(--gold);
  background: rgba(201,162,75,0.06); text-align: center; margin-top: 16px;
}
.form-success.show { display: block; }
.form-success p { color: var(--gold); font-size: 14px; }

/* ===== FOOTER ===== */
footer {
  background: #08101d; padding: 80px 5% 32px;
  border-top: 1px solid rgba(201,162,75,0.1);
}
.footer-grid {
  display: grid; grid-template-columns: 2fr 1fr 1fr 1.5fr;
  gap: 60px; margin-bottom: 60px;
}
.footer-brand {}
.footer-logo { margin-bottom: 20px; }
.footer-desc { font-size: 12px; color: var(--text-mid); line-height: 1.85; max-width: 280px; margin-bottom: 28px; }
.footer-socials { display: flex; gap: 12px; }
.social-icon {
  width: 38px; height: 38px; border: 1px solid rgba(255,255,255,0.1);
  display: flex; align-items: center; justify-content: center;
  font-size: 14px; color: var(--text-mid); text-decoration: none;
  transition: var(--transition);
}
.social-icon:hover { border-color: var(--gold); color: var(--gold); }
.footer-col-title {
  font-size: 9px; letter-spacing: 0.25em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 24px; font-weight: 500;
}
.footer-links { list-style: none; display: flex; flex-direction: column; gap: 12px; }
.footer-links a {
  font-size: 12px; color: var(--text-mid); text-decoration: none; transition: color 0.3s;
}
.footer-links a:hover { color: var(--gold); }
.footer-contact-item { font-size: 12px; color: var(--text-mid); margin-bottom: 12px; display: flex; gap: 10px; }
.footer-contact-item i { color: var(--gold); flex-shrink: 0; margin-top: 2px; }
.footer-contact-item a { color: var(--text-mid); text-decoration: none; transition: color 0.3s; }
.footer-contact-item a:hover { color: var(--gold); }

.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.05);
  padding-top: 32px; display: flex;
  align-items: center; justify-content: space-between;
  flex-wrap: wrap; gap: 16px;
}
.footer-copy { font-size: 11px; color: var(--text-mid); }
.footer-legal { display: flex; gap: 24px; }
.footer-legal a { font-size: 11px; color: var(--text-mid); text-decoration: none; transition: color 0.3s; }
.footer-legal a:hover { color: var(--gold); }

/* ===== WHATSAPP FLOAT ===== */
.whatsapp-float {
  position: fixed; bottom: 32px; right: 32px; z-index: 800;
  display: flex; align-items: center; gap: 12px;
}
.whatsapp-label {
  background: var(--white); color: #128C7E;
  padding: 10px 16px; border-radius: 4px;
  font-size: 12px; font-weight: 600; white-space: nowrap;
  box-shadow: 0 4px 24px rgba(0,0,0,0.2);
  opacity: 0; transform: translateX(10px);
  transition: var(--transition); pointer-events: none;
}
.whatsapp-float:hover .whatsapp-label { opacity: 1; transform: translateX(0); }
.whatsapp-btn {
  width: 60px; height: 60px; border-radius: 50%;
  background: #25D366; display: flex; align-items: center; justify-content: center;
  font-size: 26px; color: white; text-decoration: none;
  box-shadow: 0 4px 24px rgba(37,211,102,0.4);
  transition: var(--transition); animation: waPulse 2.5s ease-in-out infinite;
}
.whatsapp-btn:hover { transform: scale(1.1); }
@keyframes waPulse {
  0%,100%{box-shadow:0 4px 24px rgba(37,211,102,0.4)}
  50%{box-shadow:0 4px 40px rgba(37,211,102,0.7)}
}

/* ===== SCROLL TO TOP ===== */
.scroll-top {
  position: fixed; bottom: 100px; right: 32px; z-index: 800;
  width: 44px; height: 44px; border: 1px solid rgba(201,162,75,0.4);
  background: rgba(14,22,40,0.9); color: var(--gold);
  display: flex; align-items: center; justify-content: center;
  font-size: 16px; cursor: pointer; text-decoration: none;
  opacity: 0; transform: translateY(20px);
  transition: var(--transition); pointer-events: none;
}
.scroll-top.show { opacity: 1; transform: translateY(0); pointer-events: auto; }
.scroll-top:hover { background: var(--gold); color: var(--navy); }

/* ===== RESPONSIVE ===== */
@media (max-width: 1100px) {
  .services-grid { grid-template-columns: repeat(2, 1fr); }
  .footer-grid { grid-template-columns: 1fr 1fr; gap: 40px; }
  .process-steps { grid-template-columns: repeat(2, 1fr); gap: 48px; }
  .process-steps::before { display: none; }
}
@media (max-width: 900px) {
  .about-grid, .why-grid, .contact-grid { grid-template-columns: 1fr; gap: 48px; }
  .about-visual { aspect-ratio: 16/9; }
  .hero-stats { display: none; }
  nav .nav-links, nav .nav-cta { display: none; }
  .hamburger { display: flex; }
  .portfolio-grid { grid-template-columns: 1fr 1fr; }
  .portfolio-item:nth-child(1),
  .portfolio-item:nth-child(4) { grid-column: span 1; }
}
@media (max-width: 640px) {
  section { padding: 80px 5%; }
  .services-grid { grid-template-columns: 1fr; }
  .portfolio-grid { grid-template-columns: 1fr; }
  .portfolio-item { aspect-ratio: 4/3 !important; }
  .form-row { grid-template-columns: 1fr; }
  .process-steps { grid-template-columns: 1fr; }
  .hero-actions { flex-direction: column; }
  .services-header { flex-direction: column; align-items: flex-start; }
  .about-values { grid-template-columns: 1fr; }
  .about-badge { width: 100px; height: 100px; bottom: -10px; right: -10px; }
  .about-badge-num { font-size: 28px; }
  .footer-grid { grid-template-columns: 1fr; gap: 36px; }
  body { cursor: auto; }
  .cursor, .cursor-ring { display: none; }
}
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- NAVBAR -->
<nav id="navbar">
  <a href="#" class="nav-logo">
    <div class="logo-icon">B</div>
    <div class="logo-text">
      <span class="logo-name">Babytch Design</span>
      <span class="logo-tagline">Groupe • Abidjan & Cameroun</span>
    </div>
  </a>
  <ul class="nav-links">
    <li><a href="#about">À propos</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Réalisations</a></li>
    <li><a href="#process">Processus</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#contact" class="nav-cta"><span>Devis gratuit</span></a>
  <div class="hamburger" id="hamburger" onclick="toggleMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- MOBILE MENU -->
<div class="mobile-menu" id="mobileMenu">
  <a href="#about" onclick="toggleMenu()">À propos</a>
  <a href="#services" onclick="toggleMenu()">Services</a>
  <a href="#portfolio" onclick="toggleMenu()">Réalisations</a>
  <a href="#process" onclick="toggleMenu()">Processus</a>
  <a href="#contact" onclick="toggleMenu()">Contact</a>
  <a href="tel:+2250705626922" onclick="toggleMenu()" style="color:var(--gold)">+225 07 05 62 69 22</a>
</div>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid-lines"></div>
  <div class="hero-orb"></div>
  <div class="hero-content">
    <div class="hero-badge">Abidjan · Cameroun · Depuis 2015</div>
    <h1 class="hero-title">
      <em>Transformez</em><br>
      <strong>vos espaces.</strong><br>
      Révélez votre<br><em>style.</em>
    </h1>
    <p class="hero-sub">
      Babytch Design Groupe — votre partenaire d'excellence en aménagement intérieur, rénovation, sécurité et confort thermique. Du concept à la livraison, nous réalisons vos projets avec précision et passion.
    </p>
    <div class="hero-actions">
      <a href="#contact" class="btn-primary">
        <span>Demander un devis</span>
        <i class="fas fa-arrow-right"></i>
      </a>
      <a href="#portfolio" class="btn-outline">
        <i class="fas fa-images"></i>
        <span>Voir nos réalisations</span>
      </a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat-item">
      <div class="stat-num counter" data-target="200">0</div>
      <div class="stat-label">Projets réalisés</div>
    </div>
    <div class="stat-item">
      <div class="stat-num counter" data-target="10">0</div>
      <div class="stat-label">Années d'expertise</div>
    </div>
    <div class="stat-item">
      <div class="stat-num counter" data-target="2">0</div>
      <div class="stat-label">Pays d'opération</div>
    </div>
  </div>
  <div class="hero-scroll">
    <span>Défiler</span>
    <div class="scroll-line"></div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-band">
  <div class="marquee-track" id="marqueeTrack">
    <div class="marquee-item"><span class="marquee-dot"></span>Aménagement Intérieur</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Carrelage & Sol</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Peinture Décorative</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Faux-Plafonds Placoplatre</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Caméras de Sécurité</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Climatisation</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Abidjan · Côte d'Ivoire</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Cameroun</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Devis Gratuit</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Aménagement Intérieur</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Carrelage & Sol</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Peinture Décorative</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Faux-Plafonds Placoplatre</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Caméras de Sécurité</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Climatisation</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Abidjan · Côte d'Ivoire</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Cameroun</div>
    <div class="marquee-item"><span class="marquee-dot"></span>Devis Gratuit</div>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-visual reveal">
      <div class="about-img-placeholder">
        <div class="about-corner tl"></div>
        <div class="about-corner br"></div>
        <i class="fas fa-drafting-compass about-img-icon"></i>
        <span class="about-img-text">Notre savoir-faire</span>
      </div>
      <div class="about-badge">
        <div class="about-badge-num">10+</div>
        <div class="about-badge-text">Ans<br>d'expertise</div>
      </div>
    </div>
    <div class="about-content reveal" style="transition-delay:0.2s">
      <div class="section-label">Notre histoire</div>
      <h2 class="section-title">L'excellence au<br>service de <em>votre</em> cadre de vie</h2>
      <p class="section-intro">
        Fondée sur la passion du beau et l'exigence du travail bien fait, Babytch Design Groupe est une entreprise de référence dans l'aménagement intérieur et la rénovation en Côte d'Ivoire et au Cameroun. Nous accompagnons particuliers, professionnels et promoteurs dans la réalisation de leurs projets, de A à Z.
      </p>
      <p class="section-intro" style="margin-top:16px;">
        Notre équipe pluridisciplinaire maîtrise l'ensemble des corps de métier du second œuvre. Une seule entreprise, un seul interlocuteur, une qualité d'exécution irréprochable.
      </p>
      <div class="about-values">
        <div class="value-card">
          <div class="value-icon"><i class="fas fa-medal"></i></div>
          <div class="value-title">Excellence</div>
          <div class="value-desc">Des finitions impeccables à chaque projet, sans compromis sur la qualité.</div>
        </div>
        <div class="value-card">
          <div class="value-icon"><i class="fas fa-handshake"></i></div>
          <div class="value-title">Confiance</div>
          <div class="value-desc">Transparence des prix, respect des délais, communication permanente.</div>
        </div>
        <div class="value-card">
          <div class="value-icon"><i class="fas fa-lightbulb"></i></div>
          <div class="value-title">Innovation</div>
          <div class="value-desc">Intégration des dernières tendances et technologies pour vos espaces.</div>
        </div>
        <div class="value-card">
          <div class="value-icon"><i class="fas fa-users"></i></div>
          <div class="value-title">Proximité</div>
          <div class="value-desc">Des équipes dédiées à Abidjan et au Cameroun, à votre service.</div>
        </div>
      </div>
      <div class="about-flags">
        <div class="flag-tag"><span class="flag-emoji">🇨🇮</span> Abidjan, Côte d'Ivoire</div>
        <div class="flag-tag"><span class="flag-emoji">🇨🇲</span> Cameroun</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="services-header">
    <div>
      <div class="section-label reveal">Nos expertises</div>
      <h2 class="section-title reveal">Six métiers,<br>une <em>vision</em></h2>
    </div>
    <p class="section-intro reveal" style="transition-delay:0.2s">
      Du design d'espace jusqu'à la sécurité de votre bien, Babytch Design Groupe maîtrise l'ensemble des corps de métier du second œuvre.
    </p>
  </div>
  <div class="services-grid reveal" style="transition-delay:0.3s">

    <div class="service-card">
      <div class="service-num">01</div>
      <i class="fas fa-couch service-icon"></i>
      <div class="service-name">Aménagement Intérieur & Décoration</div>
      <p class="service-desc">Conception et réalisation d'espaces intérieurs sur mesure, résidentiels et commerciaux. De la visualisation 3D à la livraison clés en main.</p>
      <ul class="service-items">
        <li>Design d'espace & architecture intérieure</li>
        <li>Agencement salon, chambre, cuisine, bureau</li>
        <li>Mobilier, matériaux & accessoires décoratifs</li>
        <li>Rendu 3D avant réalisation</li>
      </ul>
    </div>

    <div class="service-card">
      <div class="service-num">02</div>
      <i class="fas fa-border-all service-icon"></i>
      <div class="service-name">Carrelage & Revêtements de Sol</div>
      <p class="service-desc">Pose experte de carrelage sur toutes surfaces. Découpe de précision, joints professionnels, finitions soignées.</p>
      <ul class="service-items">
        <li>Carrelage sol, mur, façade, terrasse</li>
        <li>Salle de bain & cuisine</li>
        <li>Découpe & ajustement sur mesure</li>
        <li>Joints et finitions irréprochables</li>
      </ul>
    </div>

    <div class="service-card">
      <div class="service-num">03</div>
      <i class="fas fa-paint-roller service-icon"></i>
      <div class="service-name">Peinture & Finitions</div>
      <p class="service-desc">Peinture intérieure et extérieure de qualité. Enduits décoratifs, stucs, textures tendance, ravalement de façades.</p>
      <ul class="service-items">
        <li>Peinture intérieure & extérieure</li>
        <li>Enduits décoratifs & stucs</li>
        <li>Ravalement de façades</li>
        <li>Peinture époxy & béton ciré</li>
      </ul>
    </div>

    <div class="service-card">
      <div class="service-num">04</div>
      <i class="fas fa-layer-group service-icon"></i>
      <div class="service-name">Placoplatre & Faux-Plafonds</div>
      <p class="service-desc">Installation de cloisons, faux-plafonds et caissons lumineux en placoplatre. Vente de matériaux et accessoires.</p>
      <ul class="service-items">
        <li>Cloisons & faux-plafonds placoplatre</li>
        <li>Caissons lumineux & niches déco</li>
        <li>Isolation thermique & phonique</li>
        <li>Vente de placoplatre & accessoires</li>
      </ul>
    </div>

    <div class="service-card">
      <div class="service-num">05</div>
      <i class="fas fa-video service-icon"></i>
      <div class="service-name">Caméras de Sécurité & Surveillance</div>
      <p class="service-desc">Installation de systèmes de vidéosurveillance professionnels. Audit, installation, maintenance et accès à distance.</p>
      <ul class="service-items">
        <li>Audit sécuritaire & plan d'installation</li>
        <li>Caméras IP, dôme, bullet & PTZ</li>
        <li>Systèmes NVR/DVR & cloud</li>
        <li>Accès smartphone & maintenance</li>
      </ul>
    </div>

    <div class="service-card">
      <div class="service-num">06</div>
      <i class="fas fa-wind service-icon"></i>
      <div class="service-name">Climatisation & Confort Thermique</div>
      <p class="service-desc">Installation et maintenance de climatiseurs adaptés au climat local. Particuliers et professionnels.</p>
      <ul class="service-items">
        <li>Split, multi-split & cassette</li>
        <li>Climatisation réversible chaud/froid</li>
        <li>Maintenance & recharge frigorigène</li>
        <li>Conseil marques & modèles</li>
      </ul>
    </div>

  </div>
</section>

<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="section-label reveal">Nos réalisations</div>
  <h2 class="section-title reveal">Chaque espace,<br>une <em>signature</em></h2>
  <div class="portfolio-filters reveal" style="transition-delay:0.2s">
    <button class="filter-btn active" onclick="filterPortfolio(this,'all')">Tout voir</button>
    <button class="filter-btn" onclick="filterPortfolio(this,'decoration')">Décoration</button>
    <button class="filter-btn" onclick="filterPortfolio(this,'carrelage')">Carrelage</button>
    <button class="filter-btn" onclick="filterPortfolio(this,'peinture')">Peinture</button>
    <button class="filter-btn" onclick="filterPortfolio(this,'placo')">Faux-plafond</button>
    <button class="filter-btn" onclick="filterPortfolio(this,'securite')">Sécurité</button>
    <button class="filter-btn" onclick="filterPortfolio(this,'clim')">Climatisation</button>
  </div>
  <div class="portfolio-grid reveal" style="transition-delay:0.3s">
    <div class="portfolio-item" data-cat="decoration">
      <div class="portfolio-placeholder">
        <i class="fas fa-couch portfolio-icon"></i>
        <span class="portfolio-label">Ajouter une photo</span>
      </div>
      <div class="portfolio-overlay">
        <div class="po-tag">Décoration</div>
        <div class="po-title">Salon moderne Cocody</div>
        <div class="po-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Côte d'Ivoire</div>
      </div>
    </div>
    <div class="portfolio-item" data-cat="carrelage">
      <div class="portfolio-placeholder">
        <i class="fas fa-border-all portfolio-icon"></i>
        <span class="portfolio-label">Ajouter une photo</span>
      </div>
      <div class="portfolio-overlay">
        <div class="po-tag">Carrelage</div>
        <div class="po-title">Salle de bain luxe</div>
        <div class="po-loc"><i class="fas fa-map-marker-alt"></i> Douala, Cameroun</div>
      </div>
    </div>
    <div class="portfolio-item" data-cat="placo">
      <div class="portfolio-placeholder">
        <i class="fas fa-layer-group portfolio-icon"></i>
        <span class="portfolio-label">Ajouter une photo</span>
      </div>
      <div class="portfolio-overlay">
        <div class="po-tag">Faux-plafond</div>
        <div class="po-title">Caissons lumineux villa</div>
        <div class="po-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Côte d'Ivoire</div>
      </div>
    </div>
    <div class="portfolio-item" data-cat="peinture">
      <div class="portfolio-placeholder">
        <i class="fas fa-paint-roller portfolio-icon"></i>
        <span class="portfolio-label">Ajouter une photo</span>
      </div>
      <div class="portfolio-overlay">
        <div class="po-tag">Peinture</div>
        <div class="po-title">Rénovation appartement</div>
        <div class="po-loc"><i class="fas fa-map-marker-alt"></i> Yaoundé, Cameroun</div>
      </div>
    </div>
    <div class="portfolio-item" data-cat="securite">
      <div class="portfolio-placeholder">
        <i class="fas fa-video portfolio-icon"></i>
        <span class="portfolio-label">Ajouter une photo</span>
      </div>
      <div class="portfolio-overlay">
        <div class="po-tag">Sécurité</div>
        <div class="po-title">Surveillance résidence</div>
        <div class="po-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Côte d'Ivoire</div>
      </div>
    </div>
    <div class="portfolio-item" data-cat="clim">
      <div class="portfolio-placeholder">
        <i class="fas fa-wind portfolio-icon"></i>
        <span class="portfolio-label">Ajouter une photo</span>
      </div>
      <div class="portfolio-overlay">
        <div class="po-tag">Climatisation</div>
        <div class="po-title">Bureau climatisé Akwa</div>
        <div class="po-loc"><i class="fas fa-map-marker-alt"></i> Douala, Cameroun</div>
      </div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section id="process">
  <div style="text-align:center; margin-bottom: 0;">
    <div class="section-label reveal" style="justify-content:center">Comment nous travaillons</div>
    <h2 class="section-title reveal" style="text-align:center">Un processus <em>simple</em><br>et transparent</h2>
  </div>
  <div class="process-steps">
    <div class="process-step reveal" style="transition-delay:0.1s">
      <div class="step-num">1</div>
      <div class="step-title">Consultation</div>
      <p class="step-desc">Premier contact gratuit. Nous écoutons votre projet, vos besoins et vos attentes avec attention.</p>
    </div>
    <div class="process-step reveal" style="transition-delay:0.2s">
      <div class="step-num">2</div>
      <div class="step-title">Devis détaillé</div>
      <p class="step-desc">Un devis précis, transparent et sans surprise vous est remis sous 24h. Chaque poste est détaillé.</p>
    </div>
    <div class="process-step reveal" style="transition-delay:0.3s">
      <div class="step-num">3</div>
      <div class="step-title">Réalisation</div>
      <p class="step-desc">Notre équipe intervient avec précision, dans les délais convenus. Vous êtes informé à chaque étape.</p>
    </div>
    <div class="process-step reveal" style="transition-delay:0.4s">
      <div class="step-num">4</div>
      <div class="step-title">Livraison</div>
      <p class="step-desc">Réception et validation avec vous. Votre satisfaction est notre seul critère de réussite.</p>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="section-label reveal">Ils nous font confiance</div>
  <h2 class="section-title reveal">La satisfaction,<br>notre <em>meilleure</em> référence</h2>
  <div class="testi-track-wrapper reveal" style="transition-delay:0.2s">
    <div class="testi-track" id="testiTrack">
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Babytch Design a transformé mon appartement en quelque chose d'extraordinaire. Le travail de carrelage et la peinture sont parfaits. Je recommande vivement à tous !</p>
        <div class="testi-author">
          <div class="testi-avatar">K</div>
          <div>
            <div class="testi-name">Koné Mariam</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Cocody</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">L'installation des caméras de sécurité et la climatisation de nos bureaux ont été réalisées avec un professionnalisme exemplaire. Équipe sérieuse et ponctuelle.</p>
        <div class="testi-author">
          <div class="testi-avatar">N</div>
          <div>
            <div class="testi-name">Njomo Patrick</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Douala, Cameroun</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Le faux-plafond placoplatre de ma villa est une merveille ! Les finitions sont impeccables et l'équipe a respecté le délai prévu. Prix très compétitif pour une qualité premium.</p>
        <div class="testi-author">
          <div class="testi-avatar">D</div>
          <div>
            <div class="testi-name">Diabaté Ibrahim</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Marcory</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Très satisfaite de la rénovation complète de ma boutique à Yaoundé. L'aménagement intérieur a boosté l'attrait de mon commerce. Merci Babytch Design Groupe !</p>
        <div class="testi-author">
          <div class="testi-avatar">A</div>
          <div>
            <div class="testi-name">Abena Sophie</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Yaoundé, Cameroun</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Devis rapide, intervention soignée, résultat bluffant. Mon nouveau sol en carrelage et ma peinture fraîche ont complètement changé l'atmosphère de la maison.</p>
        <div class="testi-author">
          <div class="testi-avatar">T</div>
          <div>
            <div class="testi-name">Touré Aminata</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Plateau</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <!-- Duplicates for infinite scroll -->
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Babytch Design a transformé mon appartement en quelque chose d'extraordinaire. Le travail de carrelage et la peinture sont parfaits. Je recommande vivement à tous !</p>
        <div class="testi-author">
          <div class="testi-avatar">K</div>
          <div>
            <div class="testi-name">Koné Mariam</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Cocody</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">L'installation des caméras de sécurité et la climatisation de nos bureaux ont été réalisées avec un professionnalisme exemplaire. Équipe sérieuse et ponctuelle.</p>
        <div class="testi-author">
          <div class="testi-avatar">N</div>
          <div>
            <div class="testi-name">Njomo Patrick</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Douala, Cameroun</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Le faux-plafond placoplatre de ma villa est une merveille ! Les finitions sont impeccables et l'équipe a respecté le délai prévu. Prix très compétitif pour une qualité premium.</p>
        <div class="testi-author">
          <div class="testi-avatar">D</div>
          <div>
            <div class="testi-name">Diabaté Ibrahim</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Marcory</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Très satisfaite de la rénovation complète de ma boutique à Yaoundé. L'aménagement intérieur a boosté l'attrait de mon commerce. Merci Babytch Design Groupe !</p>
        <div class="testi-author">
          <div class="testi-avatar">A</div>
          <div>
            <div class="testi-name">Abena Sophie</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Yaoundé, Cameroun</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Devis rapide, intervention soignée, résultat bluffant. Mon nouveau sol en carrelage et ma peinture fraîche ont complètement changé l'atmosphère de la maison.</p>
        <div class="testi-author">
          <div class="testi-avatar">T</div>
          <div>
            <div class="testi-name">Touré Aminata</div>
            <div class="testi-loc"><i class="fas fa-map-marker-alt"></i> Abidjan, Plateau</div>
            <div class="testi-stars">★★★★★</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- WHY US -->
<section id="why">
  <div class="why-grid">
    <div>
      <div class="section-label reveal">Pourquoi nous</div>
      <h2 class="section-title reveal">Ce qui nous rend<br><em>différents</em></h2>
      <div class="why-list">
        <div class="why-item reveal" style="transition-delay:0.1s">
          <div class="why-item-icon"><i class="fas fa-certificate"></i></div>
          <div class="why-item-text">
            <div class="why-item-title">Expertise multi-corps de métier</div>
            <div class="why-item-desc">Carrelage, peinture, faux-plafond, sécurité, climatisation : un seul prestataire pour tous vos besoins.</div>
          </div>
        </div>
        <div class="why-item reveal" style="transition-delay:0.2s">
          <div class="why-item-icon"><i class="fas fa-clock"></i></div>
          <div class="why-item-text">
            <div class="why-item-title">Devis sous 24 heures</div>
            <div class="why-item-desc">Nous vous remettons un devis détaillé, transparent et sans engagement sous 24 heures.</div>
          </div>
        </div>
        <div class="why-item reveal" style="transition-delay:0.3s">
          <div class="why-item-icon"><i class="fas fa-globe-africa"></i></div>
          <div class="why-item-text">
            <div class="why-item-title">Présence binationale</div>
            <div class="why-item-desc">Des équipes dédiées et opérationnelles à Abidjan et dans toutes les grandes villes du Cameroun.</div>
          </div>
        </div>
        <div class="why-item reveal" style="transition-delay:0.4s">
          <div class="why-item-icon"><i class="fas fa-shield-alt"></i></div>
          <div class="why-item-text">
            <div class="why-item-title">Garantie qualité</div>
            <div class="why-item-desc">Chaque réalisation est garantie. Nous intervenons rapidement en cas de problème après livraison.</div>
          </div>
        </div>
      </div>
    </div>
    <div class="why-visual reveal" style="transition-delay:0.2s">
      <div class="why-big-stat">
        <div class="why-big-num counter" data-target="200">0</div>
        <div class="why-big-label">Projets réalisés avec succès</div>
      </div>
      <div class="why-mini-stats">
        <div class="mini-stat">
          <div class="mini-num counter" data-target="98">0</div>
          <div class="mini-label">% de clients satisfaits</div>
        </div>
        <div class="mini-stat">
          <div class="mini-num counter" data-target="10">0</div>
          <div class="mini-label">Années d'expertise</div>
        </div>
        <div class="mini-stat">
          <div class="mini-num counter" data-target="6">0</div>
          <div class="mini-label">Corps de métier</div>
        </div>
        <div class="mini-stat">
          <div class="mini-num counter" data-target="2">0</div>
          <div class="mini-label">Pays d'opération</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CTA BAND -->
<div class="cta-band reveal">
  <div class="section-label" style="justify-content:center; margin-bottom:24px;">Passez à l'action</div>
  <h2 class="section-title">Votre projet mérite<br>le meilleur. <em>Commençons.</em></h2>
  <p class="cta-sub">Devis gratuit, réponse sous 24h. Nous intervenons à Abidjan et au Cameroun.</p>
  <div class="cta-actions">
    <a href="#contact" class="btn-primary"><span>Demander un devis gratuit</span><i class="fas fa-arrow-right"></i></a>
    <a href="tel:+2250705626922" class="btn-outline"><i class="fas fa-phone"></i><span>+225 07 05 62 69 22</span></a>
  </div>
</div>

<!-- CONTACT -->
<section id="contact">
  <div class="section-label reveal">Nous contacter</div>
  <h2 class="section-title reveal">Parlons de votre <em>projet</em></h2>
  <div class="contact-grid">
    <div class="contact-info reveal">
      <p class="section-intro">Que vous soyez à Abidjan ou au Cameroun, notre équipe est disponible pour vous conseiller et réaliser votre projet dans les meilleures conditions.</p>
      <div class="contact-items" style="margin-top:40px;">
        <div class="contact-item">
          <div class="contact-item-icon"><i class="fas fa-phone"></i></div>
          <div>
            <div class="contact-item-label">Téléphone</div>
            <div class="contact-item-val"><a href="tel:+2250705626922">+225 07 05 62 69 22</a></div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-item-icon"><i class="fas fa-envelope"></i></div>
          <div>
            <div class="contact-item-label">Email</div>
            <div class="contact-item-val"><a href="mailto:babytchdesigngroupe237@gmail.com">babytchdesigngroupe237@gmail.com</a></div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-item-icon"><i class="fab fa-whatsapp"></i></div>
          <div>
            <div class="contact-item-label">WhatsApp</div>
            <div class="contact-item-val"><a href="https://wa.me/2250705626922" target="_blank">+225 07 05 62 69 22</a></div>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-item-icon"><i class="fas fa-globe"></i></div>
          <div>
            <div class="contact-item-label">Site de référence</div>
            <div class="contact-item-val"><a href="https://sites.google.com/view/babytchdesigngroupe/index" target="_blank">Voir notre portfolio</a></div>
          </div>
        </div>
      </div>
      <div class="contact-zones">
        <div class="zone-pill"><span>🇨🇮</span> Abidjan, Côte d'Ivoire</div>
        <div class="zone-pill"><span>🇨🇲</span> Cameroun</div>
      </div>
    </div>
    <div class="contact-form reveal" style="transition-delay:0.2s">
      <div class="form-row">
        <div class="form-group">
          <label>Votre nom *</label>
          <input type="text" id="fname" placeholder="Prénom et nom" required/>
        </div>
        <div class="form-group">
          <label>Téléphone *</label>
          <input type="tel" id="fphone" placeholder="+225 ou +237..." required/>
        </div>
      </div>
      <div class="form-group">
        <label>Email</label>
        <input type="email" id="femail" placeholder="votre@email.com"/>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Ville *</label>
          <select id="fcity">
            <option value="">Sélectionner...</option>
            <option>Abidjan</option>
            <option>Douala</option>
            <option>Yaoundé</option>
            <option>Autre ville CI</option>
            <option>Autre ville Cameroun</option>
          </select>
        </div>
        <div class="form-group">
          <label>Service souhaité *</label>
          <select id="fservice">
            <option value="">Sélectionner...</option>
            <option>Aménagement intérieur</option>
            <option>Carrelage</option>
            <option>Peinture</option>
            <option>Faux-plafond / Placoplatre</option>
            <option>Caméras de sécurité</option>
            <option>Climatisation</option>
            <option>Plusieurs services</option>
          </select>
        </div>
      </div>
      <div class="form-group">
        <label>Description de votre projet *</label>
        <textarea id="fmessage" placeholder="Décrivez votre projet : surface, type de bien, budget estimatif, délais souhaités..."></textarea>
      </div>
      <button class="form-submit" onclick="submitForm()">
        <i class="fas fa-paper-plane"></i> &nbsp; Envoyer ma demande de devis
      </button>
      <p class="form-note"><i class="fas fa-lock"></i> Vos données sont confidentielles. Réponse garantie sous 24h.</p>
      <div class="form-success" id="formSuccess">
        <p><i class="fas fa-check-circle" style="color:var(--gold); font-size:24px; display:block; margin-bottom:10px;"></i>
        Merci pour votre message ! <br>Notre équipe vous contactera dans les 24 heures.</p>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <div class="footer-logo">
        <a href="#" class="nav-logo" style="text-decoration:none;">
          <div class="logo-icon">B</div>
          <div class="logo-text">
            <span class="logo-name">Babytch Design</span>
            <span class="logo-tagline">Groupe • Excellence & Confiance</span>
          </div>
        </a>
      </div>
      <p class="footer-desc">Votre partenaire de référence en aménagement intérieur, rénovation, sécurité et climatisation à Abidjan et au Cameroun. Excellence, confiance et innovation depuis 2015.</p>
      <div class="footer-socials">
        <a href="#" class="social-icon" title="Facebook"><i class="fab fa-facebook-f"></i></a>
        <a href="#" class="social-icon" title="Instagram"><i class="fab fa-instagram"></i></a>
        <a href="https://wa.me/2250705626922" class="social-icon" title="WhatsApp" target="_blank"><i class="fab fa-whatsapp"></i></a>
        <a href="mailto:babytchdesigngroupe237@gmail.com" class="social-icon" title="Email"><i class="fas fa-envelope"></i></a>
      </div>
    </div>
    <div>
      <div class="footer-col-title">Navigation</div>
      <ul class="footer-links">
        <li><a href="#about">À propos</a></li>
        <li><a href="#services">Nos services</a></li>
        <li><a href="#portfolio">Réalisations</a></li>
        <li><a href="#process">Notre processus</a></li>
        <li><a href="#testimonials">Témoignages</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Services</div>
      <ul class="footer-links">
        <li><a href="#services">Aménagement intérieur</a></li>
        <li><a href="#services">Carrelage</a></li>
        <li><a href="#services">Peinture</a></li>
        <li><a href="#services">Placoplatre</a></li>
        <li><a href="#services">Caméras sécurité</a></li>
        <li><a href="#services">Climatisation</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Contact</div>
      <div class="footer-contact-item"><i class="fas fa-phone"></i><a href="tel:+2250705626922">+225 07 05 62 69 22</a></div>
      <div class="footer-contact-item"><i class="fas fa-envelope"></i><a href="mailto:babytchdesigngroupe237@gmail.com">babytchdesigngroupe237<br>@gmail.com</a></div>
      <div class="footer-contact-item"><i class="fas fa-map-marker-alt"></i><span>Abidjan, Côte d'Ivoire</span></div>
      <div class="footer-contact-item"><i class="fas fa-map-marker-alt"></i><span>Cameroun</span></div>
      <div class="footer-contact-item"><i class="fas fa-clock"></i><span>Lun – Sam : 7h – 19h</span></div>
    </div>
  </div>
  <div class="footer-bottom">
    <div class="footer-copy">© 2025 Babytch Design Groupe. Tous droits réservés.</div>
    <div class="footer-legal">
      <a href="#">Mentions légales</a>
      <a href="#">Confidentialité</a>
    </div>
  </div>
</footer>

<!-- WHATSAPP FLOAT -->
<div class="whatsapp-float">
  <div class="whatsapp-label">Discutons sur WhatsApp !</div>
  <a href="https://wa.me/2250705626922?text=Bonjour%2C%20je%20souhaite%20un%20devis%20pour%20un%20projet%20d'am%C3%A9nagement." class="whatsapp-btn" target="_blank" title="WhatsApp">
    <i class="fab fa-whatsapp"></i>
  </a>
</div>

<!-- SCROLL TO TOP -->
<a href="#" class="scroll-top" id="scrollTop">
  <i class="fas fa-chevron-up"></i>
</a>

<script>
// CUSTOM CURSOR
const cursor = document.getElementById('cursor');
const ring = document.getElementById('cursorRing');
document.addEventListener('mousemove', e => {
  cursor.style.left = e.clientX + 'px';
  cursor.style.top = e.clientY + 'px';
  setTimeout(() => {
    ring.style.left = e.clientX + 'px';
    ring.style.top = e.clientY + 'px';
  }, 80);
});
document.querySelectorAll('a, button, .service-card, .portfolio-item, .filter-btn').forEach(el => {
  el.addEventListener('mouseenter', () => { cursor.classList.add('hovered'); ring.classList.add('hovered'); });
  el.addEventListener('mouseleave', () => { cursor.classList.remove('hovered'); ring.classList.remove('hovered'); });
});

// NAVBAR SCROLL
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => {
  navbar.classList.toggle('scrolled', window.scrollY > 60);
  document.getElementById('scrollTop').classList.toggle('show', window.scrollY > 400);
});

// MOBILE MENU
function toggleMenu() {
  document.getElementById('mobileMenu').classList.toggle('open');
}

// SCROLL REVEAL
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      e.target.classList.add('visible');
      revealObserver.unobserve(e.target);
    }
  });
}, { threshold: 0.1, rootMargin: '0px 0px -60px 0px' });

document.querySelectorAll('.reveal').forEach(el => revealObserver.observe(el));

// COUNTERS
function animateCounter(el) {
  const target = parseInt(el.dataset.target);
  const duration = 2000;
  const step = target / (duration / 16);
  let current = 0;
  const timer = setInterval(() => {
    current += step;
    if (current >= target) { current = target; clearInterval(timer); }
    el.textContent = Math.floor(current) + (el.dataset.target === '98' ? '%' : '+');
  }, 16);
}

const counterObserver = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      animateCounter(e.target);
      counterObserver.unobserve(e.target);
    }
  });
}, { threshold: 0.5 });

document.querySelectorAll('.counter').forEach(el => counterObserver.observe(el));

// PORTFOLIO FILTER
function filterPortfolio(btn, cat) {
  document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  document.querySelectorAll('.portfolio-item').forEach(item => {
    const show = cat === 'all' || item.dataset.cat === cat;
    item.style.opacity = show ? '1' : '0.2';
    item.style.transform = show ? 'scale(1)' : 'scale(0.97)';
    item.style.pointerEvents = show ? 'auto' : 'none';
    item.style.transition = 'opacity 0.4s, transform 0.4s';
  });
}

// FORM SUBMIT
function submitForm() {
  const name = document.getElementById('fname').value.trim();
  const phone = document.getElementById('fphone').value.trim();
  const city = document.getElementById('fcity').value;
  const service = document.getElementById('fservice').value;
  const message = document.getElementById('fmessage').value.trim();

  if (!name || !phone || !city || !service || !message) {
    alert('Veuillez remplir tous les champs obligatoires (*)');
    return;
  }

  const subject = encodeURIComponent(`Demande de devis – ${service} – ${city}`);
  const body = encodeURIComponent(
    `Nom: ${name}\nTéléphone: ${phone}\nEmail: ${document.getElementById('femail').value}\nVille: ${city}\nService: ${service}\n\nProjet:\n${message}`
  );
  window.location.href = `mailto:babytchdesigngroupe237@gmail.com?subject=${subject}&body=${body}`;
  document.getElementById('formSuccess').classList.add('show');
}

// SMOOTH ANCHOR NAVIGATION
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    const target = document.querySelector(a.getAttribute('href'));
    if (target) {
      e.preventDefault();
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
  });
});

// HERO PARALLAX (subtle)
window.addEventListener('scroll', () => {
  const hero = document.getElementById('hero');
  const orb = document.querySelector('.hero-orb');
  if (orb && window.scrollY < window.innerHeight) {
    orb.style.transform = `translateY(calc(-50% + ${window.scrollY * 0.3}px))`;
  }
});
</script>
</body>
</html>
