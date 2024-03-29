# rbenvを使用して最新とひとつ前のRubyをインストールする方法
## 実行環境
- 
- CentOS Linux 7 (Core)
## rbenvとは？
- Rubyのバージョン管理ツールのひとつ。
  - 異なるプロジェクトやアプリケーションで異なるRubyバージョンを利用することが可能となる。

## Homebrewのインストール
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## rbenvのインストール
```
brew install rbenv
```

## インストール手順

### 最新バージョン
- インストール可能なバージョンリストの確認
```
rbenv install --list
```
- 確認した最新バージョンのRubyをインストール
```
rbenv install <最新バージョン>
```
- インストールした最新バージョンをカレントディレクトリに適用
```
rbenv local <最新バージョン>
```
- バージョン確認
```
rbenv versions
```


### ひとつ前のバージョン
- 確認したバージョンリストの中から最新バージョンのひとつ前のRubyをインストール
```
rbenv install <ひとつ前のバージョン>
```
- インストールしたバージョンをカレントディレクトリに適用
```
rbenv local <ひとつ前のバージョン>
```
- バージョン確認
```
rbenv versions
```
