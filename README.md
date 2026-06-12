# marp-template

ビジネス向け Marp スライドテンプレート集。

## minimal-pro テンプレート(本番用)

`demo/minimal-pro.md` のミニマル白基調デザインを、共有テーマCSS + 12種のスライドタイプに拡充したもの。

- テーマ本体: `themes/minimal-pro.css`(`/* @theme minimal-pro */`、Marp Core の `default` テーマを継承)
- サンプルデック: `templates/minimal-pro.md`(日本語ビジネス文面・12スライド)
- フォント: `templates/fonts/`(Inter 可変フォント + Noto Sans JP 可変フォント を同梱、オフラインで日本語表示可)
- レンダリング結果: `templates/out/`

### 用意したスライドタイプ

| クラス | 用途 |
|---|---|
| `cover` | 表紙 |
| `agenda` | 目次 |
| `section` | セクション区切り(章番号付き) |
| `content` | 本文テキスト + 写真 |
| `duo` | 2カラム(写真+テキスト) |
| `gallery` | 写真3枚グリッド |
| `stats` | 統計・指標 |
| `quote` | 引用(`>` のMarkdown記法を使用) |
| `list` | アイコン付き特徴リスト(2×2) |
| `table` | 表(Markdownの表記法を使用) |
| `team` | メンバー紹介 |
| `closing` | クロージング |

`cover` / `closing` / `section`(区切り)はページ番号・ヘッダーをCSSで非表示にしている。
`<!-- _paginate: skip -->` を付けたスライド(cover/closing)はページ番号のカウントからも除外される。

### 使い方

```sh
# CLIでテーマを指定してPNG出力
npx marp --theme-set themes --allow-local-files --images png -o templates/out/minimal-pro.png templates/minimal-pro.md

# npm script でも同じことができる
npm run render

# プレビュー(ブラウザでホットリロード)
npm run preview
```

md側は以下のようにフロントマターで `theme: minimal-pro` を指定し、`<!-- _class: ... -->` でスライドタイプを切り替える。

```yaml
---
marp: true
theme: minimal-pro
size: 16:9
paginate: true
header: '会社名 — タイトル'
---
```

### VS Code でのプレビュー

[Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) 拡張を入れた状態で、本リポジトリの `.vscode/settings.json` に以下が設定済み:

```json
{ "markdown.marp.themes": ["./themes/minimal-pro.css"] }
```

これにより `templates/minimal-pro.md` をVS Codeで開いてプレビューすれば、`theme: minimal-pro` がそのまま適用される。

### フォントの配置規約(重要)

**テーマCSS内の `url()` で参照するフォントは、変換対象の Markdown ファイルと同じ階層の `fonts/` ディレクトリに置くこと。**

marp-cli は PNG/PDF/PPTX 変換時、一時HTMLに `<base href="(入力mdファイルの絶対パス)">` を注入するため、テーマCSS内の相対パスは**テーマファイル基準ではなく md ファイル基準**で解決される([参考](https://github.com/marp-team/marp/discussions/86))。そのため、このテンプレートを他のディレクトリにコピーして使う場合は、`templates/minimal-pro.md` と `templates/fonts/` を**セットでコピー**すること(ルート共有の `fonts/` には依存しない)。

- `templates/fonts/inter-var.woff2` — Inter(可変フォント)
- `templates/fonts/NotoSansJP.ttf` — Noto Sans JP(可変フォント、[google/fonts](https://github.com/google/fonts/tree/main/ofl/notosansjp) より取得、SIL Open Font License 1.1。`OFL.txt` を同梱)

`--allow-local-files` 変換時にフォントが見つからない場合、marp-cli が `Not found local file(s)` という警告を出すので、レンダリング時はこの警告が出ていないか確認する。

## 検証用プロトタイプ(demo/)

参考デザイン3種を Marp で再現できるか検証し、`demo/` にプロトタイプを作成済み。
いずれも再現可能(レンダリング結果は `demo/out/` を参照)。

| デモ | 元デザイン | 再現度 | 備考 |
|---|---|---|---|
| `demo/business-blue.md` | 青系コーポレート(PowerPoint風) | ほぼ完全 | 図形・帯・カードは全て CSS で再現。アイコンは絵文字を仮置き(SVG アイコンに差し替え可) |
| `demo/wabi-sabi.md` | 漆喰テクスチャ × コンデンス書体 | 高 | テクスチャは SVG `feTurbulence` で生成(画像ファイル不要)。実写の漆喰質感が必要なら写真素材に差し替え |
| `demo/minimal-pro.md` | ミニマル白基調(Slide Pro) | ほぼ完全 | 写真はプレースホルダ。実運用では `img` タグまたは `![bg]` 構文で配置 |

## 技術メモ

- 複雑なレイアウト(カード、円形アイコン、絶対配置)はインライン HTML + CSS で実現。
  `div` / `span` などは Marp Core v4 のデフォルト許可リストに含まれるためそのまま動くが、
  環境差異を避けるなら CLI の `--html` や VS Code の `markdown.marp.html` を有効にする。
- `<header>` / `<footer>` タグは許可リスト外でエスケープされるため、
  Marp 標準の `header:` ディレクティブ(フロントマター)を使うこと。
  ディレクティブ内は Markdown が使える(例: `header: '**Business** *template*'`)。
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
