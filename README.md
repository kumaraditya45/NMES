<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>न्यू मॉडर्न इंग्लिश स्कूल | मोहनपुर, सहरसा</title>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;600;700;800&family=Hind:wght@300;400;500;600;700&family=Rozha+One&display=swap" rel="stylesheet">
<style>
:root {
  --green-dark: #0c3320;
  --green:      #1A5C2A;
  --green-mid:  #2d7a40;
  --green-light:#EEF7F1;
  --gold-dark:  #8B6914;
  --gold:       #C9A84C;
  --gold-light: #F0D060;
  --red:        #C0392B;
  --cream:      #FEFAF2;
  --text:       #1a1a1a;
  --text-muted: #555;
  --white:      #ffffff;
  --shadow:     0 8px 32px rgba(0,0,0,0.12);
}

* { margin:0; padding:0; box-sizing:border-box; scroll-behavior:smooth; }

body {
  font-family:'Hind', sans-serif;
  background: var(--cream);
  color: var(--text);
  overflow-x: hidden;
}

/* ══════════════════════════════
   TOP BAR
══════════════════════════════ */
.topbar {
  background: var(--green-dark);
  padding: 6px 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 11px;
  color: rgba(255,255,255,0.65);
}
.topbar a { color: var(--gold-light); text-decoration: none; font-weight: 600; }
.topbar .tb-right { display:flex; gap:20px; align-items:center; }

/* ══════════════════════════════
   NAVBAR
══════════════════════════════ */
.navbar {
  background: var(--cream);
  padding: 0 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 2px 20px rgba(0,0,0,0.08);
  position: sticky;
  top: 0;
  z-index: 999;
  border-bottom: 3px solid var(--gold);
}

.nav-brand {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 10px 0;
}
.nav-logo {
  width: 52px; height: 52px;
  border-radius: 50%;
  background: linear-gradient(145deg, var(--green), var(--green-dark));
  border: 2.5px solid var(--gold);
  display: flex; align-items:center; justify-content:center;
  font-size: 22px;
  flex-shrink: 0;
}
.nav-brand-text .brand-name {
  font-family: 'Baloo 2', cursive;
  font-size: 16px;
  font-weight: 800;
  color: var(--green-dark);
  line-height: 1.1;
}
.nav-brand-text .brand-loc {
  font-size: 10px;
  color: var(--text-muted);
  font-weight: 500;
}

.nav-links {
  display: flex;
  gap: 4px;
  list-style: none;
}
.nav-links a {
  text-decoration: none;
  color: var(--text);
  font-size: 13.5px;
  font-weight: 600;
  padding: 8px 16px;
  border-radius: 6px;
  transition: all 0.25s;
  position: relative;
}
.nav-links a:hover, .nav-links a.active {
  color: var(--green);
  background: var(--green-light);
}
.nav-links a.active::after {
  content: '';
  position: absolute;
  bottom: -3px; left: 16px; right: 16px;
  height: 3px;
  background: var(--gold);
  border-radius: 2px;
}
.nav-cta {
  background: var(--green) !important;
  color: var(--white) !important;
  padding: 8px 20px !important;
  border-radius: 30px !important;
}
.nav-cta:hover { background: var(--green-mid) !important; }

/* ══════════════════════════════
   PAGES
══════════════════════════════ */
.page-section { display: none; }
.page-section.active { display: block; }

/* ══════════════════════════════
   HOME — HERO
══════════════════════════════ */
.hero {
  background: linear-gradient(135deg, var(--green-dark) 0%, var(--green) 50%, var(--green-dark) 100%);
  min-height: 88vh;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  padding: 60px 40px;
}

/* Decorative circles */
.hero::before {
  content: '';
  position: absolute;
  top: -100px; right: -100px;
  width: 500px; height: 500px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(201,168,76,0.12) 0%, transparent 70%);
}
.hero::after {
  content: '';
  position: absolute;
  bottom: -80px; left: -80px;
  width: 350px; height: 350px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(255,255,255,0.05) 0%, transparent 70%);
}

/* Grid dots */
.hero-grid {
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle, rgba(255,255,255,0.06) 1px, transparent 1px);
  background-size: 30px 30px;
  pointer-events: none;
}

.hero-content {
  max-width: 1100px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  position: relative;
  z-index: 2;
  width: 100%;
}

.hero-left { }
.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  background: rgba(201,168,76,0.2);
  border: 1px solid rgba(201,168,76,0.5);
  padding: 5px 14px;
  border-radius: 20px;
  font-size: 11px;
  color: var(--gold-light);
  font-weight: 600;
  letter-spacing: 1px;
  margin-bottom: 18px;
  animation: fadeUp 0.6s ease both;
}
.hero h1 {
  font-family: 'Baloo 2', cursive;
  font-size: 52px;
  font-weight: 800;
  color: var(--white);
  line-height: 1.05;
  margin-bottom: 16px;
  animation: fadeUp 0.7s ease 0.1s both;
}
.hero h1 .gold { color: var(--gold-light); }
.hero-sub {
  font-size: 15px;
  color: rgba(255,255,255,0.75);
  line-height: 1.8;
  margin-bottom: 28px;
  animation: fadeUp 0.7s ease 0.2s both;
}
.hero-btns {
  display: flex;
  gap: 12px;
  animation: fadeUp 0.7s ease 0.3s both;
}
.btn-primary {
  background: linear-gradient(135deg, var(--gold), var(--gold-light));
  color: var(--green-dark);
  border: none;
  padding: 12px 28px;
  border-radius: 30px;
  font-size: 13.5px;
  font-weight: 700;
  cursor: pointer;
  transition: all 0.25s;
  font-family: 'Hind', sans-serif;
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 25px rgba(201,168,76,0.4); }
.btn-outline {
  background: transparent;
  color: var(--white);
  border: 2px solid rgba(255,255,255,0.4);
  padding: 12px 28px;
  border-radius: 30px;
  font-size: 13.5px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.25s;
  font-family: 'Hind', sans-serif;
}
.btn-outline:hover { background: rgba(255,255,255,0.1); border-color: rgba(255,255,255,0.7); }

.hero-right {
  display: flex;
  flex-direction: column;
  gap: 14px;
  animation: fadeUp 0.7s ease 0.2s both;
}

.hero-card {
  background: rgba(255,255,255,0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255,255,255,0.15);
  border-radius: 14px;
  padding: 18px 20px;
  display: flex;
  align-items: center;
  gap: 14px;
  transition: all 0.25s;
}
.hero-card:hover { background: rgba(255,255,255,0.15); transform: translateX(5px); }
.hc-icon {
  width: 48px; height: 48px;
  background: linear-gradient(135deg, var(--gold), var(--gold-light));
  border-radius: 12px;
  display: flex; align-items:center; justify-content:center;
  font-size: 22px;
  flex-shrink: 0;
}
.hc-title { font-size: 14px; font-weight: 700; color: var(--white); }
.hc-desc { font-size: 11.5px; color: rgba(255,255,255,0.65); margin-top: 2px; }

/* Stats strip */
.stats-strip {
  background: var(--white);
  padding: 30px 40px;
  display: flex;
  justify-content: center;
  gap: 0;
  box-shadow: var(--shadow);
}
.stat-item {
  text-align: center;
  padding: 0 48px;
  border-right: 1px solid #e8e8e8;
}
.stat-item:last-child { border-right: none; }
.stat-num {
  font-family: 'Baloo 2', cursive;
  font-size: 36px;
  font-weight: 800;
  color: var(--green);
  line-height: 1;
}
.stat-num span { color: var(--gold-dark); }
.stat-label { font-size: 12px; color: var(--text-muted); margin-top: 4px; font-weight: 500; }

/* ── Notice / Admission Banner ── */
.notice-bar {
  background: var(--red);
  padding: 12px 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
}
.notice-bar .nb-badge {
  background: var(--gold-light);
  color: var(--red);
  padding: 3px 10px;
  border-radius: 4px;
  font-size: 10px;
  font-weight: 800;
  letter-spacing: 1px;
  flex-shrink: 0;
}
.notice-bar .nb-text {
  color: var(--white);
  font-size: 13px;
  font-weight: 600;
}
.notice-bar .nb-text b { color: var(--gold-light); }

/* ── Features section ── */
.section {
  padding: 60px 40px;
  max-width: 1100px;
  margin: 0 auto;
}
.section-header {
  text-align: center;
  margin-bottom: 40px;
}
.section-eyebrow {
  font-size: 11px;
  color: var(--gold-dark);
  font-weight: 700;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  margin-bottom: 8px;
}
.section-title {
  font-family: 'Baloo 2', cursive;
  font-size: 34px;
  font-weight: 800;
  color: var(--green-dark);
  line-height: 1.15;
}
.section-title span { color: var(--green); }
.section-line {
  width: 60px; height: 3px;
  background: linear-gradient(90deg, var(--gold), var(--gold-light));
  margin: 12px auto 0;
  border-radius: 2px;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
}
.feature-card {
  background: var(--white);
  border-radius: 14px;
  padding: 24px 20px;
  text-align: center;
  border: 1.5px solid #eeeeee;
  box-shadow: 0 2px 12px rgba(0,0,0,0.05);
  transition: all 0.3s;
}
.feature-card:hover {
  border-color: var(--gold);
  transform: translateY(-5px);
  box-shadow: 0 12px 30px rgba(0,0,0,0.1);
}
.fc-icon {
  width: 56px; height: 56px;
  border-radius: 14px;
  background: var(--green-light);
  display: flex; align-items:center; justify-content:center;
  font-size: 26px;
  margin: 0 auto 14px;
  transition: all 0.3s;
}
.feature-card:hover .fc-icon { background: var(--green); }
.fc-title { font-size: 13.5px; font-weight: 700; color: var(--green-dark); margin-bottom: 6px; }
.fc-desc { font-size: 11px; color: var(--text-muted); line-height: 1.65; }

/* ── Photo gallery strip ── */
.photo-strip-section {
  background: var(--green-dark);
  padding: 50px 40px;
}
.photo-strip-section .section-title { color: var(--white); }
.photo-strip-section .section-eyebrow { color: var(--gold-light); }
.photos-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  max-width: 1100px;
  margin: 30px auto 0;
}
.photo-placeholder {
  aspect-ratio: 4/3;
  background: rgba(255,255,255,0.08);
  border: 2px dashed rgba(201,168,76,0.3);
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 8px;
  transition: all 0.25s;
  cursor: pointer;
}
.photo-placeholder:hover { background: rgba(255,255,255,0.14); border-color: var(--gold); }
.photo-placeholder .ph-icon { font-size: 28px; opacity: 0.6; }
.photo-placeholder .ph-label { font-size: 11px; color: rgba(255,255,255,0.5); text-align: center; }

/* ══════════════════════════════
   ABOUT PAGE
══════════════════════════════ */
.page-hero {
  background: linear-gradient(135deg, var(--green-dark), var(--green));
  padding: 60px 40px;
  text-align: center;
  position: relative;
  overflow: hidden;
}
.page-hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
  background-size: 25px 25px;
}
.page-hero h2 {
  font-family: 'Baloo 2', cursive;
  font-size: 40px;
  font-weight: 800;
  color: var(--white);
  position: relative;
}
.page-hero p {
  font-size: 15px;
  color: rgba(255,255,255,0.7);
  margin-top: 8px;
  position: relative;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: center;
  max-width: 1100px;
  margin: 0 auto;
}

.about-img-wrap {
  border-radius: 16px;
  overflow: hidden;
  background: var(--green-light);
  aspect-ratio: 4/3;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  border: 2px dashed rgba(26,92,42,0.2);
}
.about-img-wrap .ai-icon { font-size: 50px; opacity: 0.5; }
.about-img-wrap .ai-text { font-size: 13px; color: var(--text-muted); }

.about-text-content { }
.about-text-content h3 {
  font-family: 'Baloo 2', cursive;
  font-size: 26px;
  font-weight: 800;
  color: var(--green-dark);
  margin-bottom: 14px;
  line-height: 1.2;
}
.about-text-content p {
  font-size: 13px;
  color: var(--text-muted);
  line-height: 1.85;
  margin-bottom: 12px;
}
.about-text-content p b { color: var(--green); }

.highlight-points {
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-top: 16px;
}
.hp-item {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 13px;
  color: var(--text);
  font-weight: 500;
}
.hp-dot {
  width: 22px; height: 22px;
  background: var(--green);
  border-radius: 6px;
  display: flex; align-items:center; justify-content:center;
  color: var(--white);
  font-size: 10px;
  flex-shrink: 0;
}

.vision-mission-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  max-width: 1100px;
  margin: 0 auto;
}
.vm-card {
  border-radius: 14px;
  padding: 28px 26px;
  position: relative;
  overflow: hidden;
}
.vm-card.vision { background: linear-gradient(135deg, var(--green-dark), var(--green)); color: var(--white); }
.vm-card.mission { background: var(--white); border: 1.5px solid #eee; }
.vm-card h4 {
  font-family: 'Baloo 2', cursive;
  font-size: 20px;
  font-weight: 800;
  margin-bottom: 10px;
}
.vm-card.vision h4 { color: var(--gold-light); }
.vm-card.mission h4 { color: var(--green-dark); }
.vm-card p { font-size: 13px; line-height: 1.8; }
.vm-card.vision p { color: rgba(255,255,255,0.78); }
.vm-card.mission p { color: var(--text-muted); }
.vm-icon { font-size: 36px; margin-bottom: 12px; display: block; }

/* Team */
.team-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  max-width: 1100px;
  margin: 0 auto;
}
.team-card {
  background: var(--white);
  border-radius: 14px;
  padding: 28px 20px;
  text-align: center;
  border: 1.5px solid #eee;
  box-shadow: 0 2px 10px rgba(0,0,0,0.05);
  transition: all 0.3s;
}
.team-card:hover { border-color: var(--gold); transform: translateY(-4px); }
.team-avatar {
  width: 70px; height: 70px;
  border-radius: 50%;
  background: var(--green-light);
  border: 3px solid var(--gold);
  display: flex; align-items:center; justify-content:center;
  font-size: 28px;
  margin: 0 auto 14px;
}
.team-name { font-family: 'Baloo 2', cursive; font-size: 16px; font-weight: 800; color: var(--green-dark); }
.team-role { font-size: 11.5px; color: var(--gold-dark); font-weight: 600; margin-top: 3px; }
.team-desc { font-size: 11.5px; color: var(--text-muted); margin-top: 8px; line-height: 1.6; }

/* ══════════════════════════════
   ADMISSIONS PAGE
══════════════════════════════ */
.admission-hero-section {
  background: linear-gradient(135deg, var(--red) 0%, #922b21 100%);
  padding: 50px 40px;
  text-align: center;
}
.admission-hero-section h2 {
  font-family: 'Baloo 2', cursive;
  font-size: 40px;
  font-weight: 800;
  color: var(--white);
}
.admission-hero-section p { font-size: 15px; color: rgba(255,255,255,0.75); margin-top: 8px; }
.adm-badge {
  display: inline-block;
  background: var(--gold-light);
  color: var(--red);
  padding: 5px 16px;
  border-radius: 20px;
  font-size: 11px;
  font-weight: 800;
  letter-spacing: 1px;
  margin-bottom: 14px;
}

.process-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  max-width: 1100px;
  margin: 0 auto;
}
.process-card {
  background: var(--white);
  border-radius: 14px;
  padding: 26px 18px;
  text-align: center;
  border: 1.5px solid #eee;
  position: relative;
  transition: all 0.3s;
}
.process-card:hover { border-color: var(--green); transform: translateY(-4px); }
.process-num {
  position: absolute;
  top: -14px; left: 50%;
  transform: translateX(-50%);
  width: 28px; height: 28px;
  background: var(--green);
  color: var(--white);
  border-radius: 50%;
  font-size: 12px;
  font-weight: 800;
  display: flex; align-items:center; justify-content:center;
  border: 2px solid var(--cream);
}
.process-icon { font-size: 30px; margin-bottom: 10px; }
.process-title { font-family: 'Baloo 2', cursive; font-size: 14px; font-weight: 800; color: var(--green-dark); margin-bottom: 6px; }
.process-desc { font-size: 11px; color: var(--text-muted); line-height: 1.65; }

/* Classes table */
.classes-table {
  width: 100%;
  border-collapse: collapse;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: var(--shadow);
}
.classes-table th {
  background: var(--green);
  color: var(--white);
  padding: 12px 16px;
  font-size: 13px;
  font-weight: 700;
  text-align: left;
}
.classes-table td {
  padding: 11px 16px;
  font-size: 12.5px;
  border-bottom: 1px solid #f0f0f0;
}
.classes-table tr:last-child td { border-bottom: none; }
.classes-table tr:nth-child(even) td { background: var(--green-light); }
.classes-table .badge-open {
  background: #e8f5e9;
  color: #2e7d32;
  padding: 2px 10px;
  border-radius: 12px;
  font-size: 10.5px;
  font-weight: 700;
}

/* Offer box */
.offer-box {
  background: linear-gradient(135deg, #6a1b9a, #9c27b0);
  border-radius: 16px;
  padding: 30px 32px;
  display: flex;
  align-items: center;
  gap: 24px;
  max-width: 1100px;
  margin: 0 auto;
  box-shadow: 0 8px 30px rgba(106,27,154,0.25);
}
.offer-left { flex: 1; }
.offer-box h3 {
  font-family: 'Baloo 2', cursive;
  font-size: 24px;
  font-weight: 800;
  color: var(--gold-light);
  margin-bottom: 8px;
}
.offer-box p { font-size: 13px; color: rgba(255,255,255,0.85); line-height: 1.75; }
.offer-box p b { color: var(--white); }
.offer-right {
  background: rgba(255,255,255,0.12);
  border: 1.5px solid rgba(240,208,96,0.4);
  border-radius: 12px;
  padding: 16px 22px;
  text-align: center;
  flex-shrink: 0;
}
.offer-right .or1 { font-size: 10px; color: rgba(255,255,255,0.6); letter-spacing: 1px; }
.offer-right .or2 {
  font-family: 'Baloo 2', cursive;
  font-size: 28px;
  font-weight: 800;
  color: var(--gold-light);
  line-height: 1.1;
}

/* ══════════════════════════════
   CONTACT PAGE
══════════════════════════════ */
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 40px;
  max-width: 1100px;
  margin: 0 auto;
}

.contact-info-col { }
.contact-info-col h3 {
  font-family: 'Baloo 2', cursive;
  font-size: 28px;
  font-weight: 800;
  color: var(--green-dark);
  margin-bottom: 20px;
}

.ci-item {
  display: flex;
  gap: 14px;
  align-items: flex-start;
  margin-bottom: 18px;
  padding: 16px;
  background: var(--white);
  border-radius: 12px;
  border: 1.5px solid #eee;
  transition: all 0.25s;
}
.ci-item:hover { border-color: var(--gold); }
.ci-icon {
  width: 44px; height: 44px;
  background: var(--green);
  border-radius: 10px;
  display: flex; align-items:center; justify-content:center;
  font-size: 20px;
  flex-shrink: 0;
}
.ci-label { font-size: 10px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 1px; font-weight: 600; }
.ci-value { font-size: 14px; font-weight: 700; color: var(--text); margin-top: 2px; }
.ci-sub { font-size: 11px; color: var(--text-muted); margin-top: 2px; }

/* Map placeholder */
.map-placeholder {
  background: var(--green-light);
  border-radius: 14px;
  border: 2px dashed rgba(26,92,42,0.25);
  min-height: 220px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 10px;
  margin-bottom: 20px;
}
.map-placeholder .mp-icon { font-size: 40px; opacity: 0.5; }
.map-placeholder .mp-text { font-size: 13px; color: var(--text-muted); }

/* Contact form */
.contact-form { }
.contact-form h3 {
  font-family: 'Baloo 2', cursive;
  font-size: 22px;
  font-weight: 800;
  color: var(--green-dark);
  margin-bottom: 18px;
}
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
.form-group { margin-bottom: 14px; }
.form-group label {
  display: block;
  font-size: 12px;
  font-weight: 600;
  color: var(--text-muted);
  margin-bottom: 5px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
.form-group input,
.form-group textarea,
.form-group select {
  width: 100%;
  padding: 11px 14px;
  border: 1.5px solid #e0e0e0;
  border-radius: 8px;
  font-size: 13px;
  font-family: 'Hind', sans-serif;
  color: var(--text);
  background: var(--white);
  outline: none;
  transition: all 0.2s;
}
.form-group input:focus,
.form-group textarea:focus,
.form-group select:focus {
  border-color: var(--green);
  box-shadow: 0 0 0 3px rgba(26,92,42,0.08);
}
.form-group textarea { resize: vertical; min-height: 100px; }
.form-submit {
  width: 100%;
  padding: 13px;
  background: linear-gradient(135deg, var(--green), var(--green-mid));
  color: var(--white);
  border: none;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 700;
  font-family: 'Hind', sans-serif;
  cursor: pointer;
  transition: all 0.25s;
}
.form-submit:hover { transform: translateY(-2px); box-shadow: 0 8px 20px rgba(26,92,42,0.3); }

/* ══════════════════════════════
   FOOTER
══════════════════════════════ */
.footer {
  background: var(--green-dark);
  padding: 48px 40px 0;
}
.footer-grid {
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr;
  gap: 40px;
  max-width: 1100px;
  margin: 0 auto;
  padding-bottom: 36px;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}
.footer-brand .fb-name {
  font-family: 'Baloo 2', cursive;
  font-size: 20px;
  font-weight: 800;
  color: var(--white);
  margin-bottom: 4px;
}
.footer-brand .fb-loc { font-size: 12px; color: rgba(255,255,255,0.5); margin-bottom: 14px; }
.footer-brand .fb-desc { font-size: 12px; color: rgba(255,255,255,0.6); line-height: 1.75; }
.footer-col h5 {
  font-size: 12px;
  font-weight: 700;
  color: var(--gold-light);
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 14px;
}
.footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 8px; }
.footer-col ul li a {
  font-size: 13px;
  color: rgba(255,255,255,0.6);
  text-decoration: none;
  transition: color 0.2s;
}
.footer-col ul li a:hover { color: var(--gold-light); }
.footer-col .fc-contact { font-size: 12.5px; color: rgba(255,255,255,0.6); display: flex; flex-direction: column; gap: 8px; }
.footer-col .fc-contact span { display: flex; align-items: center; gap: 8px; }

.footer-bottom {
  max-width: 1100px;
  margin: 0 auto;
  padding: 16px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 11px;
  color: rgba(255,255,255,0.35);
}

/* ══════════════════════════════
   ANIMATIONS
══════════════════════════════ */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* Success popup */
.success-toast {
  position: fixed;
  bottom: 30px; right: 30px;
  background: var(--green);
  color: var(--white);
  padding: 14px 22px;
  border-radius: 10px;
  font-size: 13.5px;
  font-weight: 600;
  box-shadow: 0 8px 25px rgba(0,0,0,0.2);
  display: none;
  z-index: 9999;
  animation: fadeUp 0.3s ease;
}
</style>
</head>
<body>

<!-- TOP BAR -->
<div class="topbar">
  <span>📜 Reg. No.: SAH-PVT SCHOOL/NMES-0180/2020 &nbsp;|&nbsp; बिहार सरकार द्वारा मान्यता प्राप्त</span>
  <div class="tb-right">
    <span>📞 <a href="tel:9113788228">9113788228</a></span>
    <span>📍 मोहनपुर, नौहट्टा, सहरसा</span>
  </div>
</div>

<!-- NAVBAR -->
<nav class="navbar">
  <div class="nav-brand">
    <div class="nav-logo">📚</div>
    <div class="nav-brand-text">
      <div class="brand-name">न्यू मॉडर्न इंग्लिश स्कूल</div>
      <div class="brand-loc">मोहनपुर, नौहट्टा, सहरसा</div>
    </div>
  </div>
  <ul class="nav-links">
    <li><a href="#" class="active" onclick="showPage('home',this)">🏠 होम</a></li>
    <li><a href="#" onclick="showPage('about',this)">🏫 हमारे बारे में</a></li>
    <li><a href="#" onclick="showPage('admissions',this)">🎓 प्रवेश</a></li>
    <li><a href="#" onclick="showPage('contact',this)">📞 संपर्क</a></li>
    <li><a href="#" class="nav-cta" onclick="showPage('admissions',this)">अभी आवेदन करें →</a></li>
  </ul>
</nav>

<!-- ════════════════════════════════
     HOME PAGE
════════════════════════════════ -->
<div id="home" class="page-section active">

  <!-- Notice Bar -->
  <div class="notice-bar">
    <div class="nb-badge">नया</div>
    <div class="nb-text">🌟 Admission Open 2026–27 — <b>10 अप्रैल से पहले नामांकन पर प्रवेश निःशुल्क!</b> &nbsp;|&nbsp; सीमित सीटें उपलब्ध</div>
  </div>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-grid"></div>
    <div class="hero-content">
      <div class="hero-left">
        <div class="hero-badge">🌟 कोसी क्षेत्र में 11 वर्षों का भरोसा</div>
        <h1>बच्चों का <span class="gold">उज्ज्वल भविष्य</span> हमारी जिम्मेदारी</h1>
        <p class="hero-sub">आवासीय न्यू मॉडर्न इंग्लिश स्कूल — जहाँ आधुनिक शिक्षा, अनुशासन और नैतिक मूल्यों के साथ हर बच्चे की प्रतिभा को निखारा जाता है।</p>
        <div class="hero-btns">
          <button class="btn-primary" onclick="showPage('admissions', document.querySelectorAll('.nav-links a')[2])">प्रवेश लें 2026–27 →</button>
          <button class="btn-outline" onclick="showPage('about', document.querySelectorAll('.nav-links a')[1])">और जानें</button>
        </div>
      </div>
      <div class="hero-right">
        <div class="hero-card">
          <div class="hc-icon">📚</div>
          <div>
            <div class="hc-title">Concept Clear पढ़ाई</div>
            <div class="hc-desc">मजबूत आधार के साथ हर विषय की गहरी समझ</div>
          </div>
        </div>
        <div class="hero-card">
          <div class="hc-icon">🗣️</div>
          <div>
            <div class="hc-title">Spoken English Focus</div>
            <div class="hc-desc">रोज़ाना अंग्रेजी बोलने का अभ्यास</div>
          </div>
        </div>
        <div class="hero-card">
          <div class="hc-icon">🏆</div>
          <div>
            <div class="hc-title">सर्वांगीण विकास</div>
            <div class="hc-desc">खेल, संस्कृति, शिक्षा — सब एक छत के नीचे</div>
          </div>
        </div>
        <div class="hero-card">
          <div class="hc-icon">🚐</div>
          <div>
            <div class="hc-title">सुरक्षित स्कूल वैन</div>
            <div class="hc-desc">सुरक्षित आवागमन की सुविधा उपलब्ध</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- STATS -->
  <div class="stats-strip">
    <div class="stat-item">
      <div class="stat-num">11<span>+</span></div>
      <div class="stat-label">वर्षों का अनुभव</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">500<span>+</span></div>
      <div class="stat-label">सफल छात्र</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">10<span>+</span></div>
      <div class="stat-label">अनुभवी शिक्षक</div>
    </div>
    <div class="stat-item">
      <div class="stat-num">Nursery<span>–8</span></div>
      <div class="stat-label">कक्षाएं उपलब्ध</div>
    </div>
  </div>

  <!-- FEATURES -->
  <div style="background: var(--cream); padding: 60px 0;">
    <div class="section">
      <div class="section-header">
        <div class="section-eyebrow">हमारी विशेषताएँ</div>
        <div class="section-title">क्यों चुनें <span>न्यू मॉडर्न इंग्लिश स्कूल?</span></div>
        <div class="section-line"></div>
      </div>
      <div class="features-grid">
        <div class="feature-card">
          <div class="fc-icon">📖</div>
          <div class="fc-title">Concept Clear पढ़ाई</div>
          <div class="fc-desc">हर विषय को जड़ से समझाना हमारी प्राथमिकता है।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">👨‍🏫</div>
          <div class="fc-title">अनुभवी शिक्षक</div>
          <div class="fc-desc">समर्पित और प्रशिक्षित शिक्षक जो बच्चों को प्रेरित करते हैं।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">🗣️</div>
          <div class="fc-title">Spoken English</div>
          <div class="fc-desc">रोज़ बोलचाल के अभ्यास से आत्मविश्वास का विकास।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">📊</div>
          <div class="fc-title">नियमित टेस्ट</div>
          <div class="fc-desc">प्रगति रिपोर्ट से अभिभावकों को अपडेट रखा जाता है।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">⚽</div>
          <div class="fc-title">खेलकूद</div>
          <div class="fc-desc">शारीरिक विकास के लिए खेल और सांस्कृतिक गतिविधियाँ।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">🛡️</div>
          <div class="fc-title">सुरक्षित वातावरण</div>
          <div class="fc-desc">स्वच्छ, सुरक्षित और अनुशासित परिसर।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">🏛️</div>
          <div class="fc-title">नैतिक शिक्षा</div>
          <div class="fc-desc">संस्कार और मूल्यों पर आधारित शिक्षण पद्धति।</div>
        </div>
        <div class="feature-card">
          <div class="fc-icon">🚐</div>
          <div class="fc-title">वैन सुविधा</div>
          <div class="fc-desc">सुरक्षित स्कूल वैन सेवा उपलब्ध।</div>
        </div>
      </div>
    </div>
  </div>

  <!-- PHOTO STRIP -->
  <div class="photo-strip-section">
    <div style="max-width:1100px; margin:0 auto;">
      <div class="section-header">
        <div class="section-eyebrow">झलकियाँ</div>
        <div class="section-title" style="color:white;">हमारे <span style="color:var(--gold-light)">स्कूल की तस्वीरें</span></div>
        <div class="section-line"></div>
      </div>
    </div>
    <div class="photos-grid">
      <div class="photo-placeholder"><div class="ph-icon">🏫</div><div class="ph-label">स्कूल भवन</div></div>
      <div class="photo-placeholder"><div class="ph-icon">📚</div><div class="ph-label">कक्षाकक्ष</div></div>
      <div class="photo-placeholder"><div class="ph-icon">🎌</div><div class="ph-label">राष्ट्रीय कार्यक्रम</div></div>
      <div class="photo-placeholder"><div class="ph-icon">⚽</div><div class="ph-label">खेल का मैदान</div></div>
    </div>
  </div>

</div>

<!-- ════════════════════════════════
     ABOUT PAGE
════════════════════════════════ -->
<div id="about" class="page-section">
  <div class="page-hero">
    <h2>🏫 हमारे बारे में</h2>
    <p>जानिए न्यू मॉडर्न इंग्लिश स्कूल की कहानी, हमारी सोच और हमारे लक्ष्य</p>
  </div>

  <div style="padding: 56px 40px;">
    <div class="about-grid" style="margin-bottom: 50px;">
      <div class="about-img-wrap">
        <div class="ai-icon">🏫</div>
        <div class="ai-text">स्कूल की तस्वीर यहाँ आएगी</div>
      </div>
      <div class="about-text-content">
        <h3>कोसी क्षेत्र का एक विश्वसनीय शिक्षण संस्थान</h3>
        <p>आवासीय न्यू मॉडर्न इंग्लिश स्कूल, मोहनपुर, नौहट्टा, सहरसा में स्थित एक <b>बिहार सरकार द्वारा मान्यता प्राप्त विद्यालय</b> है। 2015 से हम इस क्षेत्र के बच्चों को गुणवत्तापूर्ण अंग्रेजी माध्यम शिक्षा प्रदान कर रहे हैं।</p>
        <p>हमारा मानना है कि <b>शिक्षा केवल किताबों तक सीमित नहीं होनी चाहिए</b> — बच्चों में आत्मविश्वास, नैतिक मूल्य और व्यावहारिक कौशल का विकास उतना ही जरूरी है।</p>
        <p>हमारा उद्देश्य प्रत्येक छात्र को एक मजबूत आधार देकर उसके <b>उज्ज्वल भविष्य की नींव रखना</b> है।</p>
        <div class="highlight-points">
          <div class="hp-item"><div class="hp-dot">✓</div> नर्सरी से कक्षा 8वीं तक — अंग्रेजी माध्यम</div>
          <div class="hp-item"><div class="hp-dot">✓</div> 11 वर्षों का सफल शैक्षणिक अनुभव</div>
          <div class="hp-item"><div class="hp-dot">✓</div> Reg. No.: SAH-PVT SCHOOL/NMES-0180/2020</div>
          <div class="hp-item"><div class="hp-dot">✓</div> आवासीय सुविधा उपलब्ध</div>
        </div>
      </div>
    </div>

    <div class="vision-mission-grid" style="margin-bottom: 50px;">
      <div class="vm-card vision">
        <span class="vm-icon">🌟</span>
        <h4>हमारी दृष्टि (Vision)</h4>
        <p>एक ऐसा शिक्षण संस्थान बनाना जहाँ हर बच्चा — चाहे किसी भी पृष्ठभूमि से हो — अपनी पूरी क्षमता को पहचाने और एक जिम्मेदार नागरिक बने।</p>
      </div>
      <div class="vm-card mission">
        <span class="vm-icon">🎯</span>
        <h4>हमारा मिशन (Mission)</h4>
        <p>आधुनिक शिक्षण पद्धतियों और नैतिक मूल्यों के माध्यम से बच्चों में आत्मविश्वास, ज्ञान और चरित्र का निर्माण करना — ताकि वे जीवन की हर चुनौती का सामना कर सकें।</p>
      </div>
    </div>

    <div class="section-header" style="margin-bottom:30px;">
      <div class="section-eyebrow">हमारी टीम</div>
      <div class="section-title">अनुभवी <span>शिक्षक एवं स्टाफ</span></div>
      <div class="section-line"></div>
    </div>
    <div class="team-grid">
      <div class="team-card">
        <div class="team-avatar">👨‍💼</div>
        <div class="team-name">सिंधु कुमार सिंह</div>
        <div class="team-role">निदेशक</div>
        <div class="team-desc">11 वर्षों से शिक्षा के क्षेत्र में समर्पित। बच्चों के सर्वांगीण विकास के लिए प्रतिबद्ध।</div>
      </div>
      <div class="team-card">
        <div class="team-avatar">👩‍🏫</div>
        <div class="team-name">वरिष्ठ शिक्षिका</div>
        <div class="team-role">प्राथमिक विभाग प्रमुख</div>
        <div class="team-desc">नर्सरी से कक्षा 5 तक के बच्चों की शिक्षा की देखरेख।</div>
      </div>
      <div class="team-card">
        <div class="team-avatar">👨‍🏫</div>
        <div class="team-name">वरिष्ठ शिक्षक</div>
        <div class="team-role">उच्च प्राथमिक विभाग</div>
        <div class="team-desc">कक्षा 6 से 8 तक विज्ञान, गणित और अंग्रेजी के विशेषज्ञ।</div>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════════════════
     ADMISSIONS PAGE
════════════════════════════════ -->
<div id="admissions" class="page-section">
  <div class="admission-hero-section">
    <div class="adm-badge">🌟 ADMISSION OPEN 2026–27</div>
    <h2>प्रवेश प्रक्रिया</h2>
    <p>सत्र 2026–27 के लिए नामांकन शुरू — अभी आवेदन करें और सीट सुरक्षित करें</p>
  </div>

  <div style="padding: 56px 40px;">

    <!-- Process -->
    <div class="section-header" style="margin-bottom:36px;">
      <div class="section-eyebrow">प्रवेश के चरण</div>
      <div class="section-title">आसान <span>प्रवेश प्रक्रिया</span></div>
      <div class="section-line"></div>
    </div>
    <div class="process-grid" style="margin-bottom: 50px;">
      <div class="process-card">
        <div class="process-num">1</div>
        <div class="process-icon">📞</div>
        <div class="process-title">संपर्क करें</div>
        <div class="process-desc">9113788228 पर कॉल करें या स्कूल में आएं।</div>
      </div>
      <div class="process-card">
        <div class="process-num">2</div>
        <div class="process-icon">📋</div>
        <div class="process-title">फॉर्म भरें</div>
        <div class="process-desc">प्रवेश फॉर्म भरें और आवश्यक दस्तावेज जमा करें।</div>
      </div>
      <div class="process-card">
        <div class="process-num">3</div>
        <div class="process-icon">✅</div>
        <div class="process-title">पुष्टि करें</div>
        <div class="process-desc">सीट की पुष्टि के बाद शुल्क जमा करें।</div>
      </div>
      <div class="process-card">
        <div class="process-num">4</div>
        <div class="process-icon">🎒</div>
        <div class="process-title">शुरुआत करें</div>
        <div class="process-desc">नई कक्षा में अपने बच्चे का स्वागत!</div>
      </div>
    </div>

    <!-- Classes table -->
    <div class="section-header" style="margin-bottom:24px;">
      <div class="section-eyebrow">उपलब्ध कक्षाएं</div>
      <div class="section-title">सत्र 2026–27 <span>प्रवेश सूची</span></div>
      <div class="section-line"></div>
    </div>
    <div style="max-width:1100px; margin: 0 auto 48px; border-radius:12px; overflow:hidden; box-shadow: var(--shadow);">
      <table class="classes-table">
        <thead>
          <tr>
            <th>कक्षा</th>
            <th>आयु सीमा</th>
            <th>माध्यम</th>
            <th>सीटें</th>
            <th>स्थिति</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>नर्सरी</td><td>3–4 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>LKG</td><td>4–5 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>UKG</td><td>5–6 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>कक्षा 1–2</td><td>6–8 वर्ष</td><td>अंग्रेजी</td><td>35</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>कक्षा 3–5</td><td>8–11 वर्ष</td><td>अंग्रेजी</td><td>35</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>कक्षा 6–8</td><td>11–14 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
        </tbody>
      </table>
    </div>

    <!-- Offer box -->
    <div class="offer-box" style="margin-bottom:50px;">
      <div class="offer-left">
        <h3>🎁 Early Bird Special Offer!</h3>
        <p><b>10 अप्रैल 2026 से पहले नामांकन</b> कराने पर —<br>
        ✨ प्रवेश शुल्क पूर्णतः <b>निःशुल्क</b><br>
        ⭐ पहले आएं, <b>ज्यादा छूट पाएं!</b><br>
        ⚠️ सीमित सीटें — जल्द संपर्क करें!</p>
      </div>
      <div class="offer-right">
        <span class="or1">ऑफर तक</span>
        <span class="or2">10 अप्रैल<br>2026</span>
      </div>
    </div>

    <!-- Documents needed -->
    <div class="section-header" style="margin-bottom:24px;">
      <div class="section-eyebrow">आवश्यक दस्तावेज</div>
      <div class="section-title">प्रवेश के लिए <span>जरूरी कागजात</span></div>
      <div class="section-line"></div>
    </div>
    <div style="max-width:1100px; margin:0 auto; display:grid; grid-template-columns: repeat(3,1fr); gap:16px;">
      <div style="background:var(--white); border:1.5px solid #eee; border-radius:12px; padding:18px; display:flex; gap:12px; align-items:center;">
        <span style="font-size:24px;">📸</span>
        <div><div style="font-weight:700; font-size:13px;">पासपोर्ट फोटो</div><div style="font-size:11px; color:var(--text-muted);">बच्चे की 2 नवीनतम फोटो</div></div>
      </div>
      <div style="background:var(--white); border:1.5px solid #eee; border-radius:12px; padding:18px; display:flex; gap:12px; align-items:center;">
        <span style="font-size:24px;">🎂</span>
        <div><div style="font-weight:700; font-size:13px;">जन्म प्रमाण पत्र</div><div style="font-size:11px; color:var(--text-muted);">आयु सत्यापन के लिए</div></div>
      </div>
      <div style="background:var(--white); border:1.5px solid #eee; border-radius:12px; padding:18px; display:flex; gap:12px; align-items:center;">
        <span style="font-size:24px;">📄</span>
        <div><div style="font-weight:700; font-size:13px;">पुरानी मार्कशीट</div><div style="font-size:11px; color:var(--text-muted);">पिछली कक्षा की रिपोर्ट</div></div>
      </div>
      <div style="background:var(--white); border:1.5px solid #eee; border-radius:12px; padding:18px; display:flex; gap:12px; align-items:center;">
        <span style="font-size:24px;">🪪</span>
        <div><div style="font-weight:700; font-size:13px;">आधार कार्ड</div><div style="font-size:11px; color:var(--text-muted);">बच्चे / अभिभावक का</div></div>
      </div>
      <div style="background:var(--white); border:1.5px solid #eee; border-radius:12px; padding:18px; display:flex; gap:12px; align-items:center;">
        <span style="font-size:24px;">📋</span>
        <div><div style="font-weight:700; font-size:13px;">TC (Transfer Certificate)</div><div style="font-size:11px; color:var(--text-muted);">पुराने स्कूल से (यदि लागू)</div></div>
      </div>
      <div style="background:var(--white); border:1.5px solid #eee; border-radius:12px; padding:18px; display:flex; gap:12px; align-items:center;">
        <span style="font-size:24px;">🏠</span>
        <div><div style="font-weight:700; font-size:13px;">पता प्रमाण</div><div style="font-size:11px; color:var(--text-muted);">निवास का कोई प्रमाण</div></div>
      </div>
    </div>

  </div>
</div>

<!-- ════════════════════════════════
     CONTACT PAGE
════════════════════════════════ -->
<div id="contact" class="page-section">
  <div class="page-hero">
    <h2>📞 संपर्क करें</h2>
    <p>किसी भी जानकारी के लिए हमसे संपर्क करें — हम सदैव तत्पर हैं</p>
  </div>

  <div style="padding: 56px 40px;">
    <div class="contact-grid">
      <div class="contact-info-col">
        <h3>हमसे मिलें</h3>
        <div class="ci-item">
          <div class="ci-icon">👨‍💼</div>
          <div>
            <div class="ci-label">निदेशक</div>
            <div class="ci-value">सिंधु कुमार सिंह</div>
          </div>
        </div>
        <div class="ci-item">
          <div class="ci-icon">📞</div>
          <div>
            <div class="ci-label">मोबाइल नंबर</div>
            <div class="ci-value">9113788228</div>
            <div class="ci-sub">सुबह 8 बजे से शाम 6 बजे तक</div>
          </div>
        </div>
        <div class="ci-item">
          <div class="ci-icon">📍</div>
          <div>
            <div class="ci-label">पता</div>
            <div class="ci-value">मोहनपुर, नौहट्टा, सहरसा</div>
            <div class="ci-sub">बिहार, भारत</div>
          </div>
        </div>
        <div class="ci-item">
          <div class="ci-icon">🕐</div>
          <div>
            <div class="ci-label">स्कूल समय</div>
            <div class="ci-value">सोम–शनि: 8:00 AM – 2:00 PM</div>
            <div class="ci-sub">रविवार: बंद</div>
          </div>
        </div>
        <div class="map-placeholder">
          <div class="mp-icon">🗺️</div>
          <div class="mp-text">मोहनपुर, नौहट्टा, सहरसा — बिहार</div>
        </div>
      </div>

      <div class="contact-form">
        <h3>संदेश भेजें</h3>
        <div class="form-row">
          <div class="form-group">
            <label>अभिभावक का नाम *</label>
            <input type="text" placeholder="आपका पूरा नाम" id="f-name">
          </div>
          <div class="form-group">
            <label>मोबाइल नंबर *</label>
            <input type="tel" placeholder="10 अंकों का नंबर" id="f-phone">
          </div>
        </div>
        <div class="form-group">
          <label>बच्चे का नाम</label>
          <input type="text" placeholder="बच्चे का पूरा नाम" id="f-child">
        </div>
        <div class="form-group">
          <label>कक्षा में प्रवेश चाहिए</label>
          <select id="f-class">
            <option value="">-- कक्षा चुनें --</option>
            <option>नर्सरी</option>
            <option>LKG</option>
            <option>UKG</option>
            <option>कक्षा 1</option>
            <option>कक्षा 2</option>
            <option>कक्षा 3</option>
            <option>कक्षा 4</option>
            <option>कक्षा 5</option>
            <option>कक्षा 6</option>
            <option>कक्षा 7</option>
            <option>कक्षा 8</option>
          </select>
        </div>
        <div class="form-group">
          <label>संदेश</label>
          <textarea placeholder="अपना प्रश्न या संदेश यहाँ लिखें..." id="f-msg"></textarea>
        </div>
        <button class="form-submit" onclick="submitForm()">📨 संदेश भेजें</button>
      </div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer class="footer">
  <div class="footer-grid">
    <div class="footer-brand">
      <div class="fb-name">📚 न्यू मॉडर्न इंग्लिश स्कूल</div>
      <div class="fb-loc">मोहनपुर, नौहट्टा, सहरसा — बिहार</div>
      <div class="fb-desc">कोसी क्षेत्र में 11 वर्षों से गुणवत्तापूर्ण शिक्षा प्रदान करते हुए हम बच्चों के उज्ज्वल भविष्य की नींव रख रहे हैं।</div>
    </div>
    <div class="footer-col">
      <h5>Quick Links</h5>
      <ul>
        <li><a href="#" onclick="showPage('home',this)">🏠 होम</a></li>
        <li><a href="#" onclick="showPage('about',this)">🏫 हमारे बारे में</a></li>
        <li><a href="#" onclick="showPage('admissions',this)">🎓 प्रवेश 2026–27</a></li>
        <li><a href="#" onclick="showPage('contact',this)">📞 संपर्क करें</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h5>संपर्क</h5>
      <div class="fc-contact">
        <span>📞 9113788228</span>
        <span>📍 मोहनपुर, नौहट्टा, सहरसा</span>
        <span>🕐 सोम–शनि: 8AM – 2PM</span>
        <span>📜 Reg: SAH-PVT SCHOOL/NMES-0180/2020</span>
      </div>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2026 न्यू मॉडर्न इंग्लिश स्कूल — सभी अधिकार सुरक्षित</span>
    <span>आपके बच्चे का सपना, हमारी जिम्मेदारी 🌟</span>
  </div>
</footer>

<!-- Toast -->
<div class="success-toast" id="toast">✅ आपका संदेश सफलतापूर्वक भेजा गया! हम जल्द संपर्क करेंगे।</div>

<script>
function showPage(id, el) {
  // Hide all pages
  document.querySelectorAll('.page-section').forEach(p => p.classList.remove('active'));
  // Show target
  document.getElementById(id).classList.add('active');
  // Update nav active
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
  if (el && el.classList && el.classList.contains('nav-links') === false) {
    // find matching nav link
    const links = document.querySelectorAll('.nav-links a');
    links.forEach(a => {
      if (a.getAttribute('onclick') && a.getAttribute('onclick').includes("'" + id + "'")) {
        a.classList.add('active');
      }
    });
  }
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function submitForm() {
  const name = document.getElementById('f-name').value.trim();
  const phone = document.getElementById('f-phone').value.trim();
  if (!name || !phone) {
    alert('कृपया अपना नाम और मोबाइल नंबर भरें।');
    return;
  }
  // Show toast
  const toast = document.getElementById('toast');
  toast.style.display = 'block';
  setTimeout(() => { toast.style.display = 'none'; }, 4000);
  // Reset form
  ['f-name','f-phone','f-child','f-msg'].forEach(id => document.getElementById(id).value = '');
  document.getElementById('f-class').value = '';
}
</script>
</body>
</html>
