---
layout: post
title: ⏲ OTP Bingo Game Time
tags: python numpy
---

I introduced OTP bingo where I work, but I hadn't considered how long it would take with numbers in the range 0-999. Luckily NumPy is very good at playing bingo, so I ran a few games to see how long it would take. You can see the code [here](https://gist.github.com/fred-cook/895ab413fe66c51d04381547d9c62c4d)

![A histogram showing the number of bingo successes at any given turn](/images/otp-bingo/winning_time.png)

It's going to be a while, 869 turns for the median player, but someone might get lucky. Out of 100000 games of OTP bingo the fastest winner was just 34 turns. However, the unluckiest player took 3384 goes. Note this is with a **FREE** cell in the middle of the card. The median number of logins to bingo without the **FREE** cell goes up to 907.

I was also interested to see how long OTP bingo takes if you only use 2 two digits, and how it varies with card size.

![A plot showing how the time to bingo changes as the size of the bingo card changes](/images/otp-bingo/time_2_bingo.png)
