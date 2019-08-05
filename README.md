# js勉強会 型のはなし <span>〜型と心理的安全性〜</span>

## 型とはなにか

## JavaScriptにおける型

- 変数に入ってくる値は、必ず下記の6つどれかの型にあてはまる
    - `undefined` `null` `boolean` `number` `string` `object`
    - ただこの６つ自体を覚えることにあんまり意味はない。

## 暗黙の型

### 落とし穴

- `+` でのString変換
- 厳密比較 `===` `!==`
- boolean
- typeof
    - `typeof null === 'object'` !?
    - 基本的にはtypeofを使わなきゃ判断がつかないようなややこしい判定式は書かないほうがいい！
- isNaN
    - number型かどうかを判断するものではない
    - isNaN使わなきゃ判断がつかないような(ry
- 「空」という値をどうやって入れておくか問題
- 基本的にはJavaScriptでは、「ここに何が入ってるか」ということは常に安心できない。常に不安に思っとくくらいでちょうどよいという険しい世界。

## TypeScript

- 暗黙の型ではなく、明示的な型を宣言時につけられるようにになる。それによりこうした落とし穴を未然に防いでくれるのが、TypeScriptを使うメリットのひとつ。
- 自分で定義したデータ型・オブジェクトも型として登録できるので、こうしたベースの部分以外でもかなりミスを防ぎやすい。

## 関連: 参照渡しと値渡し

## 参考資料

- [JavaScriptの型は6種類だけど大きく分けた2種類を絶対に覚えておくべき（JavaScript おれおれ Advent Calendar 2011 – 20日目） | Ginpen.com](https://ginpen.com/2011/12/20/types/)
- 型クイズ（おととしの勉強会の内容）
    - https://kayac.slack.com/files/T02HZH8HZ/FLTG8DR25

## おわり