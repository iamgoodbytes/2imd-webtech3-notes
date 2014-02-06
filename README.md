# Webtech 2: notes

These are extra notes, links and references used to supplement a course I teach at Interactive Multimedia Design (http://www.weareimd.be) at Thomas More university college Mechelen.

Students and readers are encouraged to participate and optimize these course materials by sending a GIT pull request.

Reusing parts of this course is allowed and encouraged as long as the following attribution and links are kept intact: 

## Licensing and attribution
Course material created by [GoodBytes](GoodBytes) for professional bachelor degree [Interactive Multimedia Design](http://www.weareimd.be/) at [Thomas More](http://www.thomasmore.be/interactive-multimedia-design-imd) Mechelen in Belgium.

## Social coding with Git
### What is git
Git is a version control system or VCS. Another famous version control system is SVN or Subversion. A version control system makes it easier to collaborate on projects in teams, especially when a project consists of source code like PHP, HTML, .. 

Git is a distributed VCS while Subversion is a centralized VCS. When using a distributed VCS like Git, you commit your changes locally on your machine until your are ready to push your changes to an online repository. In a centralized VCS like Subversion, commits are done on a central server.

A possible issue with systems like SVN is that when the online repository/server goes down, you can't commit your work until the server comes back online. With Git, that problem goes away as all commits are done locally first. Git also allows us to use multiple repositories and synchronize work between them if we wanted to. This creates greater freedom when it comes to setting up development workflows.

Without a good VCS it would be a lot harder to collaborate on projects and safely deploy them to staging and production servers. More on deployment later.

### git core concepts

#### clone
Cloning a repository means creating a copy, usually on your local development environment.

#### fetch
The fetch command gets the latest version of your files from the remote repository. The difference with the pull request is that fetching only gets your files, without merging them with your own local copy.

#### pull
Similar to the fetch command, the pull command fetches the latest version of the files from a repository and subsequently merges these files with your local copies.

#### push
Pushing to a repository sends all your committed files to a repository, ready to be fetched or pulled by others.

#### commit
Committing files tells git that you have changes you want to store or submit to your repository. 

A commit should be a container for small and related changes. Fixing two bugs for example should produce two separate commits. 

#### branch
Let's skip the technical details for a moment and talk about why you should be using branches. When you clone or create a git repository you typically get started with a main branch to work on called *master*. A popular convention is to use this master branch as a clean and stable copy of your software. At any point in time, a team member should be able to take this master branch and deploy it to a production server for the whole world to see.

Imagine you're trying out a new feature on your website or app. You could decide to just start coding in your master branch, no harm done right? Here's the problem: what if, in the middle of completing your new feature, a new bug pops up that requires immediate action. 

You need to fix the bug in the master branch right away and deploy it to your production server but you can't. You can't because that would also deploy your half-assed feature to your production server and the whole world would see that.

Enter branches. A branch creates a new history of commits that won't interfere with e.g. your master branch. Now you can start experimenting in your newly created branch called *my-new-feature-x* without having to worry about the stability of the master branch. 

Once you are ready and you have tested your new feature, switch to your master branch, merge the code from your *my-new-feature-x* branch and when you deploy your master branch again, your users will be delighted to see your new and finished feature pop up on the website.

http://git-scm.com/book/ch3-1.html

#### merge
Merging takes one set of commits and tries to merge them with a branch of a repository.

#### rebase

#### production-ready master approach

### github.com

#### Forking

https://help.github.com/articles/fork-a-repo

#### pull requests

### What is markdown
You may have noticed that this course is published on github in a file called README.md. Pay attention to the extension .md which stands for markdown. 

* https://help.github.com/articles/markdown-basics
* https://help.github.com/articles/github-flavored-markdown

### Useful links
* http://guides.github.com/
* http://try.github.io/
* http://think-like-a-git.net/
* http://www.sbf5.com/~cduan/technical/git/

## Advanced Javascript

* advanced javascript
* syntax
* closures
* objects
* prototypes
* namespacing
* bower
* https://www.openshift.com/blogs/day-1-bower-manage-your-client-side-dependencies

## CSS Pre-processors

* sass, less & stylus
* compass & bourbon 

## Backbone.js

* Backbone.js introduction

## Grunt.js

* workflow optimization with Grunt

## Building a prototype

* meetup at the Gym / building mobile apps with openData/JSON

## Angular.js

* guest speaker angular.js

## Realtime apps with node.js and socket.io

* realtime apps with node.js and socket.io
* projectorpong

## Building a prototype

* building a prototype

## Presentating your prototype

## License and attribution






