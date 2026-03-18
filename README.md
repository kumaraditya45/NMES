<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>New Modern English School | Mohanpur, Saharsa, Bihar</title>
<!-- PWA Support -->
<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#0D2137">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="NMES School">
<link rel="apple-touch-icon" href="icon-192.png">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700;800&family=Nunito:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --navy:#0D2137; --blue:#1565C0; --blue2:#1976D2; --sky:#E3F0FF;
  --gold:#D4A017; --goldf:#F5C842; --goldl:#FFF8E7;
  --red:#C62828; --green:#1B5E20; --green2:#2E7D32;
  --white:#FFFFFF; --cream:#FAFBFF; --gray:#F4F6F9; --txt:#1a1a2e; --mut:#5a6375;
  --sh1:0 4px 20px rgba(0,0,0,.08); --sh2:0 12px 40px rgba(0,0,0,.13);
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{font-family:'Nunito',sans-serif;color:var(--txt);background:var(--white);overflow-x:hidden}
a{text-decoration:none;color:inherit}
img{max-width:100%}
button,label{font-family:'Nunito',sans-serif;cursor:pointer}

/* ══════════════════════════════
   TOPBAR
══════════════════════════════ */
.topbar{
  background:var(--navy);
  padding:7px 40px;
  display:flex;justify-content:space-between;align-items:center;
  font-size:11.5px;color:rgba(255,255,255,.55);
}
.tb-left{display:flex;gap:20px;align-items:center}
.tb-right{display:flex;gap:18px;align-items:center}
.tb-right a{
  display:inline-flex;align-items:center;gap:5px;
  color:rgba(255,255,255,.75);font-weight:600;font-size:11.5px;
  transition:color .2s;
}
.tb-right a:hover{color:var(--goldf)}
.tb-right a.call-btn{
  background:var(--green2);color:#fff!important;
  padding:4px 12px;border-radius:20px;font-weight:700;
}
.tb-right a.call-btn:hover{background:#388e3c}

/* ══════════════════════════════
   NAVBAR
══════════════════════════════ */
.navbar{
  background:var(--white);
  padding:0 40px;
  display:flex;justify-content:space-between;align-items:center;
  position:sticky;top:0;z-index:900;
  box-shadow:0 2px 12px rgba(0,0,0,.09);
  border-bottom:3px solid var(--gold);
}
.nav-brand{display:flex;align-items:center;gap:14px;padding:10px 0;cursor:pointer;flex-shrink:0}
.brand-shield{
  width:54px;height:54px;border-radius:12px;
  background:linear-gradient(145deg,var(--navy),var(--blue));
  display:flex;align-items:center;justify-content:center;
  font-size:24px;border:2.5px solid var(--gold);flex-shrink:0;
}
.brand-text .b1{font-family:'Playfair Display',serif;font-size:16px;font-weight:700;color:var(--navy);line-height:1.15}
.brand-text .b2{font-size:10.5px;color:var(--mut);font-weight:600;margin-top:1px}
.brand-text .b3{font-size:10px;color:var(--gold);font-weight:700;letter-spacing:.5px}

.nav-links{list-style:none;display:flex;align-items:center;gap:2px}
.nav-links a{
  display:block;padding:9px 14px;font-size:13px;font-weight:700;
  color:var(--mut);border-radius:8px;cursor:pointer;transition:all .2s;
  position:relative;
}
.nav-links a:hover{color:var(--blue);background:var(--sky)}
.nav-links a.active{color:var(--blue)}
.nav-links a.active::after{
  content:'';position:absolute;bottom:-3px;left:10px;right:10px;
  height:3px;background:var(--gold);border-radius:2px 2px 0 0;
}
.nav-admit{
  background:linear-gradient(135deg,var(--blue),var(--blue2))!important;
  color:#fff!important;border-radius:25px!important;
  padding:9px 20px!important;
}
.nav-admit:hover{opacity:.9;transform:translateY(-1px)}
.hamburger{display:none;flex-direction:column;gap:5px;padding:6px;cursor:pointer}
.hamburger span{width:23px;height:2px;background:var(--navy);border-radius:2px;transition:.3s}

/* ══════════════════════════════
   PAGE SYSTEM
══════════════════════════════ */
.pg{display:none}
.pg.on{display:block;animation:fadeSlide .35s ease}
@keyframes fadeSlide{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}

/* ══════════════════════════════
   ANNOUNCEMENT POPUP
══════════════════════════════ */
.ann-overlay{
  position:fixed;inset:0;background:rgba(0,0,0,.6);
  z-index:9990;display:none;align-items:center;justify-content:center;
  backdrop-filter:blur(5px);
}
.ann-overlay.on{display:flex}
.ann-modal{
  background:var(--white);border-radius:20px;
  width:90%;max-width:430px;overflow:hidden;
  box-shadow:0 30px 80px rgba(0,0,0,.25);
  animation:modalPop .4s cubic-bezier(.34,1.56,.64,1);
}
.ann-top{background:linear-gradient(135deg,var(--red) 0%,#8B0000 100%);padding:20px 22px 18px;position:relative}
.ann-top h3{font-family:'Playfair Display',serif;font-size:22px;color:#fff;font-weight:700}
.ann-top p{font-size:11.5px;color:rgba(255,255,255,.7);margin-top:4px}
.ann-close{
  position:absolute;top:14px;right:14px;
  background:rgba(255,255,255,.18);border:none;color:#fff;
  width:28px;height:28px;border-radius:50%;font-size:15px;
  display:flex;align-items:center;justify-content:center;cursor:pointer;
}
.ann-close:hover{background:rgba(255,255,255,.3)}
.ann-body{padding:20px 22px}
.ann-offer-box{
  background:linear-gradient(135deg,#4A148C,#7B1FA2);
  border-radius:12px;padding:15px 16px;margin-bottom:14px;
}
.ann-offer-box .aot{font-size:14px;font-weight:800;color:var(--goldf);margin-bottom:6px}
.ann-offer-box p{font-size:12px;color:rgba(255,255,255,.88);line-height:1.75}
.ann-offer-box b{color:#fff}
.ann-alert{
  display:flex;gap:10px;align-items:center;
  background:#FFF3E0;border-left:3px solid #FF6F00;
  border-radius:8px;padding:10px 13px;margin-bottom:14px;
  font-size:12px;color:#BF360C;font-weight:700;
}
.ann-cta{
  width:100%;padding:13px;
  background:linear-gradient(135deg,var(--green),var(--green2));
  color:#fff;border:none;border-radius:10px;
  font-size:14px;font-weight:800;cursor:pointer;transition:all .25s;
}
.ann-cta:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(27,94,32,.35)}

/* ══════════════════════════════
   ADMISSION FORM POPUP
══════════════════════════════ */
.form-overlay{
  position:fixed;inset:0;background:rgba(0,0,0,.55);
  z-index:9989;display:none;align-items:center;justify-content:center;
  backdrop-filter:blur(4px);padding:14px;
}
.form-overlay.on{display:flex}
.form-modal{
  background:var(--white);border-radius:20px;
  width:100%;max-width:500px;max-height:93vh;overflow-y:auto;
  box-shadow:0 30px 80px rgba(0,0,0,.22);
  animation:modalPop .35s cubic-bezier(.34,1.56,.64,1);
}
.form-header{
  background:linear-gradient(135deg,var(--navy),var(--blue));
  padding:18px 22px;position:sticky;top:0;z-index:2;
  border-radius:20px 20px 0 0;
}
.form-header h3{font-family:'Playfair Display',serif;font-size:20px;color:#fff;font-weight:700}
.form-header p{font-size:11px;color:rgba(255,255,255,.6);margin-top:3px}
.fclose{
  position:absolute;top:14px;right:14px;
  background:rgba(255,255,255,.15);border:none;color:#fff;
  width:28px;height:28px;border-radius:50%;font-size:14px;
  display:flex;align-items:center;justify-content:center;cursor:pointer;
}
.fclose:hover{background:rgba(255,255,255,.3)}
.form-body{padding:20px 22px}
.frow{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.fg{margin-bottom:12px}
.fg label{display:block;font-size:10.5px;font-weight:800;color:var(--mut);margin-bottom:5px;text-transform:uppercase;letter-spacing:.6px}
.fg input,.fg select,.fg textarea{
  width:100%;padding:11px 13px;
  border:1.5px solid #E0E5EF;border-radius:9px;
  font-size:13px;font-family:'Nunito',sans-serif;
  color:var(--txt);outline:none;
  background:#FAFCFF;transition:all .2s;
}
.fg input:focus,.fg select:focus,.fg textarea:focus{border-color:var(--blue);box-shadow:0 0 0 3px rgba(21,101,192,.1)}
.fg textarea{resize:vertical;min-height:70px}
.f-btn{
  width:100%;padding:13px;
  background:linear-gradient(135deg,var(--green),var(--green2));
  color:#fff;border:none;border-radius:10px;
  font-size:14px;font-weight:800;transition:all .25s;margin-top:4px;
}
.f-btn:hover{transform:translateY(-2px);box-shadow:0 8px 22px rgba(27,94,32,.35)}
.f-note{text-align:center;font-size:11px;color:var(--mut);margin-top:8px}

/* ══════════════════════════════
   HERO / CAROUSEL
══════════════════════════════ */
.carousel{position:relative;height:90vh;min-height:500px;overflow:hidden}
.c-track{display:flex;height:100%;transition:transform .8s cubic-bezier(.77,0,.175,1)}
.slide{
  min-width:100%;height:100%;position:relative;
  display:flex;align-items:center;
}
.s1{background:linear-gradient(120deg,#0D2137 0%,#1565C0 60%,#0D3B6E 100%)}
.s2{background:linear-gradient(120deg,#1B2B1B 0%,#1B5E20 60%,#0a2e0f 100%)}
.s3{background:linear-gradient(120deg,#4A0E0E 0%,#C62828 60%,#7B0000 100%)}
.s-pattern{
  position:absolute;inset:0;
  background-image:
    radial-gradient(ellipse at 80% 50%, rgba(255,255,255,.07) 0%, transparent 60%),
    repeating-linear-gradient(45deg, transparent, transparent 40px, rgba(255,255,255,.02) 40px, rgba(255,255,255,.02) 41px);
}
.s-content{
  position:relative;z-index:2;
  padding:0 60px;max-width:780px;
}
.s-eyebrow{
  display:inline-flex;align-items:center;gap:8px;
  background:rgba(255,255,255,.12);border:1px solid rgba(255,255,255,.2);
  padding:6px 16px;border-radius:30px;
  font-size:11.5px;color:rgba(255,255,255,.85);font-weight:700;
  letter-spacing:1.2px;text-transform:uppercase;
  margin-bottom:20px;
}
.s-content h1{
  font-family:'Playfair Display',serif;
  font-size:52px;font-weight:800;color:#fff;
  line-height:1.1;margin-bottom:16px;
  text-shadow:0 4px 20px rgba(0,0,0,.3);
}
.s-content h1 em{color:var(--goldf);font-style:normal}
.s-content p{
  font-size:15.5px;color:rgba(255,255,255,.75);
  line-height:1.75;margin-bottom:28px;max-width:580px;
}
.s-actions{display:flex;gap:14px;flex-wrap:wrap}
.btn-primary{
  background:linear-gradient(135deg,var(--gold),var(--goldf));
  color:var(--navy);border:none;padding:14px 30px;
  border-radius:30px;font-size:14px;font-weight:800;
  transition:all .25s;cursor:pointer;
  box-shadow:0 6px 20px rgba(212,160,23,.4);
}
.btn-primary:hover{transform:translateY(-3px);box-shadow:0 12px 30px rgba(212,160,23,.5)}
.btn-outline{
  background:transparent;color:#fff;
  border:2px solid rgba(255,255,255,.4);
  padding:13px 28px;border-radius:30px;font-size:14px;font-weight:700;
  transition:all .25s;cursor:pointer;
}
.btn-outline:hover{background:rgba(255,255,255,.12);border-color:rgba(255,255,255,.8)}
.c-arrow{
  position:absolute;top:50%;transform:translateY(-50%);
  background:rgba(255,255,255,.13);backdrop-filter:blur(10px);
  border:1px solid rgba(255,255,255,.18);color:#fff;
  width:48px;height:48px;border-radius:50%;
  font-size:18px;z-index:5;transition:all .25s;
  display:flex;align-items:center;justify-content:center;cursor:pointer;
}
.c-arrow:hover{background:rgba(255,255,255,.28)}
.c-prev{left:20px}
.c-next{right:20px}
.c-dots{
  position:absolute;bottom:25px;left:50%;transform:translateX(-50%);
  display:flex;gap:8px;z-index:5;
}
.dot{width:8px;height:8px;border-radius:50%;background:rgba(255,255,255,.3);cursor:pointer;transition:all .3s}
.dot.on{background:var(--goldf);width:28px;border-radius:4px}

/* QUICK LINKS BAR — like DPS */
.quick-bar{
  background:var(--navy);
  display:flex;justify-content:center;gap:0;
  border-top:3px solid var(--gold);
}
.qb-item{
  display:flex;flex-direction:column;align-items:center;gap:5px;
  padding:16px 32px;cursor:pointer;
  border-right:1px solid rgba(255,255,255,.08);
  transition:background .2s;
  text-decoration:none;
}
.qb-item:last-child{border:none}
.qb-item:hover{background:rgba(255,255,255,.07)}
.qb-icon{font-size:22px}
.qb-label{font-size:11px;font-weight:700;color:rgba(255,255,255,.7);letter-spacing:.5px;text-transform:uppercase}

/* TICKER */
.ticker{background:var(--red);padding:9px 0;overflow:hidden;white-space:nowrap}
.ticker-inner{display:inline-flex;animation:ticker 25s linear infinite}
.t-item{display:inline-flex;align-items:center;gap:9px;padding:0 32px;font-size:12.5px;color:#fff;font-weight:600}
.t-badge{background:var(--goldf);color:var(--red);padding:2px 8px;border-radius:4px;font-size:10px;font-weight:800}
@keyframes ticker{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}

/* STATS */
.stats-row{
  background:var(--white);
  display:flex;justify-content:center;
  box-shadow:var(--sh1);
}
.stat{
  text-align:center;padding:24px 50px;
  border-right:1px solid #EEF0F5;
  opacity:0;transform:translateY(15px);transition:all .6s;
}
.stat.show{opacity:1;transform:translateY(0)}
.stat:last-child{border:none}
.stat-num{font-family:'Playfair Display',serif;font-size:38px;font-weight:700;color:var(--blue);line-height:1}
.stat-num span{color:var(--gold);font-size:28px}
.stat-label{font-size:11.5px;color:var(--mut);margin-top:4px;font-weight:600}

/* SECTIONS */
.section{padding:60px 40px;max-width:1140px;margin:0 auto}
.section-header{text-align:center;margin-bottom:40px}
.sec-badge{
  display:inline-block;background:var(--sky);color:var(--blue);
  padding:5px 14px;border-radius:20px;font-size:11px;font-weight:800;
  letter-spacing:1.5px;text-transform:uppercase;margin-bottom:10px;
}
.sec-title{font-family:'Playfair Display',serif;font-size:32px;font-weight:700;color:var(--navy);line-height:1.2}
.sec-title span{color:var(--blue)}
.sec-line{width:50px;height:3.5px;background:linear-gradient(90deg,var(--gold),var(--goldf));margin:12px auto 0;border-radius:2px}
.sec-sub{font-size:13.5px;color:var(--mut);margin-top:10px;max-width:550px;margin-left:auto;margin-right:auto;line-height:1.7}

/* WHY US */
.why-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
.why-card{
  background:var(--white);border-radius:16px;padding:26px 18px;
  text-align:center;border:1.5px solid #EEF0F5;
  box-shadow:var(--sh1);transition:all .35s;
  opacity:0;transform:translateY(22px);
}
.why-card.show{opacity:1;transform:translateY(0)}
.why-card:hover{border-color:var(--gold);transform:translateY(-7px);box-shadow:var(--sh2)}
.wc-icon{
  width:58px;height:58px;border-radius:14px;
  background:var(--sky);display:flex;align-items:center;justify-content:center;
  font-size:26px;margin:0 auto 14px;transition:background .3s;
}
.why-card:hover .wc-icon{background:var(--blue)}
.wc-title{font-size:13px;font-weight:800;color:var(--navy);margin-bottom:6px}
.wc-desc{font-size:11.5px;color:var(--mut);line-height:1.7}

/* ABOUT SECTION */
.about-wrap{background:var(--gray)}
.about-grid{display:grid;grid-template-columns:1fr 1.1fr;gap:50px;align-items:center}
.about-imgbox{
  border-radius:18px;aspect-ratio:4/3;
  background:linear-gradient(135deg,var(--sky),#C5D8FF);
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  gap:12px;border:2px dashed rgba(21,101,192,.2);
  position:relative;overflow:hidden;
}
.about-imgbox::before{
  content:'';position:absolute;bottom:-20px;right:-20px;
  width:120px;height:120px;background:rgba(21,101,192,.06);border-radius:50%;
}
.about-imgbox .ai{font-size:56px;opacity:.35}
.about-imgbox .at{font-size:12.5px;color:var(--mut)}
.about-text h3{font-family:'Playfair Display',serif;font-size:27px;font-weight:700;color:var(--navy);margin-bottom:14px;line-height:1.25}
.about-text p{font-size:13.5px;color:var(--mut);line-height:1.85;margin-bottom:11px}
.about-text p b{color:var(--blue)}
.check-list{display:flex;flex-direction:column;gap:9px;margin-top:14px}
.check-item{display:flex;align-items:center;gap:10px;font-size:13px;font-weight:600}
.check-dot{
  width:22px;height:22px;background:var(--green2);border-radius:6px;
  display:flex;align-items:center;justify-content:center;
  color:#fff;font-size:10px;flex-shrink:0;
}
.dir-card{
  display:flex;gap:14px;align-items:flex-start;
  background:linear-gradient(135deg,var(--navy),var(--blue));
  border-radius:14px;padding:18px;margin-top:18px;
}
.dir-photo{
  width:56px;height:56px;border-radius:50%;background:rgba(255,255,255,.15);
  border:2.5px solid var(--goldf);display:flex;align-items:center;justify-content:center;
  font-size:26px;flex-shrink:0;
}
.dir-info .dn{font-weight:800;font-size:14px;color:#fff}
.dir-info .dr{font-size:11.5px;color:var(--goldf);font-weight:700;margin-top:2px}
.dir-info .dq{font-size:11.5px;color:rgba(255,255,255,.65);margin-top:5px;line-height:1.65;font-style:italic}

/* GALLERY */
.gal-section{background:linear-gradient(160deg,var(--navy) 0%,#0a2444 100%);padding:60px 40px}
.gal-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;max-width:1140px;margin:28px auto 0}
.gal-item{
  aspect-ratio:4/3;border-radius:12px;overflow:hidden;position:relative;
  cursor:pointer;background:rgba(255,255,255,.06);
  border:1.5px solid rgba(255,255,255,.08);
  display:flex;align-items:center;justify-content:center;
  transition:all .3s;
}
.gal-item.big{grid-column:span 2;grid-row:span 2;aspect-ratio:auto}
.gal-item:hover{border-color:var(--gold);transform:scale(1.03);box-shadow:0 15px 40px rgba(0,0,0,.4)}
.gal-item img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}
.gal-ph{display:flex;flex-direction:column;align-items:center;gap:6px}
.gal-ph span{font-size:26px;opacity:.4}
.gal-ph small{font-size:10px;color:rgba(255,255,255,.35);text-align:center}
.gal-add{
  display:block;margin:18px auto 0;
  background:linear-gradient(135deg,var(--gold),var(--goldf));
  color:var(--navy);border:none;padding:11px 26px;border-radius:30px;
  font-size:13px;font-weight:800;transition:all .25s;
}
.gal-add:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(212,160,23,.4)}

/* LIGHTBOX */
.lbox{position:fixed;inset:0;background:rgba(0,0,0,.93);z-index:9980;display:none;align-items:center;justify-content:center}
.lbox.on{display:flex}
.lbox img{max-width:90vw;max-height:85vh;border-radius:10px}
.lbox-x{position:absolute;top:18px;right:20px;background:rgba(255,255,255,.1);border:none;color:#fff;width:38px;height:38px;border-radius:50%;font-size:18px;display:flex;align-items:center;justify-content:center;cursor:pointer}

/* TESTIMONIALS */
.testi-section{background:var(--gray);padding:60px 40px}
.testi-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;max-width:1140px;margin:30px auto 0}
.testi-card{
  background:var(--white);border-radius:16px;padding:24px 20px;
  box-shadow:var(--sh1);border:1.5px solid #EEF0F5;
  transition:all .35s;opacity:0;transform:translateY(20px);
}
.testi-card.show{opacity:1;transform:translateY(0)}
.testi-card:hover{transform:translateY(-6px);box-shadow:var(--sh2);border-color:var(--gold)}
.t-quote{font-size:36px;color:var(--gold);line-height:1;margin-bottom:8px;font-family:Georgia,serif}
.t-text{font-size:12.5px;color:var(--mut);line-height:1.85;margin-bottom:16px;font-style:italic}
.t-stars{color:var(--gold);letter-spacing:2px;font-size:13px;margin-bottom:12px}
.t-author{display:flex;align-items:center;gap:11px}
.t-avatar{width:40px;height:40px;border-radius:50%;background:linear-gradient(135deg,var(--blue),var(--navy));display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}
.t-name{font-size:13px;font-weight:800;color:var(--navy)}
.t-role{font-size:10.5px;color:var(--mut);margin-top:1px}

/* EVENTS */
.ev-section{background:var(--white);padding:60px 40px}
.ev-wrap{display:grid;grid-template-columns:1fr 1fr;gap:28px;max-width:1140px;margin:30px auto 0}
.cal-box{background:var(--white);border-radius:16px;padding:20px;box-shadow:var(--sh1);border:1.5px solid #EEF0F5}
.cal-nav-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:16px}
.cal-month{font-family:'Playfair Display',serif;font-size:18px;font-weight:700;color:var(--navy)}
.cal-btn{background:var(--sky);border:none;width:30px;height:30px;border-radius:50%;font-size:13px;cursor:pointer;color:var(--blue);display:flex;align-items:center;justify-content:center;transition:all .2s}
.cal-btn:hover{background:var(--blue);color:#fff}
.cal-dnames{display:grid;grid-template-columns:repeat(7,1fr);margin-bottom:6px}
.cal-dn{text-align:center;font-size:9.5px;font-weight:800;color:var(--mut);padding:3px;text-transform:uppercase}
.cal-days{display:grid;grid-template-columns:repeat(7,1fr);gap:3px}
.cday{text-align:center;padding:7px 3px;font-size:11.5px;border-radius:8px;cursor:pointer;transition:all .2s}
.cday:hover{background:var(--sky);color:var(--blue)}
.cday.today{background:var(--blue);color:#fff;font-weight:800}
.cday.has-ev{background:var(--goldl);color:#7B4F00;font-weight:800;position:relative}
.cday.has-ev::after{content:'';position:absolute;bottom:2px;left:50%;transform:translateX(-50%);width:4px;height:4px;border-radius:50%;background:var(--gold)}
.cday.empty{color:#DDD;cursor:default}
.cday.empty:hover{background:transparent}
.ev-list{display:flex;flex-direction:column;gap:12px}
.ev-card{
  display:flex;gap:14px;align-items:flex-start;
  background:var(--white);border-radius:12px;padding:14px 16px;
  border:1.5px solid #EEF0F5;box-shadow:var(--sh1);transition:all .25s;
}
.ev-card:hover{border-color:var(--gold);transform:translateX(5px)}
.ev-date{
  border-radius:10px;padding:8px 10px;text-align:center;
  flex-shrink:0;min-width:50px;background:var(--blue);
}
.ev-date .ed{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:#fff;line-height:1}
.ev-date .em{font-size:8.5px;font-weight:800;color:rgba(255,255,255,.75);letter-spacing:.5px}
.ev-info .et{font-size:13px;font-weight:800;color:var(--navy);margin-bottom:3px}
.ev-info .ed2{font-size:11px;color:var(--mut);line-height:1.5}
.ev-tag{display:inline-block;background:var(--sky);color:var(--blue);font-size:9px;font-weight:800;padding:2px 8px;border-radius:8px;margin-top:5px;letter-spacing:.5px}

/* PAGE HERO */
.pg-hero{
  background:linear-gradient(135deg,var(--navy) 0%,var(--blue) 100%);
  padding:52px 40px;text-align:center;position:relative;overflow:hidden;
}
.pg-hero::before{content:'';position:absolute;inset:0;background-image:radial-gradient(circle,rgba(255,255,255,.04) 1px,transparent 1px);background-size:25px 25px}
.pg-hero h2{font-family:'Playfair Display',serif;font-size:36px;font-weight:700;color:#fff;position:relative}
.pg-hero p{font-size:13.5px;color:rgba(255,255,255,.6);margin-top:8px;position:relative}
.pg-hero .bread{
  display:flex;align-items:center;gap:6px;justify-content:center;
  font-size:11.5px;color:rgba(255,255,255,.5);margin-bottom:12px;position:relative;
}
.pg-hero .bread span{color:var(--goldf);font-weight:700}

/* ABOUT PAGE */
.vm-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;max-width:1140px;margin:0 auto}
.vm-card{border-radius:16px;padding:26px 24px}
.vm-card.v1{background:linear-gradient(135deg,var(--navy),var(--blue));color:#fff}
.vm-card.v2{background:var(--white);border:1.5px solid #EEF0F5;box-shadow:var(--sh1)}
.vm-card h4{font-family:'Playfair Display',serif;font-size:20px;font-weight:700;margin-bottom:10px}
.vm-card.v1 h4{color:var(--goldf)}
.vm-card.v2 h4{color:var(--navy)}
.vm-card p{font-size:13px;line-height:1.85}
.vm-card.v1 p{color:rgba(255,255,255,.72)}
.vm-card.v2 p{color:var(--mut)}
.vm-icon{font-size:32px;margin-bottom:12px;display:block}

/* TEACHER SECTION */
.team-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;max-width:1140px;margin:0 auto}
.tc{
  background:var(--white);border-radius:16px;padding:26px 18px 20px;
  text-align:center;border:1.5px solid #EEF0F5;
  box-shadow:var(--sh1);transition:all .3s;position:relative;
}
.tc:hover{border-color:var(--gold);transform:translateY(-6px);box-shadow:var(--sh2)}
.tc-circle{
  width:88px;height:88px;border-radius:50%;overflow:hidden;position:relative;
  border:3px solid var(--gold);background:var(--sky);
  display:flex;align-items:center;justify-content:center;
  font-size:34px;margin:0 auto 6px;
}
.tc-circle img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;border-radius:50%;display:block}
.tc-upload{
  display:inline-block;background:var(--blue);color:#fff;
  padding:6px 14px;border-radius:20px;font-size:11.5px;font-weight:800;
  margin-bottom:10px;cursor:pointer;transition:all .2s;
}
.tc-upload:hover{background:var(--blue2);transform:translateY(-1px)}
.tc-name{font-family:'Playfair Display',serif;font-size:16px;font-weight:700;color:var(--navy)}
.tc-post{font-size:11.5px;color:var(--gold);font-weight:800;margin-top:3px}
.tc-bio{font-size:11.5px;color:var(--mut);margin-top:7px;line-height:1.65}
.add-tc{
  display:block;margin:22px auto 0;
  background:linear-gradient(135deg,var(--blue),var(--blue2));
  color:#fff;border:none;padding:11px 26px;border-radius:30px;
  font-size:13px;font-weight:800;transition:all .25s;
}
.add-tc:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(21,101,192,.35)}

/* ADMISSIONS */
.adm-hero{
  background:linear-gradient(135deg,var(--red) 0%,#7B0000 100%);
  padding:52px 40px;text-align:center;
}
.adm-badge{
  display:inline-block;background:var(--goldf);color:var(--red);
  padding:5px 16px;border-radius:20px;font-size:11px;font-weight:800;
  letter-spacing:1px;text-transform:uppercase;margin-bottom:13px;
}
.adm-hero h2{font-family:'Playfair Display',serif;font-size:36px;font-weight:700;color:#fff}
.adm-hero p{font-size:14px;color:rgba(255,255,255,.7);margin-top:8px}
.open-adm-btn{
  display:inline-flex;align-items:center;gap:8px;
  background:linear-gradient(135deg,var(--gold),var(--goldf));color:var(--navy);
  border:none;padding:14px 32px;border-radius:30px;font-size:15px;font-weight:800;
  cursor:pointer;margin-top:20px;transition:all .25s;
  box-shadow:0 6px 20px rgba(212,160,23,.4);
}
.open-adm-btn:hover{transform:translateY(-3px);box-shadow:0 12px 30px rgba(212,160,23,.5)}
.proc-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px;max-width:1140px;margin:0 auto}
.proc-card{
  background:var(--white);border-radius:14px;padding:24px 16px;
  text-align:center;border:1.5px solid #EEF0F5;
  position:relative;transition:all .3s;box-shadow:var(--sh1);
}
.proc-card:hover{border-color:var(--blue);transform:translateY(-5px)}
.proc-num{
  position:absolute;top:-13px;left:50%;transform:translateX(-50%);
  width:27px;height:27px;background:var(--blue);color:#fff;
  border-radius:50%;font-size:12px;font-weight:800;
  display:flex;align-items:center;justify-content:center;
  border:3px solid var(--gray);
}
.proc-ico{font-size:30px;margin-bottom:10px}
.proc-t{font-size:13.5px;font-weight:800;color:var(--navy);margin-bottom:5px}
.proc-d{font-size:11.5px;color:var(--mut);line-height:1.65}
.cls-table{width:100%;border-collapse:collapse;border-radius:14px;overflow:hidden;box-shadow:var(--sh1)}
.cls-table th{background:var(--blue);color:#fff;padding:13px 16px;font-size:13px;font-weight:800;text-align:left}
.cls-table td{padding:11px 16px;font-size:12.5px;border-bottom:1px solid #EEF0F5}
.cls-table tr:last-child td{border:none}
.cls-table tr:nth-child(even) td{background:var(--sky)}
.open-badge{background:#E8F5E9;color:#2E7D32;padding:3px 10px;border-radius:12px;font-size:10.5px;font-weight:800}
.offer-strip{
  background:linear-gradient(135deg,#4A148C,#7B1FA2);
  border-radius:16px;padding:28px 30px;
  display:flex;align-items:center;gap:24px;
  max-width:1140px;margin:0 auto;
  box-shadow:0 8px 30px rgba(74,20,140,.3);
}
.offer-strip h3{font-family:'Playfair Display',serif;font-size:23px;font-weight:700;color:var(--goldf);margin-bottom:8px}
.offer-strip p{font-size:13px;color:rgba(255,255,255,.85);line-height:1.8}
.offer-strip p b{color:#fff}
.offer-dt{background:rgba(255,255,255,.12);border:1.5px solid rgba(245,200,66,.3);border-radius:12px;padding:14px 20px;text-align:center;flex-shrink:0}
.offer-dt .o1{font-size:9px;color:rgba(255,255,255,.5);letter-spacing:1px;text-transform:uppercase;display:block}
.offer-dt .o2{font-family:'Playfair Display',serif;font-size:24px;font-weight:700;color:var(--goldf);display:block;line-height:1.15}
.docs-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;max-width:1140px;margin:0 auto}
.doc-item{background:var(--white);border:1.5px solid #EEF0F5;border-radius:12px;padding:14px 16px;display:flex;gap:12px;align-items:center;transition:all .25s;box-shadow:var(--sh1)}
.doc-item:hover{border-color:var(--gold);transform:translateY(-2px)}
.doc-ico{font-size:24px}
.doc-t{font-weight:800;font-size:13px}
.doc-s{font-size:11px;color:var(--mut);margin-top:2px}

/* CONTACT */
.con-grid{display:grid;grid-template-columns:1fr 1.15fr;gap:36px;max-width:1140px;margin:0 auto}
.ci-card{display:flex;gap:14px;align-items:flex-start;margin-bottom:13px;padding:14px 16px;background:var(--white);border-radius:12px;border:1.5px solid #EEF0F5;box-shadow:var(--sh1);transition:all .25s}
.ci-card:hover{border-color:var(--gold)}
.ci-icon{width:44px;height:44px;background:var(--blue);border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
.ci-label{font-size:9.5px;color:var(--mut);text-transform:uppercase;font-weight:800;letter-spacing:.8px}
.ci-val{font-size:13.5px;font-weight:800;margin-top:2px}
.ci-sub{font-size:11px;color:var(--mut);margin-top:1px}
.map-box{background:var(--sky);border-radius:14px;min-height:160px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:9px;margin-bottom:15px;border:2px dashed rgba(21,101,192,.2)}
.cf-title{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:var(--navy);margin-bottom:18px}
.cf-btn{width:100%;padding:13px;background:linear-gradient(135deg,var(--green),var(--green2));color:#fff;border:none;border-radius:10px;font-size:14px;font-weight:800;cursor:pointer;transition:all .25s}
.cf-btn:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(27,94,32,.35)}

/* FOOTER */
.footer{background:var(--navy);padding:50px 40px 0}
.foot-grid{display:grid;grid-template-columns:1.6fr 1fr 1fr;gap:40px;max-width:1140px;margin:0 auto;padding-bottom:32px;border-bottom:1px solid rgba(255,255,255,.07)}
.fn{font-family:'Playfair Display',serif;font-size:19px;font-weight:700;color:#fff;margin-bottom:5px}
.fl{font-size:11px;color:rgba(255,255,255,.35);margin-bottom:13px}
.fd{font-size:12.5px;color:rgba(255,255,255,.5);line-height:1.8}
.fh{font-size:10px;font-weight:800;color:var(--goldf);letter-spacing:1.8px;text-transform:uppercase;margin-bottom:14px}
.flinks{list-style:none;display:flex;flex-direction:column;gap:8px}
.flinks li a{font-size:13px;color:rgba(255,255,255,.5);cursor:pointer;transition:color .2s;display:flex;align-items:center;gap:6px}
.flinks li a:hover{color:var(--goldf)}
.fcontact{display:flex;flex-direction:column;gap:8px}
.fcontact a{font-size:12.5px;color:rgba(255,255,255,.5);transition:color .2s}
.fcontact a:hover{color:var(--goldf)}
.foot-bot{max-width:1140px;margin:0 auto;padding:15px 0;display:flex;justify-content:space-between;font-size:11px;color:rgba(255,255,255,.25)}

/* FLOATING WA */
.wa-float{position:fixed;bottom:26px;right:26px;width:54px;height:54px;background:#25D366;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:25px;text-decoration:none;box-shadow:0 6px 20px rgba(37,211,102,.5);z-index:888;transition:all .3s;animation:bounceIn .8s 2s both}
.wa-float:hover{transform:scale(1.12)}

/* TOAST */
.toast{position:fixed;bottom:26px;left:50%;transform:translateX(-50%);background:var(--green);color:#fff;padding:12px 22px;border-radius:10px;font-size:13px;font-weight:700;box-shadow:var(--sh2);display:none;z-index:9999;white-space:nowrap}

/* ANIMATIONS */
@keyframes modalPop{from{opacity:0;transform:scale(.85)}to{opacity:1;transform:scale(1)}}
@keyframes bounceIn{0%{opacity:0;transform:scale(.3)}55%{opacity:1;transform:scale(1.1)}75%{transform:scale(.95)}100%{transform:scale(1)}}

/* MOBILE */
@media(max-width:768px){
  .topbar{padding:5px 14px;flex-direction:column;gap:3px;font-size:10px;text-align:center}
  .navbar{padding:0 14px;flex-wrap:wrap}
  .hamburger{display:flex}
  .nav-links{display:none;width:100%;flex-direction:column;padding:6px 0 12px}
  .nav-links.open{display:flex}
  .quick-bar{flex-wrap:wrap}
  .qb-item{padding:12px 18px}
  .stats-row{flex-wrap:wrap}
  .stat{width:50%;border-right:none;border-bottom:1px solid #EEF0F5;padding:16px 10px}
  .s-content{padding:0 24px}
  .s-content h1{font-size:30px}
  .why-grid,.testi-grid,.team-grid,.proc-grid,.docs-grid{grid-template-columns:1fr 1fr}
  .about-grid,.vm-grid,.ev-wrap,.con-grid,.foot-grid{grid-template-columns:1fr}
  .gal-grid{grid-template-columns:1fr 1fr}
  .gal-item.big{grid-column:1;grid-row:1}
  .offer-strip{flex-direction:column}
  .frow{grid-template-columns:1fr}
}
</style>
</head>
<body>

<!-- ══════════ ANNOUNCEMENT POPUP ══════════ -->
<div class="ann-overlay" id="annPop">
  <div class="ann-modal">
    <div class="ann-top">
      <h3>🌟 Admission Open 2026–27</h3>
      <p>आवासीय न्यू मॉडर्न इंग्लिश स्कूल, मोहनपुर, सहरसा</p>
      <button class="ann-close" onclick="closeAnn()">✕</button>
    </div>
    <div class="ann-body">
      <div class="ann-offer-box">
        <div class="aot">🎁 Early Bird Special Offer</div>
        <p><b>10 अप्रैल 2026 से पहले</b> नामांकन पर<br>
        ✨ प्रवेश शुल्क <b>पूर्णतः निःशुल्क!</b><br>
        ⭐ पहले आएं — <b>ज्यादा छूट पाएं!</b></p>
      </div>
      <div class="ann-alert">
        ⚠️ सीमित सीटें उपलब्ध हैं! &nbsp;
        <a href="tel:+919113788228" style="color:var(--green2)">📞 9113788228 पर Call करें</a>
      </div>
      <button class="ann-cta" onclick="closeAnn();openForm()">📋 प्रवेश फॉर्म भरें →</button>
    </div>
  </div>
</div>

<!-- ══════════ FORM POPUP ══════════ -->
<div class="form-overlay" id="formPop">
  <div class="form-modal">
    <div class="form-header" style="position:relative">
      <h3>📋 प्रवेश फॉर्म — 2026–27</h3>
      <p>न्यू मॉडर्न इंग्लिश स्कूल, मोहनपुर, सहरसा, बिहार</p>
      <button class="fclose" onclick="closeForm()">✕</button>
    </div>
    <div class="form-body">
      <div class="frow">
        <div class="fg"><label>अभिभावक का नाम *</label><input type="text" id="fn-name" placeholder="पूरा नाम"></div>
        <div class="fg"><label>मोबाइल नंबर *</label><input type="tel" id="fn-phone" placeholder="10 अंक"></div>
      </div>
      <div class="fg"><label>बच्चे का पूरा नाम *</label><input type="text" id="fn-child" placeholder="बच्चे का नाम"></div>
      <div class="frow">
        <div class="fg"><label>जन्म तिथि</label><input type="date" id="fn-dob"></div>
        <div class="fg"><label>कक्षा चाहिए *</label>
          <select id="fn-class">
            <option value="">-- कक्षा चुनें --</option>
            <option>नर्सरी</option><option>LKG</option><option>UKG</option>
            <option>कक्षा 1</option><option>कक्षा 2</option><option>कक्षा 3</option>
            <option>कक्षा 4</option><option>कक्षा 5</option><option>कक्षा 6</option>
            <option>कक्षा 7</option><option>कक्षा 8</option>
          </select>
        </div>
      </div>
      <div class="fg"><label>पता</label><input type="text" id="fn-addr" placeholder="गांव / मोहल्ला, जिला"></div>
      <div class="fg"><label>संदेश / सवाल</label><textarea id="fn-msg" placeholder="कोई सवाल हो तो लिखें..."></textarea></div>
      <button class="f-btn" onclick="submitAdmForm()">💬 WhatsApp पर फॉर्म भेजें →</button>
      <p class="f-note">WhatsApp खुलेगा — सिर्फ Send दबाएं ✅</p>
    </div>
  </div>
</div>

<!-- ══════════ TOPBAR ══════════ -->
<div class="topbar">
  <div class="tb-left">
    <span>📜 Reg: SAH-PVT SCHOOL/NMES-0180/2020</span>
    <span>|</span>
    <span>📍 मोहनपुर, नौहट्टा, सहरसा, बिहार</span>
  </div>
  <div class="tb-right">
    <a href="tel:+919113788228" class="call-btn">📞 9113788228 — Call Now</a>
    <a href="https://wa.me/919113788228" target="_blank">💬 WhatsApp</a>
  </div>
</div>

<!-- ══════════ NAVBAR ══════════ -->
<nav class="navbar">
  <div class="nav-brand" onclick="showPage('home')">
    <div class="brand-shield">📚</div>
    <div class="brand-text">
      <div class="b1">New Modern English School</div>
      <div class="b2">न्यू मॉडर्न इंग्लिश स्कूल</div>
      <div class="b3">मोहनपुर, नौहट्टा, सहरसा</div>
    </div>
  </div>
  <div class="hamburger" onclick="toggleMob()">
    <span></span><span></span><span></span>
  </div>
  <ul class="nav-links" id="navLinks">
    <li><a class="active" onclick="showPage('home',this)">Home</a></li>
    <li><a onclick="showPage('about',this)">About Us</a></li>
    <li><a onclick="showPage('admissions',this)">Admissions</a></li>
    <li><a onclick="showPage('contact',this)">Contact</a></li>
    <li><a class="nav-admit" onclick="openForm()">Apply Now →</a></li>
  </ul>
</nav>

<!-- ══════════════════════════════════════
     HOME PAGE
══════════════════════════════════════ -->
<div id="home" class="pg on">

  <!-- CAROUSEL -->
  <div class="carousel">
    <div class="c-track" id="cTrack">

      <!-- Slide 1 -->
      <div class="slide s1">
        <div class="s-pattern"></div>
        <div class="s-content">
          <div class="s-eyebrow">🏆 11 Years of Excellence — Kosi Region, Bihar</div>
          <h1>Nurturing <em>Bright Futures</em><br>Since 2015</h1>
          <p>आधुनिक शिक्षा, अनुशासन और नैतिक मूल्यों के साथ<br>हर बच्चे की प्रतिभा को निखारा जाता है।</p>
          <div class="s-actions">
            <button class="btn-primary" onclick="openForm()">📋 Apply for Admission →</button>
            <button class="btn-outline" onclick="showPage('about')">Know More</button>
          </div>
        </div>
      </div>

      <!-- Slide 2 -->
      <div class="slide s2">
        <div class="s-pattern"></div>
        <div class="s-content">
          <div class="s-eyebrow">📚 English Medium | Nursery to Class 8</div>
          <h1>Concept Clear <em>Teaching</em><br>Every Subject, Every Day</h1>
          <p>हर विषय को जड़ से समझाना हमारी प्राथमिकता।<br>अनुभवी शिक्षकों की देखरेख में बेहतरीन शिक्षा।</p>
          <div class="s-actions">
            <button class="btn-primary" onclick="openForm()">Enroll Now</button>
            <button class="btn-outline" onclick="window.location.href='tel:+919113788228'">📞 Call Us</button>
          </div>
        </div>
      </div>

      <!-- Slide 3 -->
      <div class="slide s3">
        <div class="s-pattern"></div>
        <div class="s-content">
          <div class="s-eyebrow">🎁 Limited Time — Free Admission Offer</div>
          <h1>Enroll Before <em>10 April</em> —<br>Admission Free!</h1>
          <p>Early Bird Special Offer — पहले आएं, ज्यादा छूट पाएं!<br>⚠️ सीमित सीटें — आज ही संपर्क करें।</p>
          <div class="s-actions">
            <button class="btn-primary" onclick="openForm()">📋 Fill Form Now →</button>
            <button class="btn-outline" onclick="window.open('https://wa.me/919113788228','_blank')">💬 WhatsApp</button>
          </div>
        </div>
      </div>

    </div>
    <button class="c-arrow c-prev" onclick="moveSlide(-1)">❮</button>
    <button class="c-arrow c-next" onclick="moveSlide(1)">❯</button>
    <div class="c-dots" id="cDots">
      <div class="dot on" onclick="goSlide(0)"></div>
      <div class="dot" onclick="goSlide(1)"></div>
      <div class="dot" onclick="goSlide(2)"></div>
    </div>
  </div>

  <!-- QUICK BAR — DPS Style -->
  <div class="quick-bar">
    <a class="qb-item" href="tel:+919113788228">
      <div class="qb-icon">📞</div>
      <div class="qb-label">Call Now</div>
    </a>
    <div class="qb-item" onclick="openForm()">
      <div class="qb-icon">📋</div>
      <div class="qb-label">Admission</div>
    </div>
    <div class="qb-item" onclick="showPage('about')">
      <div class="qb-icon">🏫</div>
      <div class="qb-label">About Us</div>
    </div>
    <a class="qb-item" href="https://wa.me/919113788228" target="_blank">
      <div class="qb-icon">💬</div>
      <div class="qb-label">WhatsApp</div>
    </a>
    <div class="qb-item" onclick="showPage('contact')">
      <div class="qb-icon">📍</div>
      <div class="qb-label">Location</div>
    </div>
  </div>

  <!-- TICKER -->
  <div class="ticker">
    <div class="ticker-inner">
      <div class="t-item"><span class="t-badge">NEW</span> 🌟 Admission Open 2026–27 — 10 अप्रैल से पहले प्रवेश निःशुल्क! ⚠️ सीमित सीटें</div>
      <div class="t-item"><span class="t-badge">CALL</span> 📞 9113788228 पर अभी Call करें | 💬 WhatsApp पर संदेश करें</div>
      <div class="t-item"><span class="t-badge">NEW</span> 🌟 Admission Open 2026–27 — 10 अप्रैल से पहले प्रवेश निःशुल्क! ⚠️ सीमित सीटें</div>
      <div class="t-item"><span class="t-badge">CALL</span> 📞 9113788228 पर अभी Call करें | 💬 WhatsApp पर संदेश करें</div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-row" id="statsRow">
    <div class="stat"><div class="stat-num">11<span>+</span></div><div class="stat-label">Years of Excellence</div></div>
    <div class="stat"><div class="stat-num">500<span>+</span></div><div class="stat-label">Students Mentored</div></div>
    <div class="stat"><div class="stat-num">10<span>+</span></div><div class="stat-label">Expert Teachers</div></div>
    <div class="stat"><div class="stat-num">Nur<span>–8</span></div><div class="stat-label">Classes Available</div></div>
  </div>

  <!-- WHY US -->
  <div style="background:var(--gray);padding:60px 0">
    <div class="section" style="padding-top:0;padding-bottom:0">
      <div class="section-header">
        <div class="sec-badge">Our Highlights</div>
        <div class="sec-title">Why Choose <span>New Modern English School?</span></div>
        <div class="sec-line"></div>
        <div class="sec-sub">11 वर्षों के अनुभव के साथ हम बच्चों को एक बेहतरीन भविष्य देने के लिए प्रतिबद्ध हैं।</div>
      </div>
      <div class="why-grid" id="whyGrid">
        <div class="why-card"><div class="wc-icon">📖</div><div class="wc-title">Concept Clear Teaching</div><div class="wc-desc">हर विषय को जड़ से समझाना — रटने पर नहीं, समझने पर जोर।</div></div>
        <div class="why-card"><div class="wc-icon">👨‍🏫</div><div class="wc-title">Experienced Faculty</div><div class="wc-desc">समर्पित और प्रशिक्षित शिक्षक जो बच्चों को प्रेरित करते हैं।</div></div>
        <div class="why-card"><div class="wc-icon">🗣️</div><div class="wc-title">Spoken English Daily</div><div class="wc-desc">रोज़ अभ्यास से English communication में आत्मविश्वास।</div></div>
        <div class="why-card"><div class="wc-icon">📊</div><div class="wc-title">Regular Assessments</div><div class="wc-desc">नियमित test और Progress Report से parents को हमेशा अपडेट।</div></div>
        <div class="why-card"><div class="wc-icon">⚽</div><div class="wc-title">Sports & Activities</div><div class="wc-desc">शारीरिक विकास के लिए खेल और सांस्कृतिक गतिविधियाँ।</div></div>
        <div class="why-card"><div class="wc-icon">🛡️</div><div class="wc-title">Safe Campus</div><div class="wc-desc">स्वच्छ, सुरक्षित और अनुशासित परिसर — आपके बच्चे की सुरक्षा।</div></div>
        <div class="why-card"><div class="wc-icon">🏛️</div><div class="wc-title">Moral Values</div><div class="wc-desc">संस्कार और नैतिक मूल्यों पर आधारित शिक्षण पद्धति।</div></div>
        <div class="why-card"><div class="wc-icon">🏠</div><div class="wc-title">Residential Facility</div><div class="wc-desc">आवासीय सुविधा उपलब्ध — घर जैसा माहौल।</div></div>
      </div>
    </div>
  </div>

  <!-- ABOUT PREVIEW -->
  <div class="about-wrap">
    <div class="section">
      <div class="about-grid">
        <div class="about-imgbox">
          <div class="ai">🏫</div>
          <div class="at">School Campus — Mohanpur, Saharsa</div>
        </div>
        <div class="about-text">
          <h3>Kosi Region का विश्वसनीय शिक्षण संस्थान</h3>
          <p>आवासीय न्यू मॉडर्न इंग्लिश स्कूल 2015 से <b>बिहार सरकार द्वारा मान्यता प्राप्त</b> विद्यालय है जो मोहनपुर, नौहट्टा, सहरसा में स्थित है।</p>
          <p>हमारा मानना है कि शिक्षा केवल किताबों तक सीमित नहीं होनी चाहिए — बच्चों में <b>आत्मविश्वास, नैतिक मूल्य और व्यावहारिक कौशल</b> का विकास उतना ही जरूरी है।</p>
          <div class="check-list">
            <div class="check-item"><div class="check-dot">✓</div>Nursery to Class 8 — English Medium</div>
            <div class="check-item"><div class="check-dot">✓</div>11 Years of Successful Academic Journey</div>
            <div class="check-item"><div class="check-dot">✓</div>Reg: SAH-PVT SCHOOL/NMES-0180/2020</div>
            <div class="check-item"><div class="check-dot">✓</div>Residential Facility Available</div>
          </div>
          <div class="dir-card">
            <div class="dir-photo">👨‍💼</div>
            <div class="dir-info">
              <div class="dn">Sindhu Kumar Singh</div>
              <div class="dr">Director, NMES</div>
              <div class="dq">"हर बच्चे में एक असाधारण प्रतिभा छुपी है — हमारा काम उसे निखारना है।"</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- GALLERY -->
  <div class="gal-section">
    <div style="max-width:1140px;margin:0 auto">
      <div class="section-header">
        <div class="sec-badge" style="background:rgba(255,255,255,.1);color:rgba(255,255,255,.8)">School Life</div>
        <div class="sec-title" style="color:#fff">Our <span style="color:var(--goldf)">Gallery</span></div>
        <div class="sec-line"></div>
        <p style="color:rgba(255,255,255,.45);font-size:12px;margin-top:9px">📸 "फोटो जोड़ें" button से असली तस्वीरें upload करें</p>
      </div>
    </div>
    <div class="gal-grid" id="galGrid">
      <div class="gal-item big"><div class="gal-ph"><span>🏫</span><small>School Building</small></div></div>
      <div class="gal-item"><div class="gal-ph"><span>📚</span><small>Classroom</small></div></div>
      <div class="gal-item"><div class="gal-ph"><span>🎌</span><small>Independence Day</small></div></div>
      <div class="gal-item"><div class="gal-ph"><span>⚽</span><small>Sports</small></div></div>
      <div class="gal-item"><div class="gal-ph"><span>🎭</span><small>Cultural Event</small></div></div>
      <div class="gal-item"><div class="gal-ph"><span>🏆</span><small>Prize Distribution</small></div></div>
    </div>
    <input type="file" id="galInput" accept="image/*" multiple style="display:none" onchange="addGalPics(event)">
    <div style="text-align:center">
      <button class="gal-add" onclick="document.getElementById('galInput').click()">📸 फोटो जोड़ें</button>
    </div>
  </div>

  <!-- TESTIMONIALS -->
  <div class="testi-section">
    <div style="max-width:1140px;margin:0 auto">
      <div class="section-header">
        <div class="sec-badge">Parent Reviews</div>
        <div class="sec-title">What <span>Parents Say</span></div>
        <div class="sec-line"></div>
      </div>
    </div>
    <div class="testi-grid" id="testiGrid">
      <div class="testi-card">
        <div class="t-quote">"</div>
        <div class="t-stars">★★★★★</div>
        <div class="t-text">मेरे बेटे को यहाँ आकर बहुत फायदा हुआ। Spoken English में जबरदस्त सुधार आया। शिक्षक बहुत समर्पित हैं।</div>
        <div class="t-author"><div class="t-avatar">👩</div><div><div class="t-name">सुनीता देवी</div><div class="t-role">Mother of Class 5 Student</div></div></div>
      </div>
      <div class="testi-card">
        <div class="t-quote">"</div>
        <div class="t-stars">★★★★★</div>
        <div class="t-text">बच्चों का सर्वांगीण विकास यहाँ सच में होता है। पढ़ाई के साथ खेलकूद और अनुशासन पर भी ध्यान दिया जाता है।</div>
        <div class="t-author"><div class="t-avatar">👨</div><div><div class="t-name">रामेश्वर प्रसाद</div><div class="t-role">Father of Class 7 Student</div></div></div>
      </div>
      <div class="testi-card">
        <div class="t-quote">"</div>
        <div class="t-stars">★★★★★</div>
        <div class="t-text">पढ़ाई का माहौल बहुत अच्छा है। मेरी बेटी का आत्मविश्वास पहले से काफी बढ़ा है। बहुत अच्छा स्कूल है।</div>
        <div class="t-author"><div class="t-avatar">👩</div><div><div class="t-name">गीता कुमारी</div><div class="t-role">Mother of Class 3 Student</div></div></div>
      </div>
    </div>
  </div>

  <!-- EVENTS -->
  <div class="ev-section">
    <div style="max-width:1140px;margin:0 auto">
      <div class="section-header">
        <div class="sec-badge">School Calendar</div>
        <div class="sec-title">Upcoming <span>Events</span></div>
        <div class="sec-line"></div>
      </div>
    </div>
    <div class="ev-wrap">
      <div class="cal-box">
        <div class="cal-nav-row">
          <button class="cal-btn" onclick="calMove(-1)">❮</button>
          <div class="cal-month" id="calMonth"></div>
          <button class="cal-btn" onclick="calMove(1)">❯</button>
        </div>
        <div class="cal-dnames">
          <div class="cal-dn">Su</div><div class="cal-dn">Mo</div><div class="cal-dn">Tu</div>
          <div class="cal-dn">We</div><div class="cal-dn">Th</div><div class="cal-dn">Fr</div><div class="cal-dn">Sa</div>
        </div>
        <div class="cal-days" id="calDays"></div>
      </div>
      <div class="ev-list">
        <div class="ev-card">
          <div class="ev-date" style="background:var(--red)"><div class="ed">10</div><div class="em">APR</div></div>
          <div class="ev-info"><div class="et">Early Bird Offer Ends</div><div class="ed2">10 अप्रैल तक नामांकन पर प्रवेश निःशुल्क</div><span class="ev-tag">ADMISSION</span></div>
        </div>
        <div class="ev-card">
          <div class="ev-date"><div class="ed">14</div><div class="em">APR</div></div>
          <div class="ev-info"><div class="et">Ambedkar Jayanti Celebration</div><div class="ed2">भाषण प्रतियोगिता एवं सांस्कृतिक कार्यक्रम</div><span class="ev-tag">EVENT</span></div>
        </div>
        <div class="ev-card">
          <div class="ev-date"><div class="ed">01</div><div class="em">JUN</div></div>
          <div class="ev-info"><div class="et">New Session 2026–27 Begins</div><div class="ed2">सभी कक्षाओं का नया सत्र आरम्भ</div><span class="ev-tag">ACADEMIC</span></div>
        </div>
        <div class="ev-card">
          <div class="ev-date" style="background:#1565C0"><div class="ed">15</div><div class="em">AUG</div></div>
          <div class="ev-info"><div class="et">Independence Day Celebration</div><div class="ed2">ध्वजारोहण एवं सांस्कृतिक कार्यक्रम</div><span class="ev-tag">NATIONAL</span></div>
        </div>
      </div>
    </div>
  </div>

</div><!-- /home -->

<!-- ══════════════════════════════════════
     ABOUT PAGE
══════════════════════════════════════ -->
<div id="about" class="pg">
  <div class="pg-hero">
    <div class="bread"><span onclick="showPage('home')" style="cursor:pointer">Home</span> › <span>About Us</span></div>
    <h2>About Our School</h2>
    <p>हमारी कहानी, हमारी सोच और हमारे लक्ष्य</p>
  </div>

  <div class="about-wrap">
    <div class="section">
      <div class="about-grid" style="margin-bottom:48px">
        <div class="about-imgbox"><div class="ai">🏫</div><div class="at">School Building</div></div>
        <div class="about-text">
          <h3>Kosi Region's Most Trusted School</h3>
          <p>आवासीय न्यू मॉडर्न इंग्लिश स्कूल 2015 से <b>बिहार सरकार द्वारा मान्यता प्राप्त</b> विद्यालय है जो मोहनपुर, नौहट्टा, सहरसा में स्थित है।</p>
          <p>हमारा मानना है कि शिक्षा केवल किताबों तक सीमित नहीं होनी चाहिए — बच्चों में <b>आत्मविश्वास, नैतिक मूल्य और व्यावहारिक कौशल</b> का विकास उतना ही जरूरी है।</p>
          <div class="check-list">
            <div class="check-item"><div class="check-dot">✓</div>Nursery to Class 8 — English Medium</div>
            <div class="check-item"><div class="check-dot">✓</div>11 Years of Successful Academic Journey</div>
            <div class="check-item"><div class="check-dot">✓</div>Reg: SAH-PVT SCHOOL/NMES-0180/2020</div>
            <div class="check-item"><div class="check-dot">✓</div>Bihar Govt. Recognized Institution</div>
            <div class="check-item"><div class="check-dot">✓</div>Residential Facility Available</div>
          </div>
        </div>
      </div>
      <div class="vm-grid" style="margin-bottom:48px">
        <div class="vm-card v1"><span class="vm-icon">🌟</span><h4>Our Vision</h4><p>एक ऐसा संस्थान जहाँ हर बच्चा अपनी पूरी क्षमता पहचाने और एक जिम्मेदार, आत्मनिर्भर नागरिक बने।</p></div>
        <div class="vm-card v2"><span class="vm-icon">🎯</span><h4>Our Mission</h4><p>आधुनिक शिक्षण पद्धतियों और नैतिक मूल्यों से बच्चों में आत्मविश्वास, ज्ञान और चरित्र का निर्माण करना।</p></div>
      </div>
    </div>
  </div>

  <!-- TEACHERS -->
  <div style="background:var(--gray);padding:60px 40px">
    <div style="max-width:1140px;margin:0 auto">
      <div class="section-header">
        <div class="sec-badge">Our Team</div>
        <div class="sec-title">Meet Our <span>Teachers & Staff</span></div>
        <div class="sec-line"></div>
        <div class="sec-sub">👇 नीले button को दबाएं — शिक्षक की असली फोटो लग जाएगी</div>
      </div>
      <div class="team-grid" id="teamGrid">

        <div class="tc">
          <div class="tc-circle" id="tcP0">👨‍💼</div>
          <label for="tp0" class="tc-upload">📷 Add Photo</label>
          <input type="file" id="tp0" accept="image/*" style="display:none" onchange="setTcPhoto('tcP0','tp0',this)">
          <div class="tc-name">Sindhu Kumar Singh</div>
          <div class="tc-post">Director</div>
          <div class="tc-bio">11 वर्षों से शिक्षा क्षेत्र में समर्पित।</div>
        </div>

        <div class="tc">
          <div class="tc-circle" id="tcP1">👩‍🏫</div>
          <label for="tp1" class="tc-upload">📷 Add Photo</label>
          <input type="file" id="tp1" accept="image/*" style="display:none" onchange="setTcPhoto('tcP1','tp1',this)">
          <div class="tc-name">Senior Teacher</div>
          <div class="tc-post">Primary Department Head</div>
          <div class="tc-bio">नर्सरी से कक्षा 5 की शिक्षा।</div>
        </div>

        <div class="tc">
          <div class="tc-circle" id="tcP2">👨‍🏫</div>
          <label for="tp2" class="tc-upload">📷 Add Photo</label>
          <input type="file" id="tp2" accept="image/*" style="display:none" onchange="setTcPhoto('tcP2','tp2',this)">
          <div class="tc-name">Senior Teacher</div>
          <div class="tc-post">Upper Primary Department</div>
          <div class="tc-bio">कक्षा 6–8 विज्ञान, गणित, अंग्रेजी।</div>
        </div>

      </div>
      <button class="add-tc" onclick="addTeacher()">➕ Add New Teacher</button>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════
     ADMISSIONS PAGE
══════════════════════════════════════ -->
<div id="admissions" class="pg">
  <div class="adm-hero">
    <div class="adm-badge">ADMISSION OPEN 2026–27</div>
    <h2>Admission Process</h2>
    <p>सत्र 2026–27 के लिए नामांकन शुरू — अभी सीट सुरक्षित करें</p>
    <button class="open-adm-btn" onclick="openForm()">📋 Fill Admission Form →</button>
  </div>

  <div style="background:var(--gray);padding:60px 40px">
    <div style="max-width:1140px;margin:0 auto">
      <div class="section-header">
        <div class="sec-badge">Process</div>
        <div class="sec-title">Simple <span>4-Step Admission</span></div>
        <div class="sec-line"></div>
      </div>
      <div class="proc-grid" style="margin-bottom:48px">
        <div class="proc-card"><div class="proc-num">1</div><div class="proc-ico">📞</div><div class="proc-t">Contact Us</div><div class="proc-d">9113788228 पर call करें या स्कूल आएं।</div></div>
        <div class="proc-card"><div class="proc-num">2</div><div class="proc-ico">📋</div><div class="proc-t">Fill Form</div><div class="proc-d">प्रवेश फॉर्म भरें और दस्तावेज जमा करें।</div></div>
        <div class="proc-card"><div class="proc-num">3</div><div class="proc-ico">✅</div><div class="proc-t">Confirm Seat</div><div class="proc-d">सीट की पुष्टि के बाद शुल्क जमा करें।</div></div>
        <div class="proc-card"><div class="proc-num">4</div><div class="proc-ico">🎒</div><div class="proc-t">Welcome!</div><div class="proc-d">नई कक्षा में आपके बच्चे का स्वागत!</div></div>
      </div>

      <div class="offer-strip" style="margin-bottom:48px">
        <div>
          <h3>🎁 Early Bird Special Offer!</h3>
          <p><b>10 अप्रैल 2026 से पहले</b> नामांकन पर — ✨ प्रवेश शुल्क <b>पूर्णतः निःशुल्क!</b><br>⭐ पहले आएं, <b>ज्यादा छूट पाएं!</b> ⚠️ सीमित सीटें — जल्द संपर्क करें!</p>
        </div>
        <div class="offer-dt"><span class="o1">Offer Valid Till</span><span class="o2">10 April<br>2026</span></div>
      </div>

      <div style="border-radius:14px;overflow:hidden;box-shadow:var(--sh1);margin-bottom:48px">
        <table class="cls-table">
          <thead><tr><th>Class</th><th>Age</th><th>Medium</th><th>Seats</th><th>Status</th></tr></thead>
          <tbody>
            <tr><td>Nursery</td><td>3–4 Years</td><td>English</td><td>30</td><td><span class="open-badge">Open</span></td></tr>
            <tr><td>LKG</td><td>4–5 Years</td><td>English</td><td>30</td><td><span class="open-badge">Open</span></td></tr>
            <tr><td>UKG</td><td>5–6 Years</td><td>English</td><td>30</td><td><span class="open-badge">Open</span></td></tr>
            <tr><td>Class 1–3</td><td>6–9 Years</td><td>English</td><td>35</td><td><span class="open-badge">Open</span></td></tr>
            <tr><td>Class 4–5</td><td>9–11 Years</td><td>English</td><td>35</td><td><span class="open-badge">Open</span></td></tr>
            <tr><td>Class 6–8</td><td>11–14 Years</td><td>English</td><td>30</td><td><span class="open-badge">Open</span></td></tr>
          </tbody>
        </table>
      </div>

      <div class="section-header" style="margin-bottom:20px">
        <div class="sec-badge">Documents</div>
        <div class="sec-title">Required <span>Documents</span></div>
        <div class="sec-line"></div>
      </div>
      <div class="docs-grid">
        <div class="doc-item"><span class="doc-ico">📸</span><div><div class="doc-t">Passport Photos</div><div class="doc-s">बच्चे की 2 नवीनतम फोटो</div></div></div>
        <div class="doc-item"><span class="doc-ico">🎂</span><div><div class="doc-t">Birth Certificate</div><div class="doc-s">आयु सत्यापन के लिए</div></div></div>
        <div class="doc-item"><span class="doc-ico">📄</span><div><div class="doc-t">Previous Marksheet</div><div class="doc-s">पिछली कक्षा की रिपोर्ट</div></div></div>
        <div class="doc-item"><span class="doc-ico">🪪</span><div><div class="doc-t">Aadhaar Card</div><div class="doc-s">बच्चे / अभिभावक का</div></div></div>
        <div class="doc-item"><span class="doc-ico">📋</span><div><div class="doc-t">Transfer Certificate</div><div class="doc-s">पुराने स्कूल से (यदि लागू)</div></div></div>
        <div class="doc-item"><span class="doc-ico">🏠</span><div><div class="doc-t">Address Proof</div><div class="doc-s">निवास का कोई प्रमाण</div></div></div>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════
     CONTACT PAGE
══════════════════════════════════════ -->
<div id="contact" class="pg">
  <div class="pg-hero">
    <div class="bread"><span onclick="showPage('home')" style="cursor:pointer">Home</span> › <span>Contact</span></div>
    <h2>Contact Us</h2>
    <p>किसी भी जानकारी के लिए हमसे संपर्क करें — हम सदैव तत्पर हैं</p>
  </div>
  <div style="padding:60px 40px;background:var(--gray)">
    <div class="con-grid">
      <div>
        <h3 style="font-family:'Playfair Display',serif;font-size:24px;color:var(--navy);margin-bottom:18px">Get In Touch</h3>
        <div class="ci-card"><div class="ci-icon">👨‍💼</div><div><div class="ci-label">Director</div><div class="ci-val">Sindhu Kumar Singh</div></div></div>

        <!-- CALL BUTTON -->
        <a href="tel:+919113788228" style="display:block;text-decoration:none">
          <div class="ci-card" style="border-color:var(--green2);background:#F1FBF3;cursor:pointer">
            <div class="ci-icon" style="background:var(--green2)">📞</div>
            <div>
              <div class="ci-label" style="color:var(--green2)">👆 Tap to Call Directly!</div>
              <div class="ci-val" style="color:var(--green2)">9113788228</div>
              <div class="ci-sub">Mon–Fri: 8:00AM – 6:00PM</div>
            </div>
          </div>
        </a>

        <!-- WHATSAPP BUTTON -->
        <a href="https://wa.me/919113788228?text=नमस्ते! मुझे प्रवेश के बारे में जानकारी चाहिए।" target="_blank" style="display:block;text-decoration:none">
          <div class="ci-card" style="border-color:#25D366;background:#F0FFF5;cursor:pointer">
            <div class="ci-icon" style="background:#25D366">💬</div>
            <div>
              <div class="ci-label" style="color:#25D366">👆 Tap to Open WhatsApp!</div>
              <div class="ci-val" style="color:#25D366">WhatsApp Message करें</div>
              <div class="ci-sub">9113788228</div>
            </div>
          </div>
        </a>

        <div class="ci-card"><div class="ci-icon">📍</div><div><div class="ci-label">Address</div><div class="ci-val">Mohanpur, Nauhatta, Saharsa</div><div class="ci-sub">Bihar, India</div></div></div>
        <div class="ci-card"><div class="ci-icon">🕐</div><div><div class="ci-label">School Timings</div><div class="ci-val">Mon–Fri: 8:00AM – 2:00PM</div><div class="ci-sub">Saturday–Sunday: Closed</div></div></div>
        <div class="map-box"><span style="font-size:36px;opacity:.35">🗺️</span><span style="font-size:12.5px;color:var(--mut)">Mohanpur, Nauhatta, Saharsa — Bihar</span></div>
      </div>
      <div>
        <div class="cf-title">Send a Message</div>
        <div class="frow">
          <div class="fg"><label>Your Name *</label><input type="text" id="cf-name" placeholder="Full Name"></div>
          <div class="fg"><label>Mobile *</label><input type="tel" id="cf-phone" placeholder="10-digit Number"></div>
        </div>
        <div class="fg"><label>Child's Name</label><input type="text" id="cf-child" placeholder="Child's full name"></div>
        <div class="fg"><label>Class Required</label>
          <select id="cf-class">
            <option value="">-- Select Class --</option>
            <option>Nursery</option><option>LKG</option><option>UKG</option>
            <option>Class 1</option><option>Class 2</option><option>Class 3</option>
            <option>Class 4</option><option>Class 5</option><option>Class 6</option>
            <option>Class 7</option><option>Class 8</option>
          </select>
        </div>
        <div class="fg"><label>Message</label><textarea id="cf-msg" placeholder="Your question here..."></textarea></div>
        <button class="cf-btn" onclick="submitContact()">💬 Send via WhatsApp →</button>
        <p style="text-align:center;font-size:11px;color:var(--mut);margin-top:8px">WhatsApp खुलेगा — सिर्फ Send दबाएं ✅</p>
      </div>
    </div>
  </div>
</div>

<!-- ══════════ FOOTER ══════════ -->
<footer class="footer">
  <div class="foot-grid">
    <div>
      <div class="fn">📚 New Modern English School</div>
      <div class="fl">Mohanpur, Nauhatta, Saharsa — Bihar</div>
      <div class="fd">Kosi क्षेत्र में 11 वर्षों से गुणवत्तापूर्ण शिक्षा प्रदान करते हुए बच्चों के उज्ज्वल भविष्य की नींव रख रहे हैं।<br><br>Reg: SAH-PVT SCHOOL/NMES-0180/2020<br>Bihar Govt. Recognized</div>
    </div>
    <div>
      <div class="fh">Quick Links</div>
      <ul class="flinks">
        <li><a onclick="showPage('home')">→ Home</a></li>
        <li><a onclick="showPage('about')">→ About Us</a></li>
        <li><a onclick="showPage('admissions')">→ Admissions 2026–27</a></li>
        <li><a onclick="showPage('contact')">→ Contact Us</a></li>
        <li><a onclick="openForm()">→ Apply Now</a></li>
      </ul>
    </div>
    <div>
      <div class="fh">Contact</div>
      <div class="fcontact">
        <a href="tel:+919113788228">📞 9113788228</a>
        <a href="https://wa.me/919113788228" target="_blank">💬 WhatsApp Us</a>
        <a>📍 Mohanpur, Nauhatta, Saharsa</a>
        <a>🕐 Mon–Fri: 8AM–2PM</a>
        <a>📜 Reg: SAH-PVT/NMES-0180/2020</a>
      </div>
    </div>
  </div>
  <div class="foot-bot">
    <span>© 2026 New Modern English School — All Rights Reserved</span>
    <span>आपके बच्चे का सपना, हमारी जिम्मेदारी 🌟</span>
  </div>
</footer>

<!-- FLOATING WA -->
<a class="wa-float" href="https://wa.me/919113788228?text=नमस्ते! प्रवेश के बारे में जानकारी चाहिए।" target="_blank">💬</a>

<!-- LIGHTBOX -->
<div class="lbox" id="lbox" onclick="closeLbox()">
  <button class="lbox-x">✕</button>
  <img id="lboxImg" src="" alt="" onclick="event.stopPropagation()">
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<script>
// ── PAGE NAV ──
function showPage(id, el){
  document.querySelectorAll('.pg').forEach(p => p.classList.remove('on'));
  document.getElementById(id).classList.add('on');
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
  if(el) el.classList.add('active');
  window.scrollTo({top:0, behavior:'smooth'});
  document.getElementById('navLinks').classList.remove('open');
  setTimeout(initAnim, 100);
}
function toggleMob(){ document.getElementById('navLinks').classList.toggle('open'); }

// ── POPUPS ──
window.addEventListener('load', () => { setTimeout(() => document.getElementById('annPop').classList.add('on'), 1800); });
function closeAnn(){ document.getElementById('annPop').classList.remove('on'); }
document.getElementById('annPop').addEventListener('click', function(e){ if(e.target===this) closeAnn(); });

function openForm(){
  document.getElementById('formPop').classList.add('on');
  document.body.style.overflow = 'hidden';
}
function closeForm(){
  document.getElementById('formPop').classList.remove('on');
  document.body.style.overflow = '';
}
document.getElementById('formPop').addEventListener('click', function(e){ if(e.target===this) closeForm(); });

// ── FORM SUBMIT ──
function submitAdmForm(){
  const name  = document.getElementById('fn-name').value.trim();
  const phone = document.getElementById('fn-phone').value.trim();
  const child = document.getElementById('fn-child').value.trim();
  const cls   = document.getElementById('fn-class').value;
  const dob   = document.getElementById('fn-dob').value;
  const addr  = document.getElementById('fn-addr').value.trim();
  const msg   = document.getElementById('fn-msg').value.trim();
  if(!name||!phone||!child||!cls){ alert('कृपया नाम, मोबाइल, बच्चे का नाम और कक्षा भरें।'); return; }
  let wa = `📋 *Admission Form — New Modern English School*\n_Session 2026–27_\n\n`;
  wa += `👤 *Parent:* ${name}\n📞 *Mobile:* ${phone}\n👦 *Child:* ${child}\n🏫 *Class:* ${cls}\n`;
  if(dob)  wa += `🎂 *DOB:* ${dob}\n`;
  if(addr) wa += `🏠 *Address:* ${addr}\n`;
  if(msg)  wa += `💬 *Message:* ${msg}\n`;
  wa += `\n✅ Please process this admission. Thank you! 🙏`;
  window.open(`https://wa.me/919113788228?text=${encodeURIComponent(wa)}`, '_blank');
  closeForm();
  showToast('✅ WhatsApp खुल रहा है — Send दबाएं!');
  ['fn-name','fn-phone','fn-child','fn-dob','fn-addr','fn-msg'].forEach(id => document.getElementById(id).value = '');
  document.getElementById('fn-class').value = '';
}

function submitContact(){
  const name  = document.getElementById('cf-name').value.trim();
  const phone = document.getElementById('cf-phone').value.trim();
  const child = document.getElementById('cf-child').value.trim();
  const cls   = document.getElementById('cf-class').value;
  const msg   = document.getElementById('cf-msg').value.trim();
  if(!name||!phone){ alert('कृपया नाम और मोबाइल नंबर भरें।'); return; }
  let wa = `📋 *Enquiry — New Modern English School*\n\n`;
  wa += `👤 *Name:* ${name}\n📞 *Mobile:* ${phone}\n`;
  if(child) wa += `👦 *Child:* ${child}\n`;
  if(cls)   wa += `🏫 *Class:* ${cls}\n`;
  if(msg)   wa += `💬 *Message:* ${msg}\n`;
  wa += `\nThank you! 🙏`;
  window.open(`https://wa.me/919113788228?text=${encodeURIComponent(wa)}`, '_blank');
  showToast('✅ WhatsApp खुल रहा है!');
  ['cf-name','cf-phone','cf-child','cf-msg'].forEach(id => document.getElementById(id).value = '');
  document.getElementById('cf-class').value = '';
}

// ── CAROUSEL ──
let cur = 0, total = 3;
let autoTimer = setInterval(() => moveSlide(1), 5000);
function moveSlide(d){ cur = (cur+d+total)%total; updateCarousel(); resetTimer(); }
function goSlide(n){ cur = n; updateCarousel(); resetTimer(); }
function updateCarousel(){
  document.getElementById('cTrack').style.transform = `translateX(-${cur*100}%)`;
  document.querySelectorAll('.dot').forEach((d,i) => d.classList.toggle('on', i===cur));
}
function resetTimer(){ clearInterval(autoTimer); autoTimer = setInterval(()=>moveSlide(1),5000); }

// ── ANIMATIONS ──
function initAnim(){
  const io = new IntersectionObserver(entries => {
    entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('show'); });
  }, {threshold:0.1});
  document.querySelectorAll('.why-card,.testi-card,.stat').forEach((el,i) => {
    el.style.transitionDelay = (i * 0.07) + 's';
    io.observe(el);
  });
}
document.addEventListener('DOMContentLoaded', initAnim);

// ── GALLERY ──
function addGalPics(e){
  const files = Array.from(e.target.files);
  const grid  = document.getElementById('galGrid');
  files.forEach(f => {
    const reader = new FileReader();
    reader.onload = ev => {
      const item = document.createElement('div');
      item.className = 'gal-item';
      item.style.cursor = 'pointer';
      const img = document.createElement('img');
      img.src = ev.target.result;
      item.appendChild(img);
      item.onclick = () => openLbox(ev.target.result);
      grid.insertBefore(item, grid.firstChild);
    };
    reader.readAsDataURL(f);
  });
  showToast(`📸 ${files.length} photo${files.length>1?'s':''} added!`);
}
function openLbox(src){ document.getElementById('lboxImg').src=src; document.getElementById('lbox').classList.add('on'); }
function closeLbox(){ document.getElementById('lbox').classList.remove('on'); }

// ── TEACHER PHOTOS ──
function setTcPhoto(divId, inputId, input){
  if(!input.files || !input.files[0]) return;
  const reader = new FileReader();
  reader.onload = function(e){
    const el = document.getElementById(divId);
    if(!el) return;
    el.innerHTML = '';
    const img = document.createElement('img');
    img.src = e.target.result;
    el.appendChild(img);
    // Change only this card's label
    const lbl = document.querySelector(`label[for="${inputId}"]`);
    if(lbl) lbl.textContent = '🔄 Change Photo';
    showToast('✅ Teacher photo added!');
  };
  reader.readAsDataURL(input.files[0]);
}

let tcCount = 3;
function addTeacher(){
  const idx = tcCount++;
  const fid = `tp${idx}`, pid = `tcP${idx}`;
  const grid = document.getElementById('teamGrid');
  const card = document.createElement('div');
  card.className = 'tc';
  card.innerHTML = `
    <button onclick="this.closest('.tc').remove()" style="position:absolute;top:10px;right:10px;background:#fee;border:1px solid #fcc;color:#c00;width:24px;height:24px;border-radius:50%;font-size:12px;cursor:pointer;display:flex;align-items:center;justify-content:center;">✕</button>
    <div class="tc-circle" id="${pid}" style="margin:0 auto 6px">👨‍🏫</div>
    <label for="${fid}" class="tc-upload">📷 Add Photo</label>
    <input type="file" id="${fid}" accept="image/*" style="display:none" onchange="setTcPhoto('${pid}','${fid}',this)">
    <div class="tc-name" contenteditable="true" style="border:1px dashed #ddd;border-radius:5px;padding:2px 6px;outline:none">Teacher Name</div>
    <div class="tc-post" contenteditable="true" style="border:1px dashed #ddd;border-radius:5px;padding:1px 6px;outline:none;margin-top:3px">Post / Subject</div>
    <div class="tc-bio" contenteditable="true" style="border:1px dashed #ddd;border-radius:5px;padding:2px 6px;outline:none;margin-top:6px">Short description...</div>
  `;
  grid.appendChild(card);
  showToast('✅ New teacher card added!');
}

// ── CALENDAR ──
const months = ['January','February','March','April','May','June','July','August','September','October','November','December'];
const evMap = {2:[10,14], 3:[1], 4:[10,15]};
let calDate = new Date(2026, 2, 1);
function renderCal(){
  const y = calDate.getFullYear(), m = calDate.getMonth();
  document.getElementById('calMonth').textContent = months[m] + ' ' + y;
  const first = new Date(y,m,1).getDay(), days = new Date(y,m+1,0).getDate();
  const today = new Date();
  let html = '';
  for(let i=0;i<first;i++) html += `<div class="cday empty"></div>`;
  for(let d=1;d<=days;d++){
    const isT = (d===today.getDate()&&m===today.getMonth()&&y===today.getFullYear());
    const isE = evMap[m] && evMap[m].includes(d);
    html += `<div class="cday${isT?' today':''}${isE?' has-ev':''}">${d}</div>`;
  }
  document.getElementById('calDays').innerHTML = html;
}
function calMove(d){ calDate.setMonth(calDate.getMonth()+d); renderCal(); }
renderCal();

// ── TOAST ──
function showToast(msg){
  const t = document.getElementById('toast');
  t.textContent = msg; t.style.display = 'block';
  clearTimeout(t._t);
  t._t = setTimeout(() => t.style.display='none', 3500);
}

// ── PWA SERVICE WORKER ──
if('serviceWorker' in navigator){
  window.addEventListener('load', () => {
    navigator.serviceWorker.register('sw.js').catch(e => {});
  });
}

// ── PWA INSTALL PROMPT ──
let deferredPrompt;
window.addEventListener('beforeinstallprompt', e => {
  e.preventDefault();
  deferredPrompt = e;
  setTimeout(() => { if(deferredPrompt) document.getElementById('installBanner').style.display='flex'; }, 3000);
});
function installApp(){
  document.getElementById('installBanner').style.display='none';
  if(deferredPrompt){ deferredPrompt.prompt(); deferredPrompt.userChoice.then(()=>{deferredPrompt=null;}); }
}
function closeBanner(){ document.getElementById('installBanner').style.display='none'; }
</script>

<!-- PWA INSTALL BANNER -->
<div id="installBanner" style="display:none;position:fixed;bottom:0;left:0;right:0;background:#0D2137;border-top:2px solid #D4A017;padding:14px 18px;z-index:9995;align-items:center;gap:12px;box-shadow:0 -4px 20px rgba(0,0,0,.3)">
  <div style="font-size:28px">📱</div>
  <div style="flex:1">
    <div style="font-size:13.5px;font-weight:800;color:#fff;font-family:'Nunito',sans-serif">App Install करें — Free!</div>
    <div style="font-size:11px;color:rgba(255,255,255,.55);margin-top:2px">NMES School App — Home Screen pe add karo</div>
  </div>
  <button onclick="installApp()" style="background:#D4A017;color:#0D2137;border:none;padding:9px 16px;border-radius:20px;font-size:12.5px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif;white-space:nowrap">Install ✓</button>
  <button onclick="closeBanner()" style="background:transparent;border:none;color:rgba(255,255,255,.4);font-size:20px;cursor:pointer;padding:4px">✕</button>
</div>
</body>
</html>
