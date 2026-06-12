---
marp: true
theme: default
size: 16:9
paginate: false
html: true
---

<style>
@font-face { font-family: 'Oswald'; font-weight: 600; src: url('fonts/oswald-600.woff2') format('woff2'); }
@font-face { font-family: 'Jost'; font-weight: 400; src: url('fonts/jost-400.woff2') format('woff2'); }

:root {
  --beige: #c9bfae;
  --dark: #1c1a17;
  --cream: #efece4;
}

section {
  padding: 70px 80px;
  font-family: 'Jost', sans-serif;
  position: relative;
}

section h1 {
  color: inherit;
  font-family: 'Oswald', sans-serif;
  font-weight: 600;
  text-transform: uppercase;
  font-size: 96px;
  line-height: 1.05;
  letter-spacing: 2px;
  margin: 0 0 40px;
}
section p {
  font-size: 24px;
  letter-spacing: 3px;
  text-transform: uppercase;
  line-height: 1.7;
  max-width: 480px;
}

/* SVG feTurbulence で漆喰風テクスチャを生成(画像ファイル不要) */
section.dark {
  background-color: var(--dark);
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.012 0.09' numOctaves='4' seed='7'/%3E%3CfeColorMatrix type='matrix' values='0 0 0 0 0.45 0 0 0 0 0.43 0 0 0 0 0.40 0 0 0 0.5 0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23n)'/%3E%3C/svg%3E");
  color: var(--beige);
}
section.dark p { color: #9e968a; }

section.beige {
  background-color: var(--beige);
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.02 0.08' numOctaves='5' seed='3'/%3E%3CfeColorMatrix type='matrix' values='0 0 0 0 1 0 0 0 0 1 0 0 0 0 0.95 0 0 0 0.35 0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23n)'/%3E%3C/svg%3E");
  color: #fdfcf8;
}
section.beige p { color: #f5f2ea; }

section.cream {
  background-color: var(--cream);
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.015 0.1' numOctaves='4' seed='11'/%3E%3CfeColorMatrix type='matrix' values='0 0 0 0 0.6 0 0 0 0 0.58 0 0 0 0 0.52 0 0 0 0.25 0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23n)'/%3E%3C/svg%3E");
  color: #9a948a;
}
section.cream h1 { text-align: center; margin-top: 60px; }
section.cream p { margin: 0 auto; text-align: center; max-width: 620px; font-size: 20px; }

/* 枠付きテキストボックス */
.frame {
  position: absolute;
  right: 90px; top: 200px;
  border: 2px solid currentColor;
  border-radius: 0 60px 0 0;
  padding: 36px 32px;
  width: 360px;
  font-size: 21px;
  letter-spacing: 2px;
  text-transform: uppercase;
  line-height: 1.7;
}
</style>

<!-- _class: dark -->

# Embrace<br>Wabi Sabi<br>Style

The term essentially means finding beauty in imperfections.

---

<!-- _class: beige -->

# DIY<br>Home<br>Decor

Thousands of do-it-yourself home decoration ideas that will brighten your surroundings within an hour

---

<!-- _class: cream -->

# Let's DIY Together

Fit right into the new normal lifestyle and start spending your time wisely with do-it-yourself projects

---

<!-- _class: dark -->

# Find<br>Beauty<br>In The<br>Ordinary

<div class="frame">Wabi sabi is all about embracing the imperfections along with appreciating the flaws in life.</div>
