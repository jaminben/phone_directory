#phone_directory

Twilio and Flask app for maintaining a database of users with their current phone numbers.


## details

This application exposes HTTP endpoints that make it possible for someone to ensure that their phone number is up to date in the database.

The flow looks like this:

1. Enter your id number
2. If your id number is correct: Enter your new phone number
3. Save phone number in the database
4. If your id number is incorrect, you can try again.

## Getting started

It can be quite confusing to get twillio up and running from scratch.  There are many tutorials to do this, but here is how we were the most successful.

1. Make sure you can run the flask app. (you will need a few basic python libraries to get started)
2. `pip install -r requirements.txt --use-mirrors` to install the required packages
3. `python run.py` to start your application on port 5000
4. Create a Twillio Account (http://www.twillio.com) you'll get a phone number from twillio, this will be important.
5. Download and install ngrok (https://www.twilio.com/blog/2013/10/test-your-webhooks-locally-with-ngrok.html) on OSX you can type `brew install ngrok`

6. Start ngrok and have it listen on port 5000 `ngrok 5000` you will get back a specific url like: http://6b405a6d.ngrok.com
7. Goto the Twillio Dashboard, click on "numbers", click on your twilio number, and for your voice url enter your ngrok server + /voice, i.e. http://6b405a6d.ngrok.com/voice

8. Now you should be able to call your twilio phone number and try things out!

(Note, this project was heavily based on: https://github.com/womensp2p/text-to-call-webapp so you might want to read more about this here.)

## TODO:

1. Get the basic app and menu working
2. update readme
3. add a real database backend
4. add more advance menu functionality
5. allow people to create accounts via phone, and receive SMS confirmation (this will require using the twillio Auth options)



