# Blazor component
> Editor: ParrotLun [LinkedLIn](www.linkedin.com/in/parrotlun)

## Some comparison

- 參考下圖ASP.NET Razor Page與ASP.NET MVC都是由用戶端瀏覽器送出一個請求，例如要求Index頁面/檢視，伺服端便將整個頁面/檢視的執行結果傳回：
![](https://i.imgur.com/5zHhyei.jpg)

- 而ASP.NET Blazor則是使用多個元件(Component)，組成一個呈現在使用者看到的使用者介面。參考下圖是Blazor Web Assembly運作方式，第一次執行時將整個應用程式下載到瀏覽器，若有需要可透過網路叫用後端服務導向程式REST API來取得資料。您可以將Blazor想像成Vue.js或Angular，只不過我們使用的程式語言不是JavaScript而是C#
![](https://i.imgur.com/9h3WpQ6.jpg)

- ASP.NET MVC、ASP.NET Razor Page與ASP.NET Blazor主要差異請參考下表：
![](https://i.imgur.com/H6PBsrS.jpg)

```razor是模板引擎```

```Blazor是一種框架，不需要頁面刷新使服務端的重新渲染，而是實现了局部渲染```

## Understanding Blazor Component
```
In Blazor, you build the UI from self-contained portions of code called components. Each component can contain a mix of HTML and C# code. Components are written using Razor syntax, in which code is marked with the @code directive and other directives can be used to access variables, bind to values, and achieve other rendering tasks. When the app is compiled, the HTML and code are compiled into a component class. Components are written as files with a .razor extension.
```
```Component是可以重複利用```

## Implement
![](https://i.imgur.com/v6UYNbW.png)
![](https://i.imgur.com/zGtZfDG.png)
![](https://i.imgur.com/Y4TS4wH.png)
![](https://i.imgur.com/ZXtbXrV.png)
```
@code 類似JS會做的事情
html裡面用到C#的程式必須以@開頭
```
```
@page指示詞，這個指示詞相當於傳統的路由，可以看到Index.razor的@page 為"/"，表示這是首頁
```
```
Blazor只有一個網頁，其他內容都是一個個Component組成的，每次觸發事件，Server或是WebAssemlby都會將相應Component呈現在瀏覽器上。
```
![](https://i.imgur.com/vGl0Vlx.png)
![](https://i.imgur.com/PZ4B4SC.png)

![](https://i.imgur.com/liCwmfd.png)

## Reference
https://ucomedu.blogspot.com/2021/06/mvcrazor-pagesblazor.html
https://blog.csdn.net/BlazorComponent/article/details/121543572
https://ithelp.ithome.com.tw/articles/10260047
