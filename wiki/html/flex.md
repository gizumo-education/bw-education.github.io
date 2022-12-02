# GizumoFAQ

## 【Question】　flexの使い方がわからない

## 【Answer】　デベロッパーツールの機能を使いこなそう

### 【確認方法】

![](https://res.cloudinary.com/gizumo-inc/image/upload/v1669963349/curriculums/GizumoFAQ/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2022-12-02_15.40.47.png)

デベロッパーツールを開き、flexが適応されている箇所を見てみましょう。  
すると謎のアイコンがありますね！それを押すとflexメニューが展開されます。  
このメニューを使うと、どの指定でどのように変化が起きるのかをコードを書かずに確認することができます！

flexってなんかたくさんあって覚える自信ないなぁ...という方も多いかと思いますが、この機能を知っておくことで、`display: flex;`の他に23個覚えなきゃいけなかったところ、一つも覚えておく必要がなくなったと言っても過言ではありません。

![](https://res.cloudinary.com/gizumo-inc/image/upload/v1669964712/curriculums/GizumoFAQ/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2022-12-02_16.04.52.png)

試しに両端に配置しようと青くなってるボタンを押してみましょう。  
そうすると`justify-content:space-between`を指定すればいいとわかりますね！

### 【簡単な解説】

- flex-direction
  - どのような順番で配置するかを指定できます。
  - 通常は左上スタートで右に向かって配置されます。
- flex-wrap
  - 折り返すかどうかを指定できます。
- align-content
  - 縦方向(行)のレイアウトの指定ができます。
- justify-content
  - 横方向(列)のレイアウトの指定ができます。
- align-items
  - 行の中での配置方法を指定できます。
