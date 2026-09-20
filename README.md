# portal — つくったもの一覧

pikaring が公開しているツールとゲームの入口ページです。

**https://pikaring.github.io/portal/**

各ツールの紹介ページからは、このポータルへの1リンクだけを貼っています。
ツールを増やしたときに全ページを直さなくて済むようにするためです。

## ファイル

| ファイル | 役割 |
| --- | --- |
| `index.html` | カードの一覧（アプリを増やすときはここだけ直す） |
| `assets/site.css` | 各ツールの紹介ページと同じ配色・書体・角丸 |
| `assets/icon.svg` | ファビコン |

## アプリを増やすとき

`index.html` の該当セクション（`あそぶ` か `つかう`）にある `<a class="card">` を
1つコピーして、リンク先・アイコン・見出し・説明・タグを書き換えます。

```html
<a class="card" href="https://pikaring.github.io/新しいアプリ/">
  <img class="card__icon" src="https://pikaring.github.io/新しいアプリ/assets/icon.png" alt="" width="64" height="64" loading="lazy">
  <div class="card__body">
    <h3>アプリの名前</h3>
    <p>ひとことの説明。</p>
    <p class="card__tags"><span class="tag">ブラウザ</span></p>
  </div>
</a>
```

アイコンは各リポジトリの公開URLをそのまま参照しているので、このリポジトリに
画像をコピーする必要はありません（同じ `pikaring.github.io` 上なので確実に読めます）。

## 掲載しているもの

あそぶ: Tap on KOTOBA / ねこの ともだち / Reach on SANMA / All in TEXAS
つかう: Ride on QC / Eat on GPX / ROCK ON MJ

## GitHub Pages

Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `/ (root)`
