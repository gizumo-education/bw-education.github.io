# GizumoFAQ

## 【Question】 ブロック要素のwidthが省略できる時ってどんな時？

## 【Answer】 親要素にwidthが指定してあって、自身が親要素と同じ大きさの指定をしたい時

### 【解説】

ブロック要素は「横幅いっぱいになる」という特徴があります。  

たとえば、親要素が「400pxの正方形」で、子要素は「横400px、縦200pxの長方形」のboxを作成したいとします。  

素直にコードを書くと以下のようになりますよね！

```html
<div class="parent">
  <div class="child"></div>
</div>
```

```css
.parent {
  width: 400px;
  height: 400px;
}

.child {
  width: 400px;
  height: 200px;
}
```

しかし、divタグは**ブロック要素**なので勝手に「横幅いっぱい」になります。  
今回は親子関係が成立しているので、子要素は親要素いっぱいに広がり、勝手に`width: 400px;`になります！

したがってコードは以下のようにしても結果は変わりません！

```html
<div class="parent">
  <div class="child"></div>
</div>
```

```css
.parent {
  width: 400px;
  height: 400px;
}

.child {
  height: 200px;
}
```

これで１行減りましたね！  
たかが１行ですが、webサイトはとんでもない量のboxで構築されています。少しでも減らせればサイト全体で多くのcssを省略できる形になりますので、ぜひ意識してやってみてください！
