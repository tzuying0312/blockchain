# WEEK7_ IOTA Part1
###### tags: `blockchain`

- 幣圈
    - 想像各式各樣的用例，ex : 紅利點數、賭場代幣，吸引消費者去使用他的服務，才可以在推廣服務的時候讓消費者買單。
    - POSEIDON NETWORK(發行區塊鏈貨幣)。
- 鏈圈
    - 不是很在乎幣的問題，也不太強調發行什麼幣。
    - 喜歡在**帳本**上存上任何攸關於信用的東西。
    - 存任何憑證進公鏈或私鏈，最重要的角色不是檢查存證，重點是誰來查驗誰認可ex:將畢業證書寫入區塊鏈。


汽車資料上鍊，如果包含定位資料，這樣不會牽扯到隱私問題嗎?
>區塊鏈預設是匿名，device(汽車)本身跟擁有人本身是分開的，一直到手上有device的代幣，要把錢領出來，才會拿者prviate key去交易所交易，這時候才會牽扯到實名字問題(人的錢包非汽車)。

- 身份證正
一個人把它可以認身份的一份文件寫到鏈上，但非把身分證upload到區塊鏈上這麼簡單。(ex:假設要去拿東吳幣，但要做一定程度的身分認證(至少要知道你是東吳學生)。後面的議題為**自主身份認證**。

- 自主身份認證
用你的身份行使哪些事情留下足跡，這個足跡不可否認的也在鏈上，而這個足跡可以給下一個Verifier來採納。
>ex:假設去超商買菸，超商店員(Verifier)要身份證，必須先知道你是否滿18歲。店員許可後，他把一份申明隨著錢包放在鏈上，下次買酒，酒行老闆就不需要再看身份證，因為有另外一份證書聲明可以用，這個證明就是超商店員給你的。

- [How Does Tangle Work](https://github.com/noneymous/iota-consensus-presentation/blob/master/iota_consensus_v1.1_spanish.md)
IOTA其實是貨幣，背後骨幹是Tangle，就如同Ethereum是貨幣，後面骨幹是blockchain。小方塊為交易，廣泛的被分為幾種。IOTA發起一筆交易，必須要去驗證之前的兩筆交易(去查別人的帳)，為唯一規則。 

    >- 越靠近左邊，ex:A，存在越久，隨者時間的推移，不斷有新的帳本從右側進來。w為新來來的帳，須選前面的兩筆帳(q或s)，把這兩筆帳當作一個起點，去檢查一定深度的帳本。
    >- 可以被稱為fully confirmed是要看這筆交易之後有多少人去認證他，越多越有機會被稱為fully，而非去驗證了誰或驗證幾個。
    >- 要驗證的區塊為random，他會在一個完全沒有被驗證的交易當作選擇入口(ex:w、x、z、y)。
    >- 交易量要夠大(成功關鍵)，才可以去驗證tip，並可以找到衝突交易。

![](https://i.imgur.com/hBj1bgA.png)

- IOTA節點種類(由大到小:permanode --> full-node --> swarm-node)
    -  Swarm-node
    -  Full-node，像儲金簿一樣常常刷。從最後一個milestone，保留一定的深度交易。不在乎Permanode，ex:小時候去郵局存壓歲錢，但不會在乎從以前到現在有多少交易，在意的是有多少錢。
    -  Permanode(永恆節點)，去郵局存錢，郵局有你的交易。