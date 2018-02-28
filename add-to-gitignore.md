# Updating a .gitignore file

Let's face it we are all human (I think) and we forget to ignore something we really don't want to commit to git. Here is a quick explanation of how to handle that situation.

You will first want to make the changes to your .gitignore file. Identify the files and/or patterns you would like to exclude. Let's say out .gitignore file looks like this:

```
node_modules
```

We just added logging to our app, and we know have a list of files that have changes as follows

* logging-config.user.js
* errors.20180101.log
* errors.20180102.log
* logs/added-cheeseburgers.log
* logs/removed-cheeseburgers.log

We don't have any desire to check these into our repo so let's add these to our .gitignore file, which should now looks like this:

```
node_modules
logging-config.user.js
*.log
```
_Note_: *.log will ignore all files with the extension .log, so it will capture the ones in our log folder.

When a new log is created, or you update your logging user configuration file, you might notice that your changes are still be tracked. In this case, the will need to remove that file, folder or pattern from cache.

```
git rm --cached {filename or pattern}
```

So in our example we could run

```
git rm --cached logging-config.user.js
git rm --cached *.log
```

Commit your changes and push them to your remote reposistory and everyone will :heart: you for removing unneeded files from your pull requests.


**Reference**
* StackOverflow [Answer](https://stackoverflow.com/a/1139797/1143670)
* A [collection](https://github.com/github/gitignore) of useful .gitignore templates
* A nice [getting started guide](https://www.atlassian.com/git/tutorials/gitignore) for .gitignore
* Official .gitignore [documentation](https://git-scm.com/docs/gitignore)