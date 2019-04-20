
# オブジェクト指向って何！？ 

## ～Javaで学ぶオブジェクト指向プログラミング～ 【基礎編】


<img src="img/a0001_017879.jpg"/>


### オブジェクト指向は難しい？

#####「オブジェクト指向」≠「難しい」

#####「オブジェクト指向」＝「シンプルに単純に...」


### オブジェクト指向が苦手になりやすい理由


1. 専門用語が多すぎる！！

(クラス、インスタンス、コンストラクタ、継承、ポリモーフィズム、抽象クラス、インターフェース....)

1. 一般的なカリキュラム上、Javaの基礎を学んだ後に学ぶので、そもそも考え方や頭の使い方が一気に変わるから...。

1. そもそも研修レベルの規模ではありがたみを感じにくい...。

1. 書き方は教えるけど、なぜそう書くかまでは教えてもらえない。

## オブジェクト指向ってなに？
そもそもプログラムを作るときの大きな考え方が３つあるのは、ご存知ですか？

**手続き型プログラミング**

上から順番に文章のようにプログラムを書く考え方

**関数型プログラミング**

関数（InputとOutputをもつ処理のかたまり）をつなげて組み立てるプログラミングの考え方

**オブジェクト指向プログラミング**

下記のWikipediaを見てもらえれば、すべてがわかります..。

<a href="javascript:alert('冗談です。');">https:\//ja.wikipedia.org/wiki/オブジェクト指向プログラミング</a>


## そもそもオブジェクトってなに？

**「オブジェクト」＝「モノ」**


(例)

<img id="pictures_1" src="img/pictures/01.JPG" style="display:block;" onclick="picturesClickEvent(1)" />
<img id="pictures_2" src="img/pictures/02.JPG" style="display:none;" onclick="picturesClickEvent(2)" />
<img id="pictures_3" src="img/pictures/03.JPG" style="display:none;" onclick="picturesClickEvent(3)" />
<img id="pictures_4" src="img/pictures/04.JPG" style="display:none;" onclick="picturesClickEvent(4)" />
<img id="pictures_5" src="img/pictures/05.JPG" style="display:none;" onclick="picturesClickEvent(5)" />
<img id="pictures_6" src="img/pictures/06.JPG" style="display:none;" onclick="picturesClickEvent(6)" />
<img id="pictures_7" src="img/pictures/07.JPG" style="display:none;" onclick="picturesClickEvent(7)" />
<img id="pictures_8" src="img/pictures/08.JPG" style="display:none;" onclick="picturesClickEvent(8)" />


　　
コップ、ペットボトル、私、クツ、ペン、パソコン、スマホ...全てオブジェクトである。


つまり、オブジェクト指向とは、**「モノ」をプログラムで表現して扱いましょう!**というものである。（ざっくり言えば...）



## オブジェクト指向を体験してみよう！

オブジェクトのスタートラインは"**モノ**"を概念的に捉える頭の使い方をする。
 
 
### ワーク1 : モノを概念としてとらえる練習
■ コップについて考えよう。
<img src="img/cup.jpg">

Q1. コップの自己紹介を作ってみよう。

- **重さ**は〇〇です。
- **素材**は〇〇です。
- **色**は〇〇です。
- **水の入る量**は〇〇です。
- **今水が入ってる量**は〇〇です。

Q2. コップを使ってできることは？
- **水を入れる**
- **水を捨てる**

　
■ それでは、自分の携帯電話についてそれぞれの考えてみよう。
<img src="img/smapho.png">

Q1. 携帯電話に自己紹介をさせてみよう！

<textarea rows="8" cols="50" ></textarea>

Q2. 携帯電話を使ってできることは？

<textarea rows="8" cols="50" ></textarea>



<input id="btn_1" type="button" onclick="getCorrect(1)" value="正解を表示" />


<div id="span_1" style="padding:5px;display:none;">

Q1. 携帯電話に自己紹介をさせてみよう！<br/>
（例）<br/>
機種、メーカー、OS、電話番号、データ容量、契約している通信会社、メールアドレス、アプリ、電池の残量....<br/>
<br/>
Q2. 携帯電話を使ってできることは？<br/>
（例）<br/>
電話をする、電話を受け取る、メールを送る、メールを受信する、アドレス帳を開く、アドレス帳に登録する、アプリを開く....

<pre style="background-color: #364549;color:#ffffff;">
public class Main {

    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character("ヒーロー");

        //キャラクターの設定
        hero.hp_max = 100;
        hero.hp = 100;
        hero.attack_point = 10;

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.run_away(); //逃げる。
       hero.call_name();//名前を名乗る
    }  
}

</pre>
</div>



## フィールドとメソッドとは？

自己紹介の項目で挙げた名詞が**フィールド**

できることを挙げた動詞が**メソッド**

` 
つまり、

**フィールド**は、**モノのステータスや状態を表す**もの。

**メソッド**は、そのモノが行う**機能**のこと。

　
プログラムで表すと....

```java
public class Cup{

    /*フィールド*/
    int height; //コップの高さ
    String madeBy; //コップの素材
    String color; //コップの色
    int max_capacity ; //水の入る量
    int now_waterState; //今の水の量
    
    /*メソッド*/
    //水を入れる
    void input(){
        System.out.println("水を入れました");       
    }
    //水を捨てる
    void output(){
       System.out.println("水を捨てました");    
    }
}
```



### ワーク2：ゲームの主人公を作ろう！

ゲームの主人公の考えられるフィールドとメソッド....

〇フィールド  
- 名前
- HP
- MP
- レベル
- 攻撃力
- 守備力
- 職業
- 装備（剣）
- 装備（盾）
- 装備（鎧）
- 持ってる道具

〇メソッド
- 話す
- 攻撃する
- 逃げる
- 道具を使う
- 移動する
- ツボを投げる


　
実際にプログラムにしてみよう。（クラスのみ）

全部書くと大変なので、今回は、以下の設定に絞って作りましょう。


＜クラス＞

|項目  |  入力値  |
| :--- | :--- |
|  名前（クラス名）  |  Character |

　
＜フィールド＞

| 型 | フィールド名 | フィールドの説明 |
| :---: | :---: | :-- |
| String | name | キャラクターの名前 |
| int | hp | 現在のHPの状態 |
| int | attackPoint | 攻撃力 |

　
＜メソッド＞

| 戻り値の型 | 引数 | メソッド名 | メソッドの処理 |
| :---: | :---: | :---: |:-- |
| なし(void) | なし | attack | "攻撃する"とコンソールに表示する。 |
|  なし(void)  | なし | runAway | "逃げる"とコンソールに表示する。 |

　


<input id="btn_2" type="button" onclick="getCorrect(2)" value="正解を表示" />


<div id="span_2" style="padding:5px;display:none;">

正解<br/>

<pre style="background-color: #364549;color:#ffffff;">
public class Character {

    /*フィールド*/
    String name; //キャラクターの名前
    int hp; //現在のHPの状態
    int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void runAway(){
        System.out.println("逃げる");
    }  
}

</pre>
</div>

　
ちなみに...
メンバとフィールドがごちゃごちゃになっているあなたへ

　
<input id="btn_y1" type="button" onclick="readDigression('y1')" value="余談" />


<div id="span_y1" style="padding:5px;display:none;">
<br/>
「フィールド」は、上記のようなクラスに定義されている変数や定数を指します。<br/>
「メンバ」は、クラスを構成する内部要素(「メソッド」や「フィールド」などを含めた)の総称です。<br/>
<br/>
ちなみに、メンバ変数と呼ばれたらフィールドのことを指します。<br/>
<br/>
他の参考書等で悩まれたら、思い出してみてください。
</div>



## クラスとインスタンス
これで、ゲームのキャラクターの必要最低限の型が出来上がりました。
この型のことを**クラス**といいます。

でも、これでは、まだキャラクターの設定をしただけで、実際にキャラクターを作っていません。

キャラクターを実際に作る作業を**インスタンス化**と呼びます。

キャラクターを実際に作る作業は以下のようにやります。

```java
Character hero = new Character();
```

これで、heroというキャラクターが出来上がりました。
このheroのことを**インスタンス**と呼びます。


実際にプログラムで書いて動かしてみましょう。
このキャラクターを作るために実行するメインクラスを用意します。

＜クラス＞

|項目  |  入力値  |
| :--- | :---: |
|  名前（クラス名）  |  Main|
|public static void main(String[] args)(V)| ☑ |


```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character();
    
    }  
}
```

これで、heroを作りました。
しかし、今の状態では、何も設定のないキャラクターになっています。

〇キャラクターに設定を加える

キャラクターに名前とhpと攻撃力を設定しましょう。
以下のプログラムを加えることで、設定することができます。(※)

```java
hero.name = "ヒーロー";
hero.hp = 100;
hero.attackPoint = 10;
```

フィールドは、以下のように呼び出すことができます。

```java
インスタンス.フィールド
```

〇キャラクターを動かす

また、メソッドを呼び出すときは、以下のようにやります。

```java
hero.attack(); //攻撃する。
hero.runAway(); //逃げる。
```

メソッドは、以下のように呼びだすことができます。

```java
インスタンス.メソッド();
```

### ワーク3：ヒーローを作って実行しよう！

それでは、これらをプログラムにしてみましょう。


```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character();

        //キャラクターの設定
        hero.name = "ヒーロー";
        hero.hp = 100;
        hero.attackPoint = 100;

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
    }  
}
```

このプログラムを実行してみましょう！

### お時間ある人用ワーク

<input id="btn_t1" type="button" onclick="moreQuestion('t1')" value="挑戦!" />
<div id="span_t1" style="padding:5px;display:none;">
<br/>
出来た人は、ヒーローだけでなく、他のキャラクターも作ってみよう。<br/>
<br/>
Q1. 以下の設定のキャラクターを作ってみよう。<br/>
<br/>
名前：ヒロイン<br/>
現在のHP：70<br/>
攻撃力：10<br/>
<br/>
Q2. 好きなキャラクターを作ってみよう！<br/>
<br/>
名前：???<br/>
現在のHP：??<br/>
攻撃力：??<br/>
<br/>
</div>

正解は...

<input id="btn_ta1" type="button" onclick="getCorrect('ta1')" value="正解を表示" />


<div id="span_ta1" style="padding:5px;display:none;">
正解<br/>
★が追加されたコードです。
同じ要領で、好きなキャラクターを作れます。
<pre style="background-color: #364549;color:#ffffff;">
public class Main {

    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character();
        Character heroine = new Character();//★

        //キャラクターの設定
        hero.name = "ヒーロー";
        hero.hp = 100;
        hero.attackPoint = 100;

        //キャラクターの設定
        heroine.name = "ヒロイン";//★
        heroine.hp = 70;//★
        heroine.attackPoint = 10;//★

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
       heroine.attack(); //攻撃する。//★
       heroine.runAway(); //逃げる。//★

    }  
}
</pre>
</div>

このように、Characterクラスから、設定を変えるだけで、たくさんのキャラクターを作ることができます。

このように、クラスを定義して、わざわざインスタンスを作成するメリットは、キャラクターをたくさん増やすことができる便利さがあります！

クラスはあくまで、**モノの概念を定義する**
インスタンス化は、クラスから**実体を作る**
インスタンスは、作られた**実体そのもの**

ちなみに、heroのように作られたインスタンスは、変数のように扱えることから、**インスタンス変数**とも呼ばれます。

## コンストラクタ

先ほどのプログラムに、主人公が自分の名前を名乗れるように、Characterクラスに下記のcallNameメソッドを追加します。

```java
void callName(){
    System.out.println("私の名前は、"+this.name+"だ！");
}  
```

実際にプログラムに追加してみましょう。

＜Characterクラス＞

```java
public class Character {

    /*フィールド*/
    String name; //キャラクターの名前
    int hp; //現在のHPの状態
    int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void runAway(){
        System.out.println("逃げる");
    }  
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }  
}
```

このように、メソッド内で、自身のクラスのフィールドを扱いたいときは、

```java
this.フィールド
```

と表現します。

thisは、自分のクラスを指しています。


それでは、名前を名乗るメソッドをMainクラスに追加します。
下のプログラムをコピーして、実行をしてみてください。

```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character();

        //キャラクターの設定
        hero.hp = 100;
        hero.attackPoint = 10;

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
       hero.callName();//名前を名乗る
    }  
}
```

実は、上のプログラムでは、以下のコードが抜けていて、名前を設定し忘れていたので、名前を名乗ることができなかったので、エラーになっていしまいます。

```java
hero.name = "ヒーロー";
```

このようなことが起こらないように、絶対に**初期設定**を忘れないようにするために、するのが**コンストラクタ**です。

**コンストラクタ**は、**インスタンスが生成されたとき**に、呼び出される特殊なメソッドです。
インスタンスが生成されたタイミングで、値を入れることができるので、上記のようなことが起こらないように防ぐことができます。。


名前を初期設定するコンストラクタは、以下のコードをCharacterクラスに書くことで作ることができます。

```java
Character(String xxx){
    this.name = xxx;
}
```

コンストラクタの引数xxxを自身のフィールドnameに値を入れていることがわかります。


<input id="btn_y2" type="button" onclick="readDigression('y2')" value="余談" />
<div id="span_y2" style="padding:5px;display:none;">

上記のプログラムでは、引数をxxxとしていますが、一般的なテキストでは、引数をnameにしています。<br/>

<pre style="background-color: #364549;color:#ffffff;">

Character(String name){
    this.name = name;
}
</pre>


これは、「変数名は、わかりやすいものにする」をいう規則から、なるもので、実際はどんな名前でもよいです。<br/>
プログラマーの初心者で、「this.name=name」をみて「なんでnameにnameを入れているのか？」と一見思わせてしまうため、xxxで表現しています。<br/>
実際に、業務などで扱うときは、引数をnameにすることが望ましいです。<br/>
</div>

実際にプログラムを変えてみましょう。


＜Characterクラス＞

```java
public class Character {

    /*コンストラクタ*/
    Character(String xxx){
        this.name = xxx;
    }
    /*フィールド*/
    String name; //キャラクターの名前
    int hp; //現在のHPの状態
    int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }    
}
```

すると...Mainクラスにエラーが出てきます。
これは、インスタンスを作る(heroを作る)時に、「名前が設定されていないじゃん」と怒られているからです。

これは、コンストラクタを定義したおかげで、インスタンスを生成したタイミングで、値を入れる制約を設けたゆえに、エラーが検出されています。

それでは、実際に名前を設定しましょう。
Mainクラスを以下のように変えてます。

＜Mainクラス＞

```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character("ヒーロー");

        //キャラクターの設定
        hero.hp = 100;
        hero.attackPoint = 10;

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
       hero.callName();//名前を名乗る
    }  
}
```

このプログラムを実際に動かしてみましょう。
これで、名前を名乗ることができたかと思います。


### ワーク4 :他の値も初期設定できるようにしましょう。
他のhpとattackPointもコンストラクタで定義をするようにしましょう。

<input id="btn_4" type="button" onclick="getCorrect(4)" value="正解を表示" />

<div id="span_4" style=";padding:5px;display:none;">
正解＜Characterクラス＞
<pre style="background-color: #364549;color:#ffffff;">
public class Character {

    /*コンストラクタ*/
    Character(String xxx, int hp, int ap){
        this.name = xxx;
        this.hp = hp;
        this.attackPoint = ap;
    }
    /*フィールド*/
    String name; //キャラクターの名前
    int hp; //現在のHPの状態
    int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }    
}
</pre>

正解＜Mainクラス＞
<pre style="background-color: #364549;color:#ffffff;">


```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character("ヒーロー", 100,  10);

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
       hero.callName();//名前を名乗る
    }  
}
```
</pre>
</div>

プログラムが少しコンパクトになりました。
このように、コンストラクタを定義することで、インスタンスの生成時に値を入れることを義務付けることができます。

コンストラクタについての余談

<input id="btn_y3" type="button" onclick="readDigression('y3')" value="余談" />
<div id="span_y3" style="padding:5px;display:none;">

コンストラクタが何者かというと、実はメソッドの仲間です。

コンストラクタが定義されていない場合でも、デフォルトで、下記のコンストラクタが実装されています。
<pre style="background-color: #364549;color:#ffffff;">

Character(){
}
</pre>
また、コンストラクタもメソッドと同様に、引数の型や個数を変えることで、オーバーライドの効果を持たせることができます。
<pre style="background-color: #364549;color:#ffffff;">

Character(String xxx){
    /*処理*/
}
Character(int hp){
    /*処理*/
}
Character(String xxx,int hp){
    /*処理*/
}
Character(String xxx,int hp,int ap){
    /*処理*/
}
</pre>

このように、コンストラクタを定義すれば、さまざまなパタンの初期値を呼び出すことができます。

また、あまりケースとして多くはないですが、クラスのメソッド内で、コンストラクタを呼ぶときは、以下のように呼び出します。

<pre style="background-color: #364549;color:#ffffff;">
this();//引数ナシ
this(name,hp);//引数アリ
</pre>

</div>
## カプセル化
コンストラクタがちゃんと定義されているので、初期設定もちゃんと行えるようにできたので、安心...

と言いたいところですが、実は、今の状態のままでは、まだまだ危険な状態です。
それは、Mainプログラムから勝手に、せっかく初期設定をしたのに値を変えることができてしまうからです。

　
試しに、いたずらで、「ヒーロー」の名前を「スライム」に変えてしまいましょう。

以下のプログラムをコピーして実行してみましょう。


＜Mainクラス＞

```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character("ヒーロー", 100,  10);

        //いたずら
        hero.name = "スライム";

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
       hero.callName();//名前を名乗る
    }  
}
```


これを実行すると、「私の名前は、スライムだ！」となってしまいました。

このように、せっかく初期設定をしたものを変えられるのはすごく嫌ですよね。
今状態では、HPの値も敵に見られてしまいます。

そのようなことを防ぐために、フィールドの値を見れないようにする方法があります。
それが、**カプセル化**です。

カプセル化は、Characterクラスに、**private**と**public**を追加するだで、守ることができます。
**private**は、プライベートなので外から値を見られないようにします。
**public**は、公なので、どこからでも見ることができます。

今回は、フィールドをprivateにして、メソッドをpublicに設定します。

Characterクラスを変えてみましょう。


＜Characterクラス＞

```java
public class Character {

    /*コンストラクタ*/
    public Character(String xxx){
        this.name = xxx;
    }
    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }    
}
```

このように設定すると、Mainクラスのいたずらを記載したところがエラーになります。
これは、privateな値を外から(他のクラスから)触ることができないですよと怒られるからです。


### ワーク5 : 考えてみよう！

プログラムを間違えて、Characterクラスを下記のように設定してしまいました。
すると、Mainクラスの方でエラーが起きてしまいます...。なぜでしょう？
プログラムを修正してみましょう。

＜Characterクラス＞

```java
public class Character {

    /*コンストラクタ*/
    private Character(String xxx){
        this.name = xxx;
    }
    /*メソッド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }    
}
```

理由：
<textarea rows="4" cols="50" ></textarea>

<input id="btn_5" type="button" onclick="getCorrect(5)" value="正解を表示" />

<div id="span_5" style=";padding:5px;display:none;">
コンストラクタは、インスタンスが生成されるときに呼び出されるメソッドなので、それがprivateになってしまうと、インスタンスが生成できなくなってしまうため...<br/>

※java.util.Calendarのように、わざとインスタンスを外から作らせないようにする手法もあります。（具体的な活用法は、応用編にて。）<br/>
</div>

#### アクセス修飾子

ちなみに...このprivateやpublicのようなものを**アクセス修飾子**と呼びます。
アクセス修飾子は、以下の4つに設定できます。

| アクセス修飾子 | アクセスを許可する範囲 |
| :---: | :-- |
| private | 自分自身のクラスのみ |
| 記載なし | 自身の属するパッケージ内のクラス |
| protected | 自身の属数パッケージ内のクラス もしくは 自身を継承したクラス |
| public | すべてのクラス |


## GetterとSetter
カプセル化がいたずらされないように、守ることであることはわかりました。
しかし、今のままでは、Mainクラスからヒーローのフィールドの値にアクセスすることができません...。

例えば、ナレーションで「ヒーローは、レベルアップしました。」と表示したいときに、
下記のようなプログラムを記載すると、もちろんエラーになってしまいます。

＜Mainクラス＞

```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character("ヒーロー", 100, 10);

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.runAway(); //逃げる。
       hero.callName();//名前を名乗る

        //ナレーション
        System.out.println(hero.name+"は、レベルアップしました。");        
    }  
}
```

そこで、登場するのが、**Getter**と**Setter**です。
**Getter**は、privateで守られているフィールドの値を**取得**します。
**Setter**は、privateで守られているフィールドの値を**設定**します。

例えば、キャラクターの名前を取得するときのGetterは以下のように書きます。

```java
public String getName(){
    return this.name;
}
```

基本的には、「getフィールド名」で書くことが多いので、Getterと呼びます。

例えば、キャラクターの名前を取得するときのSetterは以下のように書きます。コンストラクタで初期値を設定したときと似ています。

```java
public void setName(String xxxx){
    this.name = xxxx;
}
```

実際に、Characterクラスに記載すると以下のようになります。

```java
public class Character {

    /*コンストラクタ*/
    private Character(String xxx, int hp, int point){
        this.name = xxx;
        this.hp = hp;
        this.attackPoint = point;
    }
    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }  

    /*GetterとSetter*/
    // nameのGetter
    public String getName(){
        return this.name;
    }

    // nameのSetter
    public void setName(String xxxx){
        this.name = xxxx;
    }
}
```

これで、カプセル化されている値にどうしてもアクセスしたいときは、このようにアクセスすれば大丈夫です。

### GetterとSetterのメリット
例えば、**read only**のように、読み込みのみを許可したい場合は、
Getterのみを定義すればOK！

逆に、**write only**のように、書き込みのみを許可したい場合は、
Setter飲みを定義すればOK!

とても便利です。


また、値を取得・設定する際に、その値を本当に取得・設定してもいいのかをGeeterやSetterのメソッド内に書くことで、
変なデータを作らないようにすることができます。

例えば...下記のプログラムでは、setNameで「スライム」をしようとしたときに、名前を変更されないように防ぐことができます。

```java
// nameのSetter
public void setName(String xxxx){
    if("xxxx".equals("スライム")) {
        return;
    }
    this.name = xxxx;
}
```

### ワーク6: GetterとSetterを作ってみよう。

それでは、hpとattackPointのGetterとSetterを作ってみましょう。


<input id="btn_6" type="button" onclick="getCorrect(6)" value="正解を表示" />

<div id="span_6" style=";padding:5px;display:none;">
正解<br/>
★が追加したコード
<pre style="background-color: #364549;color:#ffffff;">
public class Character {

    /*コンストラクタ*/
    public Character(String xxx, int hp, int point){
        this.name = xxx;
        this.hp = hp;
        this.attackPoint = point;
    }
    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }  

    /*GetterとSetter*/
    // nameのGetter
    public String getName(){
        return this.name;
    }

    // nameのSetter
    public void setName(String xxxx){
        this.name = xxxx;
    }
     
    // hpのGetter
    public int getHp(){
        return this.hp;
    }
    // hpのSetter
    public void setHp(int hp){
        this.hp = hp;
    }

    // attackPointのGetter
    public int getAttackPoint(){
        return this.attackPoint;
    }
    // attackPointのSetter
    public void setAttackPoint(int attackPoint){
        this.attackPoint = attackPoint;
    }
}
</pre>

と書いてもらいましたけど....<br/>
実は、Eclipseには、ショートカットキーがあるの知っていましたか？<br/>
<br/>
Windowsの場合は、「Shift」+「Alt」+「s」<br/>
Macの場合は、「Command」+「Alt」+「s」<br/>
<br/>
これを押して、「getterとsetterの追加」を選択。<br/>
追加したいフィールドに☑すればOK！<br/>

</div>




## 静的メンバ
＜時間に余裕があれば..やります！＞

### メンバとは？
上記でやったように、クラスの中に定義されているものを指します。
つまり、メソッドやフィールドのことを指します。

### 静的とは？
静的の対義語で、動的という言葉がります。

このように、
**静的**とは、動かないもの。変化しないもの。
**動的**とは、動くもの。変化するもの。
というものが一般的イメージです。

Javaの**静的**は、**メモリを固定する**という意味を持ちます。

オブジェクト指向プログラミングの**静的**のイメージは、**共有部分**と**唯一無二の値**という2つの側面を持つイメージを作ることができます。

オブジェクト指向プロラミングの本質は、クラスというモノの概念の型から、インスタンスという実態を作ることでした。
例えば、インスタンスは、クラスからインスタンス化されたときに、メモリ上に作られるので、インスタンスは**動的**なものです。
また、インスタンス内のフィールドやメソッドも当然**動的**なわけです。

しかし、静的なメンバをクラスの中に定義することで、メモリを固定することができるので、どのインスタンスを作っても、メモリが固定されているため、**共有**で扱うことができるメモリを作ることができます。また、どんなにインスタンスを作っても静的なものは、新しく作られることがないので、**唯一無二**であるといえるでしょう。


と言ってもわからないと思うので、実際に実験してみましょう。

前回作ったCharacterクラスに、静的なメンバを追加します。
静的なメンバは、**static**をつければ、OKです！

例えば...

```java
private static String item;
```

みたいな感じです。
これで、String型のitemというメモリは、どのインスタンスでも共有できる値となるわけです。

実際に実験してみましょう。
★が追加したところです。

＜Characterクラス＞

```java
public class Character {

	/*コンストラクタ*/
    public Character(String xxx, int hp, int point){
        this.name = xxx;
        this.hp = hp;
        this.attackPoint = point;
    }
    
    /*静的なメンバ*/
    public static String item;//★

    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }  
    /*GetterとSetter*/
    // nameのGetter
    public String getName(){
        return this.name;
    }

    // nameのSetter
    public void setName(String xxxx){
        this.name = xxxx;
    }
     
    // hpのGetter
    public int getHp(){
        return this.hp;
    }
    // hpのSetter
    public void setHp(int hp){
        this.hp = hp;
    }

    // attackPointのGetter
    public int getAttackPoint(){
        return this.attackPoint;
    }
    // attackPointのSetter
    public void setAttackPoint(int attackPoint){
        this.attackPoint = attackPoint;
    }
}
```

これで、静的なメンバを定義しました。

実際に、この静的なメンバをMainクラスで使ってみましょう。

今回は、わかりやすいように、ヒーローとヒロインを設定します。
ヒーローが「剣」を手に入れて、ヒロインが「魔法の書物」を手に入れた時、
プログラムの動きを見てみましょう。

＜Mainクラス＞

```java
public class Main {

	public static void main(String[] args) {

		//キャラクターを作りました。
        Character hero = new Character("ヒーロー", 100,  10);
        Character heroine = new Character("ヒロイン", 40,  10);

       hero.callName();//名前を名乗る
       heroine.callName();//名前を名乗る
       
       System.out.println("#ヒーローは、剣を手に入れた");
       hero.item = "剣";
       
       System.out.println("ヒーローのアイテム："+hero.item);
       System.out.println("ヒロインのアイテム："+heroine.item);
       
       System.out.println("#ヒロインは、魔法の書物を手に入れた");
       heroine.item = "魔法の書物";
       
       System.out.println("ヒーローのアイテム："+hero.item);
       System.out.println("ヒロインのアイテム："+heroine.item);
       
	}

}
```

プログラムを実行してみましょう。
下のような結果になったかと思います。

```
私の名前は、ヒーローだ！
私の名前は、ヒロインだ！
#ヒーローは、剣を手に入れた
ヒーローのアイテム：剣
ヒロインのアイテム：剣
#ヒロインは、魔法の書物を手に入れた
ヒーローのアイテム：魔法の書物
ヒロインのアイテム：魔法の書物
```

ヒーローが「剣」を手に入れたはずなので、ヒロインも「剣」を持っています。
また、ヒロインが「魔法の書物」を手に入れたはずなのに、ヒーローも「魔法の書物」を持っています。

このように、staticで宣言したメンバは、メモリが共有されており、唯一無二の値になるので、インスタンスAで変更した結果が、
インスタンスBやインスタンスCにも影響します。

例えば、Characterクラスにて、★のように静的なメンバを追加します。
また、コンストラクタが呼び出されるたびに、+1ずつすると、インスタンスがいくつできたかを数えることができます。

```java
public class Character {

	/*コンストラクタ*/
	public Character(String xxx, int hp, int point){
	    this.name = xxx;
	    this.hp = hp;
	    this.attackPoint = point;
	    countCharacter++;//★
	}
	    
	/*静的なメンバ*/
	public static String item;
	public static int countCharacter;//★

	/*フィールド*/
	private String name; //キャラクターの名前
	private int hp; //現在のHPの状態
	private int attackPoint; //攻撃力

    /*********************
          以下省略
    **********************/
}
```

countCharacterの値を先ほどのMainクラスで出力してみましょう。
★が追加したプログラムです。

```java
public class Main {

	public static void main(String[] args) {

		//キャラクターを作りました。
        Character hero = new Character("ヒーロー", 100,  10);
        Character heroine = new Character("ヒロイン", 40,  10);

       hero.callName();//名前を名乗る
       heroine.callName();//名前を名乗る
       
       System.out.println("#ヒーローは、剣を手に入れた");
       hero.item = "剣";
       
       System.out.println("ヒーローのアイテム："+hero.item);
       System.out.println("ヒロインのアイテム："+heroine.item);
       
       System.out.println("#ヒロインは、魔法の書物を手に入れた");
       heroine.item = "魔法の書物";
       
       System.out.println("ヒーローのアイテム："+hero.item);
       System.out.println("ヒロインのアイテム："+heroine.item);
       System.out.println("キャラクター数："+Character.countCharacter);//★
       
	}

}
```

プログラムの実行結果を見ると、キャラクター数が2と表示されています。
このように、共有メモリがあることで、とても便利に扱うことができます。

また、静的なメンバに限り、というように呼び出すことができます。

```java
クラス名.静的なメンバ
```

上のプログラムでも下のように呼び出されています。

```java
Character.countCharacter
```

これは、「hero.item」と「heroine.item」が同じものさしているので、
静的メンバのみこのような表記で書くことが許されています。

しかし、動的なメンバは、同じことはできません。

```java
Character.getName();//エラーになる。
```

なぜなら、どのインスタンスのnameを取得していいかわからないですからね。


静的メンバの余談

<input id="btn_y5" type="button" onclick="getCorrect('y5')" value="余談" />
<div id="span_y5" style=";padding:5px;display:none;">
基本的な使われ方をするのは、クラス内に定数を定義するときは、staticをつけて静的にすることが多いです。<br/>

<pre style="background-color: #364549;color:#ffffff;">
public static int XXXXX = 1000;
</pre>

理由は、インスタンスの数だけメモリを消費しないようにするためです。<br/>
</div>


staticの余談

<input id="btn_y6" type="button" onclick="getCorrect('y6')" value="余談" />
<div id="span_y6" style=";padding:5px;display:none;">
staticといえば、

<pre style="background-color: #364549;color:#ffffff;">
public static void main(String[] args){

}
</pre>

でおなじみのmain関数です。
これも静的な関数なわけです。
なぜなら、main関数がいくつも存在しては、実行するときどれを実行していいかわからないですよね？
つまり、main関数は、staticである必要があります。
このように、他に存在させたくないという時に、staticは有効なので、活用してみましょう。
具体的な活用のやり方は、応用編にて。
</div>


## 継承
前章では、Characterクラスを作りましたが、ほとんど同じ設定内容だけど、一部だけ特徴的を持たせたキャラクターを作りたい！というときに、継承はとても便利です。

今回は、魔法を使えるキャラクター魔法使いを作ってみましょう。
魔法使いには、以下のフィールドとメソッドがあります。

〇フィールド
名前
HPの最大値
現在のHP
MPの最大値★
現在のMP★
攻撃力


〇メソッド
攻撃する
魔法を使う★
逃げる
名前を名乗る


このクラスをまともに作るとしたら、以下のようにプログラムを作ります。

＜MagicCharacterクラス＞

```java
public class MagicCharacter {

    /*コンストラクタ*/
    private MagicCharacter(String xxx,  int hp,  int mp, int point){
        this.name = xxx;
        this.hp = hp;
        this.hp = mp;//★
        this.attackPoint = point;
    }
    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int mp; //現在のMPの状態★
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }
    //自分の名前を名乗る
    void callName(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }  

    /*GetterとSetter*/
    // nameのGetter
    public String getName(){
        return this.name;
    }
    // nameのSetter
    public void setName(String xxxx){
        this.name = xxxx;
    }
    ・
    ・
    ・


    // mpのGetter★
    public int getMp(){
        return this.mp;
    }
    // mpのSetter★
    public void setMp(int xxxx){
        this.mp = xxxx;
    }

}
```


しかし、★を付けたところ以外は、Characterクラスと全部同じです。
例えば、setName()を新しく変えたいとしたときに、CharacterクラスとMagicCharacterクラスの両方を変えるのは、面倒くさいですよね？
また、他にもXXXCharacter, YYYCharacter, ZZZCharacterがあると、たまりません....。

このようなことが起こらないように、Javaには、**継承**という考え方があります。

この継承の考え方はとても便利で、例えば、どのキャラクターにも必要な設定をBasicキャラクタークラスを作ってまとめておき、そのクラスを継承して、勇者クラス、魔法使いクラス、盗賊クラス、格闘家クラス....などを作っていけばよいのです。

試しに、BasicCharacterクラスを作成し、それを継承する勇者キャラクタークラス(HeroCharacter)と魔法使いキャラクタークラス(MagicianCharacter)を作成します。

以前、作成したCharacterクラスを少し機能を削って作ります。

＜BasicCharacter＞

```java
public class BasicCharacter {

	/*コンストラクタ*/
    public Character(String xxx, int hp, int point){
        this.name = xxx;
        this.hp = hp;
        this.attackPoint = point;
    }
    
 
    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    /*メソッド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }

    /*GetterとSetter*/
    // nameのGetter
    public String getName(){
        return this.name;
    }

    // hpのGetter
    public int getHp(){
        return this.hp;
    }
    // hpのSetter
    public void setHp(int hp){
        this.hp = hp;
    }

    // attackPointのGetter
    public int getAttackPoint(){
        return this.attackPoint;
    }
}
```

＜HeroCharacter＞


```java
public class HeroCharacter extends BasicCharacter {

	/*コンストラクタ*/
    public HeroCharacter(String xxx, int hp, int point){
        super(xxx,hp,point);
    }

    /*メソッド*/
    //攻撃する
    @Override
    public void attack(){
        System.out.println("剣で攻撃");
    }

}
```

このように、extends 親クラスと記載することで、親クラスに書かれていることを重複して書かなくてもよくなります。

しかし、コンストラクタだけは、自身の名前で呼ばなければならないので、注意が必要です。

親のコンストラクタを呼ぶ場合は、

```java
super();
```

を使います。

**this**は、自分自身のクラスのフィールドやメソッド、コンストラクタを表していたように、

**super**は、親クラスのフィールドやメソッド、コンストラクタを表します。


また、上記のメソッドでは、BasicCharacterクラスにattackメソッドが書かれているものを、同じものを定義しています。


このように、親クラスで定義しているものを子クラスで同じものを定義すると、定義が上書きされてしまうのです。これを**オーバーライド**と言います。

上記のプログラムでは、**@Override**と記載していますが、書かなくてもプログラムは動きます。
これは、明示的にOverrideと記載することで、上書きしていることを明示しています。

うっかり親クラスで定義されているメソッドを消してオーバーライドしないように注意をしましょう。
**@Override**は、親クラスに同じメソッドがない場合は、コンパイルエラーで知らせてくれるので、
親クラスに持っているか不安な時は、**@Override**をつけて、エラーになるかどうか試してみるとよいでしょう。

試しに、コンストラクタに**@Override**をつけるとエラーになります。

```java
/*コンストラクタ*/
@Override // エラーで知らせてくれる
public HeroCharacter(String xxx, int hp, int point){
    super(xxx,hp,point);
}
```



### ワーク7：同様に、MagicaianCharacterを作ってみましょう。

それでは、下記の条件を入れて、MagicianCharacterクラスを作ってみましょう。

＜条件＞
- BasicCharacterクラスを継承する
- mpのフィールドを定義する
- コンストラクタでmpの値も設定するようにする
- attackメソッドをオーバーライドし、「杖で攻撃」を出力する
- magicメソッドを新しく追加し、「魔法を使用」を出力する


<input id="btn_7" type="button" onclick="getCorrect(7)" value="正解を表示" />

<div id="span_7" style=";padding:5px;display:none;">
正解<br/>
＜MagicianCharacter＞
<pre style="background-color: #364549;color:#ffffff;">

public class MagicianCharacter extends BasicCharacter {

	/*コンストラクタ*/
    public MagicianCharacter(String xxx, int hp, int mp, int point){
        super(xxx,hp,point);
        this.mp = mp;
    }

    /*フィールド*/
    private int mp;
    /*メソッド*/
    //攻撃する
    @Override
    public void attack(){
        System.out.println("杖で攻撃");
    }
    //魔法を使う
    public void magic(){
        System.out.println("魔法を使用");
    }
}
</pre>

</div>



## 抽象クラスとインターフェース
抽象クラス？インターフェース？という言葉を聞くだけで、少し苦手意識を持っていませんか？

実は、抽象クラスとインターフェースは「難しい」ものではなく、むしろ物事を「単純化」する考え方です。

単純化とは、すなわち、物事を**抽象的**にすることです。


### 抽象クラス

例えば、先ほど作成したクラスの中に、攻撃をするメソッドがあります。
この攻撃するメソッドは、キャラクターによって、動作が微妙に違います。

勇者は、「剣で攻撃」
魔法使いは、「杖で攻撃」
格闘家は、「パンチで攻撃」

しかし、単純に見たら、キャラクターが攻撃をしていることにはかわりありません。
これをプログラムに表したものが、抽象クラスです。
つまり、具体的なことは決めなくて、「攻撃する」ことだけを指定すれば、よいということです。

先ほど作ったBasicCharacterクラスを抽象化してみましょう。

★が変更部分です

```java
public abstract class BasicCharacter {//★

	/*コンストラクタ*/
    public Character(String xxx, int hp, int point){
        this.name = xxx;
        this.hp = hp;
        this.attackPoint = point;
    }
    
 
    /*フィールド*/
    private String name; //キャラクターの名前
    private int hp; //現在のHPの状態
    private int attackPoint; //攻撃力

    `/* 抽象メソッド */
    //攻撃する
    public abstract void attack(); //★
    
    /*メソッド*/
    //逃げる
    public void runAway(){
        System.out.println("逃げる");
    }

    /*GetterとSetter*/
    // nameのGetter
    public String getName(){
        return this.name;
    }

    // hpのGetter
    public int getHp(){
        return this.hp;
    }
    // hpのSetter
    public void setHp(int hp){
        this.hp = hp;
    }

    // attackPointのGetter
    public int getAttackPoint(){
        return this.attackPoint;
    }
}
```


これで、抽象クラスの完成です。

このようにメソッドの戻り値と引数のみを定義して、具体的な中身をあえて書かないようにすることで、
「継承したクラスで具体的なこと書いてね！」というメッセージになっているのです。

このようなメソッドを**抽象メソッド**といいます。

抽象メソッドは、子クラスに**強制的にオーバーライドさせるため**に定義するメソッドです。

例えば、HeroCharacterクラスが、attackメソッドをもし書き忘れて、以下のようなままだと、コンパイルエラーになります。


＜HeroCharacter＞

```java
public class HeroCharacter extends BasicCharacter {

	/*コンストラクタ*/
    public HeroCharacter(String xxx, int hp, int point){
        super(xxx,hp,point);
    }

}
```


抽象メソッドのままでは、当然実行できないため、必ず子クラスで定義をしなければいけません。

親の言うことは、絶対なわけです。笑

（でも、具体的にどうするかは自分で決めることができるからね！）

　

しかし、抽象クラスには、デメリットがあります。
それは、抽象クラス自身のインスタンスを作ることはできません。

なぜなら、インスタンスができてしまった場合、抽象メソッドを実行することができないからです。

試しに、Mainクラス内で、下記のコードを記述すると、エラーになります。


```java
BasicCharavter basicCharacter = new BasicCharacter("hoge", 100, 100);
```


#### なぜ、抽象クラスなんてわざわざ作るのか？
それは、基本的には、複数人でプログラムを開発するときに大きなメリットがあります。

例えば、ECサイトで、商品というクラスを作る際に、**必ず定義しておいてほしいものを決めます。**

フィールドは、

値段、商品名、カテゴリー、価格....

メソッドは、

個数に応じた合計金額を返すメソッド、海外からの輸入商品かどうかを返すメソッド...


これらを書面等で共有していても、だれか一人がコーディングミスをするだけで、バグになってしまいます。

その時に、BasicProductというクラスを作って、あとは、その「クラスを継承する」という取り決めだけ
決めてしまえば、楽になりませんか？

このように抽象は、**どんな機能を子クラスで実装してほしいかを決めるためのクラス**といってもいいでしょう。

このように、抽象クラスは、規模が大きければ大きいほど、力を発揮するとても便利な機能です。



### インターフェース
いよいよ、最後のインターフェース。
最後にまた新しい単語....と思った方も多いはず。

でも、どこかで耳にしたことがある言葉のはず。
○○インターフェースという言葉は、割とよく使われます。
インターフェースという言葉自体は、「接している面、境界面」という意味があります。

例えば、ユーザーインターフェースは、主にユーザーとアプリケーションの接するボタンやタッチパネルなど、全般を指します。

オブジェクト指向でいう
**インターフェース**は、**抽象クラスをさらに抽象化したもの**と捉えるとよいです。

基本的には、抽象クラスと同じように、「最低限の取り決めだけを決める」ためのものです。


例えば、先ほど作成したキャラクターが戦うとき、「バトル」という側面を見れば、「戦う」「攻撃する」「逃げる」「アイテムを使う」などの最低限の機能があれば、どんなキャラクターでも戦うことができます。




このように、最低限のものを揃えることを定義するときに、インターフェースが使われることがあります。


#### インターフェースと抽象クラスの違い
ここまで聞くと、インターフェースと抽象クラスって何が違うの？となります。（多くの人が持つ疑問）


実際、使う目的は、ほぼほぼ同じです。
インターフェースや抽象クラスで定義されているものを実装クラスや子クラスで具体的に決めてほしいという目的です。

しかし、インターフェースと抽象クラスは、それぞれ得意不得意があるのです。

##### 抽象クラスの得意分野・不得意分野
○得意
抽象的なメソッドを定義できる
具体的なメソッドも定義できる

○不得意
「親:子」は、必ず「1:多」にならないといけない。


##### インターフェースの得意分野・不得意分野
○得意
多重継承ができる。「親:子」は、「多:多」になってもよい。
抽象的なメソッドを定義できる

○不得意
具体的なメソッドを定義できない

```java
```

```java
```

## デザインパターンの紹介
今回学んだオブジェクト指向の概念を理解し、基礎を学ぶものでした。

今日の学んだことを理解できれば、オブジェクト指向は、難しいものではなく、よりシンプルで単純化する考えだったということがわかってもらえたかなと思います。

しかし、実際に、

このインターフェースや抽象クラスや継承やらを使うにはどうしたらよいか？
実際のプロジェクトにどのように生かしたらいいの？

という悩みは、絶えずあるでしょう。

実は、世の中に何千、何万とあるシステム開発の中で使われているオブジェクト指向を用いたプログラムをパターン化してまとめたものがあります。

それが、**デザインパターン**と言われるものです。

この分野は、次回の応用編で紹介しますので、乞うご期待！！


気になる方は、「オブジェクト指向　デザインパターン」と検索してみましょう。


<script>
function getCorrect(id){
    changeText(id,'正解を表示',"#de4e2e");
}
function moreQuestion(id){
    changeText(id,'挑戦!',"#228822");
}
function getNone(id){
    changeText(id,'表示',"#334433");
}
function getReference(id){
    changeText(id,'参考','#228822');
}
function readDigression(id){
    changeText(id,'余談','#228822');
}
function changeText(id,text,color){
    let span = document.getElementById('span_'+id);
    let btn = document.getElementById('btn_'+id);
    if(btn.value == '非表示'){
        btn.value = text;
        span.style.display = 'none';
    }else{
        btn.value = '非表示';
        span.style.display = 'block';
        span.style.color = color
    }

}

function picturesClickEvent(id){
    let nextId = id == 8 ? 1 : (id+1);
    let prev = document.getElementById('pictures_'+id);
    let next = document.getElementById('pictures_'+nextId);
    prev.style.display = 'none';
    next.style.display = 'block';
}

</script>

