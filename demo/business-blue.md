---
marp: true
theme: default
size: 16:9
paginate: false
html: true
---

<style>
@font-face { font-family: 'Lato'; font-weight: 400; src: url('fonts/lato-400.woff2') format('woff2'); }
@font-face { font-family: 'Lato'; font-weight: 700; src: url('fonts/lato-700.woff2') format('woff2'); }
@font-face { font-family: 'Lato'; font-weight: 900; src: url('fonts/lato-900.woff2') format('woff2'); }

:root {
  --blue-light: #6aaed3;
  --blue-mid: #4a7f9b;
  --teal: #3d6b7d;
  --navy: #1b2a4a;
  --gray-text: #555;
  font-family: 'Lato', 'Hiragino Kaku Gothic ProN', sans-serif;
}

section {
  background: #fff;
  padding: 0;
  position: relative;
}

/* 共通ヘッダー */
section::before {
  content: '';
  position: absolute;
  top: 28px; right: 40px;
  width: 14px; height: 56px;
  background: var(--teal);
}
header {
  position: absolute;
  top: 34px; right: 70px;
  font-size: 26px;
  font-weight: 900;
  color: var(--navy);
}
header em {
  font-style: normal;
  font-weight: 400;
  color: #aaa;
}

/* ===== タイトルスライド ===== */
section.title .left-box {
  position: absolute;
  left: 0; top: 70px;
  width: 280px; height: 320px;
  background: var(--blue-light);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 38px;
  text-align: center;
  line-height: 1.3;
}
section.title .circles {
  position: absolute;
  left: 340px; top: 110px;
  display: flex;
  gap: 60px;
}
section.title .circle-item { width: 200px; text-align: center; }
section.title .circle-item .icon {
  width: 160px; height: 160px;
  border-radius: 50%;
  background: var(--blue-mid);
  color: #fff;
  font-size: 64px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 24px;
}
section.title .circle-item h3 {
  font-size: 26px;
  font-weight: 900;
  margin: 0 0 12px;
  color: #222;
}
section.title .circle-item p {
  font-size: 16px;
  color: var(--gray-text);
  line-height: 1.5;
  margin: 0;
}

/* ===== 番号カードスライド ===== */
section.cards .card-row {
  position: absolute;
  left: 60px; top: 110px;
  display: flex;
  gap: 40px;
}
section.cards .card {
  width: 340px; height: 480px;
  border: 3px solid var(--blue-light);
  position: relative;
}
section.cards .card .head {
  background: var(--blue-light);
  color: #fff;
  margin: -3px -3px 0;
  padding: 30px 34px 90px;
  font-size: 24px;
  line-height: 1.45;
}
section.cards .card .num {
  position: absolute;
  left: 20px; top: 130px;
  font-size: 200px;
  font-weight: 300;
  color: rgba(120, 140, 160, 0.35);
  line-height: 1;
}
section.cards .card .btn {
  position: absolute;
  bottom: 36px; left: 50%;
  transform: translateX(-50%);
  background: #777;
  color: #fff;
  padding: 10px 36px;
  font-size: 22px;
}
section.cards .card:nth-child(2) { border-color: var(--blue-mid); }
section.cards .card:nth-child(2) .head { background: var(--blue-mid); }
section.cards .card:nth-child(3) { border-color: var(--navy); }
section.cards .card:nth-child(3) .head { background: var(--navy); }

/* ===== セクション区切りスライド ===== */
section.divider {
  background: linear-gradient(rgba(106, 174, 211, 0.75), rgba(106, 174, 211, 0.75)),
              linear-gradient(160deg, #8fa6b8 0%, #5f7a90 40%, #3c5a72 100%);
}
section.divider header em { color: rgba(255,255,255,0.5); }
section.divider .boxes {
  position: absolute;
  left: 60px; top: 130px;
  display: flex;
  gap: 50px;
}
section.divider .boxes div {
  background: rgba(40, 70, 95, 0.85);
  color: #fff;
  width: 420px;
  padding: 28px 32px;
  font-size: 24px;
  line-height: 1.5;
}
section.divider .arrow {
  position: absolute;
  top: 330px; left: 50%;
  transform: translateX(-50%);
  width: 0; height: 0;
  border-left: 40px solid transparent;
  border-right: 40px solid transparent;
  border-top: 30px solid rgba(255,255,255,0.7);
}
section.divider .band {
  position: absolute;
  left: 0; bottom: 100px;
  width: 100%;
  background: var(--navy);
  color: #fff;
  text-align: center;
  font-size: 52px;
  padding: 50px 0;
}
</style>

<!-- _class: title -->

<header><b>Business</b> <em>template</em></header>

<div class="left-box">Presentation<br>Design</div>
<div class="circles">
  <div class="circle-item">
    <div class="icon">💻</div>
    <h3>SAMPLE</h3>
    <p>The wonderful Ultimate Professional Business Power point Template</p>
  </div>
  <div class="circle-item">
    <div class="icon">📈</div>
    <h3>SAMPLE</h3>
    <p>The wonderful Ultimate Professional Business Power point Template</p>
  </div>
  <div class="circle-item">
    <div class="icon">✉️</div>
    <h3>SAMPLE</h3>
    <p>The wonderful Ultimate Professional Business Power point Template</p>
  </div>
</div>

---

<!-- _class: cards -->

<header><b>Business</b> <em>template</em></header>

<div class="card-row">
  <div class="card">
    <div class="head">The wonderful Ultimate Professional Business Power point Template</div>
    <div class="num">1</div>
    <div class="btn">Design</div>
  </div>
  <div class="card">
    <div class="head">The wonderful Ultimate Professional Business Power point Template</div>
    <div class="num">2</div>
    <div class="btn">Design</div>
  </div>
  <div class="card">
    <div class="head">The wonderful Ultimate Professional Business Power point Template</div>
    <div class="num">3</div>
    <div class="btn">Design</div>
  </div>
</div>

---

<!-- _class: divider -->

<header><b>Business</b> <em>template</em></header>

<div class="boxes">
  <div>The wonderful Ultimate Professional Business Power point Template</div>
  <div>The wonderful Ultimate Professional Business Power point Template</div>
</div>
<div class="arrow"></div>
<div class="band">Presentation Design</div>
