# TIL-アロー関数について

## 学んだこと
・Javascriptのアロー関数基本構造と意味について。


## アロー関数とは。
具体的には、return, {} function　などを省略できる。
=>　この形が弓に見えることからアロー(Arrow)関数と呼ばれるようになったのだろうと考えられる。とても覚えやすくていいと思う。👍

## アロー関数の特徴　
* `function`や`retun`,`{}`の文字を省略できる。
他の関数に無名関数を引数として渡す時によく使われる。

---

## アロー関数の書きかた。
アロー関数の使い方にはいくつかのパターンが存在する。


### 1 引数がない場合
`function`という関数宣言を`const`という変数宣言に変更しないといけない。
`()`を残しておくA。


```
 functin greet(){
  console.log("Hello World"!)
}

//↑この関数をアロー関数で書くと。

 const arrowGreet = () => console.log("Hello World"!);
```
このように{}の部分が省略できる。


### 2 次に引数が一つの場合は
引数が一つの時は()を省力して書くことできる。

```
function doubled(num) {
 return 2* num;
}
// これをアロー関数で書くと。

const arrowDoubled = num => 2 * num;
```


### 3 引数が2つある場合は
引数が二つの場合は()を省略できない😱😱😱

```
function multiply(a, b) {
 return a * b;
}

//これをアロー関数で書くと。

const arrowMultiply = (a, b) => a * b;


```




### 4 他の関数に無名関数を引数として渡す時.←アロー関数はこれのためによく使われるらしい。


```
const numbers = [1,4,5,12,33,45,66]

numbers.forEach(function(number){
 console.log(number);
});

//これをアロー関数で書くと。

numbers.forEach(number => console.log(number));

```
このようになる。これだとだいぶ省略されて見やすくなったと感じる。

 
