<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Md. Ariful Islam — Pharmaceutical Professional</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet"/>
<style>
:root{
  --accent:#2563eb;--accent2:#3b82f6;--accent-dim:#1d4ed8;
  --accent-glow:rgba(37,99,235,0.15);--accent-glow2:rgba(59,130,246,0.08);
  --bg:#06090f;--surface:#0d1320;--surface2:#111927;--surface3:#162035;
  --border:rgba(255,255,255,0.06);--border2:rgba(37,99,235,0.2);
  --text:#e2e8f5;--text-muted:#7a8faf;--text-dim:#3a5070;
  --nav-h:68px;--radius:18px;--transition:0.35s cubic-bezier(0.4,0,0.2,1);
}
[data-theme="light"]{
  --bg:#f8faff;--surface:#ffffff;--surface2:#eef2ff;--surface3:#e0e9ff;
  --border:rgba(0,0,0,0.06);--border2:rgba(37,99,235,0.2);
  --text:#0f172a;--text-muted:#475569;--text-dim:#94a3b8;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{font-family:'Inter',sans-serif;background:var(--bg);color:var(--text);line-height:1.65;transition:background var(--transition),color var(--transition);overflow-x:hidden;}

/* NAV */
nav{
  position:fixed;top:0;left:0;right:0;z-index:999;
  height:var(--nav-h);display:flex;align-items:center;justify-content:space-between;
  padding:0 clamp(1.5rem,5vw,4rem);
  background:rgba(6,9,15,0.8);
  backdrop-filter:blur(24px) saturate(1.6);
  border-bottom:1px solid var(--border);
  transition:background var(--transition);
}
[data-theme="light"] nav{background:rgba(248,250,255,0.88);}
.nav-logo{
  font-family:'Playfair Display',serif;font-size:1.1rem;font-weight:700;
  color:var(--accent2);letter-spacing:0.01em;text-decoration:none;
  display:flex;align-items:center;gap:0.5rem;
}
.nav-logo-dot{width:8px;height:8px;background:var(--accent);border-radius:50%;display:inline-block;animation:pulse 2.5s infinite;}
@keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(37,99,235,0.5)}50%{box-shadow:0 0 0 6px transparent}}
.nav-links{display:flex;gap:2.2rem;align-items:center;}
.nav-links a{font-size:0.8rem;font-weight:500;letter-spacing:0.07em;text-transform:uppercase;text-decoration:none;color:var(--text-muted);transition:color 0.2s;}
.nav-links a:hover{color:var(--accent2);}
.nav-right{display:flex;gap:0.75rem;align-items:center;}
.theme-toggle{
  width:40px;height:40px;border-radius:50%;border:1px solid var(--border);
  background:var(--surface);color:var(--text-muted);cursor:pointer;
  display:grid;place-items:center;font-size:1rem;
  transition:border-color 0.2s,background 0.2s;
}
.theme-toggle:hover{border-color:var(--accent2);color:var(--accent2);}
.nav-cta{
  padding:0.5rem 1.25rem;background:var(--accent);color:#fff;
  border-radius:50px;border:none;font-size:0.78rem;font-weight:600;
  letter-spacing:0.04em;text-decoration:none;
  transition:background 0.2s,transform 0.15s,box-shadow 0.2s;
  box-shadow:0 2px 12px rgba(37,99,235,0.3);
}
.nav-cta:hover{background:var(--accent-dim);transform:translateY(-1px);box-shadow:0 4px 20px rgba(37,99,235,0.45);}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:6px;background:none;border:none;}
.hamburger span{display:block;width:22px;height:2px;background:var(--text-muted);border-radius:2px;transition:all 0.3s;}

/* HERO */
#hero{
  min-height:100vh;display:flex;align-items:center;
  padding-top:var(--nav-h);
  padding-left:clamp(1.5rem,6vw,5rem);padding-right:clamp(1.5rem,6vw,5rem);
  position:relative;overflow:hidden;gap:4rem;max-width:1200px;margin:0 auto;
}
.hero-bg{
  position:fixed;top:0;left:0;right:0;bottom:0;pointer-events:none;z-index:-1;
  background:radial-gradient(ellipse 80% 60% at 70% 40%,rgba(37,99,235,0.07),transparent 70%),
             radial-gradient(ellipse 50% 40% at 20% 70%,rgba(59,130,246,0.05),transparent 60%);
}
.hero-text{flex:1;max-width:580px;}
.hero-eyebrow{
  display:inline-flex;align-items:center;gap:0.6rem;
  padding:0.4rem 1rem;margin-bottom:1.8rem;
  background:var(--accent-glow);border:1px solid var(--border2);
  border-radius:50px;font-size:0.73rem;font-weight:600;
  color:var(--accent2);letter-spacing:0.08em;text-transform:uppercase;
}
.hero-eyebrow .dot{width:6px;height:6px;background:var(--accent2);border-radius:50%;animation:pulse 2s infinite;}
.hero-text h1{
  font-family:'Playfair Display',serif;
  font-size:clamp(2.6rem,5.5vw,4rem);font-weight:700;
  line-height:1.08;margin-bottom:1rem;letter-spacing:-0.01em;
}
.hero-text h1 .name-hi{color:var(--accent2);}
.hero-role{
  font-size:1.05rem;color:var(--text-muted);
  margin-bottom:1.8rem;line-height:1.6;max-width:480px;
}
.hero-role strong{color:var(--text);font-weight:600;}
.hero-chips{display:flex;flex-wrap:wrap;gap:0.5rem;margin-bottom:2.2rem;}
.chip{
  padding:0.3rem 0.85rem;background:var(--surface2);border:1px solid var(--border);
  border-radius:50px;font-size:0.75rem;font-weight:500;color:var(--text-muted);
  transition:border-color 0.2s,color 0.2s;
}
.chip:hover{border-color:var(--accent2);color:var(--accent2);}
.hero-btns{display:flex;gap:1rem;flex-wrap:wrap;margin-bottom:3rem;}
.btn-blue{
  padding:0.85rem 2rem;background:var(--accent);color:#fff;
  border-radius:50px;font-weight:600;font-size:0.9rem;
  text-decoration:none;border:none;cursor:pointer;
  transition:transform 0.2s,box-shadow 0.2s;
  box-shadow:0 4px 20px rgba(37,99,235,0.35);
}
.btn-blue:hover{transform:translateY(-2px);box-shadow:0 8px 32px rgba(37,99,235,0.5);}
.btn-outline{
  padding:0.85rem 2rem;background:transparent;color:var(--text);
  border:1px solid var(--border);border-radius:50px;
  font-weight:500;font-size:0.9rem;text-decoration:none;
  transition:border-color 0.2s,color 0.2s;
}
.btn-outline:hover{border-color:var(--accent2);color:var(--accent2);}
.hero-stats{
  display:flex;gap:2.5rem;padding-top:2rem;
  border-top:1px solid var(--border);
}
.stat-val{font-family:'Playfair Display',serif;font-size:1.9rem;font-weight:700;color:var(--accent2);display:block;line-height:1;}
.stat-lbl{font-size:0.72rem;color:var(--text-muted);letter-spacing:0.04em;margin-top:0.35rem;display:block;}
.hero-visual{flex:0 0 auto;display:flex;flex-direction:column;align-items:center;gap:1.5rem;}
.photo-frame{
  position:relative;width:clamp(220px,26vw,300px);height:clamp(220px,26vw,300px);
}
.photo-ring{
  position:absolute;inset:-6px;border-radius:50%;
  background:conic-gradient(from 0deg,var(--accent),var(--accent2),transparent,var(--accent));
  animation:spin 8s linear infinite;
}
@keyframes spin{to{transform:rotate(360deg);}}
.photo-ring-inner{position:absolute;inset:3px;background:var(--bg);border-radius:50%;}
.hero-photo{
  position:relative;z-index:1;
  width:100%;height:100%;border-radius:50%;
  object-fit:cover;object-position:center top;
  border:3px solid var(--surface);
  display:block;
}
.photo-badge{
  position:absolute;bottom:8px;right:8px;z-index:2;
  background:var(--accent);color:#fff;
  padding:0.3rem 0.65rem;border-radius:50px;
  font-size:0.65rem;font-weight:700;letter-spacing:0.06em;
  box-shadow:0 4px 12px rgba(37,99,235,0.4);
}

/* SECTION LAYOUT */
.section-wrap{padding:6rem clamp(1.5rem,6vw,5rem);max-width:1200px;margin:0 auto;}
.section-divider{height:1px;background:var(--border);max-width:1200px;margin:0 auto;}
.section-head{margin-bottom:3.5rem;}
.section-head.center{text-align:center;}
.section-tag{
  display:inline-block;font-size:0.7rem;font-weight:700;
  letter-spacing:0.14em;text-transform:uppercase;color:var(--accent2);
  margin-bottom:0.65rem;
}
.section-head h2{
  font-family:'Playfair Display',serif;
  font-size:clamp(1.9rem,3vw,2.6rem);font-weight:700;line-height:1.15;
}
.section-head p{color:var(--text-muted);max-width:520px;margin-top:0.75rem;font-size:0.95rem;}
.section-head.center p{margin:0.75rem auto 0;}

/* ABOUT */
.about-grid{display:grid;grid-template-columns:1.1fr 0.9fr;gap:5rem;align-items:start;}
.about-body p{color:var(--text-muted);margin-bottom:1rem;font-size:0.96rem;line-height:1.75;}
.info-cards{display:flex;flex-direction:column;gap:0.9rem;}
.info-card{
  display:flex;align-items:center;gap:1rem;
  padding:1rem 1.25rem;background:var(--surface);
  border:1px solid var(--border);border-radius:14px;
  transition:border-color 0.2s,transform 0.2s;
}
.info-card:hover{border-color:var(--border2);transform:translateX(4px);}
.info-icon{
  width:38px;height:38px;flex-shrink:0;border-radius:10px;
  background:var(--accent-glow);display:grid;place-items:center;
  font-size:1rem;
}
.info-lbl{font-size:0.68rem;color:var(--text-dim);text-transform:uppercase;letter-spacing:0.08em;}
.info-val{font-size:0.88rem;font-weight:500;color:var(--text);word-break:break-word;}

/* SKILLS */
.skills-bg{background:var(--surface);}
.skills-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(270px,1fr));gap:1.25rem;}
.skill-card{
  background:var(--bg);border:1px solid var(--border);
  border-radius:var(--radius);padding:1.5rem;
  transition:border-color 0.25s,transform 0.25s;
  position:relative;overflow:hidden;
}
.skill-card::before{
  content:'';position:absolute;top:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--accent),var(--accent2));
  transform:scaleX(0);transform-origin:left;
  transition:transform 0.35s;
}
.skill-card:hover{border-color:var(--border2);transform:translateY(-4px);}
.skill-card:hover::before{transform:scaleX(1);}
.sk-icon{font-size:1.7rem;margin-bottom:0.8rem;}
.sk-name{font-weight:700;font-size:0.92rem;margin-bottom:0.35rem;}
.sk-desc{font-size:0.8rem;color:var(--text-muted);line-height:1.55;}
.sk-bar-bg{height:3px;background:var(--border);border-radius:3px;margin-top:1.1rem;overflow:hidden;}
.sk-bar{height:100%;background:linear-gradient(90deg,var(--accent),var(--accent2));border-radius:3px;width:0%;transition:width 1.4s cubic-bezier(0.4,0,0.2,1);}

/* EXPERIENCE */
.timeline{position:relative;padding-left:2rem;}
.timeline::before{content:'';position:absolute;left:0;top:4px;bottom:0;width:1px;background:linear-gradient(to bottom,var(--accent),transparent);}
.tl-item{
  position:relative;margin-bottom:3rem;
  opacity:0;transform:translateY(20px);
  transition:opacity 0.65s,transform 0.65s;
}
.tl-item.visible{opacity:1;transform:none;}
.tl-dot{
  position:absolute;left:-2rem;top:6px;
  width:11px;height:11px;background:var(--accent);
  border-radius:50%;box-shadow:0 0 0 4px var(--accent-glow);
  transform:translateX(-5px);
}
.tl-period{
  display:inline-flex;align-items:center;gap:0.4rem;
  font-size:0.72rem;font-weight:700;color:var(--accent2);
  letter-spacing:0.07em;text-transform:uppercase;margin-bottom:0.5rem;
}
.tl-title{font-size:1.15rem;font-weight:700;margin-bottom:0.2rem;}
.tl-co{font-size:0.88rem;color:var(--text-muted);margin-bottom:0.8rem;}
.tl-body{font-size:0.86rem;color:var(--text-muted);line-height:1.7;}
.tl-tags{display:flex;flex-wrap:wrap;gap:0.45rem;margin-top:0.9rem;}
.tag{
  padding:0.22rem 0.7rem;border-radius:50px;
  background:var(--accent-glow2);border:1px solid var(--border2);
  font-size:0.7rem;font-weight:600;color:var(--accent2);letter-spacing:0.02em;
}

/* EDUCATION */
.edu-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1.25rem;}
.edu-card{
  background:var(--surface);border:1px solid var(--border);
  border-radius:var(--radius);padding:2rem;
  transition:border-color 0.25s,transform 0.25s;
  position:relative;overflow:hidden;
}
.edu-card::after{
  content:'';position:absolute;bottom:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--accent),var(--accent2));
  transform:scaleX(0);transform-origin:left;
  transition:transform 0.35s;
}
.edu-card:hover{border-color:var(--border2);transform:translateY(-4px);}
.edu-card:hover::after{transform:scaleX(1);}
.edu-icon{
  width:48px;height:48px;background:var(--accent-glow);border:1px solid var(--border2);
  border-radius:14px;display:grid;place-items:center;font-size:1.4rem;margin-bottom:1.2rem;
}
.edu-degree{font-size:1rem;font-weight:700;margin-bottom:0.3rem;}
.edu-inst{font-size:0.85rem;color:var(--accent2);font-weight:500;margin-bottom:0.4rem;}
.edu-loc{font-size:0.78rem;color:var(--text-muted);}

/* CONTACT */
.contact-card{
  background:var(--surface);border:1px solid var(--border);
  border-radius:28px;padding:clamp(2.5rem,5vw,4.5rem);
  text-align:center;position:relative;overflow:hidden;
  background-image:radial-gradient(ellipse 70% 50% at 50% -10%,rgba(37,99,235,0.12),transparent);
}
.contact-card h2{font-family:'Playfair Display',serif;font-size:clamp(1.9rem,3.5vw,2.8rem);font-weight:700;margin-bottom:1rem;}
.contact-card p{color:var(--text-muted);max-width:460px;margin:0 auto 2.5rem;font-size:0.96rem;}
.contact-links{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;}
.cl{
  display:inline-flex;align-items:center;gap:0.6rem;
  padding:0.8rem 1.6rem;background:var(--surface2);
  border:1px solid var(--border);border-radius:50px;
  color:var(--text);text-decoration:none;font-size:0.86rem;font-weight:500;
  transition:border-color 0.2s,color 0.2s,transform 0.2s,box-shadow 0.2s;
}
.cl:hover{border-color:var(--accent2);color:var(--accent2);transform:translateY(-2px);box-shadow:0 6px 20px rgba(37,99,235,0.2);}

/* FOOTER */
footer{
  border-top:1px solid var(--border);
  padding:1.75rem clamp(1.5rem,6vw,5rem);
  display:flex;align-items:center;justify-content:space-between;
  font-size:0.76rem;color:var(--text-dim);
  max-width:1200px;margin:0 auto;
}

/* REVEAL */
.reveal{opacity:0;transform:translateY(28px);transition:opacity 0.75s ease,transform 0.75s ease;}
.reveal.visible{opacity:1;transform:none;}
.reveal-l{opacity:0;transform:translateX(-28px);transition:opacity 0.75s ease,transform 0.75s ease;}
.reveal-l.visible{opacity:1;transform:none;}
.reveal-r{opacity:0;transform:translateX(28px);transition:opacity 0.75s ease,transform 0.75s ease;}
.reveal-r.visible{opacity:1;transform:none;}

/* MOBILE */
@media(max-width:768px){
  .nav-links{
    display:none;position:fixed;top:var(--nav-h);left:0;right:0;
    flex-direction:column;background:var(--bg);
    border-bottom:1px solid var(--border);padding:2rem;gap:1.5rem;
  }
  .nav-links.open{display:flex;}
  .hamburger{display:flex;}
  #hero{flex-direction:column-reverse;gap:2rem;text-align:center;padding-top:calc(var(--nav-h)+2rem);padding-bottom:3rem;}
  .hero-text h1{font-size:2.4rem;}
  .hero-btns{justify-content:center;}
  .hero-stats{justify-content:center;gap:2rem;}
  .photo-frame{width:200px;height:200px;}
  .about-grid{grid-template-columns:1fr;gap:2.5rem;}
  .contact-card{padding:2rem 1.5rem;}
  footer{flex-direction:column;gap:0.5rem;text-align:center;}
}
@media(max-width:480px){.hero-stats{flex-wrap:wrap;gap:1.5rem;}}
</style>
</head>
<body>
<div class="hero-bg"></div>

<!-- NAV -->
<nav id="navbar">
  <a class="nav-logo" href="#hero"><span class="nav-logo-dot"></span>Ariful Islam</a>
  <div class="nav-links" id="navLinks">
    <a href="#about">About</a>
    <a href="#skills">Expertise</a>
    <a href="#experience">Experience</a>
    <a href="#education">Education</a>
    <a href="#contact">Contact</a>
  </div>
  <div class="nav-right">
    <button class="theme-toggle" id="themeBtn" aria-label="Toggle theme">☀</button>
    <a href="mailto:arif54565@gmail.com" class="nav-cta">Hire Me</a>
    <button class="hamburger" id="hamburger" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-text">
    <div class="hero-eyebrow"><span class="dot"></span>Pharmaceutical Professional</div>
    <h1>Md. <span class="name-hi">Ariful</span><br>Islam</h1>
    <p class="hero-role">
      <strong>Sr. Executive &amp; Quality Leader</strong> — a decade of excellence in pharmaceutical manufacturing, quality control, and team leadership across Bangladesh's pharma sector.
    </p>
    <div class="hero-chips">
      <span class="chip">Quality Control</span>
      <span class="chip">GMP Compliance</span>
      <span class="chip">Group Leader</span>
      <span class="chip">Pharma Analyst</span>
      <span class="chip">Training &amp; Development</span>
    </div>
    <div class="hero-btns">
      <a href="#contact" class="btn-blue">Get in Touch</a>
      <a href="#experience" class="btn-outline">View Experience</a>
    </div>
    <div class="hero-stats">
      <div><span class="stat-val">10+</span><span class="stat-lbl">Years Experience</span></div>
      <div><span class="stat-val">M.Pharm</span><span class="stat-lbl">Qualification</span></div>
      <div><span class="stat-val">GMP</span><span class="stat-lbl">Expert</span></div>
    </div>
  </div>
  <div class="hero-visual">
    <div class="photo-frame">
      <div class="photo-ring"><div class="photo-ring-inner"></div></div>
      <img class="hero-photo" src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAUDBAQEAwUEBAQFBQUGBwwIBwcHBw8LCwkMEQ8SEhEPERETFhwXExQaFRERGCEYGh0dHx8fExciJCIeJBweHx7/2wBDAQUFBQcGBw4ICA4eFBEUHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh7/wAARCAGkAaQDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD5OoFLRigBMUuKKWgAFKBxSUtACiigUv0oAbilHTilooASloxSgUAJRS4FGKACilxRQAUvakp340AJij8KWigBKPwpaPoKACkNLQaAEFLikpfegAxQMUp6UnegBcUhFKKU0ANIpKdijtQA00lLSUAFFHaigApKKWgAooooAKSnUYoAZRgYp2KQigBKQinUhoASjFLSUAJiilooATFJS0GgBtFKRn2ooACBQaWjigBAKXFFLQAmOKXFFFABS0ClxQAg68UU7FHFACCilooAKKBS0AJ0pTRiigApcUlO7UAFFKKKAEoopR1oAKKWjFADcUUuKU0ANopaMUAJTqBRQAlJTqTFADTSU6kP0oASj3pcUY4oAbRTsUnFAAOlL2pKUUALRSgd6KAGEUlPxTSKAG0UpoFACHpSUpFJQAUlL+tIaACiilxQA0iinUUANpaKXFACdqKWj60AFLSU4UAAoxmlFFACUuKU0CgBKKWigBMc0tLijFACAZowaWigBADS0tLQAnail/CigBKBilFGKACilxRQAlFLRQAlGKWloATFJTsUlACUH2paWgBpFNNPpDQA3FFLzRQA3FFLRQAgpRRiigBaKKO9AAaSlpDQA0jmjFOpKAG80U78aaRQAmKKXvRQA2l7UUdqACikwPWigAxSjpRRQAUUYpcUAJSilApQPyoASlFFKKAD60uKWigBMUc0tFACYpcUuKAKAG4opxFJj1oAAKXFFAoAKSnYNFACY4pR1oxRQAtJigGloAKMUoFGKAEANGKcKMUAN+tGKeQKbigBuKXFKBzShdxAAJJoAZSY/OnsMHHFNIoAb3op2KQigBpopcUYoATFLilAooAZS040mKAEpKXikoAKSloxQAlJTqTFACUCj86KAEoNLxQaAG/nRS/hRQAlLRRigApRR3pcUAGKWgUdqAAUvajFLQAfnRRRQADmlxQKUYoAQ0tGKBQAEUYFLRigBMCl+lGKcqliAO5oASjFLjn1pdpJwKAG7falRGdwijLHgAVftbGaZT5akkpuyegXPU090gtVaAy4duG2jLsPQegoAzSu0kdcdxRtOPStILDA4DhUGMtu5IH+P5Vh318PM2wKuSfvFsn6UrgXERmB2qT6kU4KuwEsATnGTxiq0TzRq7TgPsXOwdEJ4y3bPtVCW+lkGxD5SAYyOWOPei4Gm8sIBIYsF+83b8Kq/wBpRl9kMMjn1xUUVuyKrTymAScDA3OR7DtUE/7p3hjZ0XOG55P1x/Ki4GiL6BIw0kc28ngFRj/69El2iNiVHRsZwwwaz7eSRAwjwzNxvxkge3pT5IDGpZGkZmHLZA59M96VwL0dzbsdu8A993GKsJPblGCPx3IHJ/8ArVgrC+87jtPbcO9PZbl5Mgoo6Fg2Afc5p3A1wwPTGKMZrNP2qFVkUOI24GTkMfapYL8HAkRl9+1FwLuKQiiNll5jIYeoOaeVA6MCfYUwGH60mKdikoATFBpcUYoAaaKWkxQAhpp6040hoASjFLSgCgBMUhp2KSgBtFLjmg0ANopaKAGnNFKaKAFoHWlo7UAGKO9LS0AJ70YpaO9ABS4oxRigAFFH4UtAAKX8aBRQAUCil96ADFLt4BoFPI/dn2IP4GgBmKkiUgM/oMD8aYcdcVNAflIPTbn9aAFgRRGz/wAQ6ZHT/wCvWho9gk+57lgkKN87ep7KPU1BaQO6AkiOPqWY8enA6n0rdN1DbxeQrEkHZGrJgAnrkevfnH4UgMvWL4u7W9hGzt6scBewHHSo9L01rSNrm6VC7DccZ+Ue5P6AfjxUN1qE1tJujhghI5UuRJIfcdgffFZr3uq3rSGSNmRTl2l5xQMdqC3OpXHlxjYhkxHFGuSxPQcdTU9xZWmhw/LIt3fYBfB+SEHqCf7305+nWqkmoXlrEyLcPbBuTs4J/LmswreXSic73jBxvbgZ+tIAurq4mwkkhIzu8voqn6etaCWsdvZiSZJJLsjdsx8sQ7bvUn0/OoraxuoF80QKgJz5zqePpmkvz5n703jSyNwzOp/Si4WKjNun+UmSZj26j8e1MRUyyuSMA52DOT2p8Q2rtULISefm/kKtRkw25ikbCsSdgY4H1HegViOzsprgMI5lXC7sEEA0TWYBPlXSSkKCQAQRTpXmmhaWG2ykYG54/wCH0z6VVLSzIUkdGVTkhm9f60AKEYLuWVVK9ckAio1
