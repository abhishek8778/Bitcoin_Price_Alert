# Bitcoin Price Alert script


[PYTHON]

 To use IFTTT you’ll first need to set up a new account and install their mobile app (if you want to receive phone notifications from your Python app).
 
 
 To see the documentation on how to use the IFTTT webhooks go to <a href="https://ifttt.com/maker_webhooks">this page</a> and click on the “Documentation” button in the top right corner. The documentation page contains the webhook URL and it looks like this:

https://maker.ifttt.com/trigger/{event}/with/key/{your-IFTTT-key}


You’ll need to substitute the {event} part with whatever name you gave, when you created the applet. The {your-IFTTT-key} part is already populated with your IFTTT key.



[IMPORTANT]

An important thing is to avoid sending out requests too frequently, for two reasons:

-The Coinmarketcap API states that they update the data only once every 5 minutes, so there’s no point in reloading the latest pricing info more frequently than that.


-If your app sends too many requests to the Coinmarketcap API your IP might get banned or temporarily suspended.
That is why we need to “go to sleep” (stop the execution of the loop) for at least 5 minutes before we get new data. 
 
