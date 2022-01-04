# git 利用方法

1. mac に git をインストール

```
brew install git
```

2. github アカウント作成

```
https://github.com/

アクセスしてアカウント作成する
```

3. ssh アクセス可能にする

```
# ssh キー作成
ssh-keygen -t ed25519 -N "" -f ~/.ssh/github

# ssh キー登録 設定画面
https://github.com/settings/keys

# New SSH key をクリック
# クリップボードにキーをコピー
pbcopy < ~/.ssh/github.pub
# Add SSH Key で鍵登録

# ssh 接続設定追加
vi ~/.ssh/config
Host github.com
  IdentityFile ~/.ssh/github
  User git

# 接続確認 (successfullyのメッセージが出たら完了)
ssh -T github.com
```

4. clone する

```
# サイトでリポジトリを作成し cloneする
git clone git@github.com:beast-zer0-0303/note
```

5. push

```
# 変更内容をindexに追加
git add ./

# commit
git commit -m ''

# ローカルレポジトリの変更内容をリモートレポジトリに反映する
git push

# ローカルレポジトリの変更内容をリモートレポジトリに反映する
git pull

# ローカルリポジトリの情報を確認
git status
```
