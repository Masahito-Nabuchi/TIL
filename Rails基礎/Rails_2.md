部分テンプレート
application.html.erbに記入してヘッダー部分やフッター部分を使いまわす。

上記画像の様にsharedフォルダにテンプレしたいファイルを配置する。内容を記入。
下記画像内のように記入

※renderの部分がテンプレート部
link_toの使い方
<%= link_to image_tag("logo.png", class:"navbar-brand"), "/" %>
​
上記コードはイメージタグを使ったリンク作成でクラスを与えている。ルートはホームである。
<%= link_to "掲示板", "#", class:"nav-link dropdown-toggle", data: {bs_toggle: "dropdown"}, arta: {haspopup: "true"},aria: {expanded: "false"} %>
​
上記は掲示板という文字がリンクの文字でクラスと各属性を指定している。
<%= link_to "#",class: "nav-link",id: "header-profile",data:{bs_toggle:"dropdown"},aria:{haspopup:"true"},aria:{expanded:"false"} do %>
           <div>
            <%= image_tag("sample.jpg",class:"rounded-circle mr15",width:"40",height:"40") %>
           </div>
          <% end %>
​
リンクとイメージにそれぞれクラスを与えてブロックで渡す。