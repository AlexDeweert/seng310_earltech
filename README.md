### Welcome to the Earl Technologies project website collaboration page
This is just the code repository for our group project (in case we need to roll back any disastrous changes etc).<br>
It's certainly possible for us to just sent the instructor a bunch of HTML files, but that's no fun!<br>
### Getting started
#### Editing and previewing our website

> 1. Create a Github account. If you already have one, please send AlexDeweert your username so I can add you as a collaborator.
> 2. Install git on your machine (if you don't already have it) https://www.atlassian.com/git/tutorials/install-git
> 3. Clone the group project with: <p>`git clone https://github.com/AlexDeweert/seng310_earltech`<p>
> 4. Make any changes to the project files as you deem necessary.
> 5. From within the project directory, add any changes: <p>`git add filename` or `git add .` for all files changed<p>
> 6. Commit your changes so that they are staged for pushing (to the remote server): <p>`git commit -m "a message explaining what you did"`<p>
> 7. Push you changes: <p>`git push`<p>
> 8. Preview you changes at https://alexdeweert.github.io/seng310_earltech/index.html (or applicable html file)

#### Make changes live under the team URL
###### I should preface this by saying: this part isn't necessarily required, but I just didn't want to send the instructor the github site link with just one name attached to it. So instead, we have earl-technologies.surge.sh
We're using the static site hosting service, Surge.sh. It's quite a nice tool that might serve you in future should you decide to get into web development. It's great for sending static site prototypes to customers, friends, supervisors, co-workers etc. In our case, the stakeholders (prof and markers haha).

> 1. Instructions taken from https://surge.sh/help/getting-started-with-surge so you can follow this if you want.
> 2. In any case: make sure you clone the git project as above OR git pull to  make sure you have any updated changes from the team. Navigate to the project directory and notice the "docs" folder that's present. This is the folder we're publishing to Surge.
> 3. Assuming you have npm installed (which is node package manager for Node.JS): <p>`npm install --global surge`<p> (you might need to run this as admin or sudo)
> 4. From within the seng310_earltech git project folder type <p>`surge --domain earl-technologies.surge.sh`<p> (which sets the domain that we're using)
> 5. add /docs/ to the end of the project path when prompted.
> 6. Enter your e-mail when prompted.
> 7. Make sure the url is earl-technologies.surge.sh (it should be because of the surge --domain command you ran above)
> 8. The /docs/ folder will be published to the live site and you should be able to preview!
