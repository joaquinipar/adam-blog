---
layout: post
title:  Basics of C
date:   2019-04-06 23:43:20 +0300
description: A humble introduction to this powerful programming language. # Add post description (optional)
img: list-methods-cover.jpg # Add image post (optional)
tags: [Blog, Programming]
author: Joaquin Ipar # Add name author (optional)
---

I want this post to be really straight forward. This is meant to be a memo. Hope it's useful.

## ¿How to print in C?


{% highlight c %}
#include <iostream>

main () {
	
	printf("Hello World");
}
{% endhighlight %}

## ¿How does C input/output data?

We're able to do it thanks to the standard input/output library `<stdio.h>`.

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
`i++` means that the increment will be +1. If we wanted a higher number, we could write `i= i + x` been x the increment that we want.

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

/* we are inputting a letter to a variable */
letter = getchar();
/* now lets print it */
putchar(letter);


{% endhighlight %}

## File Copying

Let's say we want to loop until an End of File is reached.
For that, C includes a special value, `EOF`. This value is unique, so it can't be confused with any real character.
EOF is an integer defined in `<stdio.h>`, so we cannot store it in a char, we're going to use int.

{% highlight c %}
main()
{
int c;
c = getchar();
while (c != EOF) {
putchar(c);
c = getchar();
}
}
{% endhighlight %}

If you try this in your compiler, entering the value `EOF` won't do the job. You must press `F6` or `Ctrl+Z`, that's how you enter `EOF` on Windows.

## Array

A really useful way to store more than a value in a variable.

{% highlight c %}
main(){
	int fourNumbers[3];

	fourNumbers[0]= 1
	fourNumbers[1]= 2
	fourNumbers[2]= 3
	fourNumbers[3]= 4

}

{% endhighlight %}

## Functions

We've been using built-in functions as `getchar()` , `putchar()`. It's time to make our own functions.

Functions have three parts: Prototype, Call and Declaration.

Prototype: Informs compiler about function name, functions parameters and what it's going to return. Prototype always must be written above the main function. Specifying the parameters names, are optional.

Call: Informs compiler we're going to use the function.

Declaration: Contains all the statements to be executed.

{% highlight c %}
#include <stdio.h>

int power (int, int) /* Prototype of power function */

main(){

printf( "%d", power(2,4) );  /* Calling and printing the function*/

}

/* Declaring the function */
int power(int base, int exponent)
{
	int result,i;
	result=1;
	
 	for (i=0 ; i < exponent ; i++){
 	
 	result = result*base;
 	
 	};
 	
 	return result;
 }

{% endhighlight %}

## Type Conversions

In general, if an operator like + or * that takes two operands (a binary operator) has operands of different types, the ''lower'' type is promoted to the ''higher'' type before the operation proceeds

For Example:
If we sum an int to a float, the int will be converted to a float.

Hopefully, C does this by itself and let us focus on more important problems.

## Increment and Decrement Operators

C includes two special operators `++` and `--`, they act as an adder and subtractor respectively. These operators can be used as prefix or postfix operators.

{% highlight c %}

int a,b,c;

c=12

while (a > b){

	b++; // Adds 1 to b.
	--c; // Subtracts 1 from c
}

{% endhighlight %}

## Conditional Expressions


The statements will compute the maximum between a and b. 

{% highlight c %}

int a=5;
int b=3;
int result;

if (a > b) {
	result = a;
}
else {
	result = b;
}

return result;
{% endhighlight %}

There's an alternative version for the if/else statement, the Ternary Operator `:?`

{% highlight c %}

result = a > b :? a : b ;

{% endhighlight %}

It's true that the traditional if/else statement will be more readable for people watching our code, but it's good to know about `:?` existence.



