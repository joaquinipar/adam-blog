---
layout: post
title:  Basics of C
date:   2019-04-06 23:43:20 +0300
description: A humble introduction to this powerful programming language. # Add post description (optional)
img: list-methods-cover.jpg # Add image post (optional)
tags: [Blog, Programming]
author: Joaquin Ipar # Add name author (optional)
---

I want this post to be really straight foward. This is meant to be a memo. Hope its useful.

## ¿How to print in C?


{% highlight c %}
#include <iostream>

main () {
	
	printf("Hello World");
}
{% endhighlight %}

## ¿How to input/output data?

We use the standard input/output library

{% highlight c %}
#include <stdio.h>

{% endhighlight %}

## Types of Data

| int | Integer|
| float | Floating Number (10^-38 and 10^38.)|
| char | a character - a single byte|
| short | short integer |
|long | long integer|
|double | double-precision floating point|

## Ways to print a floating point

|%d |print as decimal integer|
|%6d |print as decimal integer, at least 6 characters wide|
|%f| print as floating point|
|%6f |print as floating point, at least 6 characters wide|
|%.2f| print as floating point, 2 characters after decimal point|
|%6.2f| print as floating point, at least 6 wide and 2 after decimal point|

	example : 

	{% highlight c %}
	while (fahr <= upper) {
	celsius = (5.0/9.0) * (fahr-32.0);
	printf("%3.0f %6.1f\n", fahr, celsius);
	fahr = fahr + step;
	{% endhighlight %}

## The for statement

{% highlight c %}
x=0
for (i=0 ; i<=100 ; i++){
	x++;
	printf(x);
}
{% endhighlight %}

`i=0` represents the start of the loop. 
`i<=100` means that i won't go higher than 100.
`i++` means that the increment will be +1. I we wanted a higher number, we could write `i= i + x` been x the increment that we want.

## While loop

{% highlight c %}
x=0
while ( i<=100 ) {
	
	x++;
	printf(x);

}
{% endhighlight %}

`i<=100` will be the condition of the while loop. The code will be repeating if the condition returns `True`. If the condition returns `False`, the loop will stop iterating.

## Symbolic Constants

If we wanted to assign a number (for example) to a variable that won't change in the future, its a better idea to `define` it beforehand.

{% highlight c %}
#include <iostream>

#define MINIMUMAGE 18 /* minimum age to enter to a pub * /

#define YEAR 365 /* number of days in a year * /

{% endhighlight %}

## Character Input and Output

To input and print a single character (char) we are provided with getchar and putchar functions.

`getchar` allows us to receive a char from the user.

`putchar` prints the character.

{% highlight c %}

/* here we are inputing a letter to a variable * /
letter = getchar();
/* now let's print it * /
putchar(letter);


{% endhighlight %}

## File Copying



