# DOM操作

## 練習問題1

### ヒント

1. [要素の取得について](#1-要素の取得について)
2. [アニメーションについて](#2-アニメーションについて)
3. [cssプロパティの変更について](#3-cssプロパティの変更について)

#### 1. 要素の取得について

今回DOM操作の対象になる要素が下記2つの要素になります。
- `<article class="card-type card-type--mocha">`
- `<article class="card-type card-type--yellow animate__animated" style="display: none;">`  

まずは、それぞれ対象要素のクラス名をセレクタとして指定し要素の取得をしましょう。  
今回は`.card-type--mocha`と`.card-type--yellow`をセレクタにします。  

要素の取得する場合は変数に代入するのが一般的なので、下記を参考に変数に代入してみてください。  
```javascript
const 任意の変数名 = document.querySelector('対象のセレクタ');
// 任意の変数名は分かりやすい命名をしましょう
// querySelector()の引数はセレクタ指定なので先頭の'.'を忘れないように記述しましょう
```

取得したら`console.log(任意の変数名)`で子要素も含めた対象の要素が取得できていればOKです。  
※`card-type--mocha`の結果のみ記載しています

```html
<article class="card-type card-type--mocha">
  <h2 class="card-type__title">
    <span class="card-type__circle"></span>
    Node Type
  </h2>
  <ul class="menu">
    <li>Document</li>
    <li>Element</li>
    <li>Text</li>
  </ul>
</article>
```

#### 2. アニメーションについて
DOM操作セクションの下部に記載されているヒントを参考にします。
> ヒント  
「Node Type」のアニメーションクラス: card-animation  
「Event Type」が下からフェードインするアニメーションクラス:animate__fadeInUp  

この問題では対象の要素にクラスを付与することで、アニメーションが実行されるようになっています。  
クラスは`対象の要素.classList.add(付与したいクラス名)`で付与することができるので、ヒント1で取得した要素(変数)を使ってクラスの付与をします。

```javascript
const 任意の変数名 = document.querySelector('対象のセレクタ');
// 追記↓
任意の変数名.classList.add('付与したいクラス名');
// add()の引数はクラス名なので'.'をつけないように気をつけましょう
```

ブラウザをリロードする度に「Node Type」がアニメーションすればOKです。  
アニメーションが実行されることが確認できたら、「DOM Operation」という文字の落下アニメーションが完了したタイミングで、クラスが付与されるようにしましょう。  

#### 3. cssプロパティの変更について
DOM操作セクションの下部に記載されているヒントを参考にします。
> ヒント  
「Event Type」カードはdisplay: none;で非表示になっています

`display: none;`で非表示になっている要素を表示させるには`display: none;`を`display: block;`に変更する必要があります。  
cssプロパティは`対象の要素.style.プロパティ名 = '値';`で変更することができます。  
今回変更したいプロパティはdisplayなので下記のように記載します。  
```javascript
対象の要素.style.display = 'block';
```
要素が表示されることが確認できたら、「DOM Operation」という文字の落下アニメーションが完了したタイミングで、cssプロパティを変更するようにしましょう。  