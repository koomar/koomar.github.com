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
	/Users/abhijeet/.rvm/bin/textmate_ruby
	
	$ ls -l /Users/abhijeet/.rvm/bin/textmate_ruby	
	Users/abhijeet/.rvm/bin/textmate_ruby -> 
	/Users/abhijeet/.rvm/wrappers/ruby-1.9.2-p290@koomar/ruby
	
## Textmate Variable

Now, we need to point TM\_RUBY to 
	
	/Users/abhijeet/.rvm/bin/textmate_ruby
