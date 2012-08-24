---
layout: post
title: "Mixpanel in Jekyll Bootstrap"
category: 
tags: [github, analytics]
---
{% include JB/setup %}


## Mixpanel Analytics Support

Mixpanel analytics support is added to [Jekyll Bootstrap](https://github.com/plusjade/jekyll-bootstrap) with my [commit](https://github.com/plusjade/jekyll-bootstrap/pull/49)

Usage is dead simple 

	analytics :
	  provider : mixpanel 
	  mixpanel :
	      token : 'YOUR_MIXPANEL_TOKEN_HERE'
	
	
If you want analytics to work on your local system, you want to use

	jekyll --safe
	
The configuration variable <code> safe:true </code> is automatically enabled when hosted on github!
	
	