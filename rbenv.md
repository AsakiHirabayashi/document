# rbenvを使用して最新とひとつ前のRubyをインストールする方法
## 実行環境
- macOS
- CentOS Linux 7 (Core)
## rbenvとは？
- Rubyのバージョン管理ツールのひとつ。
  - 異なるプロジェクトやアプリケーションで異なるRubyバージョンを利用することが可能となる。
  
## macOSの場合

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

## CentOS7の場合

### Git
-  インストール
```
sudo yum -y install git
```


- バージョン確認
```
git --version
```

### rbenv
- rbenvインストール
```
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
```
- ディレクトリ確認
```
ls -d ~/.rbenv
```

### ruby-build
- インストール
```
git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
```
- ディレクトリ確認
```
ls -d ~/.rbenv/plugins/ruby-build
```

### .bash_profile
- 設定
```
echo '# rbenv' >> ~/.bash_profile
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
```

- 確認
```
cat ~/.bash_profile
```

- 反映
```
exec $SHELL --login
```

### パッケージ
- rubyのインストールに必要なパッケージをインストール
```
sudo yum -y install bzip2 gcc openssl-devel readline-devel zlib-devel
```

- バージョン確認
```
bzip2 --version
gcc --version
yum list installed | grep openssl-devel
yum list installed | grep readline-devel
yum list installed | grep zlib-devel
```

### ruby
- バージョン確認
```
rbenv --version
```
- インストールできるrubyのバージョンを確認
```
rbenv install --list
```
- rubyインストール
```
rbenv install 3.2.3
```
- 切り替え可能なrubyのバージョンを確認
```
rbenv versions
```
- rubyのバージョンを切り替え
```
rbenv local 3.2.3
```
- rubyのバージョンが切り替わったことを確認
```
rbenv versions
```
