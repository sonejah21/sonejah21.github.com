---
layout: post
title: "Winning Arguments."
date: 2013-10-11 
comments: true
categories: 
---

Parentheses are a subtle to include information in literature. They group numbers together in math equations, trail behind long organization titles in news reports, and even distinguish between an area code and a person's unique telephone number. 

When we switch gears into Ruby, parentheses are no longer representative of a polite nudge like they once were to us. Sitting alongside a method, they're now considered powerful argumentation.

<!-- more -->

![Required arguments.](/images/2013-10-11/image-1.jpg)

In a blogpost written by a [Alan Skorkin](http://www.skorks.com/2009/08/method-arguments-in-ruby/), he says that contrary to popular belief, a method argument should be broken up into three separate, and easily digestible categories: 

## Required arguments (aka: "Ordinal Params")


Required arguments are your run-of-the-mill arguments. Nothing left to the imagination, require arguments are straightforward in their approach to gathering information from other sources. 

    def method_example( x, y )
    end 

Once you have defined your method, you will always need to provide the same number of arguments when calling the method. 

    method_example( 2013, "Flatiron School" ) 

![Arguments with Default Values.](/images/2013-10-11/image-4.jpg)

## Arguments with Default Values** (aka: "Params with Default Values")

Instead of assigning a specific number of arguments, you may also assign assigning a default value to an argument.

    def horse_method( x, y, z = "appaloosa" )
    end

You can then call this method in one of two ways:

    horse_method( 2, "shire" )

 *- OR -*

    horse_method( 41,  "shire",  2013 )


The first example (above) calls the method without placing a value as its third parameter, resulting in the default value filled in as its third parameter. The second example has three parameters set and does not need to use the default value.

![Optional Arguments.](/images/2013-10-11/image-2.jpg)

## Optional arguments (aka: "Arguments as an Array")

This is a special method argument that Ruby allows you to use that many refer to as "splat". 

To see an excellent blogpost describing splat's usage in more depth, check out [Manuel Neuhauser](http://manu3569.github.io/blog/2013/10/08/what-the-splat/)'s blog on the topic.

At a basic level, the optional argument allows you to decide at runtime how many arguments you'll supply to a method:

    def caffe_method( *italian_favorites )
    end

Which could be called with: 

    caffe_method( "cappuccino", "espresso", "macchiato" )

You can then call it with any number of arguments, or no methods at all, resulting in an array with the exact number of arguments specified (or none at all if no arguments were defined).

![Arguments that combine a bit of everything.](/images/2013-10-11/image-3.jpg)

### Combinations

In addition to the three general uses of method arguments in Ruby, all of them can be mixed and matched together, creating a unique assortment of required, default values, and optional arguments. 

For example:

    def combination_method( a,  b,  c = 5, *d , e)
    end

If called with:

    combination_method( 21, 31, 11 )

It would result in:

    a = 21, b = 31, c = 5, d=[], e = 11

Since each required value gets an assigned value, the default value kicks in with its default, and the optional, or splat(*) argument would return an empty array. 

While method arguments are seemingly basic at first glance, understanding the way they work by themselves, with default values and optional parameters, as well in unison while all hanging out in the same set of parentheses is an integral stepping stone to making your beginner Ruby methods function properly. 

Happy arguments!