---
title: "Automate Crypto Portfolio Using Google Sheets"
date: 2017-12-07T12:45:53-08:00
draft: true
---

Today I will show you how to create a makeshift Google Sheet in order to pull pricing and totals for your portfolio in your favourite currencies.

First, browse to ```sheets.google.com```

Then, name your sheet and save it. 

Now, to fill out the sheet. Make sure the very first row of your sheet just has labels and fiat currencies you want to get rates for. For example, my first row has labels:  Coins, Qty, USD, CAD, JPY. See the image below.




{{< figure src="/crypto-sheet/cryptosheet1.jpg" title="crypto sheet example" >}}



Now under the "Coins" column, fill out all your coins in full name, not symbols. For example: ethereum, iota, request-network. Under the quantities, fill out the corresponding quantities you hold for each crypto.

Setup the script.

Click on Tools, Script Editor...  It should create a new file called code.gs and show code like below:

<pre>
  function myFunction() {
  
  }
</pre>

Delete everything in there and copy and paste the following:

{{<gist johnny-coin fc5769e9fbbf5bdd880289733220e589>}}

At the top of this file you should see comments about entering your initial investment currency and amount. Currently it is "USD" and 0. You can replace it with your currency that you invested with, and your investment amount. This will allow the script to calculate profits for you in all the currencies you requested.

Now run the script by hitting the button that looks like "play" button. Make sure the function myFunction is selected first. See the image below.

{{< figure src="/crypto-sheet/script1.jpg" title="crypto script example" >}}

This will prompt google to give you a warning since this seems like an untrusted script asking for permission to your Google account. Click "advance" and then type in "Continue" as it prompts you to. This will finally run the script on your sheet and do all the calculations.

Flip back over to your script to see the results. Now you can always load up this script, click Tools, Script Editor, and run the script to look at fresh prices and rising profits!

Thanks for reading!

If you are interested in new tools or updates from me, feel free to leave your email below:

<form action="https://formspree.io/jccryptoblogger@gmail.com"
      method="POST">
      <!-- honeypot field which will cause formspree to throw away this response if filled. -->
    <input type="text" name="_gotcha" style="display:none" />
    <input type="email" placeholder="your@email.com" name="_replyto">
    <input type="submit" value="Send">
</form> 