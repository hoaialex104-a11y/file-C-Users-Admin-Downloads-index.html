
[index.html](https://github.com/user-attachments/files/24566444/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>The White Unicorn Shop</title>
  <style>
/* ===== Brand / FOMO ===== */
.brand-sub{margin-top:6px;font-size:1rem;letter-spacing:3px;text-transform:uppercase;color:#c7d2fe}
.fomo-bar{margin-top:18px;font-size:.95rem;color:#22c55e;font-weight:800;letter-spacing:.6px;animation:pulseFomo 2.4s infinite}
@keyframes pulseFomo{0%,100%{opacity:.55}50%{opacity:1}}
@keyframes floatCore{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}

/* ===== Desktop Layout ===== */
body{
  margin:0;
  font-family:system-ui,-apple-system,BlinkMacSystemFont,sans-serif;
  /* Emerald / Luxury Dark */
  background:
    radial-gradient(1400px 700px at 20% 10%, rgba(16,185,129,.35), transparent 60%),
    radial-gradient(1200px 600px at 85% 15%, rgba(20,184,166,.30), transparent 60%),
    radial-gradient(900px 500px at 50% 85%, rgba(52,211,153,.22), transparent 60%),
    linear-gradient(180deg, #020617 0%, #02130f 55%, #042018 100%);
  color:#e5e7eb;
  overflow-x:hidden;
}

body::before{
  content:"";
  position:fixed;
  inset:0;
  background:
    radial-gradient(circle at 20% 30%, rgba(255,255,255,.04), transparent 40%),
    radial-gradient(circle at 80% 70%, rgba(255,255,255,.03), transparent 45%);
  pointer-events:none;
  z-index:-1;
}

body::after{
  content:"";
  position:fixed;
  inset:0;
  background:linear-gradient(120deg, transparent 40%, rgba(255,255,255,.03), transparent 60%);
  animation:backgroundSweep 18s linear infinite;
  pointer-events:none;
  z-index:-1;
}

@keyframes backgroundSweep{
  0%{transform:translateX(-30%)}
  100%{transform:translateX(30%)}
}
.hero{min-height:100vh;display:flex;align-items:center;justify-content:center;animation:heroPulse 1.4s ease-out both}
@keyframes heroPulse{0%{filter:brightness(.8)}100%{filter:brightness(1)}}
.hero-inner{max-width:1200px;margin:0 auto;padding:80px 32px;text-align:center}
.logo-3d{font-size:4.2rem;letter-spacing:1px;position:relative}
.glow-text{text-shadow:0 0 20px rgba(168,85,247,.6),0 0 40px rgba(99,102,241,.4)}
.tagline{max-width:720px;margin:18px auto 0;font-size:1.1rem;opacity:.9}
.token-core{margin:42px auto 0;max-width:560px;padding:34px 28px;border-radius:26px;background:linear-gradient(180deg,rgba(255,255,255,.08),rgba(255,255,255,.02));backdrop-filter:blur(16px);box-shadow:0 60px 160px rgba(0,0,0,.55);animation:floatCore 6s ease-in-out infinite;position:relative;z-index:2}
.token-core::after{content:"";position:absolute;inset:-22px;border-radius:42px;--glow-r:16;--glow-g:185;--glow-b:129;background:radial-gradient(circle at var(--gx,50%) var(--gy,50%), rgba(var(--glow-r),var(--glow-g),var(--glow-b),.45), transparent 65%);filter:blur(34px);opacity:.65;transition:opacity .2s,transform .2s;background-size:120% 120%;z-index:-1}
.core-text{font-size:1rem;line-height:1.8}
.cta{margin-top:36px;display:flex;gap:18px;justify-content:center}
.btn{padding:14px 26px;border-radius:14px;text-decoration:none;font-weight:700}
.btn.primary{background:linear-gradient(135deg,#6366f1,#a855f7);color:white}
.btn.secondary{background:rgba(255,255,255,.08);color:white}

/* ===== Shop Desktop Grid ===== */
.shop{max-width:1200px;margin:120px auto 0;padding:0 32px}
.products{display:grid;grid-template-columns:repeat(3,1fr);gap:28px;margin-top:40px}
.card{background:rgba(255,255,255,.04);border-radius:22px;padding:28px;box-shadow:0 30px 80px rgba(0,0,0,.35);transition:transform .25s ease,box-shadow .25s ease}
.card:hover{transform:translateY(-6px);box-shadow:0 50px 120px rgba(0,0,0,.5)}
.tag{display:inline-block;margin-bottom:10px;font-size:.8rem;font-weight:800}

/* ===== Responsive ===== */
@media (max-width: 900px){
  .logo-3d{font-size:3rem}
  .products{grid-template-columns:1fr}
  .cta{flex-direction:column}
}
/* ===== Star Dust Layer ===== */
.starfield{position:fixed;inset:0;pointer-events:none;z-index:-2;background-image:
  radial-gradient(1px 1px at 20% 30%, rgba(255,255,255,.6), transparent 60%),
  radial-gradient(1px 1px at 80% 20%, rgba(255,255,255,.5), transparent 60%),
  radial-gradient(1px 1px at 60% 70%, rgba(255,255,255,.4), transparent 60%),
  radial-gradient(1px 1px at 30% 80%, rgba(255,255,255,.5), transparent 60%),
  radial-gradient(1px 1px at 50% 50%, rgba(255,255,255,.3), transparent 60%);
background-size:400px 400px;animation:starDrift 120s linear infinite}
@keyframes starDrift{from{transform:translateY(0)}to{transform:translateY(-400px)}}

/* ===== Scroll Parallax ===== */
.parallax-bg{will-change:transform;transition:transform .1s linear}
</style>
</head>
<body class="meteor-all">
<div class="starfield parallax-bg"></div>
<div class="meteor-layer">
  <div class="meteor"></div>
  <div class="meteor"></div>
  <div class="meteor"></div>
  <div class="meteor"></div>
</div>

<header class="hero hero-3d">
  <div class="hero-inner advanced center-hero">

    <div class="hero-top">
      <span class="badge glow">🦄 Web3 • Memecoin • pump.fun</span>
    </div>

    <div class="hero-main hero-center">
      <h1 class="logo-3d text-outline glow-text">The White Unicorn</h1>
      <div class="brand-sub">The Calm Power of Web3 Luxury</div>
      <p class="tagline">Luxury-born memecoin with strong narrative, clean visuals, and community-first momentum.</p>

      <div class="token-core">
        <div class="ring"></div>
        <div class="core-text">
          🚀 <strong>Launch:</strong> pump.fun<br/>
          📜 <strong>Contract:</strong> Coming Soon<br/>
          🔥 <strong>Status:</strong> Early • Low Cap • High Momentum
        </div>
        <div class="fomo-bar">⚡ Live attention building • Community forming fast</div>
      </div>

      <div class="cta" style="margin-bottom:60px">
        <a href="https://t.me/thewhiteunicornX" target="_blank" class="btn primary">🚀 Enter Telegram</a>
        <a href="https://x.com/baohoai887" target="_blank" class="btn secondary">📣 Follow the Story on X</a>
      </div>

      <!-- BUY SECTION -->
      <div class="buy-section" style="margin-top:80px;position:relative;z-index:1;" id="buy">
        <div class="buy-glow"></div>
        <h2 class="buy-title">Buy $TWU</h2>
        <p class="buy-sub">Be early. Ride the narrative. Contract address coming soon.</p>
        <a href="#" class="btn primary buy-btn">💎 BUY SOON</a>
      </div>
    </div>

    <div class="hero-bottom" style="margin-top:80px;display:flex;justify-content:center"><div class="signal" style="font-size:1rem;font-weight:800;letter-spacing:.6px;color:#22c55e">📈 Early stage • Low cap • High potential</div></div>
    </div>

  </div>
</header>





<footer>
  © 2026 The White Unicorn. All rights reserved.
</footer>

<script>
const parallax=document.querySelector('.parallax-bg');
const token=document.querySelector('.token-core');
const isDesktop=window.matchMedia('(pointer:fine)').matches;
window.addEventListener('scroll',()=>{
  const y=window.scrollY;
  parallax.style.transform=`translateY(${y*0.15}px)`;
  if(token){
    const t=Math.min(1,y/800);
    // emerald (16,185,129) -> cyan (34,211,238)
    const r=Math.round(16+(34-16)*t);
    const g=Math.round(185+(211-185)*t);
    const b=Math.round(129+(238-129)*t);
    token.style.setProperty('--glow-r',r);
    token.style.setProperty('--glow-g',g);
    token.style.setProperty('--glow-b',b);
    token.style.boxShadow=`0 60px 160px rgba(0,0,0,.55), 0 0 ${40+t*90}px rgba(${r},${g},${b},${0.45+t*0.35})`;
  }
});

if(isDesktop && token){
  window.addEventListener('mousemove',(e)=>{
    const rect=token.getBoundingClientRect();
    const x=((e.clientX-rect.left)/rect.width)*100;
    const y=((e.clientY-rect.top)/rect.height)*100;
    token.style.setProperty('--gx',`${x}%`);
    token.style.setProperty('--gy',`${y}%`);
  });
}
</script>
</body>
</html>
