# Markdownの拡張機能

Python-Markdownの公式サポート拡張機能が使用できます。

* <https://python-markdown.github.io/sitemap.html>

## Abbreviations

* 略語の定義で、略語に対し、チップで説明文を表示します
* 単語区切りにスペースが必要で、日本語のように繋げて書く言語ではうまく動作しません
* 標準ライブラリに含まれます

```md
HTML 仕様書。
HTML仕様書。スペースがないため、認識しません。

*[HTML]: Hyper Text Markup Language
```

以下のようにレンダリングされます。

---

HTML 仕様書。

HTML仕様書。スペースがないため、認識しません。

*[HTML]: Hyper Text Markup Language

---

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - abbr
```

## Admonition

* 注記です。GitHubのAlertと記述方法が異なります
* 標準ライブラリに含まれます

```md
!!! note "タイトル (オプション)"
    これは注記として表示されます。
    改行時はインデントします。
```

以下のようにレンダリングされます。

---

!!! note "タイトル (オプション)"
    これは注記として表示されます。
    改行時はインデントします。

---

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - admonition
```

## Attribute Lists

* 出力されるHTMLに任意の属性を追加します
* 標準ライブラリに含まれます

```md
属性が付与される段落。`<p class="attr_class" id="attr_id">属性が付与される段落。</p>`となっており、`id`と`class`が付与されます。
{: #attr_id .attr_class }
```

以下のようにレンダリングされます。

---

属性が付与される段落。`<p class="attr_class" id="attr_id">属性が付与される段落。</p>`となっており、`id`と`class`が付与されます。
{: #attr_id .attr_class }

---

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - attr_list
```

## CodeHilite

* コードブロックをハイライト表示します
* 標準ライブラリに含まれます

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - codehilite:
    noclasses: true
    pygments_style: colorful
    linenums: false
```

## Definition Lists

* 用語などの定義リストです
* 標準ライブラリに含まれます

```md
MkDocs
:   プロジェクトドキュメントの構築を目的とした、高速、シンプル、
    そして、ゴージャスな静的サイトジェネレーターです。
```

以下のようにレンダリングされます。

---

MkDocs
:   プロジェクトドキュメントの構築を目的とした、高速、シンプル、
    そして、ゴージャスな静的サイトジェネレーターです。

---

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - def_list
```


<!-- * Extra -->

## Fenced Code Blocks

* ```で囲うコードブロックです
* 標準ライブラリに含まれます

````md
```
コードブロック
```
````

## Footnotes

* 脚注です
* 標準ライブラリに含まれます

```md
文章の中で補足したい内容は脚注[^1]として表現します。

[^1]: こちらは脚注です。
```

以下のようにレンダリングされます。脚注は文章の末尾にまとめて表示されます。

---

文章の中で補足したい内容は脚注[^1]として表現します。

[^1]: こちらは脚注です。

---

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - footnotes
```

## Meta-Data

* メタデータを記述します
* 標準ライブラリに含まれます

## New Line to Break

* 改行がハードブレイク (`<br/>`) として扱われます。
  改行して続けた場合、通常スペースに変換されますが、
  このオプションが有効な場合、`<br/>`になります。

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - nl2br
```

## Markdown in HTML

* HTMLタグ内の文字列をMarkdownとして処理します

```md
<div markdown="1">
* **ここに記述した文字列はMarkdownとして処理されます**
</div>
```

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - md_in_html
```

##  Sane Lists

* Markdownのリストの動作を少し変えます。通常、番号付きと番号なしの箇条書きを続けて記載すると、番号なしの箇条書きとして表示されますが、拡張機能が有効な場合は、別のリストとして表示されます。
* 標準ライブラリに含まれます

```md
4. 通常は1から始まるが、4からの箇条書きになる
5. 番号なし箇条書きとして表示される

* 別の箇条書きとして表示される
* 箇条書き
```

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - sane_lists
```

## SmartyPants

* ダッシュ、クォート、カッコを同等のHTMLエンティティに変換します

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - smarty
```

## Table of Contents

* `[TOC]`と記述することで、目次を追加します
* 標準ライブラリに含まれます

```md
[TOC]
```

以下のようにレンダリングされます。

---

[TOC]

---

## Tables

* 表をサポートします
* 標準ライブラリに含まれます

```md
ヘッダ | ヘッダ
------ | ------
セル   | セル
セル   | セル
```

以下のようにレンダリングされます。

---

ヘッダ | ヘッダ
------ | ------
セル   | セル
セル   | セル

---

## WikiLinks

* Wikiスタイルのリンク表記をサポートします。
* 標準ライブラリに含まれます

```md
[[how-to-start]]
```

有効化するには以下のように記述します。

```yaml
markdown_extensions:
  - wikilinks
```
