---
layout: post
title:      "CLI Data Gem Project"
date:       2017-10-09 01:18:03 +0000
permalink:  cli_data_gem_project
---

![Imgur](https://i.imgur.com/dPaAslQ.png)

## The Challenge
For my first portfolio project, I was challenged to program a CLI application with good object oriented code. I had to scrape a website and write a program that would offer a list of available data and information about that data that went at least one level deep. Sounds easy, right? Wrong. The task was actually quite daunting for a beginner like me.

All of our previous lessons and labs offered pretty direct instructions on what we were supposed to do. Now that I was on my own, I started to panic. Which website would I choose? What kind of methods should I write? Do I really even know how to code?? Fortunately, my senses came back to me after a few minutes (or hours) of freaking out.

I remembered that I had spent weeks preparing for this very moment. All the information I had absorbed from the lessons, labs, and lectures before was still there in my brain. I just needed to fish it out.

## Getting Started
I was given a few requirements to meet:

1. Provide a CLI
2. CLI must provide access to data from a web page.
3. The data provided must go at least one level deep, generally by showing the user a list of available data and then being able to drill down into a specific item.
4. The CLI application can not be a Music CLI application as that is too similiar to the other OO Ruby final project. Also please refrain from using Kickstarter as that was used for the scraping 'code along'.
5. Use good OO design patterns. You should be creating a collection of objects - not hashes.

There were also bonus points up for grab if I could create and publish a gem to [RubyGems](https://rubygems.org/).

After contemplating for some time, I decided on programming a science news reader. I quickly browsed my way over to the [Science](http://www.sciencemag.org/) website in order to check it out. Bingo! It was perfect. The latest news was laid out in a nice order, and each story was contained within a list element that could easily be scraped. Now, I just had to figure out how to make a gem.

There were a number of resources provided to help me get started. Among them was this [walkthrough video](https://www.youtube.com/watch?v=_lDExWIhYKI) filmed by Avi. Admittedly, I had to start over a couple of times before getting everything in order, but I ended up successfully creating my first Ruby gem! Awesome.

## Development
I began by creating two classes called CLI and Story. The CLI class would be responsible for greeting the user, listing the stories available to read, and providing menu options. I decided to include the scraper methods in my Story class rather than creating a separate class for scraping. This was because my scraper methods were rather small, and the class itself didn't contain much else.

![Imgur](https://i.imgur.com/RaRZfDq.png)

The code quickly came together thanks to my earlier method stubs. If you don't know what method stubs are, they're basically little pieces of code that act as a placeholder for later functionality. For example, instead of the functional code written in the list method pictured above, I originally had something like:

```
puts "Bees!"
puts "Volcano Story"
puts "Why Science Rocks"
```

After writing all the necessary code, I was finally ready to publish my gem. 

## Publishing the Gem
Publishing my gem to RubyGems was super easy. Bundler created a rakefile when I made my gem so all I had to do was run 'rake install'. This allowed me to make sure everything was in working order before actually releasing my gem into the wild. When I was satisfied with the program, I used 'rake release' to publish.

You can check it out [here](https://rubygems.org/gems/sciencemag_latest_news).

I'm planning on refactoring the code and adding more functionality soon. Stay tuned!
