> **The goal of this guide:** Explain how you can enable automated services to communicate with Firebase

# Two types of automatic services communicate with Firebase

[CircleCi](https://circleci.com/) is a [continous integration](https://en.wikipedia.org/wiki/Continuous_integration) and [build automation](https://en.wikipedia.org/wiki/Build_automation) service that will run tests on your code. This ranges from checking whether running the script returns an error to running all custom tests of the script.

Bots listen to events and perform an action based on the type of event.
For example: we currently use a bot to push a message to slack when a client adds a message to a conversation on the interface

## Difference between CircleCi and other bots in communicating with Firebase
Usually bots use the Firebase secret. Go to the ```[your-database-name].firebaseio.com``` url of your database and go to secrets.

CircleCi needs a token, not a secret! A token is a string of 'random' letters and numbers that functions as a key to Firebase. You can only read and write to Firebase if you know the correct token.

### Generate a token for CircleCi:
In the folder of the repository you want to deploy there is a ```circle.yml``` file.
In it you will find the token name that CircleCi wįll use when deploying.
Remember the token name (e.g. ```FIREBASE_TOKEN_READY```) of the branch you want to deploy to e.g.:
```
--firebase repository-name --token $FIREBASE_TOKEN_READY
```


In your terminal:
- ```npm install -g firebase-tools```
- ```firebase login``` (this will open a browser window to Github)
- ```firebase prefs:token```
- receive a token.


Open your browser and go to the relevant repository in your [CircleCi](https://circleci.com/) account.
In the right-top corner you'll see milestone settings.
In Milestone settings you have environment variables.

Fill in the token name that is in your ```circly.yml```: e.g. ```FIREBASE_TOKEN_READY```
Fill in the token that you received in your terminal.
