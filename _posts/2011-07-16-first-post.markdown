---
layout: default
title:  Time to learn Assembly Language
tags:
- Language
- Assembly  
---

In the past I found it extremely hard to find my way within assembly language. Lately, I stumbled upon a course on compiler which is and area I have'
been longing to study. While going through the course material... I immediately found that I need to have some assembly in order to get through with the course. Being infinitely lazy, I decided to abandon the course and move on. However, I along the way I checked out System programming course.Hmm, I met Assembly again. Finally, I just decided to check it out. 
I was amazed by what when I found that when it comes to characters/string manipulation that Assembly used the natural means. That means that I need not worry
myself too much. I was able to create C's equivalent of strcpy , title case , and other funny stuff. I enjoyed Assembly so much that I devoted time learning it. 

{% highlight gas %}
movl $0, %eax
xol %eax, %eax
{% endhighlight %}

Started making sense.. I enjoyed the way stack is manipulated in Assembly language. It is pure Turing.... And above all you don't need to memorize alot here. Just remember base pointer and stack pointer and know when to create extra memory space and when to tank space.Don't ask me why I am using immediate mode addressing and 4. Okay, just to help you out a bit, I am using long, so everything would be 4 bytes. Is that clear? Or Its multiple. And if you use indirect addressing mode here, where that meaning you are not creating extra space or tanking it.... but giving address to the stack point
{% highlight gas %}
subl $4, %esp
addl $4, %esp
{% endhighlight %}
When I started seeing things like. I know you may be asking okay how do I define constants. You may use just symbols, like the following.
{% highlight gas %}
.equ HIGHT, 200
joots:
 .asciz , "AssemblyWay"
{% endhighlight %}

And Assembly comes with a lot of basic stuffs that are repeated everywhere... All you need is to remember them and you are done. When you want to make function call, this is very important because you will use stack to hold your parameters, so you push from right to left.
{% highlight gas %}
pushl %ebp
movl %esp , %ebp
{% endhighlight %}
Or 
{% highlight gas %}
movl %ebp, %esp
popl %ebp
ret
{% endhighlight %}
I felt at home...  But never forget indirect addressing more. This is going to save your life some day. It is pretty easy to itched in your memory.
{% highlight gas %}
pointer(reg,ind_reg,byte_number)
{% endhighlight %}

This will be the best blog ever Good.Above all, you may choose to study AT&T or Intel notations, it does not matter. The import thing is that you are able to create something of your own. when indexing ... remember to use destination pointer and source pointer. I would advice you attempt to port some of your C codes to Assembly and see for yourself how Assembly feels. And don't forget to join Assembly mailing list out there. You will gain a lot by hanging out there and asking questions. 

