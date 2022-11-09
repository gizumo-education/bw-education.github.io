# GizumoFAQ

## 【Question】^の配置がうまくいきません。

## 【Answer】　translateをしてからrotateしましょう。

### 【原因】

rotateをすると、基準とする支点ごと回転してしまいます。
その為、右に移動させたつもりが、斜めに移動してしまうなどの事象が発生してしまいます。
では、どうすれば良いかというと、translateで移動させた後で回転する様に実装しましょう。

🙅‍♂️
`transform: rotate() translateY() translateX();`

🙆‍♀️
`transform: translateY() translateX() rotate();`

![rotate](https://res.cloudinary.com/gizumo-inc/image/upload/v1667991677/curriculums/GizumoFAQ/Screen_Shot_2022-10-06_at_16.33.51.png)