# WEEK10
###### tags: `blockchain`

- 傳統資料庫
> 不一定網站讀取的資料都要往後端送，可以有些留在瀏覽器上(ex:cookie即為使用者自己保留的部分)，需要的資料塞成json，往伺服器丟，存置實體資料庫(集中式資料庫管理)。

![](https://i.imgur.com/08V2nlz.png)

- 區塊鏈
>json傳到AWS，AWS負責上鏈到IOTA的各個節點上。

![](https://i.imgur.com/b3FF6Nn.png)

HTML
- 主要分為兩個部分:head、body
- body呈現出網頁內容
- head控制body
- 內容以TAG +attribute呈現(可巢狀)
- h1、h2...h6標題
- p段落文字
- span就是只文字
- div區塊
- svg畫布

CSS
- 在head加style
- 在head匯入外部的CSS檔案
- 直接打在TAG的attribute當中的(style="")
- 基本樣式:color,background-color
- 基本樣式:border-color,border-with
- 基本樣式:width,height

JavaScript
- 一切都是var
- function object
- 在head加script
- 在head匯入外部的js檔案

SVG
- 可以做向量圖的繪製
- body內的一種tag
- 記得要給寬、高
- attribute不等於style(ex:color->fill)
- 不能包div span等東西(變成g,text...)

JSON
- 跟IOTA溝通
- 單純html的from收下來的資料會存成xml的樣子
- 用JavaScript轉成json的格式才能去呼叫post的動作

GET
- 網址後面有問號跟一大堆參數
- 網址後面跟著就是所有變數，因此可以當成整個網址直接往API送
- 評估被看到有沒有關係，不見得所有資料都要被隱藏

POST
- 一樣可以填資料，送出去看不到送甚麼
- 因為不是跟在網址後面，所以會多一個取出來轉成某一種後端能吃的排版動作
- 麻煩但安全
