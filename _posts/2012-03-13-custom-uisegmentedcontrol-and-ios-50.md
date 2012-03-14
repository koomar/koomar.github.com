---
layout: post
title: "Custom UISegmentedControl and iOS 5.0"
category: tutorials
tags: [iOS, programming]
---
{% include JB/setup %}

I wanted to create an experience exactly similar to UISegmentedControl but with
custom images

	[segmentedControl insertSegmentWithImage:[UIImage imageNamed:@"image.png"] 
	                                 atIndex:0 
                                    animated:NO];

Before iOS 5.1, I got away using *(not an ideal solution)*

	segmentedControl.tintColor = RGBCOLOR(99, 77, 58); //Divider color
	segmentedControl.segmentedControlStyle = UISegmentedControlStyleBezeled;
	

but, after updating to 5.1 OS, I started seeing some blue tint style de-coloration. 

![De-coloration](/assets/images/segment-decolor.png "Blue de-colorations")

Following API which is new to iOS 5.0 fixed it!


	if ([segmentedControl 
		respondsToSelector:@selector(setDividerImage:forLeftSegmentState:
			                       rightSegmentState:barMetrics:)]) {
	    [segmentedControl setDividerImage:[UIImage imageNamed:@"segmentDivider.png"]
                      forLeftSegmentState:UIControlStateNormal 
                        rightSegmentState:UIControlStateNormal 
                               barMetrics:UIBarMetricsDefault];
	}


Following is still required for iOS 4.3

	segmentedControl.segmentedControlStyle = UISegmentedControlStyleBezeled;


![Fixed with Divider Image](/assets/images/segment-color.png)
