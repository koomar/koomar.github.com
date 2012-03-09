---
layout: post
title: "Multiple Github Accounts"
category: tutorials
tags: [github, ssh]
---
{% include JB/setup %}

## Rake Tasks

I try to use the [rake tasks] (https://gist.github.com/fa83a48a87c9a7a81f1c). A lot can be automated but I've just left it to this so far. Please feel free to contribute and suggest enhancements.
	
Now, use the tasks to add multiple ssh profiles in **~/.ssh/config**

	Host koomar.github.com
	  HostName github.com
	  User git
	  IdentityFile /Users/koomar/.ssh/id_github_koomar

	Host work.github.com
	  HostName github.com
	  User git
	  IdentityFile /Users/koomar/.ssh/id_github_work
	
## Usage
	
While cloning repositories, use the ssh URLs like this

	git clone git@koomar.github.com:koomar/koomar.github.com.git
	
	
Also, add the key to **ssh-agent** to avoid typing the passphrase.

	ssh-add ~/.ssh/id_github_koomar