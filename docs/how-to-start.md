# MkDocsを始める

## 公式サイト

* <https://www.mkdocs.org>

## Pythonの準備

Python環境を準備します。

```zsh
% python -m venv .venv
% . .venv/bin/activate
% pip install -U pip
```

## MkDocsのインストール

`pip`でインストールしますが、Material for MkDocs[^1]を利用する場合は、直接Material for MkDocsをインストールします。Material for MkDocsは互換性のあるMkDocsやその他の関連パッケージを自動的にインストールします[^2]。

```zsh
$ pip install mkdocs-material
```

MkDocsのみから始める場合は以下のようにします。

```zsh
% pip install mkdocs
```

[^1]: <https://squidfunk.github.io/mkdocs-material/>
[^2]: <https://squidfunk.github.io/mkdocs-material/getting-started/#installation>

## ドキュメント作成の開始

ドキュメントの作成は`mkdocs`コマンドを利用して開始します。リポジトリルートで以下のように実行すると良いです。

```zsh
% mkdocs new .
```

これで以下のようにファイルが作成されます。

```
/
|-docs
|  |- index.md
|- mkdocs.yml
```

次のコマンドでサーバーが実行され、ブラウザで作成中のドキュメントを確認できます。ホットリロードに対応しており、ドキュメントを編集し保存すると、自動的にリロードされます。

```zsh
% mkdocs serve
```

次のコマンドでドキュメントをビルドできます。

```zsh
% mkdocs build
```
