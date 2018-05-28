## Slack to Jenkins

This repository is going to give you an idea to control jenkins job from slack command. For this you need to configure both jenkins and slack application.

* Login to jenkins and go to Jenkins > People > LoginUser > Configure.
* Click `SHOW API TOKEN`
* Now you already possess jenkins login username and user api token.
* Install `Build Authorization Token Root Plugin` and `Build Token Trigger Plugin`.
* In slack app, go to Menu > Customize Slack > Configure Apps.
* Install `Slash Commands` app and gather app token.
* Use `/deploy` as custom command, `https://JenkinsLoginUserName:APIToken@JenkinsServer/job/JobName/build?token=SlashAppToken` as URL and `GET` as method.
* Now go to Jenkins job configuration window and click `Trigger builds remotely (e.g., from scripts)` under `Build Triggers` option.
* Use the slash app token here.
* Invoke `/deploy` command and jenkins job status from dashboard.
