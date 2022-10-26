# GizumoFAQ

## 【Question】inline-blockの横並びをしようとしたら段落ちしてしまってうまくいかない

## 【Answer】　親要素にfont-size: 0;を指定しよう

### 【原因】

inline要素は文の一部として扱うので基本的に改行をせずに書きます。

```html
// 例
<p>こんにちは<span>❤︎</span></p>
```
しかし、元々block要素のものはインデントを揃えて書くのが当然ですよね！

```html
// 例
<div>
  <p>おはよう</p>
  <p>こんにちは</p>
  <p>こんばんは</p>
</div>
```

この状況でpタグをinline-blockにした時
