# authorization-app-practice

## 概要
COACHTECH 教材 Tutorial 10-3「認可機能 ハンズオン演習」で作成した成果物です。ポリシーを使って、投稿の作成者のみが編集・削除できる「投稿管理機能」を作成しました。

## 使用技術
- PHP 8.x
- Laravel 10.x
- Policy / Gate（認可）
- Laravel Fortify（認証）

## 学んだこと
- @canディレクティブを使った、Bladeでの権限チェック
- $this->authorize()を使った、コントローラーでの権限チェック
- 権限管理における、ポリシーとゲートについて

## 動作確認の手順
- ブラウザで http://localhost にアクセス
- usera@example.com / password でログインする
- ユーザーAの投稿にのみ「編集」「削除」のボタンが表示されることを確認する
- ユーザーBの投稿を直接編集しようとする（http://localhost/posts/3/edit）と403エラーが表示されることを確認する
- ログアウト後、userb@example.com / password でログインするとユーザーBの投稿にのみ「編集」「削除」ボタンが表示されることを確認する