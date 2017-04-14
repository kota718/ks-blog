+++ 
tags = ["RSpec", "RuboCop", "rubocop-rspec", "rspec3.5.2", "rubocop0.42.0", "rubocop-rspec1.5.2"] 
slug = "" 
date = "2017-04-11T11:41:31+09:00" 
title = "RuboCop（RSpec/DescribedClass）に怒られずにConcen moduleをテストする方法" 
draft = true 
+++

```diff
- let(:klass) { Class.new { include described_class } }	
+ let(:klass) { Class.new.tap { |klass| klass.include described_class } }
```
