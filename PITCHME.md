### 今日の成果一覧

- ECSのec2コンテナインスタンス上にawsvpcモードでtaskを起動させることの闇をここ一週間ずっと体感している

- [Amazon Web Services 基礎からのネットワーク＆サーバー構築 改訂版](https://www.amazon.co.jp/Amazon-Web-Services-%E5%9F%BA%E7%A4%8E%E3%81%8B%E3%82%89%E3%81%AE%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF%EF%BC%86%E3%82%B5%E3%83%BC%E3%83%90%E3%83%BC%E6%A7%8B%E7%AF%89-%E6%94%B9%E8%A8%82%E7%89%88-ebook/dp/B06Y5ZSYY4/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1540015149&sr=1-1&keywords=aws+%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)でマスタリングTCP/IPで得た知識を活用しながら、awsのvpc辺りの組み立てをしてみた。

---

ECSのあるクラスターでtaskをawsvpcモードでtaskを起動させると並行実行できずタイムアウトで死ぬ

--- 

- cpu足りてないんじゃない？
  - 足りてなかったら `Provisioning`ステータスにならずにしんでたはず
 
--- 
- memory足りてないんじゃない？
  - そんなこともなかった
  
---
- ENIがたりてないんじゃない？
  - そんなこともなかった
  
---

## 笑

---

## END
