+++
tags = ["Rails", "Rails5.0.2", ""] 
slug = "" 
date = "2017-04-11T11:41:31+09:00" 
title = "This is test" 
draft = true
+++

# Content-Disposition ヘッダーでファイル名の文字セットを指定して
+    # URLエンコードしたファイル名を指定した形に変換するモンキーパッチ。
+    # ※ RFC6266によってRFC5987の書き方にするべきとなってる&URLエンコードしておけばIE用に分岐する必要がない
+    #   "Content-Disposition attachment; filename*=UTF-8 (urlエンコードしたファイル名)"
+    # @see ActionController::DataStreaming.send_file_headers!
+    # @see https://tools.ietf.org/html/rfc6266#section-4.3
