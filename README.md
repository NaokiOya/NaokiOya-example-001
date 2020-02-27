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


