# POG マネージャー

## ファイル構成
```
index.html          ← メインビューワー（これをGitHub Pagesで公開）
data/
  manifest.json     ← シーズン一覧（ここに追加していく）
  スマ勢24-25.json  ← 各シーズンのデータ
  スマ勢25-26.json  ← 追加していく
  ...
```

## 新シーズンの追加方法

1. `index.html` を開く
2. 右上の「＋ データ追加」でPOGスタリオンのグループ一覧HTMLを貼り付け
3. JSONファイルがダウンロードされるので `data/` フォルダに保存
4. `data/manifest.json` にエントリを追加：

```json
{
  "seasons": [
    { "key": "スマ勢24-25", "file": "data/スマ勢24-25.json", "name": "スマ勢24-25", "year": "2024/05/26〜2025/06/01" },
    { "key": "スマ勢25-26", "file": "data/スマ勢25-26.json", "name": "スマ勢25-26", "year": "2025/05/25〜2026/06/01" }
  ]
}
```

5. GitHubにpush → GitHub Pagesで自動反映

## 馬データの追加（より詳細に）

グループ一覧を取り込んだ後、各ユーザーの馬一覧HTMLも同様に取り込むと馬データが充実します。
その場合はJSONを手動で編集して `horses` 配列を追加してください。

## GitHub Pages の設定

1. GitHubで新しいリポジトリを作成
2. このフォルダの中身を全部push
3. Settings → Pages → Branch: main / folder: / (root)
4. 公開URLにアクセス
