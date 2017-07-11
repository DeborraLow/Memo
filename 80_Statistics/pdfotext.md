pdftotextというコマンドがあるらしい

[xpdfを使ってPDFから日本語抽出](http://akkunchoi.github.io/xpdf-japanese.html)を参考にした。

## 1. brewを経由してxpdfをインストール

```
brew install xpdf
```
このままだと文字化けしてしまう。

## 2. 日本語に対応させる
> xpdfのサイトからLanguage Support Packagesの xpdf-japanese.tar.gz をダウンロード。
> 解凍したものを /Ryohei/local/share/xpdf/japanese に配置する。

```
sudo mkdir xpdf
mkdir: xpdf: Operation not permitted
```
[初心者向け MacでOperation not permittedの解決方法](http://qiita.com/iwaseasahi/items/9d2e29b02df5cce7285d)

> /usr/local/etc/xpdfrc に add-to-xpdfrc の内容を追記する。
> ここまでだと、エラーはなくなるが、日本語が読み飛ばされる。textEncoding設定のコメントを外す