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

https://noumenon-th.net/programming/2018/12/15/gitreset/
・git reset --soft
git resetでコミット自体をなかったことにして、過去のコミットの状態へ戻すことができます。その方法には主にMixed・Soft・Hardの3つのパターンが存在します。
まずは視覚的に分かりやすいSourcetreeで説明してみます。
下記画像は、1つのファイルを生成し、単純にテキストでabcdと一文字づつ追加していくごとにコミットしていったSourcetreeの様子です。
この状態から「bを追加」の状態のコミットに戻してみます。「bを追加」上で右クリックし、「このコミットまでmasterを元に戻す」を選択します。
すると「Soft」「Mixed」「Hard」の3つのモードを選択することができます。デフォルトはMixedです。
それぞれのモードを選択した時のコミットの戻り方は以下のようになります。
2. Softを選択した場合
Softでコミットを戻した場合、編集しているファイルは「abcd」のままです（作業コピーの変更内容を保持）。ファイルはステージにいるのが分かります。




