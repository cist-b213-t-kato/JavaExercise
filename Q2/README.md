Cupは水を入れるためのクラスです。Cupの中には水を表すwater変数があり、中の数値は水の量(ml)を表します。

下記の条件を満たすようにCupを実装してください。

1. Cupに入れられる水の量は常に300mlを超えてはならない
2. あなた以外の人はCupの実装を書き換えられない
3. あなた以外の人はコンパイルの通る範囲でCup以外の実装を自由に書き換えられる

Cup.java

```java
public class Cup {
    int water;
}
```

Main.java

```java
public class Main {
    public static void main(String[] args) {
        Cup cup = new Cup();
        cup.water = 500;
        System.out.println(cup.water);
    }
}
```
