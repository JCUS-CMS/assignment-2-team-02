# CMS: Assignmnet 2
## Group 007

------------------------------------
### Group Members -

1. Nyan Ye Htun - nyanyehtun@my.jcu.edu.au
2. Nurul - 
3. Hung - 
4. Benedict Ryan - 
------------------------------------

------------------------------------
## Architecture Diagram

![AWS CMS Architecture Diagram](docs/AWS-CMS-Deployment.png)
<p align="center">
<img src="docs/AWS-CMS-Deployment.png">
</p>


## Local Environment Setup -
<br/><br/>
**Setting up VVV in your local machine**
<br/>
*run the following commands:*

```
git clone https://github.com/Varying-Vagrant-Vagrants/VVV.git
cd VVV
vagrant plugin install vagrant-hostsupdater --local
vagrant up
```
delete the **wordpress-one** project folder:
```
rm -rf www/wordpress-onecd 
```
Clone the current repo as wordpress project called **wordpress-one**:
```
cd  www
git clone git@github.com:JCUS-CMS/assignment-2-team-02.git wordpress-one
cd ..
```

Now you have successfully setup workpress project on your Vagrant

<br/>

**Note: Work on the WordPress Project called wordpress-one after cloning the repo**

<br/>

##Edit your wp-config.php and change the DB settings to:

```
  define( 'DB_NAME', '<YOUR DB_NAME>' );  
  define( 'DB_USER', '<YOUR DB_USERNAME>' );  
  define( 'DB_PASSWORD', '<YOUR DB_PASSWORD>' );  
  define( 'DB_HOST', '<YOUR DB_SERVER IP>' );  
```

<br/>
  
**SETTING UP STAGING ON YOUR LOCAL ENVIRONMENT:**

<br/>

create a new branch and link it with your git remote staging <branch>:<br/>
  
```
git checkout -b staging
```

now for easy pull and push upstream it to your origin/<branch>=staging.<br/>
  
```
git branch --set-upstream-to=origin/staging staging
```

now pull the latest staging branch commits:<br/>

```
git pull
```

<br/>

**CHANGING GIT BRANCH IN LOCAL ENVIRONMENT:**

<br/>

this is the command to shift between branches in your local environment:<br/>

```
git checkout <branch-name>
```

for example if you are in staging branch and want to shift to development branch:<br/>

```
git checkout development
```

<br/>

**EXAMPLE - FOR STAGING**

<br/>

_For example lets say you have added some new feature to your development branch and now want to update it to staging branch
Then follow the following command:<br/>
You have to run the following command from your development branch -_<br/>
<br/>
Add the changed files to your git:

```
git add .
```

now commit the changes you have made:<br/>

```
git commit -m "<your-commit-message>"
```

now push the changes from development to staging :<br/>

```
git push origin staging
```

_**origin** = your remote git repo_
<br/>
_**staging** = your <branch> that you want to push to_

<br/>
  
now check out the staging URL for changes:<br/>

http://staging.cms-a2.ayushmank.sgedu.site/group-007/<br/>

------------------------------------