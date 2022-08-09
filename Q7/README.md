あなたはチャットアプリの開発をしています。

チャットアプリでは2種類ユーザが存在し、それぞれ一般ユーザ、管理者ユーザと呼称されます。

一般ユーザでは入力した文字列がそのまま出力されます。一方で、管理者ユーザについては入力した文字列の前後に `***` が付与されて出力されます。

以下の条件を満たすようにコーディングしなさい。

1. Mainクラスにある通り、各ユーザのprintメソッドの引数に対して渡された文字列が入力を表す。上述のルールを満たすようにprintで出力の処理を行うこと。
1. Mainクラス、Userクラス、UserStoreクラスは書き換えてはならない。ただし、package宣言は行なってよい。
1. コード中でif文や三項演算子は使用してはならない。

## コード


Main.java

```
public class Main {
    public static void main(String[] args) {
        UserStore store = new UserStore();

        // 一般ユーザ
        User normalUser = store.getNormalUser();
        normalUser.print("こんにちは。");

        // 管理者ユーザ
        User admin = store.getAdminUser();
        admin.print("17時からメンテナンスです。");
    }
}
```

User.java

```
class User {
    public void print(String message) {

    }
}
```

UserStore.java

```
class UserStore {
    public User getAdminUser() {
        return new AdminUser();
    }

    public User getNormalUser() {
        return new NormalUser();
    }
}
```


## 出力

```
こんにちは。
***17時からメンテナンスです。***
```

