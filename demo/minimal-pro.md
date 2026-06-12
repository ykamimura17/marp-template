---
marp: true
theme: default
size: 16:9
paginate: false
html: true
header: 'Creative Professional Presentation'
---

<style>
@font-face { font-family: 'Inter'; font-weight: 100 900; src: url('fonts/inter-var.woff2') format('woff2'); }

:root { font-family: 'Inter', 'Hiragino Sans', sans-serif; }

section {
  background: #fafaf8;
  color: #222;
  padding: 60px 80px;
  position: relative;
}

/* 共通ヘッダー(小さなキャプション) */
header {
  position: absolute;
  top: 44px; left: 80px;
  right: auto;
  width: auto;
  font-size: 15px;
  color: #999;
  letter-spacing: 0.5px;
}

section h1 {
  color: #222;
  font-size: 80px;
  font-weight: 500;
  letter-spacing: -1px;
  margin: 90px 0 30px;
}
section p { font-size: 19px; color: #888; line-height: 1.8; max-width: 420px; }

/* 写真プレースホルダ(実運用では img タグに差し替え) */
.ph {
  background: linear-gradient(135deg, #d8d8d4, #b8b8b2);
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 14px;
  letter-spacing: 1px;
}

/* タイトルスライド */
section.cover .ph {
  position: absolute;
  right: 200px; top: 150px;
  width: 230px; height: 320px;
  box-shadow: 30px 30px 0 #eceae5;
}
section.cover .sub {
  font-size: 16px;
  color: #aaa;
  margin-top: 60px;
}

/* 2カラム画像スライド */
section.duo .row {
  display: flex;
  gap: 60px;
  margin-top: 50px;
}
section.duo .col { flex: 1; }
section.duo .ph { width: 100%; height: 260px; margin-bottom: 20px; }
section.duo .col p { font-size: 16px; max-width: none; }

/* 統計スライド */
section.stats .grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 50px 100px;
  margin-top: 40px;
  width: 560px;
  float: right;
}
section.stats .stat .num { font-size: 56px; font-weight: 600; }
section.stats .stat .label { font-size: 16px; color: #999; margin-top: 6px; }
section.stats .ph {
  position: absolute;
  left: 80px; top: 230px;
  width: 380px; height: 330px;
}
</style>

<!-- _class: cover -->


# Slide Pro.

Creative Professional Template

<p class="sub">Lorem ipsum is simply dummy text of the printing and typesetting industry. Lorem ipsum has been the industry's standard dummy text.</p>

<div class="ph">PHOTO</div>

---

<!-- _class: duo -->


# Clean Style

<div class="row">
  <div class="col">
    <div class="ph">PHOTO</div>
    <p>Lorem ipsum is simply dummy text of the printing and typesetting industry.</p>
  </div>
  <div class="col">
    <div class="ph">PHOTO</div>
    <p>Lorem ipsum is simply dummy text of the printing and typesetting industry.</p>
  </div>
</div>

---

<!-- _class: stats -->


# Our Goals

<div class="grid">
  <div class="stat"><div class="num">15 +</div><div class="label">Top Values</div></div>
  <div class="stat"><div class="num">3465 +</div><div class="label">Happy Clients</div></div>
  <div class="stat"><div class="num">5465 +</div><div class="label">Projects Done</div></div>
  <div class="stat"><div class="num">735 +</div><div class="label">Coworker Office</div></div>
</div>

<div class="ph">PHOTO</div>
