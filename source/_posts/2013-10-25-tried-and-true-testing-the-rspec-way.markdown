---
layout: post
title: "Tried and True Testing the RSpec Way."
date: 2013-10-25
comments: true
categories: 
---

This week we powered through week 5 at Flatiron. Once petrified by the typhoon of fresh terms, further abstracted concepts and a growing number of triple-letter acronyms being added to my vocabulary, I am now fully embracing all things Ruby, SQL, and Sinatra. 
<br>

-><img src="/images/2013-10-25/rspec_blogpost_5.png" alt= "RSpec image" style="width: 400px;"/><-

<!-- more -->

Thinking I could forever hide from writing RSpec tests has been another story. In an effort to meet my nemesis head-on, I decided to dedicate this post to the RSpec testing conventions that have silently betrayed my native language (English) with its seemingly lenient codes that are easily digestible and therefore impossible to remember.

Sidenote: Check out Gregg Pollack's <a href="http://blog.envylabs.com/post/29015255528/we-aint-got-no-rspec">"We Ain't Got No RSpec" </a>blogpost from a couple years ago. It's a voicemail left on the Envy Labs voicemail that they remixed, and it will definitely get you in the mood to write some RSpec.

-><a href="http://blog.envylabs.com/post/29015255528/we-aint-got-no-rspec"><img src="/images/2013-10-25/rspec_blogpost_6.jpg" alt="We Ain't Got No RSpec - Envy Labs." style="width: 400px;"/></a><-

My first homework assignment that dealt with RSpec was among the most frustrating because I had no idea I could look at the test results. Needless to say, I spent hours not passing any at all. If I recall correctly, I asked Avi for help the next day and mid-way through the exercise, we had this first conversation:
<br>

->![Initial RSpec conversation.](/images/2013-10-25/rspec_blogpost_1.jpg)<-

In the same way that I wrote about fanatically mimicking smart programmers like Sandi Metz (in my recent<a href="http://sonejah21.github.io/2013-10-11-mimic-metz-speak-matz">post</a>) one must mimic the pros of RSpec. The best way to start learning about RSpec testing is simply by copying and pasting a fool-proof test and changing out the values. Or as Avi recommended the first time we discussed RSpec...
<br>

Backing up for a moment, let's make sure we understand that RSpec is a Domain Specific Language (or DSL) used to describe the expected behavior of a system with executable examples. Just like in the English language, we use terms like "should" and "do" to make sure our tests are intuitive to the program itself.

That said, here are a couple of the basic patterns to get used to seeing and understanding in RSpec:

    describe 'A Computer' do 
    end

=>  A Computer

    describe Computer do
    end

=>  Computer

    describe Computer, 'with new software' do
    end

=>  Computer with new software
 
* Here, the ```describe Array do``` block in RSpec refers to the behavior of a Ruby class, this would be a ```class Array```. You can tell because the word "Array" it is capitalized, and thus, RSpec is hinting to the programmer what it is looking for. 

-------------

    describe Array do
      it "should return a blank instance" do
        Array.new.should == []
      end
    end

* The ```it``` block + ```string``` as first argument gives you the opportunity to write a detailed, specific expectation of the behavior using ```"should"``` and ```do```. 

-------------

* ```assert_xxx```in Ruby == ```object.should_be xxx``` in RSpec.

-------------

* ```def test_shout``` in Ruby == ```It 'should shout'``` in RSpec.

--------------

* ```def setup``` in Ruby == ```before(:each) {}``` in RSpec.

--------------

Instead of heading deeper into the syntax of RSpec - since you can always just copy and paste the syntax if you understand how it works - check out my new favorite cheat sheet <a href="http://www.anchor.com.au/wp-content/uploads/rspec_cheatsheet_attributed.pdf">here</a> (and below) in a blogpost by Barney Desmond of Anchor Managed Hosting. There are actually two sides to it (but only one is shown). They recommend printing it out as a reference guide to RSpec if you're just starting to run test suites.

<br>

-><img src="/images/2013-10-25/rspec_blogpost_4.jpg" alt= "RSpec cheat sheet by Anchor" style="width: 600px;"/><-


