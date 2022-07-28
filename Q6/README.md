Appクラスを実行したときに、下記の実行結果が出力されるようにプログラムを実装しなさい。

ただし、AppクラスおよびAnimalインタフェースのコードについては書き換えできないものとする（packageは追加してよい）。


Appクラス

```
public class App {
    public static void main(String[] args) {
        AnimalStore store = new AnimalStore();
        Animal[] animals = store.getAnimals();
        for (Animal animal : animals) {
            animal.cry();
        }
    }
}
```

Animalインタフェース

```
public interface Animal {
    void cry();
}
```

実行結果

```
わんわん
にゃにゃー
ちゅんちゅん
```
