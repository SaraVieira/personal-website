---
title: 'Pimp Out them Logs'
date: '2017-10-30T22:12:03.284Z'
template: 'post'
slug: '/posts/pimp-out-them-logs/'
category: 'Javascript'
tags:
  - 'Javascript'
description: 'I use a lot of console based debugging a lot in my javascript coding on a daily basis and you may think: Nooob, use debugger ! But the…'
---

![](https://cdn-images-1.medium.com/max/800/1*HYkFuYWtiLtXAp23KZhTig.png)

Code: [https://jsbin.com/dukocabobe/10/edit?js,console](https://jsbin.com/dukocabobe/10/edit?js,console)

I use a lot of console based debugging a lot in my javascript coding on a daily basis and you may think: Nooob, use debugger !
But the thing is I got pretty damn good a console.logging my way to the top so today I’m gonna show some awesome stuff you can actually do with console that is not just console.log.

### Text Options

What you are most used to is just writing:

Well there is at least 3 more I currently use besides log, we have `error` , `warn` and `info`

---

![](https://cdn-images-1.medium.com/max/400/1*VExepHvEyuGnNtNzRHBLZw.png)

![](https://cdn-images-1.medium.com/max/400/1*Ck5yHIrwrhFYZiTPMis_SA.png)

![](https://cdn-images-1.medium.com/max/600/1*9mlzL7ZqnDaKpQO7YquBBA.png)

Browsers handle this different

This is very useful if you already have a lot of logs all over the place, also when doing an error you get a stack trace to know where that console comes from and what actually happened to get there.

### Timers

Ever wanted to run [https://jsperf.com/](https://jsperf.com/) without actually going to the website. This is exactly what timers do and you do it like so:

![](https://cdn-images-1.medium.com/max/800/1*-HVePTvgQOR64AxSU2iy6A.png)

How it looks on chrome

The way that this works is that the tag inside the time function must be the same as the one in timeEnd and what happens is that the browser will connect these two and give you just how long the code between took to run.

Pretty sweet ah ?

### Tables

So let’s imagine you have an object like this:

When you log it to the console you get something like this:

![](https://cdn-images-1.medium.com/max/800/1*0qFjfjQ9Wu-SW07aFuVeLw.png)

Not suuuuuper useful right ?

If only switch the log to table like this:

You get something way more awesome:

![](https://cdn-images-1.medium.com/max/800/1*l2gXxYXqulazd_E-LhbOkA.png)

Better, ah ?

### Groups

Another useful feature you have in your average console is the group one, this one allows to groups logs in the same group, so if have something like this:

I know this will never happen in real life but by doing this would just have all your logs shown like so:

![](https://cdn-images-1.medium.com/max/800/1*mCis5NhmyDQDolBg71uPkA.png)

logmess.png

With groups you encapsulate these logs into the part of the code they belong.
By adding some lines of code you get something way more organized:

![](https://cdn-images-1.medium.com/max/800/1*6QXoNqz2JtangJrCvWeUKg.png)

You can also collapse these groups by default for a cleaner view of what’s going on:

![](https://cdn-images-1.medium.com/max/800/1*bhjLNp8doOByJDNoW_PmDg.png)

### Count

Did you ever manually counted logs just to know how many times a function was called?
Turns out you don’t have to , there is a method called count on the console object that will do that for you.

Something like this:

Would give you:

![](https://cdn-images-1.medium.com/max/800/1*-VWk2KOajOIR-i5gVENUIg.png)

Waaaay fancier

### Last trick

You can also add css to your logs but only if the first argument is a string. To do this you need to prepend _%c_ to your text and then pass the css in the second argument, like so:

![](https://cdn-images-1.medium.com/max/800/1*5ePMOapD5kk94_F_4vg5-w.png)

I’m not saying this last one is very useful , but it’s certainly very cool.

That’s it folks! Have fun !

![](https://cdn-images-1.medium.com/max/800/1*kRJ3buv6d1vvGRI74Dw9RQ.gif)
