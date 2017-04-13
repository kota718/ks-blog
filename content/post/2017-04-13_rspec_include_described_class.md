+++ 
tags = ["RSpec", "RSpec3.5.2"] 
slug = "" 
date = "2017-04-11T11:41:31+09:00" 
title = "This is test" 
draft = true 
+++

```diff
- let(:klass) { Class.new { include described_class } }	
+ let(:klass) { Class.new.tap { |klass| klass.include described_class } }
```
