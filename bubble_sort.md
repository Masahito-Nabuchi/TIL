課題1、バブルソート

配列の中にランダムに配置されている要素を背の順にソートさせるアルゴリズム。

色々調べて考えたけど理想の経験値は得られないし現状が好転しないので次の課題に進む。

```ruby
# number_arrayには[3, 5, 9, 7, 1]のような配列が入ってきます。
# その引数だった場合の返り値が[1, 3, 5, 7, 9]となるようにします。

def chapter01_01(number_array)
  # ここから下に解答コードを記載する
  number_array_size = number_array.size
  # 比べる数値の要素分をループ処理
  number_array_size.times do |i|
    # 比べられる残りの要素分をループ処理
    # 注意点：iの初期値は0のため(i + 1)にして残りの配列の要素の個数を計算している
    (number_array_size - (i + 1)).times do |j|
      # 隣同士の数値を比較して左の数値の方が大きい場合、配列内の数値の位置を入れ替える
      if number_array[j] > number_array[j + 1]
        tmp = number_array[j]
        number_array[j] = number_array[j + 1]
        number_array[j + 1] = tmp
      end
    end 
  end
  p number_array
end
```

### 疑問点

- jとiはループするたびに１ずつ増える？
- そうする事で確定して比較回数が１つづつ減っている？