# Drum kit

透過監聽鍵盤事件(keydown)的keycode，並利用DOM的data-key判斷對應的div及audio，實現敲擊的聲音及css特效。

## 基礎語法

### 反引號``組成的字串樣板(template literal)

在字串樣板中，可以透過 ${...} 的方式，嵌入變量或任何的表達式。

```
`audio[data-key="${e.keyCode}"]`
```

另外也可利用字串樣板在 JS 中放入 HTML 的內容，或是包含換行的長字串，
[更多關於字串樣板](https://pjchender.blogspot.tw/2017/01/javascript-es6-template-literalstagged.html)。

### 用 const 宣告常數

const 就是常數 constant 的意思，宣告之後是不能再被改變的，除了 array 及 object 的數據值。

> const 實際上保證的，並不是變量的值不得改動，而是變量指向的那個內存地址不得改動。對於簡單類型的數據（數值、字符串、布林值），值就保存在變量指向的那個內存地址，因此等同於常量。但對於復合類型的數據（主要是對象和數組），變量指向的內存地址，保存的只是一個指針，const 只能保證這個指針是固定的，至於它指向的數據結構是不是可變的，就完全不能控制了。因此，將一個對象聲明為常量必須非常小心。

const 和 let 一樣是 block-scoped 的，只在代碼區塊內有效。

參考： [let 和 const 命令](http://es6.ruanyifeng.com/#docs/let)

### '=>' 箭頭函數(Arrow Function)

箭頭函數有兩個重要的特性：更短的函數寫法與 this 變數綁定。

範例:

```
var a = [
  "Hydrogen",
  "Helium",
  "Lithium",
  "Beryl­lium"
];

var a2 = a.map(function(s){ return s.length }); //一般寫法

var a3 = a.map( s => s.length );
```

參考： [MDN JavaScript 參考文件](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Functions/Arrow_functions)


##參考資料:

- 查找keycode: [keycode.info](keycode.info)
- [ECMAScript 6 入門](http://es6.ruanyifeng.com/?search=querySelector&x=0&y=0)
