## Clickbait or not?
### EECS 349: Machine Learning - Final Project

Charikleia Iakovidou, Northwestern University

e-mail: chariako [at] nu [dot] northwestern [dot] edu

The purpose of this project is to investigate whether it is possible to identify a “click-bait” article using ML techniques with only the article headline is an input. According to Oxford dictionaries, a click-bait is defined as “content whose main purpose is to attract attention and encourage visitors to click on alink to a particular web page”. However, there is still no absolute consensus on what a click-bait is and definitions are often subjective. Most people generally agree that click-bait headlines are eye-catching and promise a thrilling experience, while the actual content tends to be trivial or inaccurate. Legitimate news websites also employ sensationalist headlines from time to time and occasionally publish more light-hearted material. Do those articles qualify as click-baits or not? The answer is unclear.

In this project, a click-bait will be defined by its trivial content. Consider these headlines

"Photographer Captures Hilarious Moments Of Dogs Trying To Eat Peanut Butter” <br>
"Is This The Biggest Bovine In Australia? You'll Have To See It To Believe It!"<br>
“5 Celebrities You Didn't Know Had Dark Sides”

vs. these headlines:

"West African Leaders to Visit Gambia President Again Amid Crisis” <br>
"Exclusive: Airbus May Post 8 Percent Rise in 2016 Deliveries, Narrow Gap With Boeing"<br>
“Migrants Battle Freezing Temperatures and Cold Shoulder at Hungarian Border"

It is fairly easy to see that the first 3 articles do not contain important information, unlike the last 3 ones.

There are many reasons why filtering out click-baits could be useful, their poor quality content being the primary one. Some experts consider click-baits a threat to the future of journalism, as they decrease the profit of legitimate news sources and the revenue of professional journalists while shifting the focus away from actual news. Many are also concerned with the heavy advertising usually combined with click-baits and its effects on those exposed to it. The fact remains however, that click-baits are dishonest and commonly result in a waste of time; even when users willingly seek entertaining content, they often have to click on a substantial number of links to get it and the outcome usually does not live up to expectation.

The task at hand is a binary classification task, so the outputs belong in the set {0,1} characterizing non-click-bait and click-bait headlines respectively. The inputs are click-bait and news headlines represented using a Bag of Words model (TF-IDF).

This will be replaced with a figure someday:

![This will be replaced with a figure someday](http://scontent-sea1-1.cdninstagram.com/t51.2885-15/s480x480/e35/c9.0.1061.1061/13392900_836520003119649_764459364_n.jpg?ig_cache_key=MTI2NDkyNzQxMDY3ODk3MTgwNA%3D%3D.2.c)

[Download full report](https://www.youtube.com/watch?v=nSc5-RkndnQ)
