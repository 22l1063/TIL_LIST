# GridLayoutについて
<details>
<summary>ここをクリックするとHTMLが開きます</summary>  
  
``` html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./assets/css/station8.css" type="text/css" />
    <title>Station 8</title>
  </head>
  <body>
    <div id="container">
      <header>ヘッダー</header>
      <div class="one">アイテム1</div>
      <div class="two">アイテム2</div>
      <div class="three">アイテム3</div>
      <div class="four">アイテム4</div>
      <footer>フッター</footer>
    </div>
  </body>
</html>
```
</details>


<details>
<summary>ここをクリックするとCSSが開きます</summary>

```css


#container{
  display: grid;
  grid-template-columns: 0.2fr 1fr ;
  grid-template-rows: auto 100px 100px 100px auto;
  gap: 10px;
}

header{
    background-color: #ff9999;
    grid-column:1/3;
    grid-row: 1/2;
}


.one{
    background-color: #ff9999;
    grid-column:1/2;
    grid-row:2/5;
}
.two{
    background-color: #99ff99;
    grid-column: 2/3;
    grid-row: 2/3;
}
.three{
    background-color: #9999ff;
    grid-column: 2/3;
    grid-row: 3/4;
}
.four{
    background-color: #ffff99;
    grid-column: 2/3;
    grid-row: 4/5;
}
footer{
    background-color: #ff9999;
    grid-column:1/3;    
    grid-row:5/6;
}
```

</details>


## GridLayoutとは
親要素の大きな土台に線（グリッド線）を引いて区画を作成する。（←重要）
区切られた中に要素を設置する。

---


##GridLayout書き方。

まずは親要素である。`container`に土台を作成する。
```
#container{
  display: grid;
  grid-template-columns: 0.2fr 1fr ;
  grid-template-rows: auto 100px 100px 100px auto;
  gap: 10px;
}
```
まず、`display: grid;` で土台を作成した。
次に、`grid-template-columns: 0.2fr 1fr ;`で横幅の設定をした。これは、1対5で2つに分けている。
`grid-template-columns: `　の後の入力を増やすことで3つに分けたり4つに分けたりできる。
`grid-template-rows:`は縦幅である。

```

header{
    background-color: #ff9999;
    grid-column:1/3;
    grid-row: 1/2;
}
```
なぜ、横を二つに分けたのに`grid-column:1/3;`では1/3とあるのか。
それは、1/3はグリッド線のことを指しているからである。
現在のグリッド線は以下のようになっている。
```
【線①】         【線②】                【線③】
         ↓                ↓                       ↓
         |                |                       |
         |   0.2frの部屋   |       1frの部屋        |
         |    (1つ目)     |        (2つ目)        |
         |                |                       |
```



















