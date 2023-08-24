#plugin
pluginはJavaScriptのライブラリであるJQueryを入れることで様々なpluginを利用することができます。

今回はcsshakeというpluginを使用してブルブルさせる。

まずはhttps://elrumordelaluz.github.io/csshake/#install

上記URLでアクセス

1. 
    
    ![スクリーンショット 2023-08-23 15.11.53.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/28b76fbc-3dc6-4b4a-a847-9493f2158e88/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2023-08-23_15.11.53.png)
    
2. 
    
    ![スクリーンショット 2023-08-23 15.12.26.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/963e7e4d-c6b4-4888-ad15-bdf494361711/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2023-08-23_15.12.26.png)
    
    コピーしたリンクをHTMLに貼り付け
    
    ![スクリーンショット 2023-08-23 15.14.36.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b6294aa3-45ed-45da-a6ab-4af430a75392/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2023-08-23_15.14.36.png)
    
    <script〜の下の<link〜の部分がコピーしてきたコード
    

### 導入はここまで

### 実装方法

![スクリーンショット 2023-08-23 15.17.12.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/52157e1c-e7bb-4732-9f4d-0a8d0c5eeded/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2023-08-23_15.17.12.png)

今回は左上あたりの<div class="shake"></div>を実装します

![スクリーンショット 2023-08-23 15.19.13.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b5dec04d-e413-4958-a9eb-47dfc63f97ac/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2023-08-23_15.19.13.png)

これでRUNTEQの文字が震えます。

その他のpluginはJQuery pluginなどで調べる必要がある