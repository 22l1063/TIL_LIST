<details>
<summary>HTMLを開く</summary>

``` HTML
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./assets/css/station9.css" type="text/css" />
    <title>Station 9</title>
  </head>
  <body>
    <div id="animation">
      <p>フェードイン</p>
    </div>
  </body>
</html>
```
</details>




<details>
<summary>CSSを開く</summary>

``` CSS
#animation{
    animation-name: fadein;
    animation-duration: 2s;
    animation-timing-function: ease-out;
    animation-fill-mode: forwards;
}

@keyframes fadein {
  0% {
     opacity: 0;
     transform: translateY(0);
  }
  100% {
     opacity: 1;
     transform: translateY(20px);
  }
}
```
</details>
---


## @keyframes  とは
動きの設計図である。アニメーションを作成できる。
アニメーションの動作を特定の時点での動作を指定するものである。
今回はfadeinというアニメーションを `@keyframes`で作成している。

0%つまり始まりの時は
```
  0% {
     opacity: 0;
     transform: translateY(0);
  }
```
透明度: 0
位置：0（動かない）

次に１００％の時
```
100% {
     opacity: 1;
     transform: translateY(20px);
  }
```
透明度:1
位置:元の位置から20px動く


```
#animation{
    animation-name: fadein;
    animation-duration: 2s;
    animation-timing-function: ease-out;
    animation-fill-mode: forwards;
}
```
`animation-name:fadein` これは`@keyframes`でルール定義したアニメーションに名前をつける。
` animation-duration: 2s;` アニメーションが1回のサイクルを完了するまでにかける時間を設定している。
`animation-timing-function: ` 時間の経過に伴い動きを変化させるためのもの。`ease-out;`ではじめは早く、最後はゆっくりになるようにする。
他にもいくつかある。
```
値	動きの特徴
ease (デフォルト)|	緩やかに始まり、速くなり、また緩やかに終わる。
linear	|常に一定の速度（緩急なし）。機械的な動き。
ease-in |	緩やかに始まり、終了に向けて加速する。
ease-in-out	 |緩やかに始まり、中央で最速になり、また緩やかに終わる。
```

`animation-fill-mode: forwards;`これはアニメーションを100%の状態でキープする。通常アニメーションは100%まで達成すると、0%に戻っています。しかし、`forward`を指定すると、100%の状態で停止する。






