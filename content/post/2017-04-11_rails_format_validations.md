+++ 
tags = ["Rails", "Rails5.0.2", ""] 
slug = "" 
date = "2017-04-11T11:41:31+09:00"
title = "This is test"
draft = true
+++

 railsでは、numericality,とformatを同時にやると下記のように2つのメッセージがでて微妙です。
```
    [2] "ataiは数値で入力してください",
    [3] "ataiは半角数値のみで入力してください",
```
 なので formatのみのチェックにしようとしましたが、全角文字はキャストされて0に変換されてしまいます。
NumericalityValidator では `before_type_cast` の値に対してバリデーションをするのに対して、
FormatValidatorはキャスト後の値をバリデーションの対象とするので検知できない。。

https://github.com/rails/rails/blob/v5.0.2/activemodel/lib/active_model/validations/format.rb
https://github.com/rails/rails/blob/v5.0.2/activemodel/lib/active_model/validations/numericality.rb
