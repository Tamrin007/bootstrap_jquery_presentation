## DHACKS

# フロントエンド勉強会

### Presented by Tamrin



## 自己紹介

- @Tamrin007
- 情シス 4回
- 趣味はテニス
- 応用メディア情報（大久保）研究室
- 研究では Microsoft Kinect v2 を使ってセンシング



## あじぇんだ

1. フロントエンドとは？
1. 今日学ぶもの
1. Bootstrap
1. jQuery
1. フロントエンド開発環境



## フロントエンドって？


めちゃくちゃざっくり言うと、

- HTML
- CSS
- JavaScript

を使って開発する部分のこと


逆にバックエンドとは、

- サーバサイドプログラミング
- サービスのロジック部分
- Java, Perl, PHP, Python, Ruby, 等々


ここでのフロントエンドやバックエンドというくくりはウェブプログラミングに限った話であることに注意。



## 今回紹介するもの


フロントエンド開発を楽にするためのツール

- Bootstrap
- jQuery


### 用意するもの
- ブラウザ（IEは非推奨）
- テキストエディタ



## Bootstrap


Bootstrap とは

- CSSフレームワーク
- 米 Twitter 社が開発 / 提供
- オープンソース（Apache License 2.0）
- 複数ブラウザ対応
- レスポンシブデザイン（グリッドシステム）


### ダウンロード

http://getbootstrap.com/getting-started/#download

今回は ZIP 版をダウンロードします


### 準備

1. 解凍したフォルダの直下に index.html を作成
1. ダウンロードページの "Basic template" を貼り付け
1. lang=en の部分を lang=ja に変更


### グリッドシステム

Bootstrap では横幅を12個に分割したグリッドシステムが採用されています


以下のコードを body 内に貼り付け

```html
<div class="container">

  <div class="page-header">
    <h1>Bootstrap グリッドシステム</h1>
    <p class="lead">グリッドシステムの練習</p>
  </div>

</div>
```

以降はこの .container 内に例を書いていきます


#### 例1. 3つの等しいボックス

```html
<h3>3つの同じ幅のボックス</h3>
<p>同じ width を持つボックスが3つできます。
  <strong>表示領域の幅が広い（992px 以上）場合は3つ並んで表示されます。</strong> スマホやタブレット等の狭い画面（992px 未満）は縦に積まれて表示されます。</p>
<div class="row">
  <div class="col-md-4" style="background: #e74c3c;">.col-md-4</div>
  <div class="col-md-4" style="background: #32ce74;">.col-md-4</div>
  <div class="col-md-4" style="background: #3498db;">.col-md-4</div>
</div>
```


#### 例2. 1:2:1 のボックス

```html
<h3>1:2:1 の幅のボックス</h3>
<p>1:2:1 の比率の width を持つボックスができます。 先ほどと同じように
  <strong>表示領域の幅が広い（992px 以上）場合は3つ並んで表示されます。</strong> スマホやタブレット等の狭い画面（992px 未満）では縦に積まれて表示されます。</p>
<div class="row">
  <div class="col-md-3" style="background: #e74c3c;">.col-md-3</div>
  <div class="col-md-6" style="background: #32ce74;">.col-md-6</div>
  <div class="col-md-3" style="background: #3498db;">.col-md-3</div>
</div>
```


#### 例3. デスクトップとモバイルでの切り替え

```html
<h3>デスクトップとモバイルでの切り替え</h3>
<p>Bootstrap では xs (phones), sm (tablets), md (desktops), lg (larger desktops) の 4 つのサイズが設定されています。 これらを組み合わせることで、異なる画面解像度でのレイアウトを一つのHTMLコードで切り替えることが可能となります。</p>
<p>例えばクラスに col-xs-12 と col-md-8 を設定しておけば、”表示領域が md（992px） 以上の場合は 8 の幅、それ以下の場合は col-xs-6 が選択されて 6 の幅”となります。</p>
<h4>md 以上で 8:4, md 未満で 12 と 6</h4>
<div class="row">
  <div class="col-xs-12 col-md-8" style="background: #f1c40f;">.col-xs-12 .col-md-8</div>
  <div class="col-xs-6 col-md-4" style="background: #e67e22;">.col-xs-6 .col-md-4</div>
</div>
<h4>md 以上で 3等分, md 未満で 6:6 と 6</h4>
<div class="row">
  <div class="col-xs-6 col-md-4" style="background: #95a5a6;">.col-xs-6 .col-md-4</div>
  <div class="col-xs-6 col-md-4" style="background: #7f8c8d;">.col-xs-6 .col-md-4</div>
  <div class="col-xs-6 col-md-4" style="background: #bdc3c7;">.col-xs-6 .col-md-4</div>
</div>
<h4>ずっと 6:6</h4>
<div class="row">
  <div class="col-xs-6" style="background: #16a085;">.col-xs-6</div>
  <div class="col-xs-6" style="background: #d35400;">.col-xs-6</div>
</div>
```


### 各種コンポーネント

Bootstrap では便利なコンポーネントがいくつも用意されています


以下のコードを body 内に貼り付け

```html
<div class="container">

  <div class="page-header">
    <h1>Bootstrap 各種コンポーネント</h1>
    <p class="lead">各種コンポーネントの練習</p>
  </div>

</div>
```

以降はこの .container 内に例を書いていきます


#### グラフィックアイコン & アラート

```html
<h3>Glyphicons & Alerts</h3>
<div class="alert alert-danger" role="alert">
  <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
  <span class="sr-only">エラー:</span>
  不正なメールアドレスです。
</div>
```


#### パネル

```html
<h3>Panel</h3>
<div class="panel panel-default">
  <div class="panel-heading">
    <h3 class="panel-title">Panel title</h3>
  </div>
  <div class="panel-body">
    Panel content
  </div>
</div>
```


#### ナビゲーション

```html
<h3>Navs</h3>
<ul class="nav nav-tabs">
  <li role="presentation" class="active"><a href="#">Home</a></li>
  <li role="presentation"><a href="#">Profile</a></li>
  <li role="presentation"><a href="#">Messages</a></li>
</ul>
```


#### ページネーション

```html
<h3>Pagenation</h3>
<nav>
  <ul class="pagination">
    <li class="disabled">
      <a href="#" aria-label="Previous">
        <span aria-hidden="true">&laquo;</span>
      </a>
    </li>
    <li class="active"><a href="#">1 <span class="sr-only">(current)</span></a></li>
    <li><a href="#">2</a></li>
    <li><a href="#">...</a></li>
    <li><a href="#">4</a></li>
    <li><a href="#">5</a></li>
    <li>
      <a href="#" aria-label="Next">
        <span aria-hidden="true">&raquo;</span>
      </a>
    </li>
  </ul>
</nav>
```


### 公式リファレンス

ここではとてもすべての機能を紹介しきれないので、以下をご覧下さい

http://getbootstrap.com/css/
http://getbootstrap.com/components/



## jQuery


jQuery とは

- JavaScript を簡潔に書くためのライブラリ
- John Resig 氏が2006年にリリース
- オープンソース（MIT, GPL License）
- "write less, do more."
- 複数のブラウザに対応


#### write less, do more.

例えば red クラスの要素の色を一括で赤にしたいとき

```js
// JavaScript の場合
var redElements = document.getElementsByClassName("red");
for (var i = 0; i < redElements.length; i++) {
  redElements[i].style.color = "red";
}

// jQuery の場合
$(".red").css("color", "red");
```


#### 複数のブラウザに対応

例えば要素の透明度を設定する場合

```js
// JavaScript の場合 IE 用の記述が必要
document.getElementById('translucent').style.opacity = 0.5;
document.getElementById('translucent').filter = "alpha(opacity = 50)";

// jQuery の場合
$("#translucent").fadeTo(0, 0.5);
```


### 準備

1. どこにでもいいので index.html, script.js を作成
1. http://learn.jquery.com/about-jquery/how-jquery-works/ にアクセス
1. jQuery: The Basics を貼り付け
1. jQuery のソースを Google CDN から読み込み
 - https://developers.google.com/speed/libraries/#jquery
1. body 終了直前に script.js を読み込み


### 書き方その1. 操作対象を指定する

jQuery(セレクタ)

jQuery は $ と書くことも出来る

$(セレクタ)

```js
$(".red")

$("#translucent")
```


セレクタとは

**「CSS でスタイルを適用する対象を指定する仕組み」**

具体的にはタグ名や ID 名、クラス名など

```js
$("tag")      // タグ
$("#id")      // ID
$(".class")   //クラス
$("a img")    // 子要素
```


### 書き方その2. オブジェクトを操作する

$(セレクタ).メソッド(引数)

```js
$(".red").css("color", "red");

$("#translucent").fadeTo(0, 0.5);
```


メソッド以外にプロパティというものも少数ながらある

$(セレクタ).プロパティ

```js
// div 要素の個数を取得して変数 num に格納する処理
var num = $("div").length;
```


### イベント

- インタラクティブなコンテンツ作りに必要な仕組み
- ユーザの操作や状態の変化など


#### 構文

```js
$(セレクタ).イベント(function (){
  // 処理
});
```


### ready イベント

HTML をロードする前に JavaScript が実行されると

**もちろん JavaScript は正しく動作しません**


そこで、 ready イベントを用いて HTML が読み込まれるのを待ちます

ready イベントの中には必ず関数を記述します

```js
jQuery(document).ready(function hoge() {
  // html 読み込み後にこの部分が実行されます
});

// 省略記法
$(function hoge() {
  // html 読み込み後にこの部分が実行されます
});
```


いちいち関数名を付けるのは面倒な上に管理も大変なので、無名関数を用います

```js
$(function() {
  // html 読み込み後にこの部分が実行されます
});
```


主なイベントは以下のようなものがあります

- .ready()
- .click()
- .hover()
- .keydown()
- .select()
- .scroll()


### 例. クリックイベント

```js
var clicked_props = {
  "color" : "#fff",
  "background" : "#D2527F"
};

$(function() {
  $("button").click(function() {
    $("div").css(clicked_props);
    $("div").text("buttonがクリックされました");
  });
});
```


### メソッドチェイン

- jQuery オブジェクトの生成には負荷がかかる
- 1回の生成で複数の処理ができるようにする

$("セレクタ").メソッド().メソッド().メソッド()...

```js
$(function() {
  $("button").click(function() {
    $("div").css(clicked_props).text("buttonがクリックされました");
  });
});
```



## フロントエンド開発環境


### （流行りの）ツール

- Emmet
- Haml, Slim
- Sass, LESS
- Gulp, Grunt


#### Emmet

- HTMLを書くのが面倒臭い人に
- 使いこなせば爆速マークアップが可能に


#### ERB, Haml, Slim

- HTML

```html
<h1 id='title'>H1 タイトル</h1>
<br>
<ul>
  <li>0: リスト</li>
  <li>1: リスト</li>
  <li>2: リスト</li>
</ul>
<a href='#'>リンク</a>
```

- Slim

```slim
h1#title H1 タイトル
br
ul
  - 3.times do |i|
    li #{i}: リスト

a(href="#") リンク
```


#### Sass, LESS

- CSS でプログラミングの様に入れ子構造が書けたり、変数が使えたり
- Bootstrap はLESSで書かれていた（4 からはSass）


- CSS

```css
h1{
    font-size:24px;
    color:#000099;
}
h2{
    font-size:17px;
    color:#ff0099;
    background-image:url("http://sample.com/img/background.png");
}
```


- LESS

```less
@blue: #000099;
@red: #FF0000;
@h1: 24px;
@h2: (@h1 / 2) + 5;
@url: "http://sample.com";

h1 {
    font-size: @h1;
    color: @blue;
}

h2{
    font-size: @h2;
    color: @blue + @red;
    background-image: url("@{url}/img/background.png");
}
```


#### Gulp, Grunt

- タスクランナー
- Sass のコンパイル、ローカルサーバの立ち上げ、リロードなどのタスクを自動化



# 以上、ありがとうございました
