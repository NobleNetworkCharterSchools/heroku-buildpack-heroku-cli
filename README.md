# heroku-buildpack-heroku-cli

This Heroku buildback lets you run [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) commands in your Heroku dynos.

## Usage

1. Add `https://github.com/fletom/heroku-buildpack-heroku-cli.git` as a buildpack URL.
2. Optionally, if you're sharing the app with others, create a dedicated less-privileged Heroku account to authenticate with.
3. Generate a Heroku API token for the account using `heroku auth:token`. 
4. Add a `HEROKU_API_KEY` environment variable to your app with the token you generated.
5. Use the `heroku` command from your web, worker, or Heroku Scheduler dynos.

Note that anyone with this auth token can perform actions using its corresponding Heroku account, including on other apps it has access to.