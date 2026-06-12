# marp-template

ビジネス向け Marp スライドテンプレート集(検証中)。

## 再現可能性の検証結果

参考デザイン3種を Marp で再現できるか検証し、`demo/` にプロトタイプを作成済み。
いずれも再現可能(レンダリング結果は `demo/out/` を参照)。

| デモ | 元デザイン | 再現度 | 備考 |
|---|---|---|---|
| `demo/business-blue.md` | 青系コーポレート(PowerPoint風) | ほぼ完全 | 図形・帯・カードは全て CSS で再現。アイコンは絵文字を仮置き(SVG アイコンに差し替え可) |
| `demo/wabi-sabi.md` | 漆喰テクスチャ × コンデンス書体 | 高 | テクスチャは SVG `feTurbulence` で生成(画像ファイル不要)。実写の漆喰質感が必要なら写真素材に差し替え |
| `demo/minimal-pro.md` | ミニマル白基調(Slide Pro) | ほぼ完全 | 写真はプレースホルダ。実運用では `img` タグまたは `![bg]` 構文で配置 |

## 技術メモ

- 複雑なレイアウト(カード、円形アイコン、絶対配置)はインライン HTML + CSS で実現。
  フロントマターの `html: true`(または CLI の `--html`)が必要。
- フォントは `demo/fonts/` に同梱(woff2、Google Fonts 由来)。オフラインでもレンダリング可能。
  オンライン前提なら `@import url('https://fonts.googleapis.com/...')` でも可。
- スライドごとのレイアウト切り替えは `<!-- _class: title -->` などのクラス指定で行う。

## レンダリング方法

```sh
npm install

# PNG 出力(全スライド)
npx marp --html --allow-local-files --images png -o demo/out/business-blue.png demo/business-blue.md

# PDF 出力
npx marp --html --allow-local-files --pdf demo/business-blue.md

# プレビュー(VS Code の Marp 拡張でも可。その場合は markdown.marp.html を有効にする)
npx marp --html -s demo/
```

※ PNG / PDF 出力には Chrome / Chromium が必要(`CHROME_PATH` で指定可)。
