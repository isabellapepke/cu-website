---
title: Why, About the Tech
date: 2019-03-21 21:48:52
tags:
---
There is a lot of awesome stuff you can build with site generators and Hexo specifically.

## Templates

This demo uses [ejs](https://ejs.co/) which is a templating language that lets you 
use normal JavaScript to make make HTML. This also makes making the website easy 
because you only need to know one programming language!

For example: 

{% codeblock %}
<p class="h1 mb-3">
    <%- page.title %>
</p>
{% endcodeblock %}

Outputs:

{% codeblock %}
<p class="h1 mb-3">
    Why, About the Tech
</p>
{% endcodeblock %}

So we don&apos;t have to manually add the title to each blog post, everywhere it is needed. 

There are a lot of other cool ways templates help us, like [partials](https://hexo.io/docs/templates.html#Partials), [helpers](https://hexo.io/docs/helpers.html), and more!

## SASS

[Sass](https://sass-lang.com/) also lets us write CSS more efficiently, by providing additional syntax that 
compiles to pure CSS.

For example: 

{% codeblock %}
$grey: #626262;


.date {
  color: $grey;
  margin-bottom: 0;
} 
{% endcodeblock %}

Allows use to use variables, ie $grey, which results in:

{% codeblock %}
.date {
  color: #626262;
  margin-bottom: 0; 
}
{% endcodeblock %}

## Markdown

[Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is a simple, but powerful way to change a document&apos;s visuals.
This post for example is written in Markdown, mostly. 

New posts can be created with: 

`hexo new post --title [your title here]`

Then it&apos;s automatically added as a page to the website and is available on the homepage!
**Awesome** : )

## Extensions

There are a lot potential using Hexo, due to their large number of [plugins](https://hexo.io/plugins/index.html).

Since this project is also built with [Node.js](https://nodejs.org/en/) anything from it&apos;s ecosystem can be used. 