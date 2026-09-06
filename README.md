# sanc-official.github.io

GitHub Pages（ユーザーサイト）配信用リポジトリ。
**クライアントへ配布する静的ページだけを置く。公開されて困るものは絶対に置かない。**

## 経緯

記入シートは元々 `sanc-official/Tools` の GitHub Pages で配信していたが、
2026-09-04 に同リポジトリを private 化した時点で Pages が無効化され、
配布済みURLが 404 になった（無料アカウントでは private リポジトリの Pages が使えない）。

`Tools` を public に戻すと請求書PDFのGASコードや他クライアントの記入シートまで
公開されるため、**同一URLを再現できる本リポジトリへ該当ファイルだけを切り出した**。

## 配信中のページ

| パス | 用途 | 配布先 |
|---|---|---|
| `Tools/HearingSheet/jgs-2026-k4f9d2/naika.html` | 内科ページ 掲載内容 記入シート | 荒井 研 先生 |
| `Tools/HearingSheet/jgs-2026-k4f9d2/ganka.html` | 眼科ページ 掲載内容 記入シート | 荒井 陽夏 先生 |

`Tools/HearingSheet/...` というパスは、2026-09-02 に先生へ送信済みのURLを
そのまま生かすために維持している。**リネームしないこと。**

## 運用ルール

- 各ページに `noindex,nofollow,noarchive` を付与し、`robots.txt` で全体を Disallow。
  URLを知っている人だけが開ける状態を維持する
- 記入内容の送信は「コピー → メール返信」方式。サーバへは何も送らない
  （`SUBMIT_URL` は空のまま。GASは未使用）
- 正本は案件フォルダ側の `forms/genko_naika_arai-ken.html` /
  `forms/genko_ganka_arai-haruka.html`。修正はそちらを直してからここへ反映する
