---
layout: post
title: "Xcode: codesign : User interaction is not allowed"
category: 
tags: [xcodebuild, codesign, iOS]
---
{% include JB/setup %}

When you run into the error : "codesign: User interaction is not allowed", try the following
command to get by.

	sudo security unlock-keychain /Users/koomar/Library/Keychains/login.keychain
