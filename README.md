# mauton-deployment :cat:

## Purpose
Describe the procedures of deployment to Heruko.

## Prerequisites 📋
You'll need:
* [mauton-api](https://github.com/ikhvjs/mauton-api) 
* [Git](https://git-scm.com) 
* [NPM](http://npmjs.com)
* [Google reCAPTCHA v3](https://developers.google.com/recaptcha/docs/v3) (which you need to register for a key)
* [Heroku](https://heroku.com) (which is for the platform to launch your website)

## Deployment 📦

### Step 1 - Create Heroku Account

Create a account in Heroku

### Step 2 - Install Heroku CLI

please install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

### Step 3 - Create Heroku App using Heroku CLI

```bash
# create a Heroku App
$ heroku create $YOUR_APP_NAME
# check git remote 
$ git remote -v
#you should see something like below
heroku  https://git.heroku.com/$YOUR_APP_NAME.git (fetch)
heroku  https://git.heroku.com/$YOUR_APP_NAME.git (push)
```

### Step 4 - Change your Google reCAPTCHA v3 public Key in ```src/constants.js```
```js
export const RECAPTCHAT_KEY = 'your public key';
```
**NOTE**: Remember to add your domain (eg. ```$YOUR_APP_NAME.herokuapp.com``` ) in [Google reCAPTCHA v3 setting](https://developers.google.com/recaptcha/docs/settings).

### Step 5 - Change your API port in ```src/constants.js```

**NOTE**: you need to set up your [mauton-api](https://github.com/ikhvjs/mauton-api) first.

```js
export const API_PORT = 'https://$YOUR_APP_NAME.herokuapp.com';
```

### Step 6 - Change your hompage to your heroku app domain in ```package.json```
```json
"homepage":https://$YOUR_APP_NAME.herokuapp.com/
```

### Step 7 - Commit your changes to your App
```bash
# Go into your mauton clone repository
$ cd mauton
$ git add .
$ git commit -m "heroku setup"
# push your changes to Heroku
$ git push heroku master
```

### Step 8 - Finished!!! See your App
```bash
# See your app
$ heroku open
```

## Acknowledgments 🎁
[Create React App Deployment](https://create-react-app.dev/docs/deployment/)
