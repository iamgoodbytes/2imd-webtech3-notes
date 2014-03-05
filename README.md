# Webtech 2: notes

These are extra notes, links and references used to supplement a course I teach at Interactive Multimedia Design (http://www.weareimd.be) at Thomas More university college Mechelen.

Students and readers are encouraged to participate and optimize these course materials by sending a GIT pull request.

Reusing parts of this course is allowed and encouraged as long as the following attribution and links are kept intact: 

## Licensing and attribution
Course material created by [GoodBytes](GoodBytes) for professional bachelor degree [Interactive Multimedia Design](http://www.weareimd.be/) at [Thomas More](http://www.thomasmore.be/interactive-multimedia-design-imd) Mechelen in Belgium.


## Markdown
You may have noticed that this course is published on github in a file called README.md. By default, GitHub will display the contents of a README.md file on a repository's landing page. See the extension .md? That stands for [markdown](http://en.wikipedia.org/wiki/Markdown). 

Markdown is a super simple way to add formatting to text, without having to use complex and irritating word processing software. It gives you a lot of freedom to do whatever you want with your documents, like converting it to HTML.

* http://daringfireball.net/projects/markdown/
* https://help.github.com/articles/markdown-basics
* https://help.github.com/articles/github-flavored-markdown


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
Put simply, merging takes two snapshots of your code (e.g. your *my-new-feature-x* branch and the *master* branch) and merges them together. 

If you have coded up a new feature in your *my-new-feature-x* branch and you want to make that available into your production ready application, you'll probably want to merge that branch with your master branch.

There's a whole lot more to be said about merging. For details, check out [this link](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging)

#### production-ready master approach
The production-ready master approach is a popular approach when developming with git. 

With this approach, we guarantee that any commit we make in the *master* branch is stable, production-ready code. That means that at any time of the day, it is safe to deploy the master branch to our production server.

Development and experimentation with new features is done in so called *feature branches*.

### github.com
[GitHub.com](GitHub.com) is a commercial business that provides a hosting platform for Git repositories. It's especially known for hosting open source projects (which is free on GitHub) and for facilitating social coding with others. Private repositories aren't free.

GitHub is not the only provider of Git hosting, but it's one of the most famous ones, if not the most famous. Another popular Git hosting provider is [Bitbucket](https://bitbucket.org). Bitbucket offers private repositories for free to small teams which can be interesting.

#### Forking
GitHub makes it easy to contribute to a project, even when it's not owned by your own team or company. If you want to contribute to a project, or start a new project based on another, you could *fork* a repository.

*Forking* creates a copy of an existing repository on your GitHub account. To start working in that copy, you need to clone it to your local machine first. 

Imagine that you fixed a nasty bug in your favourite open source project (Let's hope yo used a topic branch for that). Now it's time for your moment de gloire and contribute that fix back to the project you've been using and abusing for so long. To contribute your fix, create a [pull request](https://help.github.com/articles/using-pull-requests).

#### pull requests

Pull requests notify users about changes you pushed to a repository. After you initiate a pull request on GitHub, your changes can be reviewed and people can comment on your work. Once approved, the owner of the forked repository can decide to merge your changes into the repository so that anyone can pull in your changes. 

Congratulations, you've just made the internet better! Why not send in a pull request to improve this course material while you're at it? See what I did there ;)?.

Make sure to read the following guide in detail if you want to start contributing on a project: https://help.github.com/articles/fork-a-repo

### Useful links
* http://guides.github.com/
* http://try.github.io/
* http://think-like-a-git.net/
* http://dotnet.dzone.com/articles/intro-git
* http://www.sbf5.com/~cduan/technical/git/
* http://www-cs-students.stanford.edu/~blynn/gitmagic/index.html

## Advanced Javascript
* syntax
* prototypes
* event handling
* objects
* inheritance
* namespacing
* closures
* module pattern
* bower

### Useful links
* https://www.openshift.com/blogs/day-1-bower-manage-your-client-side-dependencies

## Animating with CSS

### Transitions

### Transforms

#### 2D Transforms
* translate()
* rotate()
* scale()
* skew()
* matrix()

#### 3D Transforms
* rotateX
* rotateY
* perspective

### Animations



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






