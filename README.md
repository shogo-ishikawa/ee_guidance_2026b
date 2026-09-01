# 電気電子工学科 2026年度後期 履修ガイダンス

2026年度3Q・4Qの履修ガイダンスを、電気電子工学科1年生向けに整理したQuartoサイトです。

## サイト構成

- `index.qmd`：重要日程と、最初に行うこと
- `guidance.qmd`：9月14日の教科ガイダンス、9月16日の履修相談
- `registration.qmd`：履修登録、時間割作成、定員超過時の対応
- `textbooks.qmd`：教科書販売場所、期間、取扱教科書
- `_variables.yml`：Boxリンク、更新日などの頻繁に変わる情報

元のPowerPoint、Word、PDFは公開リポジトリに保存していません。必要な内容だけをHTML向けに再構成しています。

## Boxファイルを掲載する

クラス分け表をBoxへ置いたら、`_variables.yml` の次の項目を変更します。

```yaml
box_file_url: "Boxの共有URL"
box_file_status: "掲載中"
box_file_updated: "2026年9月○日 ○:○○"
```

Box側では、同じファイルに「新しいバージョンをアップロード」して更新します。ファイルを削除して作り直さなければ、サイト側のURLを変更せずに最新版を案内できます。学籍番号などを含む場合は、Boxの共有範囲を学内利用者限定・閲覧のみとしてください。

## ローカルで確認する

Quartoをインストールした環境で実行します。

```bash
quarto preview
```

## 公開

`main` への更新時にGitHub ActionsがQuartoを描画し、GitHub Pagesへ公開します。初回だけ、リポジトリの `Settings` → `Pages` → `Build and deployment` で、`Source` を `GitHub Actions` に設定してください。

公開先：<https://shogo-ishikawa.github.io/ee_guidance_2026b/>

公開期間終了後は、GitHub Pagesを無効化します。`noindex` は検索結果への掲載を抑えるための指定であり、アクセス制限ではありません。
