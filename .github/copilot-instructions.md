# リポジトリの説明

このリポジトリは、『代数学2 環と体とガロア理論 [第2版]』（雪江明彦, 日本評論社）の演習問題解答を管理するものです。

## ドキュメント構成

- `main.tex` — エントリーポイント。プリアンブルのインクルードと各章ファイルの入力
- `preamble.tex` — パッケージと独自マクロの定義
- `chapters/chXX/secXX_YY.tex` — 節ごとの解答ファイル（例: `ch01/sec01_01.tex`）

## ans 環境

各解答は、**手動で番号を指定する**独自の `ans` 環境を使用する:

```latex
\begin{ans}{1.1.3}
  ...
\end{ans}
```

番号の形式は `章.節.問番号`。番号引数なしの `\begin{ans}` は使用しない。

## レビュー観点

Pull Request レビュー時は [REVIEW_GUIDELINES.md](../REVIEW_GUIDELINES.md) の観点に従って確認する。

## ビルド

LuaLaTeX を使用して `latexmk` でコンパイルする。GitHub Actions により `main` ブランチへの push 時に自動でコンパイルされ、PDF がリリースとして公開される。
