# NaokiOya-example-001

https://www.qript.co.jp/blog/technique/1268/

・git commeit --amend（コミットやりなおし）
直前のCommitに対してコメントの修正したいときや、追加するファイルを忘れてそのままCommitしてしまったので修正したいときにはamendを使います。
Commitした後で「Commit」→「Amend latest commit」をチェック
さっき自分が入力したメッセージが表示されるので、これに上書きをして再度Commitします。
(直前のCommitデータを上書きする形になるので、最終的には1つのCommitになります。)

・git reset --head（強制的にワーキングスペースを対象のリビジョンに書き換え）
Commitがこまかすぎて、後になってまとめたいときにもresetは使えます。
戻りたい地点のCommitを選択し、「Reset current branch to this commit」
その後、新しくCommitすることでCommitをまとめることができます。

https://noumenon-th.net/programming/2018/12/16/gitrevert/
・git revert（特定のリビジョンをうちけすコミットを作成する）
「cを追加」コミットをrevertによって取り消してみます。右クリックで「コミット適用前に戻す…」を選択します。
「cを追加」コミットは残ったままで、「Revert”cを追加”」といコミットが新しく生成されます。この時ファイルの文字列は「abc」から「ab」になります。

https://qiita.com/coa00/items/1206a9538d4d108ff9ba
・git pull --rebase（fetch&margeではなくて、fetch&rebaseでremoteの情報をもってくる）
pull時にmergeではなくrebaseする。
環境設定->Gitで設定します。
日本版だとmergeのかわりにrebaseを使います。
英語版だとUse rebase instead of merge by ...
をチェックをいれます。
pull時に選択も可能です。

