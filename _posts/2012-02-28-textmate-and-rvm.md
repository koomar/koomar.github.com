---
layout: post
title: "Textmate and RVM"
category: tutorials
tags: [textmate, rvm]
---
{% include JB/setup %}

## RVM Wrapper

	$ rvm wrapper [ruby_string] [wrapper_prefix]
	
For example,

	$ rvm wrapper ruby-1.9.2-p290@koomar textmate

	$ which textmate_ruby
	/Users/koomar/.rvm/bin/textmate_ruby
	
	$ ls -l /Users/koomar/.rvm/bin/textmate_ruby	
	Users/koomar/.rvm/bin/textmate_ruby -> 
	/Users/koomar/.rvm/wrappers/ruby-1.9.2-p290@koomar/ruby
	
## Textmate Variable

Now, we need to point TM\_RUBY to 
	
	/Users/koomar/.rvm/bin/textmate_ruby
