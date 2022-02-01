<b>Here is a Repo which can help you to deploy Jackett to Heroku</b>

<i>Several of the most commonly used ndexers are already set up. If you'd like to alter or replace any of these, look in the repository under "config/Jackett/Indexers."</i>

### Deploying with CLI
- Clone the [repo](https://github.com/missemily2022/Jackett_Heroku)
- Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

```
cd Jackett-Heroku
heroku login 
heroku create --region eu appname
git init
heroku git:remote -a appname
heroku stack:set container
git add . -f
git commit -m "Init"
git push heroku master -f
```

### Deploying with Workflow
- Fork the [repo](https://github.com/missemily2022/Jackett_Heroku)
- On the forked repo, go to *Settings* -> *Secrets* and click on the *New repository secret* button
- Now enter the vars one by one with value
1. `HEROKU_API_KEY`: Get the API Key from Heroku [Account Settings](https://dashboard.heroku.com/account)
2. `HEROKU_EMAIL`: Email address of your Heroku Account
3. `HEROKU_APP_NAME`: Name of your Heroku App. It must be unique on Heroku.
- Then go to the *Actions* tab on your repo
- Select *Deploy to Heroku* from the *All workflow* list
- Click on *Run workflow* -> *Run workflow*
- After that turn on the app dyno and enjoy the Jackett

<br>

<b><i>Credits : </i></b>[Levi](https://t.me/l3v11)