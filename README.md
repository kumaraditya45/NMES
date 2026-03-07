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
  --muted:      #666;
  --white:      #ffffff;
  --shadow-sm:  0 2px 12px rgba(0,0,0,0.08);
  --shadow:     0 8px 32px rgba(0,0,0,0.12);
  --shadow-lg:  0 20px 60px rgba(0,0,0,0.18);
}
*{margin:0;padding:0;box-sizing:border-box;scroll-behavior:smooth}
body{font-family:'Hind',sans-serif;background:var(--cream);color:var(--text);overflow-x:hidden}

/* ── POPUP ANNOUNCEMENT ── */
.popup-overlay{position:fixed;inset:0;background:rgba(0,0,0,0.65);z-index:10000;display:flex;align-items:center;justify-content:center;backdrop-filter:blur(4px);animation:fadeIn .3s ease}
.popup-box{background:var(--white);border-radius:20px;width:90%;max-width:480px;overflow:hidden;box-shadow:var(--shadow-lg);animation:popUp .4s cubic-bezier(.34,1.56,.64,1)}
.popup-header{background:linear-gradient(135deg,var(--red),#922b21);padding:20px 24px;position:relative}
.popup-header h3{font-family:'Baloo 2',cursive;font-size:22px;font-weight:800;color:var(--white)}
.popup-header p{font-size:12px;color:rgba(255,255,255,0.75);margin-top:3px}
.popup-close{position:absolute;top:16px;right:16px;background:rgba(255,255,255,0.2);border:none;color:var(--white);width:30px;height:30px;border-radius:50%;font-size:16px;cursor:pointer;display:flex;align-items:center;justify-content:center;transition:all .2s}
.popup-close:hover{background:rgba(255,255,255,0.35)}
.popup-body{padding:24px}
.popup-offer{background:linear-gradient(135deg,#6a1b9a,#9c27b0);border-radius:12px;padding:16px 18px;color:var(--white);margin-bottom:14px}
.popup-offer .po-title{font-family:'Baloo 2',cursive;font-size:17px;font-weight:800;color:var(--gold-light);margin-bottom:6px}
.popup-offer p{font-size:12.5px;color:rgba(255,255,255,0.88);line-height:1.7}
.popup-offer b{color:var(--white)}
.popup-date{display:flex;align-items:center;gap:10px;background:var(--green-light);border-radius:10px;padding:12px 14px;margin-bottom:16px}
.popup-date .pd-icon{font-size:22px}
.popup-date .pd-text{font-size:12.5px;color:var(--green-dark);font-weight:600}
.popup-btn{width:100%;padding:13px;background:linear-gradient(135deg,var(--green),var(--green-mid));color:var(--white);border:none;border-radius:10px;font-size:14px;font-weight:700;font-family:'Hind',sans-serif;cursor:pointer;transition:all .25s}
.popup-btn:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(26,92,42,.3)}

/* ── TOPBAR ── */
.topbar{background:var(--green-dark);padding:7px 32px;display:flex;justify-content:space-between;align-items:center;font-size:11px;color:rgba(255,255,255,0.6)}
.topbar a{color:var(--gold-light);text-decoration:none;font-weight:600}
.tb-right{display:flex;gap:18px;align-items:center}

/* ── NAVBAR ── */
.navbar{background:var(--white);padding:0 32px;display:flex;justify-content:space-between;align-items:center;box-shadow:var(--shadow-sm);position:sticky;top:0;z-index:999;border-bottom:3px solid var(--gold)}
.nav-brand{display:flex;align-items:center;gap:12px;padding:10px 0}
.nav-logo{width:50px;height:50px;border-radius:50%;background:linear-gradient(145deg,var(--green),var(--green-dark));border:2.5px solid var(--gold);display:flex;align-items:center;justify-content:center;font-size:22px;flex-shrink:0}
.brand-name{font-family:'Baloo 2',cursive;font-size:15px;font-weight:800;color:var(--green-dark);line-height:1.1}
.brand-loc{font-size:10px;color:var(--muted);font-weight:500}
.nav-links{display:flex;gap:2px;list-style:none}
.nav-links a{text-decoration:none;color:var(--text);font-size:13px;font-weight:600;padding:8px 14px;border-radius:6px;transition:all .25s;cursor:pointer}
.nav-links a:hover,.nav-links a.active{color:var(--green);background:var(--green-light)}
.nav-links a.active{border-bottom:3px solid var(--gold)}
.nav-cta{background:var(--green)!important;color:var(--white)!important;border-radius:30px!important}
.nav-cta:hover{background:var(--green-mid)!important;transform:translateY(-1px)}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:5px}
.hamburger span{width:24px;height:2px;background:var(--green-dark);border-radius:2px;transition:all .3s}

/* ── PAGES ── */
.page-section{display:none;animation:fadeIn .4s ease}
.page-section.active{display:block}

/* ══ HOME ══ */

/* CAROUSEL */
.carousel{position:relative;overflow:hidden;height:88vh;min-height:500px}
.carousel-track{display:flex;height:100%;transition:transform .7s cubic-bezier(.77,0,.175,1)}
.slide{min-width:100%;height:100%;position:relative;display:flex;align-items:center;justify-content:center;overflow:hidden}
.slide-bg{position:absolute;inset:0;background-size:cover;background-position:center}
.slide-1 .slide-bg{background:linear-gradient(135deg,#0c3320 0%,#1A5C2A 40%,#0c4a1f 100%)}
.slide-2 .slide-bg{background:linear-gradient(135deg,#1a237e 0%,#283593 50%,#1565c0 100%)}
.slide-3 .slide-bg{background:linear-gradient(135deg,#b71c1c 0%,#c62828 50%,#880e4f 100%)}
.slide-overlay{position:absolute;inset:0;background:rgba(0,0,0,0.35)}
.slide-pattern{position:absolute;inset:0;background-image:radial-gradient(circle,rgba(255,255,255,0.05) 1px,transparent 1px);background-size:28px 28px}
.slide-content{position:relative;z-index:2;text-align:center;padding:0 32px;max-width:780px}
.slide-badge{display:inline-flex;align-items:center;gap:7px;background:rgba(201,168,76,0.25);border:1px solid rgba(201,168,76,0.5);padding:5px 16px;border-radius:20px;font-size:11px;color:var(--gold-light);font-weight:600;letter-spacing:1px;margin-bottom:18px;animation:fadeUp .6s ease both}
.slide-content h1{font-family:'Baloo 2',cursive;font-size:52px;font-weight:800;color:var(--white);line-height:1.05;margin-bottom:14px;text-shadow:0 3px 12px rgba(0,0,0,.4);animation:fadeUp .7s ease .1s both}
.slide-content h1 .gold{color:var(--gold-light)}
.slide-content p{font-size:16px;color:rgba(255,255,255,0.82);line-height:1.7;margin-bottom:26px;animation:fadeUp .7s ease .2s both}
.slide-btns{display:flex;gap:12px;justify-content:center;animation:fadeUp .7s ease .3s both}
.btn-primary{background:linear-gradient(135deg,var(--gold),var(--gold-light));color:var(--green-dark);border:none;padding:13px 30px;border-radius:30px;font-size:14px;font-weight:700;cursor:pointer;transition:all .25s;font-family:'Hind',sans-serif}
.btn-primary:hover{transform:translateY(-3px);box-shadow:0 10px 28px rgba(201,168,76,.45)}
.btn-outline{background:transparent;color:var(--white);border:2px solid rgba(255,255,255,0.5);padding:13px 30px;border-radius:30px;font-size:14px;font-weight:600;cursor:pointer;transition:all .25s;font-family:'Hind',sans-serif}
.btn-outline:hover{background:rgba(255,255,255,.12);border-color:rgba(255,255,255,.8)}
.carousel-prev,.carousel-next{position:absolute;top:50%;transform:translateY(-50%);background:rgba(255,255,255,0.15);backdrop-filter:blur(8px);border:1px solid rgba(255,255,255,0.2);color:var(--white);width:48px;height:48px;border-radius:50%;font-size:18px;cursor:pointer;z-index:5;transition:all .25s;display:flex;align-items:center;justify-content:center}
.carousel-prev{left:20px}
.carousel-next{right:20px}
.carousel-prev:hover,.carousel-next:hover{background:rgba(255,255,255,0.3)}
.carousel-dots{position:absolute;bottom:24px;left:50%;transform:translateX(-50%);display:flex;gap:8px;z-index:5}
.dot{width:10px;height:10px;border-radius:50%;background:rgba(255,255,255,0.4);cursor:pointer;transition:all .3s}
.dot.active{background:var(--gold-light);width:28px;border-radius:5px}

/* NOTICE BAR */
.notice-bar{background:var(--red);padding:11px 32px;display:flex;align-items:center;justify-content:center;gap:12px;overflow:hidden}
.notice-scroll{display:flex;align-items:center;gap:12px;animation:marquee 20s linear infinite}
.nb-badge{background:var(--gold-light);color:var(--red);padding:3px 10px;border-radius:4px;font-size:10px;font-weight:800;letter-spacing:1px;flex-shrink:0}
.nb-text{color:var(--white);font-size:13px;font-weight:600;white-space:nowrap}
.nb-text b{color:var(--gold-light)}

/* STATS */
.stats-strip{background:var(--white);padding:28px 32px;display:flex;justify-content:center;gap:0;box-shadow:var(--shadow-sm)}
.stat-item{text-align:center;padding:0 44px;border-right:1px solid #eee;opacity:0;transform:translateY(20px);transition:all .6s ease}
.stat-item.visible{opacity:1;transform:translateY(0)}
.stat-item:last-child{border-right:none}
.stat-num{font-family:'Baloo 2',cursive;font-size:36px;font-weight:800;color:var(--green);line-height:1}
.stat-num span{color:var(--gold-dark)}
.stat-label{font-size:11.5px;color:var(--muted);margin-top:4px;font-weight:500}

/* SECTION */
.section{padding:56px 32px;max-width:1100px;margin:0 auto}
.section-header{text-align:center;margin-bottom:40px}
.eyebrow{font-size:11px;color:var(--gold-dark);font-weight:700;letter-spacing:2.5px;text-transform:uppercase;margin-bottom:8px}
.sec-title{font-family:'Baloo 2',cursive;font-size:32px;font-weight:800;color:var(--green-dark);line-height:1.15}
.sec-title span{color:var(--green)}
.sec-line{width:56px;height:3px;background:linear-gradient(90deg,var(--gold),var(--gold-light));margin:12px auto 0;border-radius:2px}

/* FEATURES GRID */
.features-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
.feature-card{background:var(--white);border-radius:14px;padding:24px 18px;text-align:center;border:1.5px solid #eee;box-shadow:var(--shadow-sm);transition:all .35s;opacity:0;transform:translateY(30px)}
.feature-card.visible{opacity:1;transform:translateY(0)}
.feature-card:hover{border-color:var(--gold);transform:translateY(-6px);box-shadow:var(--shadow)}
.fc-icon{width:56px;height:56px;border-radius:14px;background:var(--green-light);display:flex;align-items:center;justify-content:center;font-size:26px;margin:0 auto 14px;transition:all .3s}
.feature-card:hover .fc-icon{background:var(--green)}
.fc-title{font-size:13px;font-weight:700;color:var(--green-dark);margin-bottom:6px}
.fc-desc{font-size:11px;color:var(--muted);line-height:1.65}

/* PHOTO GALLERY */
.gallery-section{background:var(--green-dark);padding:56px 32px}
.gallery-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;max-width:1100px;margin:30px auto 0}
.gallery-item{aspect-ratio:4/3;border-radius:12px;overflow:hidden;position:relative;cursor:pointer;border:2px solid rgba(201,168,76,0.2);transition:all .35s}
.gallery-item:hover{transform:scale(1.04);border-color:var(--gold);box-shadow:0 10px 30px rgba(0,0,0,.4)}
.gallery-item.large{grid-column:span 2;grid-row:span 2;aspect-ratio:auto}
.gallery-bg{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px;background:rgba(255,255,255,0.07);transition:all .3s}
.gallery-item:hover .gallery-bg{background:rgba(255,255,255,0.14)}
.gallery-bg .gi-icon{font-size:32px;opacity:0.6}
.gallery-bg .gi-label{font-size:11px;color:rgba(255,255,255,0.6);text-align:center;font-weight:500}
.gallery-upload-btn{display:flex;align-items:center;gap:10px;background:linear-gradient(135deg,var(--gold),var(--gold-light));color:var(--green-dark);border:none;padding:11px 22px;border-radius:30px;font-size:13px;font-weight:700;cursor:pointer;font-family:'Hind',sans-serif;margin:20px auto 0;display:block;transition:all .25s}
.gallery-upload-btn:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(201,168,76,.35)}
/* Lightbox */
.lightbox{position:fixed;inset:0;background:rgba(0,0,0,0.92);z-index:9999;display:none;align-items:center;justify-content:center;flex-direction:column;gap:14px}
.lightbox.open{display:flex}
.lightbox img{max-width:90vw;max-height:80vh;border-radius:10px;box-shadow:0 20px 60px rgba(0,0,0,.6)}
.lightbox-close{position:absolute;top:20px;right:24px;background:rgba(255,255,255,0.1);border:none;color:var(--white);width:40px;height:40px;border-radius:50%;font-size:20px;cursor:pointer;display:flex;align-items:center;justify-content:center}
#gallery-file-input{display:none}

/* TESTIMONIALS */
.testimonials-section{background:linear-gradient(160deg,var(--green-dark),#0f4025);padding:60px 32px;position:relative;overflow:hidden}
.testimonials-section::before{content:'';position:absolute;inset:0;background-image:radial-gradient(circle,rgba(255,255,255,0.03) 1px,transparent 1px);background-size:30px 30px}
.testimonials-wrap{max-width:1100px;margin:0 auto}
.testimonials-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin-top:32px}
.testi-card{background:rgba(255,255,255,0.07);backdrop-filter:blur(10px);border:1px solid rgba(255,255,255,0.1);border-radius:16px;padding:24px 20px;transition:all .35s;opacity:0;transform:translateY(30px)}
.testi-card.visible{opacity:1;transform:translateY(0)}
.testi-card:hover{background:rgba(255,255,255,0.12);transform:translateY(-5px)}
.testi-stars{color:var(--gold-light);font-size:14px;margin-bottom:12px;letter-spacing:2px}
.testi-text{font-size:12.5px;color:rgba(255,255,255,0.82);line-height:1.8;margin-bottom:16px;font-style:italic}
.testi-author{display:flex;align-items:center;gap:10px}
.testi-avatar{width:40px;height:40px;border-radius:50%;background:linear-gradient(135deg,var(--gold),var(--gold-light));display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}
.testi-name{font-size:13px;font-weight:700;color:var(--white)}
.testi-role{font-size:10.5px;color:rgba(255,255,255,0.5)}

/* EVENTS CALENDAR */
.events-section{padding:56px 32px;background:var(--cream)}
.events-wrap{max-width:1100px;margin:0 auto}
.events-grid{display:grid;grid-template-columns:1.2fr 1fr;gap:28px;margin-top:32px}
.calendar-widget{background:var(--white);border-radius:16px;padding:20px;box-shadow:var(--shadow-sm);border:1.5px solid #eee}
.cal-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:16px}
.cal-month{font-family:'Baloo 2',cursive;font-size:18px;font-weight:800;color:var(--green-dark)}
.cal-nav{background:var(--green-light);border:none;width:32px;height:32px;border-radius:50%;cursor:pointer;font-size:14px;display:flex;align-items:center;justify-content:center;transition:all .2s;color:var(--green)}
.cal-nav:hover{background:var(--green);color:var(--white)}
.cal-days-header{display:grid;grid-template-columns:repeat(7,1fr);gap:2px;margin-bottom:6px}
.cal-day-name{text-align:center;font-size:10px;font-weight:700;color:var(--muted);padding:4px 0;text-transform:uppercase}
.cal-days{display:grid;grid-template-columns:repeat(7,1fr);gap:3px}
.cal-day{text-align:center;padding:7px 3px;font-size:12px;border-radius:8px;cursor:pointer;transition:all .2s;color:var(--text)}
.cal-day:hover{background:var(--green-light);color:var(--green)}
.cal-day.today{background:var(--green);color:var(--white);font-weight:700}
.cal-day.has-event{background:rgba(201,168,76,0.2);color:var(--gold-dark);font-weight:700;position:relative}
.cal-day.has-event::after{content:'';position:absolute;bottom:3px;left:50%;transform:translateX(-50%);width:4px;height:4px;border-radius:50%;background:var(--gold)}
.cal-day.empty{color:#ddd;cursor:default}
.cal-day.empty:hover{background:transparent}
.events-list{display:flex;flex-direction:column;gap:12px}
.event-item{background:var(--white);border-radius:12px;padding:14px 16px;display:flex;gap:14px;align-items:flex-start;border:1.5px solid #eee;box-shadow:var(--shadow-sm);transition:all .25s;cursor:pointer}
.event-item:hover{border-color:var(--gold);transform:translateX(4px)}
.event-date-box{background:var(--green);color:var(--white);border-radius:10px;padding:8px 12px;text-align:center;flex-shrink:0;min-width:52px}
.event-date-box .ed-day{font-family:'Baloo 2',cursive;font-size:22px;font-weight:800;line-height:1}
.event-date-box .ed-mon{font-size:9px;font-weight:600;letter-spacing:1px;opacity:0.85}
.event-info .ei-title{font-size:13.5px;font-weight:700;color:var(--green-dark);margin-bottom:3px}
.event-info .ei-desc{font-size:11px;color:var(--muted);line-height:1.55}
.event-info .ei-tag{display:inline-block;background:var(--green-light);color:var(--green);font-size:9.5px;font-weight:700;padding:2px 8px;border-radius:10px;margin-top:5px}

/* ══ PAGE HERO ══ */
.page-hero{background:linear-gradient(135deg,var(--green-dark),var(--green));padding:52px 32px;text-align:center;position:relative;overflow:hidden}
.page-hero::before{content:'';position:absolute;inset:0;background-image:radial-gradient(circle,rgba(255,255,255,0.05) 1px,transparent 1px);background-size:25px 25px}
.page-hero h2{font-family:'Baloo 2',cursive;font-size:38px;font-weight:800;color:var(--white);position:relative}
.page-hero p{font-size:14px;color:rgba(255,255,255,0.7);margin-top:8px;position:relative}

/* ══ ABOUT PAGE ══ */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:40px;align-items:center;max-width:1100px;margin:0 auto}
.about-img{border-radius:16px;overflow:hidden;background:var(--green-light);aspect-ratio:4/3;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:10px;border:2px dashed rgba(26,92,42,0.2)}
.about-img .ai-icon{font-size:50px;opacity:.45}
.about-img .ai-text{font-size:13px;color:var(--muted)}
.about-text h3{font-family:'Baloo 2',cursive;font-size:26px;font-weight:800;color:var(--green-dark);margin-bottom:14px;line-height:1.2}
.about-text p{font-size:13px;color:var(--muted);line-height:1.85;margin-bottom:11px}
.about-text p b{color:var(--green)}
.hp-list{display:flex;flex-direction:column;gap:8px;margin-top:14px}
.hp-item{display:flex;align-items:center;gap:10px;font-size:13px;color:var(--text);font-weight:500}
.hp-dot{width:22px;height:22px;background:var(--green);border-radius:6px;display:flex;align-items:center;justify-content:center;color:var(--white);font-size:10px;flex-shrink:0}
.vm-grid{display:grid;grid-template-columns:1fr 1fr;gap:22px;max-width:1100px;margin:0 auto}
.vm-card{border-radius:14px;padding:26px 24px;position:relative;overflow:hidden}
.vm-card.vision{background:linear-gradient(135deg,var(--green-dark),var(--green));color:var(--white)}
.vm-card.mission{background:var(--white);border:1.5px solid #eee}
.vm-card h4{font-family:'Baloo 2',cursive;font-size:20px;font-weight:800;margin-bottom:10px}
.vm-card.vision h4{color:var(--gold-light)}
.vm-card.mission h4{color:var(--green-dark)}
.vm-card p{font-size:13px;line-height:1.8}
.vm-card.vision p{color:rgba(255,255,255,.75)}
.vm-card.mission p{color:var(--muted)}
.vm-icon{font-size:34px;margin-bottom:12px;display:block}
.team-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;max-width:1100px;margin:0 auto}
.team-card{background:var(--white);border-radius:14px;padding:26px 20px;text-align:center;border:1.5px solid #eee;box-shadow:var(--shadow-sm);transition:all .3s}
.team-card:hover{border-color:var(--gold);transform:translateY(-5px)}
.team-avatar{width:68px;height:68px;border-radius:50%;background:var(--green-light);border:3px solid var(--gold);display:flex;align-items:center;justify-content:center;font-size:28px;margin:0 auto 14px}
.team-name{font-family:'Baloo 2',cursive;font-size:16px;font-weight:800;color:var(--green-dark)}
.team-role{font-size:11.5px;color:var(--gold-dark);font-weight:600;margin-top:3px}
.team-desc{font-size:11.5px;color:var(--muted);margin-top:8px;line-height:1.6}

/* ══ ADMISSIONS ══ */
.adm-hero{background:linear-gradient(135deg,var(--red),#7f1818);padding:50px 32px;text-align:center}
.adm-hero h2{font-family:'Baloo 2',cursive;font-size:38px;font-weight:800;color:var(--white)}
.adm-hero p{font-size:14px;color:rgba(255,255,255,.75);margin-top:8px}
.adm-badge{display:inline-block;background:var(--gold-light);color:var(--red);padding:5px 16px;border-radius:20px;font-size:11px;font-weight:800;letter-spacing:1px;margin-bottom:14px}
.process-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px;max-width:1100px;margin:0 auto}
.process-card{background:var(--white);border-radius:14px;padding:24px 16px;text-align:center;border:1.5px solid #eee;position:relative;transition:all .3s}
.process-card:hover{border-color:var(--green);transform:translateY(-4px)}
.process-num{position:absolute;top:-13px;left:50%;transform:translateX(-50%);width:26px;height:26px;background:var(--green);color:var(--white);border-radius:50%;font-size:12px;font-weight:800;display:flex;align-items:center;justify-content:center;border:2px solid var(--cream)}
.process-icon{font-size:30px;margin-bottom:10px}
.process-title{font-family:'Baloo 2',cursive;font-size:14px;font-weight:800;color:var(--green-dark);margin-bottom:6px}
.process-desc{font-size:11px;color:var(--muted);line-height:1.6}
.classes-table{width:100%;border-collapse:collapse;border-radius:12px;overflow:hidden;box-shadow:var(--shadow)}
.classes-table th{background:var(--green);color:var(--white);padding:12px 16px;font-size:13px;font-weight:700;text-align:left}
.classes-table td{padding:11px 16px;font-size:12.5px;border-bottom:1px solid #f0f0f0}
.classes-table tr:last-child td{border-bottom:none}
.classes-table tr:nth-child(even) td{background:var(--green-light)}
.badge-open{background:#e8f5e9;color:#2e7d32;padding:2px 10px;border-radius:12px;font-size:10.5px;font-weight:700}
.offer-box{background:linear-gradient(135deg,#6a1b9a,#9c27b0);border-radius:16px;padding:28px 30px;display:flex;align-items:center;gap:24px;max-width:1100px;margin:0 auto;box-shadow:0 8px 30px rgba(106,27,154,.25)}
.offer-left{flex:1}
.offer-box h3{font-family:'Baloo 2',cursive;font-size:23px;font-weight:800;color:var(--gold-light);margin-bottom:8px}
.offer-box p{font-size:13px;color:rgba(255,255,255,.85);line-height:1.75}
.offer-box p b{color:var(--white)}
.offer-right{background:rgba(255,255,255,.12);border:1.5px solid rgba(240,208,96,.4);border-radius:12px;padding:14px 20px;text-align:center;flex-shrink:0}
.offer-right .or1{font-size:9px;color:rgba(255,255,255,.6);letter-spacing:1px;display:block}
.offer-right .or2{font-family:'Baloo 2',cursive;font-size:26px;font-weight:800;color:var(--gold-light);display:block;line-height:1.1}
.docs-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;max-width:1100px;margin:0 auto}
.doc-item{background:var(--white);border:1.5px solid #eee;border-radius:12px;padding:16px;display:flex;gap:12px;align-items:center;transition:all .25s}
.doc-item:hover{border-color:var(--gold);transform:translateY(-2px)}
.doc-icon{font-size:24px}
.doc-title{font-weight:700;font-size:13px}
.doc-sub{font-size:11px;color:var(--muted);margin-top:2px}

/* ══ CONTACT ══ */
.contact-grid{display:grid;grid-template-columns:1fr 1.2fr;gap:36px;max-width:1100px;margin:0 auto}
.ci-item{display:flex;gap:14px;align-items:flex-start;margin-bottom:16px;padding:16px;background:var(--white);border-radius:12px;border:1.5px solid #eee;transition:all .25s}
.ci-item:hover{border-color:var(--gold)}
.ci-icon{width:44px;height:44px;background:var(--green);border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
.ci-label{font-size:10px;color:var(--muted);text-transform:uppercase;letter-spacing:1px;font-weight:600}
.ci-value{font-size:14px;font-weight:700;color:var(--text);margin-top:2px}
.ci-sub{font-size:11px;color:var(--muted);margin-top:2px}
.map-ph{background:var(--green-light);border-radius:14px;border:2px dashed rgba(26,92,42,.2);min-height:180px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:10px;margin-bottom:18px}
.map-ph .mp-icon{font-size:38px;opacity:.45}
.map-ph .mp-text{font-size:13px;color:var(--muted)}
.contact-form h3{font-family:'Baloo 2',cursive;font-size:22px;font-weight:800;color:var(--green-dark);margin-bottom:18px}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.form-group{margin-bottom:12px}
.form-group label{display:block;font-size:11px;font-weight:600;color:var(--muted);margin-bottom:5px;text-transform:uppercase;letter-spacing:.5px}
.form-group input,.form-group textarea,.form-group select{width:100%;padding:11px 13px;border:1.5px solid #e0e0e0;border-radius:8px;font-size:13px;font-family:'Hind',sans-serif;color:var(--text);background:var(--white);outline:none;transition:all .2s}
.form-group input:focus,.form-group textarea:focus,.form-group select:focus{border-color:var(--green);box-shadow:0 0 0 3px rgba(26,92,42,.08)}
.form-group textarea{resize:vertical;min-height:90px}
.form-submit{width:100%;padding:13px;background:linear-gradient(135deg,var(--green),var(--green-mid));color:var(--white);border:none;border-radius:10px;font-size:14px;font-weight:700;font-family:'Hind',sans-serif;cursor:pointer;transition:all .25s}
.form-submit:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(26,92,42,.3)}

/* ══ FOOTER ══ */
.footer{background:var(--green-dark);padding:44px 32px 0}
.footer-grid{display:grid;grid-template-columns:1.5fr 1fr 1fr;gap:36px;max-width:1100px;margin:0 auto;padding-bottom:32px;border-bottom:1px solid rgba(255,255,255,.08)}
.fb-name{font-family:'Baloo 2',cursive;font-size:19px;font-weight:800;color:var(--white);margin-bottom:4px}
.fb-loc{font-size:11px;color:rgba(255,255,255,.45);margin-bottom:12px}
.fb-desc{font-size:12px;color:rgba(255,255,255,.55);line-height:1.75}
.footer-col h5{font-size:11px;font-weight:700;color:var(--gold-light);letter-spacing:1.5px;text-transform:uppercase;margin-bottom:14px}
.footer-col ul{list-style:none;display:flex;flex-direction:column;gap:7px}
.footer-col ul li a{font-size:13px;color:rgba(255,255,255,.55);text-decoration:none;transition:color .2s;cursor:pointer}
.footer-col ul li a:hover{color:var(--gold-light)}
.fc-contact{font-size:12.5px;color:rgba(255,255,255,.55);display:flex;flex-direction:column;gap:8px}
.fc-contact span{display:flex;align-items:center;gap:8px}
.footer-bottom{max-width:1100px;margin:0 auto;padding:16px 0;display:flex;justify-content:space-between;align-items:center;font-size:11px;color:rgba(255,255,255,.3)}

/* ══ FLOATING WHATSAPP (bonus) ══ */
.whatsapp-float{position:fixed;bottom:28px;right:28px;width:56px;height:56px;background:#25D366;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:26px;cursor:pointer;box-shadow:0 6px 20px rgba(37,211,102,.45);z-index:8888;transition:all .3s;text-decoration:none;animation:bounceIn .8s ease 1s both}
.whatsapp-float:hover{transform:scale(1.15);box-shadow:0 10px 30px rgba(37,211,102,.55)}

/* ══ TOAST ══ */
.toast{position:fixed;bottom:28px;left:50%;transform:translateX(-50%);background:var(--green);color:var(--white);padding:13px 22px;border-radius:10px;font-size:13.5px;font-weight:600;box-shadow:var(--shadow);display:none;z-index:9999;animation:fadeUp .3s ease;white-space:nowrap}

/* ══ ANIMATIONS ══ */
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes fadeUp{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:translateY(0)}}
@keyframes popUp{from{opacity:0;transform:scale(.85)}to{opacity:1;transform:scale(1)}}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
@keyframes bounceIn{0%{opacity:0;transform:scale(.3)}50%{opacity:1;transform:scale(1.08)}70%{transform:scale(.95)}100%{transform:scale(1)}}

/* ══ MOBILE ══ */
@media(max-width:768px){
  .features-grid,.gallery-grid,.testimonials-grid,.team-grid,.process-grid,.docs-grid{grid-template-columns:1fr 1fr}
  .about-grid,.vm-grid,.events-grid,.contact-grid,.footer-grid{grid-template-columns:1fr}
  .stats-strip{flex-wrap:wrap}
  .stat-item{border-right:none;border-bottom:1px solid #eee;width:50%;padding:16px}
  .hero .slide-content h1{font-size:34px}
  .navbar{flex-wrap:wrap;padding:0 16px}
  .hamburger{display:flex}
  .nav-links{display:none;width:100%;flex-direction:column;padding:10px 0 16px;gap:4px}
  .nav-links.open{display:flex}
  .nav-links a{border-radius:8px}
  .topbar{padding:6px 16px;font-size:10px;flex-direction:column;gap:4px}
  .offer-box{flex-direction:column}
  .form-row{grid-template-columns:1fr}
  .gallery-item.large{grid-column:span 1;grid-row:span 1}
}
</style>
</head>
<body>

<!-- ════ POPUP ════ -->
<div class="popup-overlay" id="popup">
  <div class="popup-box">
    <div class="popup-header">
      <h3>🌟 Admission Open 2026–27!</h3>
      <p>न्यू मॉडर्न इंग्लिश स्कूल, मोहनपुर, सहरसा</p>
      <button class="popup-close" onclick="closePopup()">✕</button>
    </div>
    <div class="popup-body">
      <div class="popup-offer">
        <div class="po-title">🎁 Early Bird Special Offer</div>
        <p><b>10 अप्रैल 2026 से पहले</b> नामांकन पर<br>
        ✨ प्रवेश शुल्क <b>पूर्णतः निःशुल्क</b><br>
        ⭐ पहले आएं — <b>ज्यादा छूट पाएं!</b></p>
      </div>
      <div class="popup-date">
        <div class="pd-icon">⚠️</div>
        <div class="pd-text">सीमित सीटें बची हैं — आज ही संपर्क करें!<br><span style="color:var(--green);font-size:12px">📞 9113788228</span></div>
      </div>
      <button class="popup-btn" onclick="closePopup();showPage('admissions')">अभी प्रवेश लें →</button>
    </div>
  </div>
</div>

<!-- ════ TOPBAR ════ -->
<div class="topbar">
  <span>📜 Reg: SAH-PVT SCHOOL/NMES-0180/2020 &nbsp;|&nbsp; बिहार सरकार द्वारा मान्यता प्राप्त</span>
  <div class="tb-right">
    <span>📞 <a href="tel:9113788228">9113788228</a></span>
    <span>📍 मोहनपुर, नौहट्टा, सहरसा</span>
  </div>
</div>

<!-- ════ NAVBAR ════ -->
<nav class="navbar">
  <div class="nav-brand">
    <div class="nav-logo">📚</div>
    <div>
      <div class="brand-name">न्यू मॉडर्न इंग्लिश स्कूल</div>
      <div class="brand-loc">मोहनपुर, नौहट्टा, सहरसा</div>
    </div>
  </div>
  <div class="hamburger" onclick="toggleMenu()" id="hamburger">
    <span></span><span></span><span></span>
  </div>
  <ul class="nav-links" id="navLinks">
    <li><a class="active" onclick="showPage('home',this)">🏠 होम</a></li>
    <li><a onclick="showPage('about',this)">🏫 हमारे बारे में</a></li>
    <li><a onclick="showPage('admissions',this)">🎓 प्रवेश</a></li>
    <li><a onclick="showPage('contact',this)">📞 संपर्क</a></li>
    <li><a class="nav-cta" onclick="showPage('admissions',this)">अभी आवेदन करें →</a></li>
  </ul>
</nav>

<!-- ════════════════════
     HOME PAGE
════════════════════ -->
<div id="home" class="page-section active">

  <!-- CAROUSEL -->
  <div class="carousel" id="carousel">
    <div class="carousel-track" id="track">
      <div class="slide slide-1">
        <div class="slide-bg"></div><div class="slide-overlay"></div><div class="slide-pattern"></div>
        <div class="slide-content">
          <div class="slide-badge">🌟 कोसी क्षेत्र में 11 वर्षों का भरोसा</div>
          <h1>बच्चों का <span class="gold">उज्ज्वल भविष्य</span><br>हमारी जिम्मेदारी</h1>
          <p>आधुनिक शिक्षा, अनुशासन और नैतिक मूल्यों के साथ<br>हर बच्चे की प्रतिभा को निखारा जाता है।</p>
          <div class="slide-btns">
            <button class="btn-primary" onclick="showPage('admissions')">प्रवेश लें 2026–27 →</button>
            <button class="btn-outline" onclick="showPage('about')">और जानें</button>
          </div>
        </div>
      </div>
      <div class="slide slide-2">
        <div class="slide-bg"></div><div class="slide-overlay"></div><div class="slide-pattern"></div>
        <div class="slide-content">
          <div class="slide-badge">📚 अंग्रेजी माध्यम विद्यालय</div>
          <h1>Concept Clear <span class="gold">पढ़ाई</span> से<br>सफलता की राह</h1>
          <p>हर विषय को जड़ से समझाना हमारी प्राथमिकता है।<br>अनुभवी शिक्षकों की देखरेख में बेहतरीन शिक्षा।</p>
          <div class="slide-btns">
            <button class="btn-primary" onclick="showPage('admissions')">अभी नामांकन करें</button>
            <button class="btn-outline" onclick="showPage('contact')">संपर्क करें</button>
          </div>
        </div>
      </div>
      <div class="slide slide-3">
        <div class="slide-bg"></div><div class="slide-overlay"></div><div class="slide-pattern"></div>
        <div class="slide-content">
          <div class="slide-badge">🎁 Special Offer — सीमित समय</div>
          <h1>10 अप्रैल से पहले<br><span class="gold">प्रवेश निःशुल्क!</span></h1>
          <p>Early Bird Offer — पहले आएं, ज्यादा छूट पाएं!<br>⚠️ सीमित सीटें उपलब्ध — अभी संपर्क करें</p>
          <div class="slide-btns">
            <button class="btn-primary" onclick="showPage('admissions')">ऑफर देखें →</button>
            <button class="btn-outline" onclick="window.open('tel:9113788228')">📞 Call करें</button>
          </div>
        </div>
      </div>
    </div>
    <button class="carousel-prev" onclick="moveSlide(-1)">❮</button>
    <button class="carousel-next" onclick="moveSlide(1)">❯</button>
    <div class="carousel-dots" id="dots">
      <div class="dot active" onclick="goSlide(0)"></div>
      <div class="dot" onclick="goSlide(1)"></div>
      <div class="dot" onclick="goSlide(2)"></div>
    </div>
  </div>

  <!-- NOTICE BAR -->
  <div class="notice-bar">
    <div class="notice-scroll">
      <span class="nb-badge">नया</span>
      <span class="nb-text">🌟 Admission Open 2026–27 — <b>10 अप्रैल से पहले नामांकन पर प्रवेश निःशुल्क!</b> &nbsp;⚠️ सीमित सीटें &nbsp;|&nbsp; 📞 9113788228 &nbsp;|&nbsp;</span>
      <span class="nb-badge">नया</span>
      <span class="nb-text">🌟 Admission Open 2026–27 — <b>10 अप्रैल से पहले नामांकन पर प्रवेश निःशुल्क!</b> &nbsp;⚠️ सीमित सीटें &nbsp;|&nbsp; 📞 9113788228</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-strip" id="stats">
    <div class="stat-item"><div class="stat-num">11<span>+</span></div><div class="stat-label">वर्षों का अनुभव</div></div>
    <div class="stat-item"><div class="stat-num">500<span>+</span></div><div class="stat-label">सफल छात्र</div></div>
    <div class="stat-item"><div class="stat-num">10<span>+</span></div><div class="stat-label">अनुभवी शिक्षक</div></div>
    <div class="stat-item"><div class="stat-num">Nur<span>–8</span></div><div class="stat-label">कक्षाएं उपलब्ध</div></div>
  </div>

  <!-- FEATURES -->
  <div style="background:var(--cream);padding:56px 0">
    <div class="section">
      <div class="section-header">
        <div class="eyebrow">हमारी विशेषताएँ</div>
        <div class="sec-title">क्यों चुनें <span>न्यू मॉडर्न इंग्लिश स्कूल?</span></div>
        <div class="sec-line"></div>
      </div>
      <div class="features-grid" id="featGrid">
        <div class="feature-card"><div class="fc-icon">📖</div><div class="fc-title">Concept Clear पढ़ाई</div><div class="fc-desc">हर विषय को जड़ से समझाना हमारी प्राथमिकता।</div></div>
        <div class="feature-card"><div class="fc-icon">👨‍🏫</div><div class="fc-title">अनुभवी शिक्षक</div><div class="fc-desc">समर्पित और प्रशिक्षित शिक्षक जो बच्चों को प्रेरित करते हैं।</div></div>
        <div class="feature-card"><div class="fc-icon">🗣️</div><div class="fc-title">Spoken English</div><div class="fc-desc">रोज़ बोलचाल के अभ्यास से आत्मविश्वास का विकास।</div></div>
        <div class="feature-card"><div class="fc-icon">📊</div><div class="fc-title">नियमित टेस्ट</div><div class="fc-desc">प्रगति रिपोर्ट से अभिभावकों को हमेशा अपडेट।</div></div>
        <div class="feature-card"><div class="fc-icon">⚽</div><div class="fc-title">खेलकूद</div><div class="fc-desc">शारीरिक विकास के लिए खेल और सांस्कृतिक गतिविधियाँ।</div></div>
        <div class="feature-card"><div class="fc-icon">🛡️</div><div class="fc-title">सुरक्षित वातावरण</div><div class="fc-desc">स्वच्छ, सुरक्षित और अनुशासित परिसर।</div></div>
        <div class="feature-card"><div class="fc-icon">🏛️</div><div class="fc-title">नैतिक शिक्षा</div><div class="fc-desc">संस्कार और मूल्यों पर आधारित शिक्षण पद्धति।</div></div>
        <div class="feature-card"><div class="fc-icon">🚐</div><div class="fc-title">वैन सुविधा</div><div class="fc-desc">सुरक्षित स्कूल वैन सेवा उपलब्ध।</div></div>
      </div>
    </div>
  </div>

  <!-- PHOTO GALLERY -->
  <div class="gallery-section">
    <div style="max-width:1100px;margin:0 auto">
      <div class="section-header">
        <div class="eyebrow" style="color:var(--gold-light)">तस्वीरें</div>
        <div class="sec-title" style="color:var(--white)">हमारे स्कूल की <span style="color:var(--gold-light)">गैलरी</span></div>
        <div class="sec-line"></div>
        <p style="color:rgba(255,255,255,0.6);font-size:12px;margin-top:8px">नीचे "फोटो जोड़ें" बटन से अपनी असली तस्वीरें upload करें</p>
      </div>
    </div>
    <div class="gallery-grid" id="galleryGrid">
      <div class="gallery-item large" onclick="openLightbox(this)">
        <div class="gallery-bg"><div class="gi-icon">🏫</div><div class="gi-label">स्कूल भवन<br>मुख्य द्वार</div></div>
      </div>
      <div class="gallery-item" onclick="openLightbox(this)"><div class="gallery-bg"><div class="gi-icon">📚</div><div class="gi-label">कक्षाकक्ष</div></div></div>
      <div class="gallery-item" onclick="openLightbox(this)"><div class="gallery-bg"><div class="gi-icon">🎌</div><div class="gi-label">स्वतंत्रता दिवस</div></div></div>
      <div class="gallery-item" onclick="openLightbox(this)"><div class="gallery-bg"><div class="gi-icon">⚽</div><div class="gi-label">खेल का मैदान</div></div></div>
      <div class="gallery-item" onclick="openLightbox(this)"><div class="gallery-bg"><div class="gi-icon">🎭</div><div class="gi-label">सांस्कृतिक कार्यक्रम</div></div></div>
      <div class="gallery-item" onclick="openLightbox(this)"><div class="gallery-bg"><div class="gi-icon">🏆</div><div class="gi-label">पुरस्कार समारोह</div></div></div>
    </div>
    <input type="file" id="gallery-file-input" accept="image/*" multiple onchange="addPhotos(event)">
    <div style="text-align:center;margin-top:20px">
      <button class="gallery-upload-btn" onclick="document.getElementById('gallery-file-input').click()">📸 फोटो जोड़ें</button>
    </div>
  </div>

  <!-- TESTIMONIALS -->
  <div class="testimonials-section">
    <div class="testimonials-wrap">
      <div class="section-header">
        <div class="eyebrow" style="color:var(--gold-light)">अभिभावकों की राय</div>
        <div class="sec-title" style="color:var(--white)">Parents के <span style="color:var(--gold-light)">अनुभव</span></div>
        <div class="sec-line"></div>
      </div>
      <div class="testimonials-grid" id="testiGrid">
        <div class="testi-card">
          <div class="testi-stars">★★★★★</div>
          <div class="testi-text">"मेरे बेटे को यहाँ आकर बहुत फायदा हुआ। Spoken English में जो सुधार आया है वो कमाल है। शिक्षक बहुत समर्पित हैं।"</div>
          <div class="testi-author"><div class="testi-avatar">👩</div><div><div class="testi-name">सुनीता देवी</div><div class="testi-role">कक्षा 5 के छात्र की माँ</div></div></div>
        </div>
        <div class="testi-card">
          <div class="testi-stars">★★★★★</div>
          <div class="testi-text">"बच्चों का सर्वांगीण विकास यहाँ सच में होता है। पढ़ाई के साथ-साथ खेलकूद और अनुशासन पर भी ध्यान दिया जाता है।"</div>
          <div class="testi-author"><div class="testi-avatar">👨</div><div><div class="testi-name">रामेश्वर प्रसाद</div><div class="testi-role">कक्षा 7 के छात्र के पिता</div></div></div>
        </div>
        <div class="testi-card">
          <div class="testi-stars">★★★★★</div>
          <div class="testi-text">"इस स्कूल में पढ़ाई का माहौल बहुत अच्छा है। मेरी बेटी का आत्मविश्वास पहले से काफी बढ़ा है। बहुत अच्छा स्कूल है।"</div>
          <div class="testi-author"><div class="testi-avatar">👩</div><div><div class="testi-name">गीता कुमारी</div><div class="testi-role">कक्षा 3 की छात्रा की माँ</div></div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- EVENTS CALENDAR -->
  <div class="events-section">
    <div class="events-wrap">
      <div class="section-header">
        <div class="eyebrow">कार्यक्रम</div>
        <div class="sec-title">आने वाले <span>कार्यक्रम</span></div>
        <div class="sec-line"></div>
      </div>
      <div class="events-grid">
        <div class="calendar-widget">
          <div class="cal-header">
            <button class="cal-nav" onclick="changeMonth(-1)">❮</button>
            <div class="cal-month" id="calMonth">मार्च 2026</div>
            <button class="cal-nav" onclick="changeMonth(1)">❯</button>
          </div>
          <div class="cal-days-header">
            <div class="cal-day-name">रवि</div><div class="cal-day-name">सोम</div>
            <div class="cal-day-name">मंगल</div><div class="cal-day-name">बुध</div>
            <div class="cal-day-name">गुरु</div><div class="cal-day-name">शुक्र</div>
            <div class="cal-day-name">शनि</div>
          </div>
          <div class="cal-days" id="calDays"></div>
        </div>
        <div class="events-list">
          <div class="event-item">
            <div class="event-date-box" style="background:var(--red)"><div class="ed-day">10</div><div class="ed-mon">APR</div></div>
            <div class="event-info"><div class="ei-title">Early Bird Offer Last Date</div><div class="ei-desc">10 अप्रैल तक नामांकन पर प्रवेश निःशुल्क</div><span class="ei-tag">प्रवेश</span></div>
          </div>
          <div class="event-item">
            <div class="event-date-box"><div class="ed-day">14</div><div class="ed-mon">APR</div></div>
            <div class="event-info"><div class="ei-title">अंबेडकर जयंती समारोह</div><div class="ei-desc">सांस्कृतिक कार्यक्रम एवं भाषण प्रतियोगिता</div><span class="ei-tag">कार्यक्रम</span></div>
          </div>
          <div class="event-item">
            <div class="event-date-box"><div class="ed-day">01</div><div class="ed-mon">JUN</div></div>
            <div class="event-info"><div class="ei-title">नया सत्र 2026–27 शुरू</div><div class="ei-desc">सभी कक्षाओं का नया सत्र आरम्भ</div><span class="ei-tag">शिक्षा</span></div>
          </div>
          <div class="event-item">
            <div class="event-date-box" style="background:#1565c0"><div class="ed-day">15</div><div class="ed-mon">AUG</div></div>
            <div class="event-info"><div class="ei-title">स्वतंत्रता दिवस समारोह</div><div class="ei-desc">ध्वजारोहण एवं सांस्कृतिक कार्यक्रम</div><span class="ei-tag">राष्ट्रीय</span></div>
          </div>
        </div>
      </div>
    </div>
  </div>

</div><!-- /home -->

<!-- ════════════════════
     ABOUT PAGE
════════════════════ -->
<div id="about" class="page-section">
  <div class="page-hero">
    <h2>🏫 हमारे बारे में</h2>
    <p>जानिए हमारी कहानी, हमारी सोच और हमारे लक्ष्य</p>
  </div>
  <div style="padding:52px 32px">
    <div class="about-grid" style="margin-bottom:46px">
      <div class="about-img"><div class="ai-icon">🏫</div><div class="ai-text">स्कूल की तस्वीर</div></div>
      <div class="about-text">
        <h3>कोसी क्षेत्र का विश्वसनीय शिक्षण संस्थान</h3>
        <p>आवासीय न्यू मॉडर्न इंग्लिश स्कूल, 2015 से <b>बिहार सरकार द्वारा मान्यता प्राप्त</b> विद्यालय है जो मोहनपुर, नौहट्टा, सहरसा में स्थित है।</p>
        <p>हमारा मानना है कि <b>शिक्षा केवल किताबों तक सीमित नहीं होनी चाहिए</b> — बच्चों में आत्मविश्वास, नैतिक मूल्य और व्यावहारिक कौशल का विकास उतना ही जरूरी है।</p>
        <div class="hp-list">
          <div class="hp-item"><div class="hp-dot">✓</div> नर्सरी से कक्षा 8वीं तक — अंग्रेजी माध्यम</div>
          <div class="hp-item"><div class="hp-dot">✓</div> 11 वर्षों का सफल शैक्षणिक अनुभव</div>
          <div class="hp-item"><div class="hp-dot">✓</div> Reg. No.: SAH-PVT SCHOOL/NMES-0180/2020</div>
          <div class="hp-item"><div class="hp-dot">✓</div> आवासीय सुविधा उपलब्ध</div>
        </div>
      </div>
    </div>
    <div class="vm-grid" style="margin-bottom:46px">
      <div class="vm-card vision"><span class="vm-icon">🌟</span><h4>हमारी दृष्टि</h4><p>एक ऐसा संस्थान जहाँ हर बच्चा अपनी पूरी क्षमता पहचाने और एक जिम्मेदार नागरिक बने।</p></div>
      <div class="vm-card mission"><span class="vm-icon">🎯</span><h4>हमारा मिशन</h4><p>आधुनिक शिक्षण पद्धतियों और नैतिक मूल्यों के माध्यम से बच्चों में आत्मविश्वास, ज्ञान और चरित्र का निर्माण करना।</p></div>
    </div>
    <div class="section-header" style="margin-bottom:28px">
      <div class="eyebrow">हमारी टीम</div>
      <div class="sec-title">अनुभवी <span>शिक्षक एवं स्टाफ</span></div>
      <div class="sec-line"></div>
    </div>
    <div class="team-grid">
      <div class="team-card"><div class="team-avatar">👨‍💼</div><div class="team-name">सिंधु कुमार सिंह</div><div class="team-role">निदेशक</div><div class="team-desc">11 वर्षों से शिक्षा क्षेत्र में समर्पित। बच्चों के विकास के लिए प्रतिबद्ध।</div></div>
      <div class="team-card"><div class="team-avatar">👩‍🏫</div><div class="team-name">वरिष्ठ शिक्षिका</div><div class="team-role">प्राथमिक विभाग</div><div class="team-desc">नर्सरी से कक्षा 5 तक के बच्चों की शिक्षा की देखरेख।</div></div>
      <div class="team-card"><div class="team-avatar">👨‍🏫</div><div class="team-name">वरिष्ठ शिक्षक</div><div class="team-role">उच्च प्राथमिक विभाग</div><div class="team-desc">कक्षा 6–8 विज्ञान, गणित और अंग्रेजी के विशेषज्ञ।</div></div>
    </div>
  </div>
</div>

<!-- ════════════════════
     ADMISSIONS PAGE
════════════════════ -->
<div id="admissions" class="page-section">
  <div class="adm-hero">
    <div class="adm-badge">🌟 ADMISSION OPEN 2026–27</div>
    <h2>प्रवेश प्रक्रिया</h2>
    <p>सत्र 2026–27 के लिए नामांकन शुरू — अभी सीट सुरक्षित करें</p>
  </div>
  <div style="padding:52px 32px">
    <div class="section-header" style="margin-bottom:32px">
      <div class="eyebrow">प्रवेश के चरण</div>
      <div class="sec-title">आसान <span>4 Steps में प्रवेश</span></div>
      <div class="sec-line"></div>
    </div>
    <div class="process-grid" style="margin-bottom:46px">
      <div class="process-card"><div class="process-num">1</div><div class="process-icon">📞</div><div class="process-title">संपर्क करें</div><div class="process-desc">9113788228 पर call करें या स्कूल आएं।</div></div>
      <div class="process-card"><div class="process-num">2</div><div class="process-icon">📋</div><div class="process-title">फॉर्म भरें</div><div class="process-desc">प्रवेश फॉर्म भरें और दस्तावेज जमा करें।</div></div>
      <div class="process-card"><div class="process-num">3</div><div class="process-icon">✅</div><div class="process-title">पुष्टि करें</div><div class="process-desc">सीट की पुष्टि के बाद शुल्क जमा करें।</div></div>
      <div class="process-card"><div class="process-num">4</div><div class="process-icon">🎒</div><div class="process-title">शुरुआत!</div><div class="process-desc">नई कक्षा में अपने बच्चे का स्वागत!</div></div>
    </div>
    <div style="max-width:1100px;margin:0 auto 44px;border-radius:12px;overflow:hidden;box-shadow:var(--shadow)">
      <table class="classes-table">
        <thead><tr><th>कक्षा</th><th>आयु</th><th>माध्यम</th><th>सीटें</th><th>स्थिति</th></tr></thead>
        <tbody>
          <tr><td>नर्सरी</td><td>3–4 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>LKG</td><td>4–5 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>UKG</td><td>5–6 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>कक्षा 1–3</td><td>6–9 वर्ष</td><td>अंग्रेजी</td><td>35</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>कक्षा 4–5</td><td>9–11 वर्ष</td><td>अंग्रेजी</td><td>35</td><td><span class="badge-open">खुली है</span></td></tr>
          <tr><td>कक्षा 6–8</td><td>11–14 वर्ष</td><td>अंग्रेजी</td><td>30</td><td><span class="badge-open">खुली है</span></td></tr>
        </tbody>
      </table>
    </div>
    <div class="offer-box" style="margin-bottom:44px">
      <div class="offer-left">
        <h3>🎁 Early Bird Special Offer!</h3>
        <p><b>10 अप्रैल 2026 से पहले</b> नामांकन पर —<br>✨ प्रवेश शुल्क <b>पूर्णतः निःशुल्क</b><br>⭐ पहले आएं, <b>ज्यादा छूट पाएं!</b><br>⚠️ सीमित सीटें — जल्द संपर्क करें!</p>
      </div>
      <div class="offer-right"><span class="or1">ऑफर तक</span><span class="or2">10 अप्रैल<br>2026</span></div>
    </div>
    <div class="section-header" style="margin-bottom:22px">
      <div class="eyebrow">आवश्यक दस्तावेज</div>
      <div class="sec-title">प्रवेश के लिए <span>जरूरी कागजात</span></div>
      <div class="sec-line"></div>
    </div>
    <div class="docs-grid">
      <div class="doc-item"><span class="doc-icon">📸</span><div><div class="doc-title">पासपोर्ट फोटो</div><div class="doc-sub">बच्चे की 2 नवीनतम फोटो</div></div></div>
      <div class="doc-item"><span class="doc-icon">🎂</span><div><div class="doc-title">जन्म प्रमाण पत्र</div><div class="doc-sub">आयु सत्यापन के लिए</div></div></div>
      <div class="doc-item"><span class="doc-icon">📄</span><div><div class="doc-title">पुरानी मार्कशीट</div><div class="doc-sub">पिछली कक्षा की रिपोर्ट</div></div></div>
      <div class="doc-item"><span class="doc-icon">🪪</span><div><div class="doc-title">आधार कार्ड</div><div class="doc-sub">बच्चे / अभिभावक का</div></div></div>
      <div class="doc-item"><span class="doc-icon">📋</span><div><div class="doc-title">TC (Transfer Certificate)</div><div class="doc-sub">पुराने स्कूल से (यदि लागू)</div></div></div>
      <div class="doc-item"><span class="doc-icon">🏠</span><div><div class="doc-title">पता प्रमाण</div><div class="doc-sub">निवास का कोई प्रमाण</div></div></div>
    </div>
  </div>
</div>

<!-- ════════════════════
     CONTACT PAGE
════════════════════ -->
<div id="contact" class="page-section">
  <div class="page-hero">
    <h2>📞 संपर्क करें</h2>
    <p>किसी भी जानकारी के लिए हमसे संपर्क करें — हम सदैव तत्पर हैं</p>
  </div>
  <div style="padding:52px 32px">
    <div class="contact-grid">
      <div>
        <h3 style="font-family:'Baloo 2',cursive;font-size:26px;font-weight:800;color:var(--green-dark);margin-bottom:20px">हमसे मिलें</h3>
        <div class="ci-item"><div class="ci-icon">👨‍💼</div><div><div class="ci-label">निदेशक</div><div class="ci-value">सिंधु कुमार सिंह</div></div></div>
        <div class="ci-item"><div class="ci-icon">📞</div><div><div class="ci-label">मोबाइल</div><div class="ci-value">9113788228</div><div class="ci-sub">सुबह 8 बजे से शाम 6 बजे तक</div></div></div>
        <div class="ci-item"><div class="ci-icon">📍</div><div><div class="ci-label">पता</div><div class="ci-value">मोहनपुर, नौहट्टा, सहरसा</div><div class="ci-sub">बिहार, भारत</div></div></div>
        <div class="ci-item"><div class="ci-icon">🕐</div><div><div class="ci-label">स्कूल समय</div><div class="ci-value">सोम–शनि: 8:00 AM – 2:00 PM</div><div class="ci-sub">रविवार: बंद</div></div></div>
        <div class="map-ph"><div class="mp-icon">🗺️</div><div class="mp-text">मोहनपुर, नौहट्टा, सहरसा — बिहार</div></div>
      </div>
      <div class="contact-form">
        <h3>संदेश भेजें</h3>
        <div class="form-row">
          <div class="form-group"><label>नाम *</label><input type="text" placeholder="आपका पूरा नाम" id="f-name"></div>
          <div class="form-group"><label>मोबाइल *</label><input type="tel" placeholder="10 अंकों का नंबर" id="f-phone"></div>
        </div>
        <div class="form-group"><label>बच्चे का नाम</label><input type="text" placeholder="बच्चे का पूरा नाम" id="f-child"></div>
        <div class="form-group"><label>कक्षा चाहिए</label>
          <select id="f-class">
            <option value="">-- कक्षा चुनें --</option>
            <option>नर्सरी</option><option>LKG</option><option>UKG</option>
            <option>कक्षा 1</option><option>कक्षा 2</option><option>कक्षा 3</option>
            <option>कक्षा 4</option><option>कक्षा 5</option><option>कक्षा 6</option>
            <option>कक्षा 7</option><option>कक्षा 8</option>
          </select>
        </div>
        <div class="form-group"><label>संदेश</label><textarea placeholder="अपना प्रश्न यहाँ लिखें..." id="f-msg"></textarea></div>
        <button class="form-submit" onclick="submitForm()">📨 संदेश भेजें</button>
      </div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer class="footer">
  <div class="footer-grid">
    <div><div class="fb-name">📚 न्यू मॉडर्न इंग्लिश स्कूल</div><div class="fb-loc">मोहनपुर, नौहट्टा, सहरसा — बिहार</div><div class="fb-desc">कोसी क्षेत्र में 11 वर्षों से गुणवत्तापूर्ण शिक्षा प्रदान करते हुए बच्चों के उज्ज्वल भविष्य की नींव रख रहे हैं।</div></div>
    <div class="footer-col"><h5>Quick Links</h5><ul>
      <li><a onclick="showPage('home')">🏠 होम</a></li>
      <li><a onclick="showPage('about')">🏫 हमारे बारे में</a></li>
      <li><a onclick="showPage('admissions')">🎓 प्रवेश 2026–27</a></li>
      <li><a onclick="showPage('contact')">📞 संपर्क करें</a></li>
    </ul></div>
    <div class="footer-col"><h5>संपर्क</h5><div class="fc-contact">
      <span>📞 9113788228</span>
      <span>📍 मोहनपुर, नौहट्टा, सहरसा</span>
      <span>🕐 सोम–शनि: 8AM – 2PM</span>
      <span>📜 Reg: SAH-PVT SCHOOL/NMES-0180/2020</span>
    </div></div>
  </div>
  <div class="footer-bottom">
    <span>© 2026 न्यू मॉडर्न इंग्लिश स्कूल — सभी अधिकार सुरक्षित</span>
    <span>आपके बच्चे का सपना, हमारी जिम्मेदारी 🌟</span>
  </div>
</footer>

<!-- FLOATING WHATSAPP -->
<a class="whatsapp-float" href="https://wa.me/919113788228?text=नमस्ते! मुझे प्रवेश के बारे में जानकारी चाहिए।" target="_blank">💬</a>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
  <button class="lightbox-close" onclick="closeLightbox()">✕</button>
  <img id="lightbox-img" src="" alt="">
</div>

<!-- TOAST -->
<div class="toast" id="toast">✅ संदेश सफलतापूर्वक भेजा गया!</div>

<script>
// ── PAGE NAVIGATION ──
function showPage(id, el) {
  document.querySelectorAll('.page-section').forEach(p => p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
  document.querySelectorAll('.nav-links a').forEach(a => {
    if(a.getAttribute('onclick') && a.getAttribute('onclick').includes("'"+id+"'")) a.classList.add('active');
  });
  window.scrollTo({top:0,behavior:'smooth'});
  // close mobile menu
  document.getElementById('navLinks').classList.remove('open');
  // trigger animations
  setTimeout(()=>{ observeElements(); }, 100);
}

// ── HAMBURGER ──
function toggleMenu(){
  document.getElementById('navLinks').classList.toggle('open');
}

// ── POPUP ──
window.addEventListener('load', ()=>{ setTimeout(()=>{ document.getElementById('popup').style.display='flex'; },1500); });
function closePopup(){ document.getElementById('popup').style.display='none'; }

// ── CAROUSEL ──
let currentSlide = 0;
const totalSlides = 3;
let autoSlide = setInterval(()=>moveSlide(1), 4500);

function moveSlide(dir){
  currentSlide = (currentSlide + dir + totalSlides) % totalSlides;
  updateCarousel();
  resetAuto();
}
function goSlide(n){ currentSlide = n; updateCarousel(); resetAuto(); }
function updateCarousel(){
  document.getElementById('track').style.transform = `translateX(-${currentSlide*100}%)`;
  document.querySelectorAll('.dot').forEach((d,i)=>{ d.classList.toggle('active',i===currentSlide); });
}
function resetAuto(){ clearInterval(autoSlide); autoSlide = setInterval(()=>moveSlide(1),4500); }

// ── SCROLL ANIMATIONS ──
function observeElements(){
  const obs = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('visible'); } });
  },{threshold:0.1});
  document.querySelectorAll('.feature-card,.testi-card,.stat-item').forEach(el=>obs.observe(el));
  // staggered delay
  document.querySelectorAll('.feature-card').forEach((c,i)=>{ c.style.transitionDelay = (i*0.07)+'s'; });
  document.querySelectorAll('.testi-card').forEach((c,i)=>{ c.style.transitionDelay = (i*0.1)+'s'; });
  document.querySelectorAll('.stat-item').forEach((c,i)=>{ c.style.transitionDelay = (i*0.1)+'s'; });
}
document.addEventListener('DOMContentLoaded', observeElements);

// ── GALLERY UPLOAD ──
let galleryImages = [];
function addPhotos(event){
  const files = Array.from(event.target.files);
  const grid = document.getElementById('galleryGrid');
  files.forEach(file=>{
    const url = URL.createObjectURL(file);
    galleryImages.push(url);
    const item = document.createElement('div');
    item.className = 'gallery-item';
    item.style.backgroundImage = `url(${url})`;
    item.style.backgroundSize = 'cover';
    item.style.backgroundPosition = 'center';
    item.setAttribute('data-src', url);
    item.onclick = function(){ openLightboxImg(url); };
    grid.insertBefore(item, grid.firstChild);
  });
  showToast('📸 '+files.length+' फोटो जोड़ी गई!');
}
function openLightbox(el){
  const src = el.getAttribute('data-src');
  if(src){ openLightboxImg(src); }
}
function openLightboxImg(src){
  if(!src) return;
  document.getElementById('lightbox-img').src = src;
  document.getElementById('lightbox').classList.add('open');
}
function closeLightbox(){ document.getElementById('lightbox').classList.remove('open'); }

// ── CALENDAR ──
const months = ['जनवरी','फरवरी','मार्च','अप्रैल','मई','जून','जुलाई','अगस्त','सितंबर','अक्टूबर','नवंबर','दिसंबर'];
const eventDays = {3:[10,14,25], 4:[1,5,15], 5:[1,10]};
let calDate = new Date(2026,2,1);

function renderCal(){
  const y = calDate.getFullYear(), m = calDate.getMonth();
  document.getElementById('calMonth').textContent = months[m]+' '+y;
  const first = new Date(y,m,1).getDay();
  const days = new Date(y,m+1,0).getDate();
  const today = new Date();
  let html = '';
  for(let i=0;i<first;i++) html += `<div class="cal-day empty"></div>`;
  for(let d=1;d<=days;d++){
    const isToday = (d===today.getDate() && m===today.getMonth() && y===today.getFullYear());
    const hasEvent = eventDays[m] && eventDays[m].includes(d);
    html += `<div class="cal-day${isToday?' today':''}${hasEvent?' has-event':''}" title="${hasEvent?'कार्यक्रम है':''}">${d}</div>`;
  }
  document.getElementById('calDays').innerHTML = html;
}
function changeMonth(dir){ calDate.setMonth(calDate.getMonth()+dir); renderCal(); }
renderCal();

// ── CONTACT FORM ──
function submitForm(){
  const name = document.getElementById('f-name').value.trim();
  const phone = document.getElementById('f-phone').value.trim();
  if(!name||!phone){ alert('कृपया नाम और मोबाइल नंबर भरें।'); return; }
  showToast('✅ संदेश सफलतापूर्वक भेजा गया! हम जल्द संपर्क करेंगे।');
  ['f-name','f-phone','f-child','f-msg'].forEach(id=>{ document.getElementById(id).value=''; });
  document.getElementById('f-class').value='';
}

function showToast(msg){
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.style.display = 'block';
  setTimeout(()=>{ t.style.display='none'; }, 3500);
}
</script>
</body>
</html>
