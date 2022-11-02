---
published: true
---
## How I made my life easier, with the push of a button

Quick post for a neat little project I whipped up in no time today: a “get me my stuff” button thanks to a Amazon IoT button and Lambda functions, or serverless compute for the cool kids out there.

Let’s start with “The Internet of Things” -this is a very generic term to describe the modern day ability of wireless connectivity being applied to “things”. Refrigerators, toasters, cars, washer/dryers, alarm clocks, and even clicky-buttons that can order you Tide, amongst other things. Basically:

![1x9y37.jpg]({{site.baseurl}}/images/1x9y37.jpg)


Amazon made [IoT buttons](https://aws.amazon.com/iotbutton/) available in March of 2015, and one of my [coworkers](https://twitter.com/StevePantol) had waaaay too much fun with harassing another fellow [coworker](https://twitter.com/eric_shanks) via an IoT button and Slack integration. No really, the  [insult generator](http://stevedotnet.com/fun-with-the-aws-iot-button/) is probably one of my favorite hacked together pieces of “hilarity ensues” and made my first few weeks at Ahead even better.

Fast forward to now, where two years later we have an 18 month old who sleeps and eats like it’s his job (because, well, it is) and a wife who is tethered to this tiny one by duty and sustenance. Before we had a  beautiful red-haired viking child – she was a yoga instructor, studying to become a certified doula, full time farmer, amazing chef, had a social calendar like a church bingo card, voracious reader and world traveler with Yours Truly. Needless to say, she’s a busybody, and this phase of life doesn’t enable her to do much “busy” aside from when the baby naps. …unless by doing a thing it wakes the baby.

Why is this important? People forget things when they’ve been chasing a child all day long. Sometimes you forget where your phone is, and now your kid wants a nap and you’re stuck nursing him to sleep for an hour. Sometimes you forget where your book is, and same event happens. Maybe you don’t know where your glasses are… etc. Problematic when you're running on few hours of sleep, yes?

![aws_iot_button.png]({{site.baseurl}}/images/aws_iot_button.png)


“Do the thing, Internet of Thing(s) button!”

Essentially I took action to place an IoT button in our bedroom that’s accessible to her at all times. That way the most common of needs are tended to at the push of a button, and everyone is happy. Here’s how I did so:

1.  Not wanting to re-create the wheel, I followed [this blog](https://www.hackster.io/33996/the-i-miss-you-iot-button-b0112a) on how to register and setup an IoT button
2.  I modified their code to do what I wanted in a simple  fashion.
3.  I tested this code.
4.  It worked!

So what does the code look like?
```
'use strict';

const AWS = require('aws-sdk');
const SNS = new AWS.SNS({ apiVersion: '2010-03-31' });
const PHONE\_NUMBER = '1-555-876-5309'; // Your number goes here

exports.handler = (event, context, callback) => {
 
console.log('Received event:', event);
console.log(\`Sending SMS to ${PHONE\_NUMBER}\`);
 
 //uses randomizer to select one of the predefined messages
 var singleClick = 'Water Please!';
 var doubleClick = 'I lost my phone, help!';
 var longClick = 'ERROR-404: WIFE NOT FOUND';
 var randomMessage = singleClick;
 
 if(event.clickType == "DOUBLE"){
 randomMessage = doubleClick;
 };
 if(event.clickType == "LONG"){
 randomMessage = longClick;
 };
 
 const params = {
 PhoneNumber: PHONE\_NUMBER,
 Message: randomMessage,
 };
 // result will go to function callback
 SNS.publish(params, callback);
};
```
There’s nothing complicated behind doing this; even if you don’t know JavaScript, all you have to do is replace [Jenny’s phone number](https://youtu.be/6WTdTwcmxyo) above with your own, and then change the value of the strings after the vars “singleClick” “doubleClick” and “longClick” to whatever message you want.

Anything I can do to learn more and make my house a happy home – made this an easy vacation project!

Thanks for reading! vMikeB out
