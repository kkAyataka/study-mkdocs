# ページの構成

## インデックスページ

インデックスページ (トップページ) には特定のファイル名のファイルが使用されます。以下の2つのファイル名が使用できます[^1]。

* index.md (デフォルトで優先)
* README.md (index.mdがない場合)

GitHubなどでの見え方を考慮すると、**README.mdが良い**でしょう。ただし、HTMLに変換時はindex.htmlとなるため、リンクを貼る際には注意が必要です。

[^1]: <https://www.mkdocs.org/user-guide/writing-your-docs/#index-pages>

## ページの構成

MkDocsは既定で、すべてのMarkdownをドキュメントに取り込みますが、ファイル順にソートされます。任意の順番にするには、`mkdocs.yml`の`nav`で指定します[^2]。

[^2]: <https://www.mkdocs.org/user-guide/configuration/#nav>

```yaml
nav:
  - how-to-start.md
  - markdown.md
  - markdown-extensions.md
  # 以下のようにするとサブページとしてリストされます
  - フォルダ:
    - sub/index.md
    - sub/index2.md
```
