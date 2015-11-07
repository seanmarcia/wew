---
layout: post
title: Using NPM as a build system
category: posts
draft: true
---
When we started building [Repcoin](http://repcoin.com), [Matt](www.mattritter.me) and I were relatively inexperienced with [Node](https://nodejs.org/) and [React](https://facebook.github.io/react/). We didn't have experience setting up and maintaining build systems for large Javascript projects. [Gulp]() and [Grunt]() are standard in the industry, so we decided to go with Gulp, since it seemed newer and flashier.

Before I go on, I want to make a disclaimer: *I'm not a Gulp expert and will only discuss it in this article to the extent to which it illustrates why we switched to NPM as our build system.*

Unfortunately, our inexperience led us to struggle with Gulp. Gulp uses streams as its unifying abstraction and we found this difficult to understand and work with. We just wanted to get our frontend and backend up and running as quickly as possible. Although we finally got the project up and running with Gulp, we quickly ran into more problems, primarily due to our lack of understanding of the Gulp framework. In addition, we couldn't find Gulp-compatible plugins for certain modules.

As the primary manager of our build system, I eventually decided to seek out an alternative to Gulp. We thought about using Grunt, but the prospect of translating our now sizeable Gulpfile into a Gruntfile was off-putting to say the least. So, I sought out alternatives and found [this blog post](http://blog.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/).

Since finding this blog post, we've learned a ton. I intend to detail what we've learned in this post.

# Running the Site
