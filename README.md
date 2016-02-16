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

## Building a prototype

* meetup at the Gym / building mobile apps with openData/JSON

## Angular.js

* guest speaker angular.js

## Realtime apps with node.js and socket.io

####what is node.js
Node.js is a platform built on Chrome's JavaScript runtime for easily building fast, scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.

####non-blocking IO
Also known as asynchronous IO is short for the non-blocking input/output of a system. It basically means that while an input or output is being processed, other processing still contintues before transmission is finished.

####synchronous vs. asynchronous
Non-blocking IO is the contrary of synchronous IO, in which a system has to finish processing the current input/output before being able to process the next. This means that the progress of a program would be blocked when communication is in progress.

####single-threaded
Single-threaded means that only one command of code can be executed at a time, and it has to finish each given task in sequence before being able to start another.

####typical use-cases
It is most commonly used for real-time applications with push capability. For example: a system to exchange data fast like a chat system, massively multiplayer online games, ...

####web sockets
Node.js and Websockets are the perfect combination to write very fast, lag free applications which can send data to a huge number of clients. 

####sockets.io and faye
Both of these are types of websockets which can be installed with node.js packages. The main difference is that Faye enforces a publish-subscriber pattern/protocol of communication. In Socket.IO, you don’t have to, so it’s a simpler abstraction. Faye could be built on top of Socket.IO.

### Building a simple node.js app

####install node.js globally
Download Node.js from the website: http://nodejs.org/. Start the setup and follow the instructions, make sure you install npm with it (it's in the default options).

####install express globally
To install express globally, you have to open the command prompt and type the command: `npm install express -g`.

####generate an express app
The first thing you have to do is creating a directory somewhere on the machine using the following command: `mkdir hello-world`. Hello-world can be any name you want. Then use the command: `npm install`. This will install all the dependencies necessary to run your Express app for the first time.

####the package.json file
The package.json file will contain all of the data which will be necessary to run your application. For example, it contains the name of the application and it's dependencies in the current version(like Express, Faye, MongoDB, ...). 

####installing dependencies with npm
Npm stands for node package manager and is used to install every dependency you need for your application. Basically just add the name of the dependency to your package.json file and use the install command.
Every command starts with: `npm install` (followed by the name of the dependency to install it locally) or `npm install -g` (followed by the name of the dependency to install it globally).

####jade
Jade is a node.js template engine and is the default template engine when you use Express. It replaces basic html by using the same tags as html but without end tags. A thing to note is that you can use tabs OR spaces to indent, not both in one file.

####the MVC structure of an express app
The MVC structure consists out of three layers. To state it simply:
* You start out on the app.js layer which was created by the Express app which contains all the basics to establish a port connection and basic data for your routes.
* Immediately when you start the app, you get the route you want from the app.js file and jump to the routes folder where you pick up the right path.
* The routes folder then renders the right jade template file which is the presentation layer the user will see.

####adding Faye to the mix
Faye is a type of websocket and it is used to easily create an application to publish and subscribe to messages. To add it to your project: add it to your package.json file and install it through npm. Then you have to initialize the Faye & bayeux client in the app.js file.
* The first step to do this is by requiring faye in your variable list. 

	`var faye = require("faye");`

* Then we create a variable bayeux in which we mount it to the path "/faye" to connect and talk to the server and a timeout to give a maximum time to hold a connection open before returning a response. 

	```var bayeux = new faye.NodeAdapter({
	  mount:    "/faye",
	  timeout:  45
	});```

* Next, we can attach bayeux to an existing server by adding this code. 

	`bayeux.attach(server);`

####subscribing to and publishing events with Faye
Now that we have Faye running on the connection we already established, we can publish and subscribe to messages from within the application. 
* First you'll have to open up the layout.jade file and add the latest JQuery file and Faye file links to your head (the Faye map and files will be created at runtime so you don't have to worry about them)
   
	`script(src="http://code.jquery.com/jquery-latest.min.js")`
	
	`script(src="/faye/browser/faye-browser.js")`
	
	`script(src="/faye/client.js")`
   
* Next, you can start out by creating a Faye client in any jade file you desire by adding this code. 

	`var client = new Faye.Client("http://localhost:8000/");`

* After this, you can subscribe to a channel to get messages published to a certain path (in this case the path name is /messages)

	```client.subscribe("/messages", function(message) {
    	alert("Got a message: " + message.text);
   	});```
   
* As a last step, you still have to publish messages to that given path and we do this by publishing something, for example:

	```client.publish("/messages", {
		text: "Hello world"
	});```
   
####nodemon
Nodemon is a utility that will look for any changes in the source code of your application and will refresh the app whenever something changes. You can also restart your application yourself by just typing `rs` in the command prompt.
You can install nodemon by using the command: `npm install -g nodemon`

## Building a prototype

* building a prototype

## Presenting your prototype

## License and attribution






