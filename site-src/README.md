# site-src — CHARA CHARA LAB サイトの原本（作業PCが編集する）

このフォルダは **CHARA CHARA LAB本体サイトのテンプレート原本** です。
ここを編集して push すると、番人PC側で `pull_templates.bat` を実行したときに取り込まれ、
全ページが再生成されて本番へ反映されます。

| ファイル | 生成されるページ | 消してはいけないプレースホルダ |
|---|---|---|
| index_template.html | index.html（トップ） | `{{ARTICLE_LIST}}` |
| archive_template.html | articles.html（記事一覧） | `{{ARTICLE_LIST}}` |
| blog_template.html | posts/*.html（記事ページ） | `{{TITLE}}` `{{DATE}}` `{{PILLAR}}` `{{PILLAR_CLASS}}` `{{READ}}` `{{OG_IMAGE}}` `{{CONTENT}}` |
| service-anime.html | service-anime.html（アニメーション制作） | なし（そのままコピーされる） |

## 注意

- **プレースホルダを消すと取り込みが拒否されます**（サイトが空になる事故を防ぐため）
- `<!-- GA-AUTOPILOT-START -->` 〜 `<!-- GA-AUTOPILOT-END -->` は解析タグの自動挿入枠です。手で書かないでください
- ここを編集しても**すぐには本番に反映されません**。番人PC側の取り込みが必要です（ボスに「テンプレ更新した」と伝える）
- リポジトリ直下の `index.html` `articles.html` `posts/*` は**生成物**です。直接編集しても次の記事投稿で上書きされます

詳細は引き継ぎ書（引き継ぎ書_CHARA-CHARA-LABサイト制作_作業PC用_20260805.md）を参照。
