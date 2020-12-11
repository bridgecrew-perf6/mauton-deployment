# mauton-deployment

## Purpose
Describe the procedures of deployment to Heruko.

## Prerequisites 📋
You'll need:
* [Git](https://git-scm.com) 
* [NPM](http://npmjs.com)
* [Google reCAPTCHA v3](https://developers.google.com/recaptcha/docs/v3) (which you need to register for a key)
* [Heroku](https://heroku.com) (which is for the platform to launch your website)

## Deployment 📦

If you have Heroku Account Skip to Step 4
### Step 1 - Heroku Account

Create a account in Heroku

### Step 2 - Heroku CLI

install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

### Step 3 - Create Heroku App

```bash
# create a Heroku App
$ heroku create $yourAppName
# check git remote 
$ git remote -v
#your should see something like
heroku  https://git.heroku.com/$yourAppName.git (fetch)
heroku  https://git.heroku.com/$yourAppName.git (push)
```

### Step 4 - Change your hompage to your heroku app domain in  package.json
```json
"homepage":https://$yourAppName.herokuapp.com/
```

### Step 5 - Commit your changes to your App
```bash
# Go into the repository
$ cd $yourAppName
# commit your changes to Heroku
$ git push heroku master
```

