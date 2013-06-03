Getting Started Registering an Application with Twitter
=======================================================
This Getting Started guide will walk you through the steps of registering an application to integrate with Twitter.

The steps in this guide will all be performed in your web browser on Twitter.com. Although we'll not be writing any code in the course of this guide, we have provided a simple utility project you can use to verify that you performed the steps correctly. Instructions for getting and running the utility will be at the end of this guide.

Registering a New Application
-----------------------------
All Twitter users are potentially Twitter application developers. All you must do is visit http://dev.twitter.com and sign in using your Twitter credentials.

From http://dev.twitter.com, find your avatar in the upper-right corner and move your mouse over it. When you do, you'll see a menu that includes (among other things) "My applications". When you select "My applications", you'll be taken to a page that lists all of your Twitter applications. Since you haven't created any applications yet, the list will be empty. 

No problem. Click the ![](images/tw-new-app-button.png) button near the top. This will navigate to a new page with the _Create an application_ form. The first portion of this form asks for some basic information about your application.

![](images/tw-app-details.png)

In the _Name_ field, you can name your application. This name will be presented to users when they are prompted to authorize your application to access their Twitter information. Almost anything goes here, but it must fit within 32 characters.

The _Description_ field is where you can briefly (in 10 to 200 characters) describe your application. Again, this will be presented to users on authorization screens.

In the _Website_ field, you should give a URL that points the user back to your application. This is where they can download or find out more information about your application. As with _Name_ and _Description_, this will be presented on user-facing authorization screens.

The _Callback URL_ field is where you specify the URL that Twitter should redirect to after a successful authorization. It is best to leave this field blank and to explicitly specify the callback URL at authorization time.

Next up on the _Create an application_ form are the _Developer Rules Of The Road_. 

![](images/tw-rules-of-road.png)

These are the rules you must agree to if you are building an application that uses Twitter's API. These rules include guidelines on how to stylistically present tweets and how you shouldn't simply recreate the functionality of Twitter's own clients. We recommend that you read these rules closely to make sure you aren't violating any of them.

If you agree to the rules, simply indicate so by checking the "Yes, I agree" checkbox.

Finally, you are faced with a Captcha challenge to ensure that you're not setting up applications through some automated process.

![](images/tw-captcha.png)

Once you've satisfied the Captcha verification, click the "Create your Twitter application" button to complete the form. The next page you see will be your application's application settings page.
 
![](images/tw-app-details.png)

From the application settings page, you can configure various details about your application. The choices you make here depend largely upon what kind of application you plan to build and what you want your application to do. 

The main thing to note from the application settings page is the __Consumer key__ and __Consumer Secret__. This pair of values serves as your application's credentials to Twitter. You'll need these to do almost anything with Twitter, including going through the OAuth authorization flow and working with Twitter's REST API.

Verifying the Registration
--------------------------
One way you can use your newly registered application's Consumer ID and Consumer Secret is to use them in an application that retrieves information about itself. The sample utility application in GitHub fetches information about a registered application and displays it on the console.

You can clone the utility project from GitHub:

```sh
$ git clone https://github.com/springframework-meta/gs-register-twitter-app.git
```

To run the utility, simply run it from the command line like this:

```sh
$ gradlew run
```

You'll be prompted by two dialogs. The first will ask for the application's Consumer ID and the second will ask for the application's Consumer Secret. You can copy-n-paste those from the Twitter Developer's site.

After supplying the Consumer ID and Consumer Secret, the application will query Twitter's REST API, searching for Tweets that have "#springframework" in the text. If you've set your application up correctly, you should see the text of several matching Tweets.

Next Steps
----------
Congratulations! You have now registered an application with Twitter.

This is merely the first step in developing an application that is integrated into its users' social graph. For more information on what your Twitter-enabled application can do, we recommend that you have a look at the following Getting Started guides:

* Obtaining user authorization from Twitter
* Authenticating a user with Twitter
* Retrieving user data from Twitter
* Registering an application with Facebook

