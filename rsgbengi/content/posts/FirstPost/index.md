---
title: "Python tips and tricks"
date: 2021-08-31T12:10:00+02:00
draft: false
categories: [python]
tags: [tips and tricks]

cover:
    image: /posts/firstpost/images/lema.png # image path/url
    relative: true # when using page bundles set this to true
---
---
# Getting started
This post will contain many interesting tips and tricks that i have learned these last months and i  personally use constantly. 
So let's get started :).
## One liners
If you are familiar with python, you will know that the 
language has many powerful **one liners expressions**. For that reason, i will show you some of them. 
### List Comprehensions
The first one is probably my favorite, because it allows you to  manipulate lists in a really cool way.  
For example, instead of doing it that way, which is how almost everyone does it:
```python
list = []
for i in range(10):
    list.append(i)
```
You can do something more elegant like this one:
```python
list = [i for i in range(10)]
```
Moreover, you can use the **if/else statement** to, for example, create a list with only even numbers:
```python
list = [i for i in range(10) if i % 2 == 0]
```
### Use of join with list comprehension
Related with **list comprehensions**, you can use the function **jon** to join all elements on a list into a **string**. 
Continuing the previous example: 
```python
numbers_to_str = ",".join([str(i) for i in list if i % 2 == 0])
``` 
The result of this one will be:
*'0,2,4,6,8'*







---
