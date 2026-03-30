zx4you.com 
<!DOCTYPE html>
<html lang="ms">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Outfit of the Boy – Koleksi Musim Luruh</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Playfair+Display:ital,wght@0,700;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --burnt-orange: #C4511A;
    --forest-green: #2D5016;
    --warm-taupe: #8B7355;
    --cream: #F5F0E8;
    --dark: #1A1A1A;
    --red-promo: #C0392B;
    --gold: #D4A843;
    --leaf-rust: #A0522D;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--cream);
    font-family: 'DM Sans', sans-serif;
    color: var(--dark);
    overflow-x: hidden;
  }

  /* Leaf SVG decorations */
  .leaf {
    position: absolute;
    opacity: 0.18;
    pointer-events: none;
  }

  /* ─── HERO ─── */
  .hero {
    position: relative;
    background: var(--dark);
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden;
    padding: 60px 20px;
  }

  .hero-bg-texture {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse at 20% 50%, rgba(196,81,26,0.25) 0%, transparent 55%),
      radial-gradient(ellipse at 80% 30%, rgba(45,80,22,0.2) 0%, transparent 50%),
      radial-gradient(ellipse at 50% 80%, rgba(139,115,85,0.15) 0%, transparent 50%);
  }

  .hero-noise {
    position: absolute; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    opacity: 0.4;
  }

  .hero-leaves {
    position: absolute; inset: 0; pointer-events: none;
  }

  .hero-leaf {
    position: absolute;
    font-size: clamp(40px, 8vw, 100px);
    animation: drift linear infinite;
    opacity: 0;
  }

  @keyframes drift {
    0%   { opacity: 0; transform: translateY(-80px) rotate(0deg); }
    10%  { opacity: 0.6; }
    90%  { opacity: 0.4; }
    100% { opacity: 0; transform: translateY(110vh) rotate(720deg); }
  }

  .badge-limited {
    display: inline-block;
    background: var(--burnt-orange);
    color: #fff;
    font-family: 'DM Sans', sans-serif;
    font-weight: 600;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 6px 20px;
    border-radius: 40px;
    margin-bottom: 28px;
    animation: fadeDown 0.8s ease both;
  }

  .hero-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(56px, 13vw, 160px);
    line-height: 0.9;
    color: var(--cream);
    letter-spacing: -1px;
    animation: fadeDown 0.9s ease 0.1s both;
  }

  .hero-title span {
    color: var(--burnt-orange);
    display: block;
  }

  .hero-subtitle {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: clamp(16px, 3vw, 26px);
    color: var(--gold);
    margin-top: 16px;
    letter-spacing: 1px;
    animation: fadeDown 1s ease 0.2s both;
  }

  .hero-promo-bar {
    margin-top: 40px;
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    justify-content: center;
    animation: fadeDown 1.1s ease 0.3s both;
  }

  .promo-pill {
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.15);
    backdrop-filter: blur(10px);
    color: var(--cream);
    padding: 10px 24px;
    border-radius: 40px;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.5px;
  }

  .promo-pill strong { color: var(--gold); }

  .hero-cta {
    margin-top: 48px;
    display: inline-block;
    background: var(--burnt-orange);
    color: #fff;
    font-weight: 700;
    font-size: 15px;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    padding: 16px 48px;
    border-radius: 4px;
    transition: background 0.2s, transform 0.2s;
    animation: fadeDown 1.2s ease 0.4s both;
  }

  .hero-cta:hover { background: #a8441a; transform: translateY(-2px); }

  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ─── SECTION LABEL ─── */
  .section-label {
    text-align: center;
    padding: 80px 20px 40px;
    position: relative;
  }

  .section-label h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(36px, 7vw, 72px);
    letter-spacing: 2px;
    color: var(--dark);
  }

  .section-label p {
    font-size: 14px;
    color: var(--warm-taupe);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-top: 8px;
  }

  .divider {
    width: 60px; height: 3px;
    background: var(--burnt-orange);
    margin: 16px auto 0;
  }

  /* ─── GRID ─── */
  .collections-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2px;
    max-width: 1200px;
    margin: 0 auto 80px;
    padding: 0 20px;
  }

  /* ─── CARD ─── */
  .card {
    position: relative;
    background: #fff;
    overflow: hidden;
    cursor: pointer;
    transition: transform 0.35s cubic-bezier(0.16,1,0.3,1), box-shadow 0.35s;
  }

  .card:hover {
    transform: translateY(-6px) scale(1.01);
    box-shadow: 0 24px 60px rgba(0,0,0,0.18);
    z-index: 2;
  }

  .card-header {
    padding: 28px 28px 0;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }

  .card-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    letter-spacing: 1px;
    color: var(--dark);
    line-height: 1;
  }

  .discount-badge {
    background: var(--red-promo);
    color: #fff;
    font-weight: 700;
    font-size: 13px;
    letter-spacing: 0.5px;
    text-align: center;
    padding: 8px 14px;
    border-radius: 50%;
    width: 68px; height: 68px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    line-height: 1.2;
    box-shadow: 0 4px 16px rgba(192,57,43,0.35);
    animation: pulse 2.5s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.06); }
  }

  .discount-badge .pct { font-size: 22px; font-weight: 900; }

  .card-image-area {
    padding: 20px 28px;
    min-height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 80px;
    background: var(--cream);
    position: relative;
  }

  .card-image-area::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--burnt-orange), var(--forest-green), var(--warm-taupe));
  }

  /* emoji outfit art */
  .outfit-emoji {
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
    justify-content: center;
    font-size: 40px;
    filter: drop-shadow(0 4px 8px rgba(0,0,0,0.12));
  }

  .card-prices {
    padding: 20px 28px;
  }

  .price-promo-label {
    font-size: 11px;
    color: var(--warm-taupe);
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 600;
  }

  .price-main {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 52px;
    color: var(--red-promo);
    line-height: 1;
    margin: 2px 0;
  }

  .price-was {
    font-size: 13px;
    color: var(--warm-taupe);
    text-decoration: line-through;
  }

  .card-divider {
    height: 1px;
    background: rgba(0,0,0,0.07);
    margin: 0 28px;
  }

  .card-addon {
    padding: 16px 28px 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .addon-label {
    font-size: 12px;
    color: var(--warm-taupe);
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-weight: 600;
  }

  .addon-price { font-weight: 700; font-size: 14px; color: var(--dark); }
  .addon-was { font-size: 11px; color: #bbb; text-decoration: line-through; }

  .card-btn {
    display: block;
    margin: 0 28px 28px;
    background: var(--dark);
    color: var(--cream);
    text-align: center;
    padding: 14px;
    font-weight: 700;
    font-size: 12px;
    letter-spacing: 2px;
    text-transform: uppercase;
    border: none;
    cursor: pointer;
    transition: background 0.2s;
    border-radius: 2px;
  }

  .card-btn:hover { background: var(--burnt-orange); }

  /* card accent lines */
  .card:nth-child(1) .card-image-area { background: #f0ede6; }
  .card:nth-child(2) .card-image-area { background: #e8e8e8; }
  .card:nth-child(3) .card-image-area { background: #eeece6; }
  .card:nth-child(4) .card-image-area { background: #e8ebe4; }

  /* ─── MARQUEE STRIP ─── */
  .marquee-strip {
    background: var(--burnt-orange);
    color: #fff;
    padding: 14px 0;
    overflow: hidden;
    white-space: nowrap;
  }

  .marquee-inner {
    display: inline-flex;
    animation: marquee 18s linear infinite;
    gap: 0;
  }

  .marquee-item {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    letter-spacing: 3px;
    padding: 0 40px;
    opacity: 0.9;
  }

  .marquee-dot { opacity: 0.5; padding: 0 8px; }

  @keyframes marquee {
    from { transform: translateX(0); }
    to   { transform: translateX(-50%); }
  }

  /* ─── COLOR SWATCHES ─── */
  .swatches-section {
    text-align: center;
    padding: 60px 20px;
    background: var(--dark);
    color: var(--cream);
  }

  .swatches-section h3 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 42px;
    letter-spacing: 2px;
    margin-bottom: 8px;
  }

  .swatches-section p {
    font-size: 12px;
    color: var(--warm-taupe);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 36px;
  }

  .swatches {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
  }

  .swatch {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }

  .swatch-circle {
    width: 72px; height: 72px;
    border-radius: 50%;
    border: 3px solid rgba(255,255,255,0.1);
    box-shadow: 0 8px 24px rgba(0,0,0,0.4);
    transition: transform 0.2s;
  }

  .swatch-circle:hover { transform: scale(1.12); }
  .swatch-label { font-size: 11px; letter-spacing: 2px; text-transform: uppercase; color: rgba(255,255,255,0.6); }

  /* ─── FOOTER ─── */
  footer {
    background: var(--dark);
    border-top: 1px solid rgba(255,255,255,0.06);
    padding: 40px 20px;
    text-align: center;
    color: rgba(255,255,255,0.4);
    font-size: 12px;
    letter-spacing: 1.5px;
  }

  footer strong {
    display: block;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    color: var(--cream);
    letter-spacing: 4px;
    margin-bottom: 12px;
  }

  footer em {
    display: block;
    font-style: italic;
    font-size: 11px;
    margin-top: 16px;
    color: var(--warm-taupe);
  }

  /* ─── FAQ ─── */
  .faq-section { background: var(--cream); padding: 80px 20px; }
  .faq-inner { max-width: 760px; margin: 0 auto; }
  .faq-list { display: flex; flex-direction: column; border: 1.5px solid rgba(0,0,0,0.1); border-radius: 6px; overflow: hidden; }
  .faq-item { border-bottom: 1px solid rgba(0,0,0,0.08); }
  .faq-item:last-child { border-bottom: none; }
  .faq-q {
    width: 100%; background: #fff; border: none; padding: 22px 28px;
    display: flex; justify-content: space-between; align-items: center;
    cursor: pointer; font-family: 'DM Sans', sans-serif; font-size: 15px;
    font-weight: 600; color: var(--dark); text-align: left;
    transition: background 0.2s; gap: 16px;
  }
  .faq-q:hover { background: #faf8f3; }
  .faq-q.open { background: var(--burnt-orange); color: #fff; }
  .faq-icon { font-size: 22px; font-weight: 300; line-height: 1; flex-shrink: 0; transition: transform 0.3s; }
  .faq-q.open .faq-icon { transform: rotate(45deg); }
  .faq-a { max-height: 0; overflow: hidden; transition: max-height 0.4s ease, padding 0.3s; background: #fdfbf7; }
  .faq-a.open { max-height: 200px; padding: 0 28px 22px; }
  .faq-a p { font-size: 14px; line-height: 1.75; color: #555; padding-top: 16px; border-top: 1px solid rgba(0,0,0,0.06); }

  /* ─── CONTACT ─── */
  .contact-section { background: var(--dark); padding: 80px 20px; }
  .contact-inner { max-width: 900px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: center; }
  .contact-eyebrow { font-size: 12px; letter-spacing: 3px; text-transform: uppercase; color: var(--burnt-orange); font-weight: 600; margin-bottom: 16px; }
  .contact-title { font-family: 'Bebas Neue', sans-serif; font-size: clamp(36px, 6vw, 60px); color: var(--cream); line-height: 1.0; letter-spacing: 1px; margin-bottom: 16px; }
  .contact-sub { font-size: 14px; color: rgba(255,255,255,0.5); line-height: 1.8; }
  .contact-card { background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 12px; padding: 36px; display: flex; flex-direction: column; gap: 12px; }
  .contact-label { font-size: 11px; letter-spacing: 3px; text-transform: uppercase; color: var(--warm-taupe); font-weight: 600; }
  .contact-number { font-family: 'Bebas Neue', sans-serif; font-size: 38px; color: var(--gold); letter-spacing: 2px; text-decoration: none; line-height: 1; transition: color 0.2s; }
  .contact-number:hover { color: var(--burnt-orange); }
  .wa-btn { display: inline-flex; align-items: center; gap: 10px; background: #25D366; color: #fff; font-weight: 700; font-size: 13px; letter-spacing: 1px; text-transform: uppercase; text-decoration: none; padding: 14px 24px; border-radius: 6px; margin-top: 8px; transition: background 0.2s, transform 0.2s; }
  .wa-btn:hover { background: #1ebe5d; transform: translateY(-2px); }
  .contact-hours { font-size: 12px; color: rgba(255,255,255,0.35); margin-top: 4px; }
  @media (max-width: 700px) { .contact-inner { grid-template-columns: 1fr; gap: 36px; } }

  /* responsive */
  @media (max-width: 600px) {
    .collections-grid { padding: 0 12px; gap: 12px; }
    .hero-promo-bar { flex-direction: column; align-items: center; }
  }

  /* scroll reveal */
  .reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
</head>
<body>

<!-- ── HERO ── -->
<section class="hero">
  <div class="hero-bg-texture"></div>
  <div class="hero-noise"></div>

  <div class="hero-leaves" id="leavesContainer"></div>

  <div style="position:relative; z-index:2;">
    <div class="badge-limited">🍂 Harga Promosi · Jualan Terhad</div>

    <h1 class="hero-title">
      Koleksi<br>
      <span>Musim Luruh</span>
    </h1>

    <p class="hero-subtitle">Tawaran Hebat Sekarang — Stok Terhad</p>

    <div class="hero-promo-bar">
      <div class="promo-pill">Street &amp; Casual <strong>RM280</strong></div>
      <div class="promo-pill">Stylish Edge <strong>RM350</strong></div>
      <div class="promo-pill">Warm &amp; Relaxed <strong>RM220</strong></div>
      <div class="promo-pill">Modern Layering <strong>RM399</strong></div>
    </div>

    <a href="#koleksi" class="hero-cta">Lihat Koleksi →</a>
  </div>
</section>

<!-- ── MARQUEE ── -->
<div class="marquee-strip">
  <div class="marquee-inner" id="marqueeInner"></div>
</div>

<!-- ── COLLECTIONS ── -->
<div id="koleksi">
  <div class="section-label reveal">
    <p>Musim Luruh 2024</p>
    <h2>Pilih Gaya Anda</h2>
    <div class="divider"></div>
  </div>

  <div class="collections-grid">

    <!-- Card 1 -->
    <div class="card reveal">
      <div class="card-header">
        <div class="card-name">Street &<br>Casual</div>
        <div class="discount-badge"><span class="pct">37%</span>OFF</div>
      </div>
      <div class="card-image-area">
        <div class="outfit-emoji">
          <span>🧥</span><span>👟</span><span>🎒</span><span>👓</span>
        </div>
      </div>
      <div class="card-prices">
        <div class="price-promo-label">Harga Promosi</div>
        <div class="price-main">RM280</div>
        <div class="price-was">Asal RM450</div>
      </div>
      <div class="card-divider"></div>
      <div class="card-addon">
        <div>
          <div class="addon-label">🎒 Beg Pilihan</div>
          <div class="addon-was">Asal RM210</div>
        </div>
        <div class="addon-price">RM150</div>
      </div>
      <button class="card-btn">Dapatkan Sekarang</button>
    </div>

    <!-- Card 2 -->
    <div class="card reveal">
      <div class="card-header">
        <div class="card-name">Stylish<br>Edge</div>
        <div class="discount-badge"><span class="pct">40%</span>OFF</div>
      </div>
      <div class="card-image-area">
        <div class="outfit-emoji">
          <span>🧥</span><span>👔</span><span>🎧</span><span>💍</span>
        </div>
      </div>
      <div class="card-prices">
        <div class="price-promo-label">Harga Promosi</div>
        <div class="price-main">RM350</div>
        <div class="price-was">Asal RM580</div>
      </div>
      <div class="card-divider"></div>
      <div class="card-addon">
        <div>
          <div class="addon-label">👖 Seluar Kargo</div>
          <div class="addon-was">Asal RM290</div>
        </div>
        <div class="addon-price">RM190</div>
      </div>
      <button class="card-btn">Dapatkan Sekarang</button>
    </div>

    <!-- Card 3 -->
    <div class="card reveal">
      <div class="card-header">
        <div class="card-name">Warm &<br>Relaxed</div>
        <div class="discount-badge"><span class="pct">39%</span>OFF</div>
      </div>
      <div class="card-image-area">
        <div class="outfit-emoji">
          <span>👕</span><span>🧢</span><span>🎧</span><span>👟</span>
        </div>
      </div>
      <div class="card-prices">
        <div class="price-promo-label">Harga Promosi</div>
        <div class="price-main">RM220</div>
        <div class="price-was">Asal RM360</div>
      </div>
      <div class="card-divider"></div>
      <div class="card-addon">
        <div>
          <div class="addon-label">👟 Kasut Pilihan</div>
          <div class="addon-was">Asal RM390</div>
        </div>
        <div class="addon-price">RM260</div>
      </div>
      <button class="card-btn">Dapatkan Sekarang</button>
    </div>

    <!-- Card 4 -->
    <div class="card reveal">
      <div class="card-header">
        <div class="card-name">Modern<br>Layering</div>
        <div class="discount-badge"><span class="pct">34%</span>OFF</div>
      </div>
      <div class="card-image-area">
        <div class="outfit-emoji">
          <span>🧤</span><span>👗</span><span>👟</span><span>📿</span>
        </div>
      </div>
      <div class="card-prices">
        <div class="price-promo-label">Set Kombo Luruh</div>
        <div class="price-main">RM399</div>
        <div class="price-was">Nilai RM610</div>
      </div>
      <div class="card-divider"></div>
      <div class="card-addon">
        <div>
          <div class="addon-label">📿 Rantai Bintang</div>
          <div class="addon-was">Asal RM90</div>
        </div>
        <div class="addon-price">RM60</div>
      </div>
      <button class="card-btn">Dapatkan Sekarang</button>
    </div>

  </div>
</div>

<!-- ── SWATCHES ── -->
<div class="swatches-section reveal">
  <h3>Warna Musim Luruh</h3>
  <p>Autumn Season Colors</p>
  <div class="swatches">
    <div class="swatch">
      <div class="swatch-circle" style="background:#C4511A;"></div>
      <span class="swatch-label">Burnt Orange</span>
    </div>
    <div class="swatch">
      <div class="swatch-circle" style="background:#2D5016;"></div>
      <span class="swatch-label">Forest Green</span>
    </div>
    <div class="swatch">
      <div class="swatch-circle" style="background:#5C5248;"></div>
      <span class="swatch-label">Warm Taupe</span>
    </div>
    <div class="swatch">
      <div class="swatch-circle" style="background:#8B7355;"></div>
      <span class="swatch-label">Caramel</span>
    </div>
    <div class="swatch">
      <div class="swatch-circle" style="background:#1A1A1A;"></div>
      <span class="swatch-label">Onyx</span>
    </div>
  </div>
</div>

<!-- ── FAQ ── -->
<section class="faq-section reveal" id="faq">
  <div class="faq-inner">
    <div class="section-label" style="padding-top:0; padding-bottom:36px;">
      <p>Soalan Lazim</p>
      <h2>FAQ</h2>
      <div class="divider"></div>
    </div>

    <div class="faq-list">
      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">
          <span>Berapa lama penghantaran?</span>
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-a">
          <p>Penghantaran dalam Malaysia mengambil masa <strong>2–5 hari bekerja</strong> selepas pembayaran disahkan. Untuk kawasan Sabah &amp; Sarawak, mungkin mengambil masa sedikit lebih lama (5–7 hari).</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">
          <span>Boleh saya tukar saiz atau warna?</span>
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-a">
          <p>Ya! Pertukaran saiz atau warna boleh dibuat dalam tempoh <strong>7 hari</strong> dari tarikh terima barangan, dengan syarat item masih dalam keadaan asal (belum dipakai &amp; tag masih ada). Hubungi kami untuk bantuan.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">
          <span>Adakah harga promosi ini termasuk aksesori?</span>
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-a">
          <p>Harga promosi adalah untuk <strong>set pakaian utama</strong> sahaja. Aksesori seperti beg, kasut, dan rantai ditawarkan secara berasingan pada harga add-on yang tertera di setiap koleksi.</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">
          <span>Apakah kaedah pembayaran yang diterima?</span>
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-a">
          <p>Kami menerima <strong>FPX, TNG eWallet, GrabPay, Maybank QR</strong>, dan pindahan bank. Pembayaran secara tunai hanya untuk pelanggan walk-in. Semua transaksi dalam Ringgit Malaysia (RM).</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">
          <span>Berapa lama lagi promosi ini sah?</span>
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-a">
          <p>Promosi ini <strong>sah sehingga stok masih ada</strong>. Tiada tarikh tamat tetap — apabila stok habis, harga akan kembali kepada harga asal. Jangan tunggu lama!</p>
        </div>
      </div>

      <div class="faq-item">
        <button class="faq-q" onclick="toggleFaq(this)">
          <span>Boleh saya buat tempahan (pre-order)?</span>
          <span class="faq-icon">+</span>
        </button>
        <div class="faq-a">
          <p>Untuk pertanyaan pre-order atau tempahan khas, sila hubungi kami terus melalui WhatsApp. Kami akan maklumkan ketersediaan stok dan anggaran masa ketibaan untuk anda.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── CONTACT ── -->
<section class="contact-section reveal">
  <div class="contact-inner">
    <div class="contact-text">
      <p class="contact-eyebrow">📞 Hubungi Kami</p>
      <h2 class="contact-title">Ada Soalan?<br>Kami Sedia Membantu.</h2>
      <p class="contact-sub">Whatsapp kami terus untuk pertanyaan saiz, stok, atau tempahan.</p>
    </div>
    <div class="contact-card">
      <div class="contact-label">WhatsApp / Telefon</div>
      <a href="https://wa.me/601116251731" class="contact-number" target="_blank">
        +60 11-1625 1731
      </a>
      <a href="https://wa.me/601116251731" class="wa-btn" target="_blank">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
        Chat di WhatsApp
      </a>
      <div class="contact-hours">⏰ Balas dalam masa 1–2 jam (9am–10pm)</div>
    </div>
  </div>
</section>

<!-- ── FOOTER ── -->
<footer>
  <strong>OUTFIT OF THE BOY</strong>
  Semua Harga Dalam RM · Promosi Sah Sehingga Stok Masih Ada
  <div style="margin-top:12px; font-size:14px; color:rgba(255,255,255,0.5);">
    📞 <a href="tel:+601116251731" style="color:var(--gold); text-decoration:none;">+60 11-1625 1731</a>
  </div>
  <em>© 2024 Outfit of the Boy — Koleksi Musim Luruh</em>
</footer>

<script>
  // ─ Falling leaves animation
  const container = document.getElementById('leavesContainer');
  const leafEmojis = ['🍂','🍁','🍃'];
  function spawnLeaf() {
    const el = document.createElement('div');
    el.className = 'hero-leaf';
    el.textContent = leafEmojis[Math.floor(Math.random() * leafEmojis.length)];
    el.style.left = Math.random() * 100 + 'vw';
    el.style.fontSize = (30 + Math.random() * 40) + 'px';
    const dur = 5 + Math.random() * 8;
    el.style.animationDuration = dur + 's';
    el.style.animationDelay = (Math.random() * 4) + 's';
    container.appendChild(el);
    setTimeout(() => el.remove(), (dur + 4) * 1000);
  }
  for (let i = 0; i < 14; i++) setTimeout(spawnLeaf, i * 600);
  setInterval(spawnLeaf, 1800);

  // ─ Marquee content
  const marqueeInner = document.getElementById('marqueeInner');
  const items = [
    'Koleksi Musim Luruh','Street & Casual','Stylish Edge',
    'Warm & Relaxed','Modern Layering','Sehingga 40% Diskaun',
    'Stok Terhad','Beli Sekarang'
  ];
  const repeated = [...items, ...items];
  repeated.forEach(t => {
    const span = document.createElement('span');
    span.className = 'marquee-item';
    span.innerHTML = t + '<span class="marquee-dot">🍂</span>';
    marqueeInner.appendChild(span);
  });

  // ─ Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const obs = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        obs.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => obs.observe(el));

  // ─ FAQ toggle
  function toggleFaq(btn) {
    const answer = btn.nextElementSibling;
    const isOpen = btn.classList.contains('open');
    // close all
    document.querySelectorAll('.faq-q.open').forEach(b => {
      b.classList.remove('open');
      b.nextElementSibling.classList.remove('open');
    });
    if (!isOpen) {
      btn.classList.add('open');
      answer.classList.add('open');
    }
  }

  // ─ CTA smooth scroll
  document.querySelector('.hero-cta').addEventListener('click', e => {
    e.preventDefault();
    document.getElementById('koleksi').scrollIntoView({ behavior: 'smooth' });
  });
</script>
</body>
</html>
