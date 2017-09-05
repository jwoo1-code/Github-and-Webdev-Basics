# Github-and-Webdev-Basics
### Tutorial on basic git and webdev

## Intro/Goals
Welcome to Hacksu! Make sure to ***bring a laptop*** so you can follow along with the lesson!

Everything in this guide will be covered in the lesson -- this is just to give you an idea about what we'll cover, or to help you catch up if you miss something that was said. 

The goal of this lesson is to learn how to use Github, set up a repository, and learn how to make a basic website!

## Github - What Is It, and Why Use It?

*If you already know what github is, skip this section.*

Github is for project management!  Here's some reasons to use Github:

  * It allows you to share projects, either with a team or with the whole world, and set permissions on who can and can't contribute.
  * If you don't have permission to edit a project, you can 'fork' it -- make a copy of it -- and edit it all you want
  * Github uses Git, a version control system (like SVN, if you've used that) that lets you work on your projects from any computer, and lets you go between different saved versions anytime you want. 
  * When you have multiple people working on a project, Git also helps handle "merge conflicts" -- when two different users submit two different, conflicting submissions
  * A bunch of other neat organization tools, like issues, wikis, and readme files like this one!!
  
### -- Github Glossary
#### --- Some Github terms you might be confused by:

  * **Git** -- Version control system. You install this on your computer to let you easily move things to and from Github.
  * **Github** -- The website hosting everything submitted by Git. 
  * **Repository (or repo)** -- Any github project. Basically just a set of files hosted on github.
  * **Clone** -- You can take a Github repo and *clone* it to your local computer so you can work on it.
  * **Commit** -- Once you have a local clone of a repo, you can submit a *commit* of your changes back to the parent repo. Each commit is basically a 'version', when we talk about version control.
    * (Note that `git commit` won't submit your code to Github on its own. The full process for committing code is `git add [whatever files were changed]`, `git commit -m "your commit message"`, `git push`. We'll go over this later.)
  

## Github Setup

The first thing we need is to set up a github account. *If you already have a github account, skip this portion.*

Go to [github.com](https://www.github.com) and sign up with a unique username, and an email you can access.

Select the free account option and press continue. Fill out the survey if you'd like, it's optional. You'll now need to confirm your email. 

## Repo Setup

Once you have a confirmed Github account, click on the + icon in the upper lefthand corner of Github, and select "New Repository". 

Name your repository whatever you want -- "My first site" or something.  Add a description, decide whether you want it to be public or not, and check the box that says "initialize this repository with a README".

Congrats, you just made your first Github repo! 

## Git setup/Cloning our repo!

Now, we need to set up Git on your computer. To do this, we're going to learn some basic terminal commands!

### Mac/linux Git Install instructions:

If you're using a Mac or Linux OS, open up the terminal. On a mac, you should be able to find it by searching for "terminal", or looking in your Applications folder.  To see if you have git, type `git --version` and press enter. If you don't have it yet, follow [these instructions](https://www.atlassian.com/git/tutorials/install-git), and then restart your terminal to see if it worked.

### Windows Git Install Instructions:

If you're using a Windows computer, open up Windows Powershell. You should be able to find it by searching for it. (Command Prompt should also work, but I like powershell more.)  To see if you have git, type `git --version` and press enter. If you don't have it yet, follow [these instructions](https://www.atlassian.com/git/tutorials/install-git#windows), and then restart your powershell to see if it worked.

For either setup, remember to do these commands too:
```
 git config --global user.name "Your name"
 git config --global user.email "your@email.com"
 ```

### Cloning the Repo

Now that you have Git installed, we can finally clone our repo! But first, we need to learn how to use our terminal.  

Your terminal always points to somewhere on your computer, and we can type different commands to navigate through our computer and interact with files. (Tip: Pressing 'tab' in the terminal will try to autocomplete whatever you're typing.)

Here are the terminal commands we'll be using:

  * `cd [somewhere]` -- stands for "change directory". Replace `[somewhere]` with an existing folder.
    * `cd ..` will take you back one folder (ex: if you're in `~/Files/myfolder/`, `cd ..` takes you to `~/Files/`)
    * `cd ~` will take you to your "home directory" from wherever you are.
  * `ls` -- is an abbreviation for "list", which doesn't make sense but whatever. It lists all the files and folders in your current directory
  * `mkdir [folder name]` -- stands for "make directory". Will make a folder named `[folder name]` in the current directory

If you type `cd ~/Desktop`, you'll navigate straight to your desktop. From there, navigate to wherever you want to keep your project on your folder. You can also type `mkdir hacksuProjects` or something to make a folder named "hacksuProjects" on your desktop (You would then type `cd hacksuProjects/` to go inside of that folder.)

Once you're in the folder you want to store your projects, go back to your github repo, and click the green 

Go to your repo page on Github and find the green button that says 'Clone or download', and copy the URL it shows. Go back to the terminal and the following command, replacing `[ur]` with the URL you copied:

`git clone [url]`

Unless you have an error, congrats! You just cloned your repo to your computer! You can now enter `cd [repo name]` to go into your repo.

## ------------------
## Making Our Website


Finally, we can actually start coding. The first thing you'll want is a code text editor -- try [atom](https://atom.io/) or [brackets](http://brackets.io/). You can also work with notepad or whatever, but these will make things easier.

In your local clone of your repo, make a new file and name it with the extension `.html`, like `index.html` or `website.html`. In this file, we'll be writing HTML, our first language! Go ahead and type: 

```
<html>
 <head>
 </head>
 <body>

  <h1>My first website (or whatever)</h2>
  
 </body>
</html>
```

Then, go to the file and double click it. It should open up in your browser, just like a normal website would!

HTML is used to format text, and tell the browser what each text is for. It works by surrounding text opening tags, like `<body>`, and closing tags, like `</body>`.  The `head` tags surround information about the website, while the `body` tags show the actual content of the website.  If any of these tags confuse you, turn to google to learn about them!

Let's add a little more content to our website:

```
<html>
 <head>
 
 <title>My first website, yo !</title>
 
 </head>
 <body>

  <h1>My first website (or whatever)</h2>
  
  <p>Here's some text in a 'paragraph' tag</p>
  <p>Here's some more text, with a <a href="http://facebook.com">link!</a>
  <img src="https://cdn.pixabay.com/photo/2017/01/06/19/15/soap-bubble-1958650_1280.jpg">
  
  <div class="myDiv"> This is a special divider</div>
  
  <button onclick="alert('hello world')">Here's a button </button> 
  
  <!-- This is an HTML comment. It won't affect the actual content of the page -->
  
 </body>
</html>
```

All of this is customizable, of course, and you should try making your website to your own liking, rather than just copying this. The best way to learn code is to come up with a creative idea, and try to learn how to make it work!

Now, let's learn a little CSS. CSS is another programming language, used to *stylize* our formatted text.

Make a new file in the same folder, and call it `style.css` or something similar. Here's an example of some fun CSS code:

```
body {
  background: cyan;
}

p {
  color: red;
  font-family: Courier;
}

.myDiv {
  width: 400px;
  height: 300px;
  border: solid 2px black;
  border-radius: 25%;
  background: yellow;
  
  animation: myAnimation 10s infinite;
}

@keyframes myAnimation {
  from {
    filter: hue-rotate(0deg);
  }
  to { 
    filter: hue-rotate(360deg);
  }
}

```

Save your CSS file. Now, to link it to our HTML file, we need to add this in our `head` tags in our html file:

```
 <head>
 
 <title>My first website, yo !</title>
 <link rel="stylesheet" href="styles.css">
 
 </head>
```

Save your HTML and see if the styles were applied! Make sure that in `href="styles.css"`, "styles.css" is the exact same name as your css file. Also make sure your css file is in the same folder as your .html file!

CSS applies styles to the tags. To learn more about the style attributes, turn to google!

## Pushing to our Github Repo with Git

So, now we have a website! Let's save it to our Github repo, so the whole world can see it!

Go back to your terminal and navigate to your repo folder. There's three steps to saving to Github:

1. Add your files by typing `git add *`. The astrisk * is used to mean "everything in this folder." Alternatively, we could type `git add index.html` to only submit a single files.

2. Commit your files with `git commit -m "My first commit message"`. Instead of writing "my first commit message", you should really explain what changes you made in this commit. This is called a 'commit message'.  Note that commiting your code creates a log of what has been added, and gets it ready to put onto Github, but it doesn't actually transfer it yet!

3. Enter `git push` to "push" all your local commits to your github repo.

If you didn't get any errors, go to Github and see if your code is all there! Congratulations!

## Other resources

If you want to learn about how to host a website on Github, check out [this link](https://pages.github.com/) -- it's a lot easier than you'd think!

If you want to learn more about HTML or CSS, I'd recommend [W3Schools](https://www.w3schools.com), or google!

If you want a preview of the next lesson, look into Javascript. Javascript is easy to add to our HTML, and will let us interact with the user a lot more.
