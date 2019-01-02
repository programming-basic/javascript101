# プログラミング基礎 JavaScript編 part1

## 1. Webブラウザーでファイルを開く

**1-1. テキストエディタ（メモ帳）を開きます。**

> **メモ：**メモ帳の開き方（Windows7 の場合）
> 
> a\. \[スタート\] メニューから \[すべてのプログラム\] を選びます
> ![](media/image9.png){width="3.9270833333333335in" height="1.1041666666666667in"} 
>                                 
> b\. 現れてきたメニュー項目から \[アクセサリ\] を開きその中の \[メモ帳\] を選びます                                              
>
> ![](media/image7.png){width="3.9398534558180227in" height="3.4739588801399823in"}                                     
>

※ここではメモ帳を使った場合を例に詳しい手順を紹介していますが、テキストファイルが編集できるソフトウェアであれば、メモ帳以外でも実施可能です。メモ帳はテキストファイルを編集するソフトウェアで
Windows
に標準で入っていますので、簡単に始められるという観点でメモ帳を例にしています。

**1-2. 次のようにタイプしてください **

```
ボタンをクリックしてね！音が出ます！
```

> **メモ：**
>
> メモ帳の白い領域が編集領域です。ここに文字を入力、作業が終わるとメモ帳の画面は次のような感じになっていると思います。
> 
>
> ![](media/image6.png){width="6.114583333333333in" height="1.96875in"}

**1-3. 次のファイル名で保存します**

piano\_step0.txt

> **メモ：** 
>
> メモ帳でファイル名をつけて保存するには次のようにします
> 
> a\. \[ファイル\] -\> \[名前をつけて保存(A)\...\] を選びます
>
> ![](media/image12.png){width="4.177083333333333in" height="2.5833333333333335in"} 
>
> b. ファイルの保存場所とファイル名を入力するダイアログウィンドウが開かれます。指定のファイル名(piano\_step0.txt)を入力し、文字コードは UTF-8 を選んでください。
>
> ![](media/image10.png){width="6.114583333333333in" height="4.25in"} 
>
> c\. 保存する場所を決めて、\[保存\] ボタンを押します。上の例では「ライブラリ」の「ドキュメント」フォルダーの下に保存しようとしています。

**1-4. 作成したファイルを Google Chrome で開いてみます。次のようにタイプした文字が表示されると思います。**

![](media/image4.png){width="6.270833333333333in"
height="1.4722222222222223in"}

> **メモ：** 
> 
> PC上で自前で作ったファイル（ローカルのファイル）を Google Chrome で開くには、開きたいファイルをGoogle Chrome のドラッグ&ドロップします
>
> ![](media/image8.png){width="6.114583333333333in" height="3.3194444444444446in"} 

Google Chrome をはじめインターネットブラウザーは通常インターネットにアクセスして、インターネット上にあるファイルを開くために用いますが、このように自分のパソコンの中にあるファイルを開くこともできます。今回はこのようにしてノートパッドでプログラミングをして、これを
Google Chrome で開くことで確認していきます。

（今回作ったものを誰でも使えるようにするにはどうすればいいのかとうことは次回以降で説明します）

## 2. HTML ファイルを作る

**2-1. 前回と同じ要領で今度は piano.htmlというファイル名で、次の内容のファイルを作成してください。**

（記号のような文字も含まれていますので、打ち間違えを防ぐためこの説明文の中の内容をコピー＆ペーストされることを推奨します）

piano.html
``` 
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
</head>
<body>
ボタンをクリックしてね！音が出ます！
</body>
</html>
```

**2-2. 前回と同じ要領で Google Chrome で先ほど編集したファイルを開いてみてください。**

![](media/image4.png){width="6.270833333333333in" height="1.4722222222222223in"}

前回と同じような文字が表示されると思います。前回とは違って今回は
\<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 4.01 Transitional//EN\"\> とか
\<head\> とか色々な文字を入力したのですが、これらを Google Chrome
は表示しません。何故でしょうか？

今回作成したファイルはファイル名の最後を .html
としました。ファイル名の「.」の後の文字を拡張子と言います。この拡張子の文字が何かによって
Google Chrome
はファイルの種類を判別しました。拡張子が「html」のファイルを Google
Chrome は「HTML
形式のファイル」であると解釈し、その表示のルールにしたがってファイルの内容を表示しました。

「HTML 形式のファイル」では表示するテキストに加え、それらをどのように表示させるかという情報を付加されることができます。Webブラウザーで表示されるインターネット上のコンテンツは基本、この「HTML
形式のファイル」で記述されています。「HTML 形式のファイル」では
「\<」記号から始まり 「\>」記号までのとこを「HTMLタグ」といい、これは
Webブラウザーに直接表示されるのではなく、表示されるべき内容を修飾する働きをします。

次の作業で具体的な例をみてみましょう。

**2-3. 「ボタンをクリックしてね！音が出ます！」の文字の前に \<h1\>を、最後の文字の後に \</h1\> という文字を加えてみてください。全体としては次のような感じです。**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html lang="ja">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
</head>
<body>
<h1>ボタンをクリックしてね！音が出ます！</h1>
</body>
</html>
```

変更したら内容を上書き保存します。

> **メモ：** 
>
> メモ帳でファイルを上書き保存（変更した内容を保存する）はメニューから \[ファイル\] -\> \[上書き保存\] を選択します 
>
> ![](media/image11.png){width="6.114583333333333in" height="2.1527777777777777in"}                                        |

**2-4. Google Chrome で同じファイルをもう一度開きます。文字のサイズが大きくなったと思います。**

![](media/image14.png){width="6.270833333333333in"
height="1.5416666666666667in"}

\<h1\>
は見出しタグと呼ばれるもので、その後に続く文字を強調して表示させます。
\<h1\>
タグは見出しタグの中でも大見出しタグとも呼ばれ、見出し文字の中でも最も強調したいものに使います。「\</」から始まり「\>」で終わるのは終了タグと呼ばれるもので、\<h1\>
で指定した効果がここで終了することを示しています。　見出しタグにはこれ以外にも
\<h2\>, \<h3\>, \<h4\>, \<h5\>, \<h6\>
とあり、順番に強調の度合いが低くなります。

例えば「音が出ます！」の部分だけ h3
の見出しタグの文字として表示させたい場合はこんな感じです

\<h1\>ボタンをクリックしてね！\</h1\>\<h3\>音が出ます！\</h3\>

色々試してみて表示がどのように変わるか試してみてください。いくら変更して試してみてもパソコンが壊れるわけでも、お金がかかるわけでもありません、プログラミングや
IT
に関する技術を身に付けるには、まず色々試してみるのが最も近道だと思います。

見出しタグ以外にも文字を装飾する様々なタグがあります。詳しくはインターネットから調べてみてください。例えば次のページは参考になります。

[[http://www.htmq.com/html/indexm.shtml]{.underline}](http://www.htmq.com/html/indexm.shtml)

**3. ページにボタンを追加する**

3-1.
ページにボタンを追加します。「\<h1\>ボタンをクリックしてね！音が出ます！\</h1\>」の後に「\<button
style=\"width:80px;height:250px;\"\>ド
\</button\>」という内容を追加してください。全体は次のような感じになっていると思います。

+-----------------------------------------------------------------------+
| \<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 4.01 Transitional//EN\"\>   |
|                                                                       |
| \<html lang=\"ja\"\>                                                  |
|                                                                       |
| \<head\>                                                              |
|                                                                       |
| \<meta http-equiv=\"Content-Type\" content=\"text/html;               |
| charset=UTF-8\"\>                                                     |
|                                                                       |
| \</head\>                                                             |
|                                                                       |
| \<body\>                                                              |
|                                                                       |
| \<h1\>ボタンをクリックしてね！音が出ます！\</h1\>                     |
|                                                                       |
| \<button style=\"width:80px;height:250px;\"\>ド \</button\>           |
|                                                                       |
| \</body\>                                                             |
|                                                                       |
| \</html\>                                                             |
+-----------------------------------------------------------------------+

3-2. 保存して Google Chrome
で開きます。縦長のボタンが一つページに表示されるようになったと思います。

![](media/image3.png){width="6.270833333333333in"
height="4.347222222222222in"}

ここで追加したのは button
タグというもので、画面にボタンを表示します。button タグの中にある「
style=\"width:80px;height:250px;\"」の部分でボタンの見え方を指定しています。ここでは幅
80、高さ 250
で指定しています。このようにタグの中に含まれれ、追加の情報を与えているもののことを属性といい、style=
から始まるものは style属性といいます。 style属性では CSS
という記述ルールにしたがってタグに対する見た目（スタイル）の情報を与えています。
CSS
は通常ページ全体の見た目に統一感を持たせるために用いられるもので、タグの中で属性として直接書き込むことはあまりないのですが、ここではページの構造をシンプルにするために、style属性を用いました。

**4. ページに JavaScript のプログラムを追加し、音が鳴るようにする**

4-1. \<head\> と \</head\> の間に次の内容を追加します

+-----------------------------------------------------------------------+
| \<script\>                                                            |
|                                                                       |
| function playDo() {                                                   |
|                                                                       |
| let audio = new                                                       |
| Audio(\"http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3\");       |
|                                                                       |
| audio.play();                                                         |
|                                                                       |
| }                                                                     |
|                                                                       |
| \</script\>                                                           |
+-----------------------------------------------------------------------+

4-2. \<button\> タグに属性として onclock="playDo()"
を追加します。ここまで終了すると piano.html
は次のような感じになっていると思います。

+-----------------------------------------------------------------------+
| \<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 4.01 Transitional//EN\"\>   |
|                                                                       |
| \<html lang=\"ja\"\>                                                  |
|                                                                       |
| \<head\>                                                              |
|                                                                       |
| \<meta http-equiv=\"Content-Type\" content=\"text/html;               |
| charset=UTF-8\"\>                                                     |
|                                                                       |
| \<script\>                                                            |
|                                                                       |
| function playDo() {                                                   |
|                                                                       |
| let audio = new                                                       |
| Audio(\"http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3\");       |
|                                                                       |
| audio.play();                                                         |
|                                                                       |
| }                                                                     |
|                                                                       |
| \</script\>                                                           |
|                                                                       |
| \</head\>                                                             |
|                                                                       |
| \<body\>                                                              |
|                                                                       |
| \<h1\>ボタンをクリックしてね！音が出ます！\</h1\>                     |
|                                                                       |
| \<button style=\"width:80px;height:250px;\" onclick=\"playDo()\"\>ド  |
| \</button\>                                                           |
|                                                                       |
| \</body\>                                                             |
|                                                                       |
| \</html\>                                                             |
+-----------------------------------------------------------------------+

4-3. 再び Google Chrome
で開いてみましょう。ボタンをクリックしたら音が出ると思います。どうでしょう？

![](media/image2.png){width="6.270833333333333in"
height="4.347222222222222in"}

\<script\> タグは HTML
ページの中にプログラムを埋め込む時に使います。\<script\>
タグとその終了タグ \</script\> の間の文字はプログラムとして扱われます。

プログラムはコンピューターに実行させる命令を記述したものです。決められたルールにしたがって命令を書くことで、それが読み取られ、実行されます。

今回のプログラムは JavaScript
というプログラミング言語のルールにしたがって記述しています。プログラミングの書き方はプログラミング言語によって体系化されています。プログラミング言語には
JavaScript
言語以外にも、Python言語、C/C++言語、Java言語など様々あり、それぞれ書き方のルールが少しずつ異なっています。Webブラウザーで実行させるプログラムは通常
JavaScript 言語を使います。

ここでは JavaScript の文法ルールについてみていきましょう。

JavaScript では
「{」から「}」までを一つのブロックとして考えます。今回の例では

+-----------------------------------------------------------------------+
| {                                                                     |
|                                                                       |
| let audio = new                                                       |
| Audio(\"http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3\");       |
|                                                                       |
| audio.play();                                                         |
|                                                                       |
| }                                                                     |
+-----------------------------------------------------------------------+

が一つのかたまりです。各行の最後にある「; 」(セミコロン）記号は
一つの処理命令の終了を示すために記述します。

一つずつ処理をみていきます。

let audio = new
Audio(\"http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3\");

はドの音をだす、音楽ファイルをインターネットから読み込んでいます。読み込んだ情報は
audio
という「変数」に保存しています。「変数」は情報の一時的な保存場所です。変数を用意して、そこに情報を入れる基本的な書き方のルールは

let 変数名 = 変数に入れる内容

です。こうすることで、後ほど、「変数名」を使って「変数に入れる内容」にアクセスできるようになります。

例えば

let A = 1;

let B = A + 2;

という処理があった時、B には何が入っているでしょう？

答えは 3 です。 A + 2 の A
の部分はその前の処理で示した（定義した）Aという変数と解釈され、ここで A
には 1 が入ったので、 1 + 2 と解釈されるわけです。

let
は変数を新たに宣言する時に使うもので、新しい変数を使うよということを示します。すでに宣言された変数への値の保存（代入）の際には
let は記述しません。

例えば

let A = 1;

let B = 2;

A = A + B;

は正しい記述方法で、これを全て処理すると A の値は 3 になっています。

「(」から「)」の部分は引数と呼ばれるものを指定する所になります。引数は別の呼び方でパラメータです。
Audio( 引数 ) では　Audio に対して、引数の部分に記述した内容を渡します。

new Audio() では音楽ファイルを再生する機能をもつ Audio
というモノ（オブジェクト）を作成しています。文法的なもう少し詳しい内容はもう少し後になってからわかればいいです。まずは

let audio = new
Audio(\"http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3\");

の処理によって、[[http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3]{.underline}](http://d1fradabw4irov.cloudfront.net/piano_1do.mp3)
の音を再生することができる変数 audio が作られたと理解してください。

audio.play();

は Audio が持っている play
という処理を呼び出しています。これも文法的な詳しい内容はもう少し後になってわかれば大丈夫です。まずはここではこの処理によって
Audio に引数で渡した
[[http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3]{.underline}](http://d1fradabw4irov.cloudfront.net/piano_1do.mp3)
の音が再生させるということを理解しておけば大丈夫です。

さてここまで { }
の中身をみてきました。このブロックは次のような構造になっています

function playDo() {

}

ここで function playDo() では、playDo
という関数名の関数を記述（定義）しています。関数は一連の処理のかたまりで、関数名
(playDo)を呼び出すことで、先ほどみてきた処理のブロックを実行させることができるのです。

この関数がいつ呼ばれるのか、つまりこれまでみてきた処理がいつ実行されるのかというのは
button タグの中に記述されています。

\<button style=\"width:80px;height:250px;\" onclick=\"playDo()\"\>ド
\</button\>

ここで onclick=\"playDo()\" は、このボタンが押された時に playDo
関数を呼び出せというように記述しているのです。

まとめます。詳しい文法的なルールは後ほど理解しましょう。ここでは次の構造が理解できていれば大丈夫です。

![](media/image13.png){width="6.270833333333333in"
height="2.5694444444444446in"}

**5. ドレミファソラシドが鳴るようにする**

ドレミファソラシドのそれぞれの音を次に用意しておきました、

  音                     URL
  ---------------------- -----------------------------------------------------
  ド                     http://d1fradabw4irov.cloudfront.net/piano\_1do.mp3
  レ                     http://d1fradabw4irov.cloudfront.net/piano\_2re.mp3
  ミ                     http://d1fradabw4irov.cloudfront.net/piano\_3mi.mp3
  ファ                   http://d1fradabw4irov.cloudfront.net/piano\_4fa.mp3
  ソ                     http://d1fradabw4irov.cloudfront.net/piano\_5so.mp3
  ラ                     http://d1fradabw4irov.cloudfront.net/piano\_6ra.mp3
  シ                     http://d1fradabw4irov.cloudfront.net/piano\_7si.mp3
  ド（１オクターブ上）   http://d1fradabw4irov.cloudfront.net/piano\_8do.mp3

5-1.
先ほど作成したボタンはドの音を鳴らしました。同じ要領でレの音を鳴らすボタンを追加してみましょう。まずは
レ の音を鳴らす関数 playRe を定義します。

+-----------------------------------------------------------------------+
| function playRe() {                                                   |
|                                                                       |
| var audio = new                                                       |
| Audio(\"http://d1fradabw4irov.cloudfront.net/piano\_2re.mp3\");       |
|                                                                       |
| audio.play();                                                         |
|                                                                       |
| }                                                                     |
+-----------------------------------------------------------------------+

5-2. 「レ」ラベルのついたボタンを追加し、ボタンが押された時に関数 playRe
を呼び出すようにします。

  ----------------------------------------------------------------------------------
  \<button style=\"width:80px;height:250px;\" onclick=\"playRe()\"\>レ \</button\>
  ----------------------------------------------------------------------------------

5-3. Google Chrome でファイルを開いて確認しましょう。\[ド\]、と \[レ\]
のボタンが現れ、それぞれ押すと音が鳴ると思います。

![](media/image5.png){width="6.270833333333333in"
height="4.180555555555555in"}

5-4.
同じ要領でレ、ミ、ファ、ソ、ラ、シ、ドのボタンも追加して、それぞれの音が鳴るようにしましょう。

最終的な仕上がりは次のような見た目になるはずです

![](media/image1.png){width="6.270833333333333in" height="3.75in"}
