## Introductory talk

Think for example that you want to write a book, a *Travel Guide for Hamburg*, for instance. You start with a draft of your idea, very rough at first, perhaps a rough sketch of the contents you want the book to cover. As the draft evolves and your ideas take form in text, you will probably start adding lots of text, illustrations, perhaps some references to venues, restaurants, important landmarks, etc. As you reach the stage prior to publication you want other people to read it, to make sure that the book is communicating what you think is communicating, if its understandable, accesible, if there are no glaring mistakes, etc. Each time you push this work forward you make changes in the assets of your project.

If your tool is the word processor, most word processors today have some kind of primitive form of a feature called "change tracking". This change tracking allows you to see how the document evolves over time and allows you to roll back to previous version, see what changed when, incorporate your reviewers suggestions, etc.

However if a word processor is not your primary tool, it seems like there are not so many options that you can rely on. How does, for example, a game company do this. A game might be developed by a team of people of sometimes up to 40 people, all of which are simultaneously working on the same game assets. The graphic texture of the Ogre, the 3D shape of the Ogre's sword, the code that drives the Ogre's behaviour in a game, the code that renders the graphic for XBOX and for Playstation. In some cases millions of lines of code, sometimes written by teams of programmers upward of 10 people.

----

If you remember from the last session we had together, I did mention that code is normally stored in plain text files. Code, just like graphics, sounds, videos and other files belonging to your projects are assets that can be managed. 

Normally a project develops over time, and as you make progress the files that your project is made out of will come to change, some new files will be added, some others will be removed, some very large files might be split in a few smaller ones, this is true for all assets in your project. 

How do you handle, track the development and deliver the assets of a digital project?

If you are alone by yourself working on a digital project that nobody else will work on, or read or need it only in its final form. Simply numbering your folders, like you probably do now, will be enough. But this is not how the software world works. Version Control for example is an absolutely crucial methodology in ALL open source projects, no matter the size. The version control system enables multiple people in different geographical location to work together towards a single product. Today, as software culture penetrates more and more industries you are likely to encounter some form of version control wherever you go. Whether it is used to handle the different design iterations in an architectural project, the design of a product, an app, web application, video, etc. Most companies use one form of asset management and change tracking or another. Version Control also lets us understand the culture underpinning collaborative work a little better and as such I think it is a useful technique to learn.

## Why is git useful?

Allows you to participate in Hcakathons and other collaborative efforts, like writing a book together, etc. It will make you A LOT better at handling your digital assets, this includes all your future work. Email sucks and emailing files back and forth is a terrible way of collaborating on something or asking questions to your teachers. Using Git makes it easier for others to review and give you comments on your digital files, specially your code.

## Enter Version Control

Prior to 1986, if you were working in a team of people on a digital project with multiple assets, all those assets where likely to be in a shared drive somewhere and you would have a software called SCCS that allowed you to "lock" a file, so that you could work on it. While you were working on that file nobody else could, that file was effectively "locked" for everyone else in the project but you. You would make your contribution, commit your changes to the collective share and "unlock" that file so that others could work on it some other time.

This was the way that things were done for many years and it was slow, inneficient, it caused conflicts of all kinds and actually prevented people from collaborating effectively.

For example if one of the people collaborating on a project went on holidays and left a file locked, nobody else could work on that file while that person was away. This actually happened A LOT.

In 1986 a piece of software was published that forever chnaged the profession, it was called CVS (Concurrent Versions System) it allowed two people to work simultaneously on the same asset and it would introduce a process called "merging". Merging allowed two people to work on the same file simultaneously as long as they weren't working on the exact same lines of text. Merging would then get the changes made by person A and the changes made by person B and would figure out what the actual state of the file should be with the work of both people brought together. Of course if two people changed the exact same paragraph of the exact same file, if is imposible for the CVS system to know which of the two changes should go into the final version. In that case CVS will mark the last change commited as a "conflict" and would ask the humans to resolve that conflict and commit the result.


## A glossary of version control

"repository" - a repository is a working unit of your project, you can think of it as a container for all the working assets for a chapter in a book. A single project can be put together from assets taht come from multiple repositories.

"local" - normally we refer to "local changes" or "local copy" or "local" to refer to the copy of the project that exists in our computer, this copy might be identicaly to everybody else's if it's "sunched" or it might be different if we made any "local changes".

"remote" - this term in computing normally refers to a computer somewhere else, a computer other than our own, it might be a server somewhere, it might be a shared folder we keep with friends or co-workers, but normally a computer other than ours.

"cloning" - cloning is the process by which you make a local copy of a "remote repository", it effectively downloads all the digital assets of that project and their respective history of changes, such as who did what and when

"working copy" - this is the copy of the project that normally resides in your computer, it contains all the digital assets of a given repository.

"forking" - to fork a repo is to make a separate copy, a parallel copy that will not necessarily contribute back to the original, in open source projects you don't really want to fork. Forking in the open source world used to be considered a hostile act. Git has changed this perception a little. You can consider a fork to be a "branch in another repo".

"staging/adding changes" - this is a concept that is mostly related to git, not all version control systems support "staging" in their workflow.

"master" - we call a master the most recent version of all the assets in a given repository, the master normally evolves with time as it incorporates contributions from multiple people

"branch" - a branch is an alternative "reality" let's say that we branch from the master at a particular point in time, maybe we want to try a new technique we learned, or perhaps try another narrative angle for our book chapter, or perhaps our editor just hired a new illustrator for our book and she wants to know how our book would look like with her illustrations before making a final decision. We can "branch-out" from our "master" and try these alternative realities out. It it turns out that we like the results of our experiments we can always incorporate the innovations we introduced in one branch into our master by making a "merge".

"merge" - merging is the act of bringing together two distinct pieces of work and co-exist together in our collection of assets, for example person A added new illustrations to our paper and person B, rewrote two paragraphs in one chapter. "Merging" the work of these two people into our "master" would update our master to contain both pieces of work

"commit" - committing a piece of work means that you are satisfied with it, that you consider that specific chunk of work to be complete and that you want to add it to your change tracking, in the case of git "commits" are not publiscly shared, they are kept in your local copy until you decide to share them

"pushing" - pushing your changes, means that all your commits, all the units of work that you have been quietly working on will get pushed to the public repository shared by everybody, this will allow other people

"pulling" (also called checking out) - in Git parlance, to pull is to get any pending changes from the remote repo.  Imagine that your co-author worked on a chapter last night, before you start work today you might want to *pull* their work, to make sure you start from the latests version.

"pull request" - imagine that you found a book on github, you liked it but you didn't like the ending, you decide to *fork* the original and create your own version with a different ending. What you would do in Git is you would create a branch/fork of that project, to create your own "alternative reality" in which you would finish the book in the way that you want. If you now wanted to suggest to the original author of the book that your ending is worth her consideration and that she should really check out your work on it. You can submit a "pull request" to the original author, effectively allowing her to "pull" from your "repo" and obtain the ending you wrote to make it available to everybody else. Pull requests are the way in which a person you never knew or met can propose improvements to your book, your software project or your digital assets.

# Git

Git is a piece of software that was first designed and written by Linus Torvalds, the person resposible for the Linux kernel (~22 MLoC), which is at the core of the Linux operating system and the Android mobile OS. Software written by Linus Torvalds is now probably sitting in your pocket. The linux kernel is a very large piece of software written collaboratively by thousands of people across the world, each piece of work, is added to the collective assets known as the Linux kernel source code. Each contribution must be tracked, reviewed and merged into the kernel. A single faulty contribution can damage the master if it makes its way through it witout a proper review process. The Linux kernel source is composed of millions of lines of code and it is possible to name the person that wrote, changed and updated every single one of them, thanks in part to Version Control.

To track changes in such a large collaborative undertaking is a huge task and for years the Linux kernel maintainers had relied on tools that were not really up to the task and made collaboration difficult and often rely too much on the work of a small group of individuals. To better address these limitations Torvalds wrote the Git tool.

One of the primary features of Git, that is not easy to find in other tools of its class is that Git makes it incredibly easy to make "branches". Branches are like "alternative realities", so Git makes it very very easy (or at least easier than any other system) to try new things out. Remember Facebooks early motto of "move fast and break things", in many ways this mentality is the by product of having solid tools that allow you to try and do cheap experiements with your dogital assets and to be always able to revert back to a previous state of the master if something doesn't work as planned.

Git is very different from its predecesors, in that there's not a single canonical copy of the source code of a project handled by Git. It is a Distrivuted Version Control System or DVCS for short. This means that every person that "clones a repo" is in fact getting not just the master, but the entire history of the project. A local clone is in fact THE ENTIRE repository, containing all the assets and their respective histories, who made what change, when and how.

## Git and github

Git is a program, a piece of software that specializes in doing one thing and only one thing well. Tracking changes in digital asset files.

In order to have git repositories published on the web for others to work with you, you need a git server, setting up and maintaining a git server is not a trivial task and it requires a significant effort, this is why Git hosting services came into existence. Github is one such git respository hosting service. It is a company founded on the premise that people want to work collaboratively in digital assets without the hassle of having to maintain their own Git server.

Github offers free Git hosting services for open source projects, therefore giving back to the community that gave them much of the software that they themselves run on and at the same time encouraging the uptake of Git as the version control system of choice for many open source projects. This has triggered a kind of runaway effect which has made github the lagest repository of living code on the web.

If your assets are valuable intellectual property that you want to protect as a trade secret and you don't want to make them public, you might prefer to get yourself another Git hosting service.

For this class and to deliver assignments involving digital assets such as code, we will be using Github. Lerning to use Git and Github will make yourfuture life a lot easier. Git, like verything technical, is not trivial to learn, but there are a few basic commands that will allow you to use its basic features. 

# The Git workflow

### Step One - create a repo

Depending on where the source is located, we have two options on how to start a repo.

#### Step One A - starting from local

Starting from a clean slate, with no previously existing repo. To work with Git we first need to create a repository or "repo". We can create a "repo" in any folder in our computer where we want to keep track of change in our digital assets.

`$ git init`

This command creates a repo in currently working directory.

#### Step One B - starting from remote

Starting from a repo that already exists online (perhaps on github or other hosting service). The action we need to perform here is to create a *local copy* of that *remote repo*. You can identify addresses of remote repos online because they normally end in `.git`. This is not always so but it is a generally accepted convention.

To create a *local copy* going to *clone* it.

`$ git clone https://github.com/IDArnhem/git-white-album-collaboration.git`

### Step Two - add files to that repo

When the repo is first created it doesn't really contain anything, it will only track change in the digital assets that we tell it to. So the first thing we need to do is to add files to the repo.

`$ git add README.md`

This command will add a file named `README.md` to the repoa nd will track any changes made to it. We can also add *all* the files in the current directory (and all subdirectories) by typing this command:

`$ git add *`

Add in the context of Git can have two meanings, one is to add a file, this is what git will do when it didn't know that file from before. And another is to add any change made to that file with respect to a previous version, in that case it will not add the entire file, it will only add the change we made.

### Step Three - commit changes in our local copy

A commit is a unit of work, you are basically saying: "I have done all these changes and I am now ready to commit them all together as a piece of work". A piece of work is something we should be able to describe, something like "change all the illustrations in Chapter One", "updated the table of contents", sometimes a piece of work can be a simple and small change like "fixed a typo" and sometimes it can be a large number of changes "changed the entire book from American to British spelling". As long as it is done in one commit it will appear in our history as a single unit of work.

A commit is also a "point in time" in our project, we can revert commits if we don't like them, we can selectively merge or remove them, we can roll back to the way that our project was three weeks ago, or yesterday and all this is done at the commit level. Each commit, is a breadcrumb in the arrow of time a point where we can always come back to.

`$ git commit -m "Describe the work you did here"`

### Step Four - push changes to make them public

So far you have worked locally, local changes and local commits will not be visible to others on your *github remote repo*. You have to *push* those changes, before they become public.

`$ git push --all`

This command pushed all commits that are pending locally to the *remote repo*, making them public for others to *pull*.


## Resources

1. [A visual guide to version control](https://betterexplained.com/articles/a-visual-guide-to-version-control/) 
2. [Learn git branching](https://learngitbranching.js.org/)
3. [Learn enough Git to be dangerous](https://www.learnenough.com/git-tutorial)
4. [The Github guide to become a Git guru](https://services.github.com/on-demand/resources/learning-path/)
5. [Getting Git right](https://www.atlassian.com/git)
6. [Interactive Learn & Practice Git](https://gitexercises.fracz.com/)
7. [Got 15 minutes to learn Git](https://try.github.io/levels/1/challenges/1)
8. [Git Real](http://gitreal.codeschool.com/levels/1)
9. [Distributed Version Control: The Future of History](https://blog.kitware.com/distributed-version-control-the-future-of-history/)
10. [Synching a fork to upstream](https://help.github.com/articles/syncing-a-fork/)
11. [Git cheat sheet](https://rogerdudler.github.io/git-guide/files/git_cheat_sheet.pdf)
12. [Github cheat sheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf)
13. [Git cheat sheet with visuals](http://files.zeroturnaround.com/pdf/zt_git_cheat_sheet.pdf)

----

## Aside

You might find this article interesting.

"The Scientific Paper is Obsolete", April 5, 2018
https://www.theatlantic.com/science/archive/2018/04/the-scientific-paper-is-obsolete/556676/?utm_source=atlfb

Among other things it discusses the role of Github in academic writing and how software methods are becoming part of the reproduceability aspects of the scientific method.

----

# Exercise

#### prep

You will need to install two things from my thumbdrive.
"git" and "github desktop"

1. create an account on github.com
2. Go to https://github.com/IDArnhem/git-collaboration-exercise.git
3. Take some time to explore that repo, see who owns it, what's the history, who made what, how it evolved in time
4. *Fork* that repo

git config --global user.name "John Doe"
git config --global user.email johndoe@example.com


#### Part 1

From the music folder: get the songs provided, you will have the entire White Album from The Beatles, this album was published in 1968 and it is one cultural artifact in the English language that I deemed suitable for this exercise.

What you must do: Pick one song, try your best to transcribe the lyrics. Precision here is not really the primary goal. Don't Google! We will do that in Part 2. You can start with a best effort and we will gradually "home in" to the "correct" lyrics.

Let's collaboratively try to make a transcription of the whole album.

Once you are done with your file: 
1. push your changes to remote
2. create a *pull request* to the original owner of the *repo* you *forked* from
3. wait for that person to accept your changes

#### Part 2

You have now contributed to a collaborative effort at transcribing an album. 

1. Synch your github repo up with the original that your forked from

```
git remote add upstream https://github.com/IDArnhem/git-collaboration-exercise-streamb.git
git remote -v
git fetch upstream
git checkout master
git merge upstream/master
```

Our local copy is now up to date with respect to the repo that we originally forked, `IDArnhem/git-collaboration-exercise-streamb.git` but our personal github fork is still not 
synched with our local copy. We must push our changes from local to remote.

```
git push --all
```

2. You should now have the full album lyrics as we transcribed it together
3. Ask the person to your right what song they transcribed
4. Google for the actual lyrics of that song (compare a few websites to make sure that there are no great differences)
5. Go through their transcription in your local copy and fix the mistakes or omissions that they made
6. *Commit*, *push* and create a *pull request* again

Thank you!
