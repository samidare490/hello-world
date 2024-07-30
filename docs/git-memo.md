---
layout: page
title: "git memo"
permalink: /docs/git-memo
---

# ソフトウェア工学 2024

講義で学んだことをmarkdown形式でまとめる。

## git
gitとは、バージョン管理ツールである。ファイル更新の履歴を記録し、ロールバックなどが可能。  
また、ブランチを用いることで共同作業・並行作業が可能。

## 扱いの流れ
上位の操作は、リモートリポジトリを用いた場合に増える工程である。
1. 大元のbranchを設定(mainなど)
2. 編集用のbranchを作成(devなど)
   1. (編集用のbranch内で)編集する
   2. 編集箇所のうち、反映させたい変更をステージング
   3. ステージングされた変更をコミット
3. 変更をアップロードする(push)
4. 変更の統合を依頼する(pull-request)
5. 問題が無ければ変更を統合(merge)

### 主なコマンド
`git init` gitの初期化・設定開始  
`git status` ワークツリーのステータスを表示  
`git config` -global user.(name/email) ホスト全体のgitの設定  
  
`git add` ステージングエリアに追加  
`git commit` コミットの実行  
  -`git commit --amend --no-edit` コミットの修正  
`git checkout` 削除されたファイルの復旧、過去コミットの復元など  
`git reset` コミットのリセット  
`git revert` 「コミットの変更を打ち消す」コミット  
  
`git clone` レポジトリをコピー  
`git pull` リモートレポジトリの同期  
`git push` 変更をアップロードする  
`git request-pull` プルリクエスト  
`git remote` リモートレポジトリの設定  
  
`git branch` ブランチの作成  
`git checkout`ブランチの切り替え  
`git merge` ブランチの統合  
  -`git merge --ff-only` 変更のない統合先ブランチにマージ  
`git clone` レポジトリをコピー  
`git push` 変更をアップロードする  
  
`git log (-oneline)` 変更履歴を（1行単位で）表示  
`git stash` 一次避難