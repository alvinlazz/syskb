# SysAdmin | Help Center
Simple and responsive Jekyll theme for help center.

# Demo
[Demo online](https://alvinlaz96.github.io/syskb/)

# Color theme
edit in _config.yml
```
color_theme:  "#0081ff"
color_text:  "#fff"
```

# Install
```
git clone https://github.com/alvinlaz96/syskb
```
or
```
gem install syskb
```
https://rubygems.org/gems/jekyll-help-center-theme

# How to use
```
bundle exec jekyll serve --livereload --watch
```
Server address
```
localhost:4000/syskb/
```

# Post Example
```
---
layout: post
title: 'First category'
description: 'Sample Description'
date: 2017-11-12 17:46:41 -0300
categories: start blog
by: 'SysAdmin'
icon: 'credit-card'
questions:
  - question: 'Question 1'
    answer: 'Test1'
    image: "1.gif"
  - question: 'Question 2'
    answer: 'Test2'
    image: "2.gif"
  - question: 'Question 3'
    answer: 'Test3'
    image: "3.gif"
  - question: 'Question 4'
    answer: 'Test4'
    image: "4.gif"
---
```
## License
The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

# Inspired And Forked
- https://gustavoquinalha.github.io/jekyll-help-center-theme/
