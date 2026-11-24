# fitlife（健康管理）

FitLife（ふたり用の健康管理）のアプリ本体です（データは入っていません。ログインした本人だけが自分のデータを読み書きできます）。ルールは firestore.rules。

もとは `apps` リポジトリの中の1フォルダでしたが、2026-11-24 に独立したリポジトリに分けました。

- 本体は `index.html`、`foods.js` … 食べ物のデータ、`exercises.js` … 運動のデータ、`pet.js` … ペット（うり坊）
- `chars/` … うり坊の画像
- `shared/` … 共通の土台（ログイン・保存と同期）

## 公開

main に反映すると、GitHub Actions（`.github/workflows/pages.yml`）が GitHub Pages に公開します。公開の直前に `.github/scripts/stamp.py` が版の番号（日本時間の日時）を自動で付けます。
（リポジトリの Settings → Pages → Source は「GitHub Actions」にしておく）
