## 実践課題2-2
それでは、下記に沿って実践課題をクリアしていきましょう。



### 課題2-2-1
画面追加

### 課題2-2-2
単体テスト

### 課題2-2-3
クロステスト


# オブジェクト指向って何！？ ～Javaで学ぶオブジェクト指向プログラミング～ 【基礎編】



## オブジェクト指向が苦手になりやすい理由


1. 専門用語が多すぎる！！(クラス、インスタンス、コンストラクタ、継承、ポリモーフィズム、抽象クラス、インターフェース....)

1. 一般的なカリキュラム上、Javaの基礎を学んだ後に学ぶので、そもそも考え方や頭の使い方が一気に変わるから...。

1. そもそも研修レベルの規模ではありがたみを感じにくい...。



## そもそもオブジェクトってなに？

**「オブジェクト」＝「モノ」**


(例)
コップ、ペットボトル、私、クツ、ペン、パソコン、スマホ...全てオブジェクトである。


つまり、オブジェクト指向とは、**「モノ」をプログラムで表現して扱いましょう!**というものである。（ざっくり言えば...）



## オブジェクト指向を体験してみよう！

オブジェクトのスタートラインは"モノ"を概念的に捉える頭の使い方をする。
 
 
### ワーク1 : モノを概念としてとらえる練習

Q1. コップの自己紹介を作ってみよう。


- 長さ
- 重さ
- 水の入る量
- 今水が入ってる量


Q2. コップを使ってできることは？
・水を入れる
・水を捨てる


それでは、自分の携帯電話についてそれぞれの考えてみよう。

Q1. 携帯電話に自己紹介をさせてみよう！



Q2. 携帯電話を使ってできることは？




## フィールドとメソッドとは？

自己紹介の項目で挙げた名詞が**フィールド**
できることを挙げた動詞が**メソッド**

つまり、フィールドは、**モノのステータスや状態を表す**もの。
メソッドは、そのモノが行う**機能**のこと。

プログラムで表すと....

```java
public class Cup{

    /*フィールド*/
    int height; //コップの高さ
    int weight; //コップの重さ
    int max_capacity ; //水の入る量
    int now_water_state; //現在の水の量
    
    /*メソッド*/
    //水を入れる
    void input(){
        
    }
    //水を捨てる
    void output(){
    
    }
}
```



### ワーク2：ゲームの主人公を作ろう！

ゲームの主人公の考えられるフィールドとメソッド....

名詞
    名前
    HP
    MP
   攻撃力
   守備力
   職業
   装備（剣）
   装備（盾）
   装備（鎧）
   持ってる道具

動詞
    話す
    攻撃する
    逃げる
    道具を使う
    移動する



実際にプログラムにしてみよう。（クラスのみ）
    

```java
public class Character {

    /*フィールド*/
    String name; //キャラクターの名前
    int max_hp; //HPの最大値
    int hp; //現在のHPの状態
    int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void run_away(){
        System.out.println("逃げる");
    }  
}
```


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

実際にプログラムで書くと以下の用になります。

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

キャラクターに名前とhpと攻撃力を設定しましょう。
以下のプログラムを加えることで、設定することができます。(※)

```java
hero.name = "ヒーロー";
hero.hp_max = 100;
hero.hp = 100;
hero.attack_point = 10;
```

フィールドは、以下のように呼び出すことができます。

```java
hero.フィールド
```

また、メソッドを呼び出すときは、以下のようにやります。

```java
hero.attack(); //攻撃する。
hero.run_away(); //逃げる。
```

メソッドは、以下のように呼びだすことができます。

```java
hero.メソッド();
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
        hero.hp_max = 100;
        hero.hp = 100;
        hero.attack_point = 10;

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.run_away(); //逃げる。
    }  
}
```

このプログラムを実行してみましょう！

### お時間ある人用ワーク
出来た人は、ヒーローだけでなく、他のキャラクターも作ってみよう。

Q1. 以下の設定のキャラクターを作ってみよう。

名前：ヒロイン
HPの最大値：70
現在のHP：70
攻撃力：10

Q2. 好きなキャラクターを作ってみよう！

名前：???
HPの最大値：??
現在のHP：??
攻撃力：??


このように、Characterクラスから、設定を変えるだけで、たくさんのキャラクターを作ることができます。


## コンストラクタ

先ほどのプログラムに、主人公が自分の名前を名乗れるように、Characterクラスにメソッドを追加します。

```java
void call_name(){
    System.out.println("私の名前は、"+this.name+"だ！");
}  
```

実際にプログラムに追加してみましょう。

＜Characterクラス＞

```java
public class Character {

    /*フィールド*/
    String name; //キャラクターの名前
    int max_hp; //HPの最大値
    int hp; //現在のHPの状態
    int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void run_away(){
        System.out.println("逃げる");
    }  
    //自分の名前を名乗る
    void call_name(){
        System.out.println("私の名前は、"+this.name+"だ！");
    }  
}
```

このように、メソッド内で、自身のクラスのフィールドを使いたいときは、

```java
this.フィールド
```

と表現することで扱うことができます。

それでは、名前を名乗るメソッドをMainクラスに追加します。
しかし、プログラムを一部ミスして、以下のようにプログラムを書いてしまったらどうでしょう？（実際にしたのプログラムをコピーして実行するとエラーになってしまします。）

```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character();

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
```

実は、上のプログラムでは、以下のコードが抜けていて、名前を設定し忘れていたので、名前を名乗ることができなかったのです。

```java
hero.name = "ヒーロー";
```

このようなことが起こらないように、絶対に初期設定を忘れないようにするために、するのが**コンストラクタ**です。

名前を初期設定するコンストラクタは、以下のコードをCharacterクラスに書くことで作ることができます。

```java
Character(String xxx){
    this.name = xxx;
}
```

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
    int max_hp; //HPの最大値
    int hp; //現在のHPの状態
    int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    void run_away(){
        System.out.println("逃げる");
    }  
}
```

すると...Mainクラスにエラーが出てきます。
これは、インスタンスを作る(heroを作る)時に、名前が設定されていないじゃんと怒られているからです。

それでは、実際に名前を設定しましょう。
Mainクラスを以下のように変えてます。

＜Mainクラス＞

```java
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
```

### ワーク4 :他の値も初期設定できるようにしましょう。
<input type="button" onclick="getResult4()" value="答えを表示" />
<script>
function getResult4(){
    alert("ひ・み・つ");
}
</script>

<span>
＜正解＞

```
ここにに正解を記載
```
</span>


## カプセル化
上記のプログラムで、初期設定もちゃんと行えるようにできたので、安心...
と言いたいところですが、実は、今の状態では、Mainプログラムから勝手に、初期設定をした値を変えることができてしまいます。

試しに、いたずらで、「ヒーロー」の名前を「スライム」に変えてしまいましょう。

以下のプログラムをコピーして実行してみましょう。


＜Mainクラス＞

```java
public class Main {
    
    public static void main(String[] args){
        //heroを作りました。
        Character hero = new Character("ヒーロー", 100, 100, 10);

        //いたずら
        hero.name = "スライム";

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.run_away(); //逃げる。
       hero.call_name();//名前を名乗る
    }  
}
```


これを実行すると、「私の名前は、スライムだ！」となってしまいました。

このように、せっかく初期設定をしたものを変えられるのはすごく嫌ですよね。
今状態では、HPの値も敵に見られてしまいます。

そのようなことを防ぐために、フィールドの値を見れないようにする方法があります。
それが、**カプセル化**です。

カプセル化は、Characterクラスに、privateとpublicを追加するだで、守ることができます。

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
    private int max_hp; //HPの最大値
    private int hp; //現在のHPの状態
    private int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void run_away(){
        System.out.println("逃げる");
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
    /*フィールド*/
    private String name; //キャラクターの名前
    private int max_hp; //HPの最大値
    private int hp; //現在のHPの状態
    private int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void run_away(){
        System.out.println("逃げる");
    }  
}
```

<input type="button" onclick="getResult4()" value="答えを表示" />
<script>
function getResult4(){
    alert("ひ・み・つ");
}
</script>


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
        Character hero = new Character("ヒーロー", 100, 100, 10);

        //メソッドの呼び出し
       hero.attack(); //攻撃する。
       hero.run_away(); //逃げる。
       hero.call_name();//名前を名乗る

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
    private Character(String xxx, int max, int hp, int point){
        this.name = xxx;
        this.max_hp = max;
        this.hp = hp;
        this.attack_point = point;
    }
    /*フィールド*/
    private String name; //キャラクターの名前
    private int max_hp; //HPの最大値
    private int hp; //現在のHPの状態
    private int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void run_away(){
        System.out.println("逃げる");
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

GetterとSetterを作ることで例えば、仮に、名前は取得はできるけど、変更できないようにしたい！のであれば、Setterのメソッドを消せば、大丈夫です。（逆もしかり）

また、値を取得したり設定するときに、値を入れていいものかどうかもこのGetterやSetterでプログラムを書くことで、設定することができます。
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

### ワーク6: それでは、他のGetterとSetterを作ってみましょう。





## 静的メンバ
＜今回は省きます。＞


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
    private MagicCharacter(String xxx, int max_hp, int hp, int max_mp, int mp, int point){
        this.name = xxx;
        this.max_hp = max_hp;
        this.hp = hp;
        this.max_hp = max_mp;//★
        this.hp = mp;//★
        this.attack_point = point;
    }
    /*フィールド*/
    private String name; //キャラクターの名前
    private int max_hp; //HPの最大値
    private int hp; //現在のHPの状態
    private int max_mp; //MPの最大値★
    private int mp; //現在のMPの状態★
    private int attack_point; //攻撃力

    /*フィールド*/
    //攻撃する
    public void attack(){
        System.out.println("攻撃");
    }
    //逃げる
    public void run_away(){
        System.out.println("逃げる");
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
    // max_mpのGetter★
    public int getMaxMp(){
        return this.max_mp;
    }
    // mpのSetter★
    public void setMaxMp(int xxxx){
        this.max_mp = xxxx;
    }

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

＜BasicCharacter＞

```java
```

＜HeroCharacter＞


```java
```

このように、extends 親クラスと記載することで、親クラスに書かれていることを重複して書かなくてもよくなります。


### ワーク7：同様に、MagicianCharacterを作ってみましょう。

＜MagicianCharacter＞

```java
```


上記のプログラムでは、BasicCharacterクラスのattackメソッドで攻撃をしますが、勇者は、剣で攻撃をしたいですし、魔法使いはステッキを使って攻撃をします。この場合、勇者と魔法使いクラスにそれぞれ以下のように、attackメソッドを追加することもできます。

```java
```

```java
```


実は、親クラスで定義しているものを子クラスで同じものを定義すると、定義が上書きされてしまうのです。これを**オーバーライド**と言います。



## 抽象クラスとインターフェース
抽象クラス？インターフェース？という言葉を聞くだけで、少し苦手意識を持っていませんか？

実は、抽象クラスとインターフェースは「難しい」ものではなく、むしろ物事を「単純化」する考え方です。

単純化とは、すなわち、物事を抽象的にすることです。

### 抽象クラス

例えば、先ほど作成したクラスの中に、攻撃をするメソッドがあります。
この攻撃するメソッドは、キャラクターによって、動作が微妙に違います。

勇者は、「剣で攻撃」
魔法使いは、「ステッキで攻撃」
格闘家は、「パンチで攻撃」

しかし、単純に見たら、キャラクターが攻撃をしていることにはかわりありません。
これをプログラムに表したものが、抽象クラスです。
つまり、具体的なことは決めなくて、「攻撃する」ことだけを指定すれば、よいということです。

先ほど作ったBasicCharacterクラスを抽象化してみましょう。


```java
```


これで、抽象クラスの完成です。

### インターフェース
続いて、インターフェースについて扱います。
インターフェースは、抽象クラスをさらに抽象化したものです。
インターフェースという言葉自体は、「接している面、境界面」という意味があります。

インターフェースの考え方が用いられるのは、例えば、先ほど作成したキャラクターが戦うとき、「バトル」という側面を見れば、「戦う」「攻撃する」「逃げる」「アイテムを使う」などの最低限の機能があれば、どんなキャラクターでも戦うことができます。

このように、最低限のものを揃えることを定義するときに、インターフェースが使われることがあります。

実際にインターフェースを作ってみよう！


```java
```

```java
```




## デザインパターンの紹介
今回学んだオブジェクト指向は、概念を理解するためのものでした。

しかし、実際このインターフェースや抽象クラスや継承やらを使って何ができるの？実際のプロジェクトにどのように生かしたらいいの？ということを実践で使われているいくつかのパターンがあります。

それが、**デザインパターン**と言われるものです。
この分野は、次回の応用編で紹介しますので、乞うご期待！！

