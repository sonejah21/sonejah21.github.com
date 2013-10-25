---
layout: post
title: "Tried and True Testing the RSpec Way."
date: 2013-10-25
comments: true
categories: 
---

This week we powered through week 5 at Flatiron. Once petrified by the typhoon of fresh terms, further abstracted concepts and a growing number of triple-letter acronyms being added to my vocabulary - DSL, ORM, ERB, MVC, etc. - I am now fully embracing all things Ruby, SQL, and Sinatra. 
<br>

-><img src="/images/2013-10-25/rspec_blogpost_5.png" alt= "RSpec image" style="width: 400px;"/><-

Thinking I could forever hide from writing RSpec tests has been another story. In an effort to meet the sly nemesis head-on, I decided to dedicate this post to the testing language that has silently betrayed me and my native tongue with its seemingly lenient codes that are easily digestible and therefore impossible to remember.

<!-- more -->

My first homework assignment that dealt with RSpec was among the most frustrating because I had no idea I could look at the test results. Needless to say, I spent hours not passing any at all. If I recall correctly, I asked Avi for help the next day and mid-way through the exercise, we had this first conversation:
<br>

->![Initial RSpec conversation.](/images/2013-10-25/rspec_blogpost_1.jpg)<-

In the same way that I wrote about fanatically mimicking smart programmers like Sandi Metz (in my recent<a href="http://sonejah21.github.io/2013-10-11-mimic-metz-speak-matz">post</a>) one must mimic the pros of RSpec. The best way to start learning about RSpec testing is simply by copying and pasting a fool-proof test and changing out the values. Or as Avi recommended the first time we discussed RSpec...
<br>

->![On whether or not we need to memorize the RSpec syntax.](/images/2013-10-25/rspec_blogpost_2.jpg)<-

Backing up for a moment, let's make sure we understand that RSpec is a Domain Specific Language (or DSL) used to describe the expected behavior of a system with executable examples. Just like in the English language, we use terms like "should" and "do" to make sure our tests are intuitive to the program itself.

That said, here are a couple of the basic patterns to get used to seeing and understanding in RSpec:

    describe 'A Computer' do 
    end

=>  A Book

    describe Computer do
    end

=>  Book

    describe Computer, 'with new software' do
    end

=>  Book with new software
 
* Here, the ```describe Array do``` block in RSpec refers to the behavior of a Ruby class, this would be a ```class Array```. 

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

Instead of heading deeper into the syntax of RSpec - since you can always just copy and paste the syntax if you understand how it works - check out my new favorite cheat sheet <a href="http://www.anchor.com.au/wp-content/uploads/rspec_cheatsheet_attributed.pdf">here</a> (and below) in a blogpost by Barney Desmond of Anchor Managed Hosting, an Aussie company.

<br>

-><img src="/images/2013-10-25/rspec_blogpost_4.jpg" alt= "RSpec cheat sheet by Anchor" style="width: 600px;"/><-

<br>

Additionally, I couldn't help but include Gregg Pollack's <a href="http://blog.envylabs.com/post/29015255528/we-aint-got-no-rspec">"We Ain't Got No RSpec" </a>blogpost from a couple years ago. It's a voicemail left on the Envy Labs voicemail that they remixed.

-><img src="/images/2013-10-25/rspec_blogpost_6.jpg" alt="We Ain't Got No RSpec - Envy Labs." style="width: 400px;"/><-
