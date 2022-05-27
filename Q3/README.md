RPGゲームのキャラクターが1人ずつ行動するような戦闘システムを作りたい。

戦闘ではキャラクターは素早さ(speed)が高いほど先に行動できるようにしたい。

仕様を満たすようにBattleControllerのpresetメソッドをしなさい。


Main.java

```java
import java.util.ArrayList;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<Character> list = new ArrayList<>();

        list.add(new Character("スライム", 20));
        list.add(new Character("イザベル", 40));
        list.add(new Character("マンドラゴラ", 10));

        BattleController controller = new BattleController();
        list = controller.preset(list);

        list.forEach(c -> c.attack());
    }
}
```

Character.java

```java
public class Character {
    private String name;
    private int speed;

    Character(String name, int speed) {
        this.name = name;
        this.speed = speed;
    }

    public void attack() {
        System.out.println(name + "の攻撃！");
    }

    public int getSpeed() {
        return speed;
    }
}

```

BattleController.java

```java
import java.util.List;

public class BattleController {
    public List<Character> preset(List<Character> list) {
         return list;
    }
}
```