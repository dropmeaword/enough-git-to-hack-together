## Enough Git to hack together
---
Let's think of the process of writing a book, for a moment. Let's say we write a *Travel Guide to Hamburg*. And let's say that we write it together, as a collaborative effort.
---
Perhaps you start with a draft and a rough sketch of what you want the Travel Guide to cover
---
You follow a similar process with each chapter and inch your way arduously through the text of the book
---
Later you start adding illustrations, photographs, etc.
---
Your daily workflow looks something like this:
1. Edit the chapter files
2. Manage supporting files
3. Review
4. Backup
---
Today:
1. You wrote a whole section on the Elbphilharmonie building
2. You added three stock photographs of the building to your assets
3. Mailed the visual editor to take a pick of the three
4. You updated the phone number of three restaurants in the St. Pauli section
5. You fixed all the spelling mistakes in the introduction
6. The Haven section was getting too large, so you branched into another document
---
Eventually when you feel the Travel Guide can be useful, you hand it over for review to a few people. One person helps because she has good English, another because they know Hamburg really well, another because she's an information designer and can help you to convey a message, etc.
---
If your tool is the word processor, most modern word processors have a feature to *track changes*. That can help you see how your book writing effort has evolved over time.
---
Normally a project develops over time, and as you make progress the files that your project is made out of will come to change, some new files will be added, some others will be removed, some very large files might be split in a few smaller ones, this is true for all assets in your project. 
---
*Track changes* is great, if you work alone. But when we start the review process and mail the preview of the book to our collaborators, each of them works in a separate file and they send us back their comments by email. It quickly becomes a whole job in itself to manage and incorporate their suggestions.
---
How do you handle, track the development of your project across time and deliver the assets of a digital project?
---
At each stage in time of our book project we want to know:
- when the asset was modified
- what changed
- why was it modified
- who modified it
---
This is what Version Control is for, making these types of workflows easier to manage and facilitate collaboration between people working in the same project.
---
## Version Control
---
Code is normally stored in plain-text files
---
Code, just like graphics, videos, sounds, etc. are all digital assets
---
Version Control Systems (VCS) help you track your digital assets throughout their lifetime
---
VCS is a critical methodology in software development and to a very large extent the open source movement couldn't have happened without version control
---
Before 1986: the SCCS model, "lock" before you edit
---
In 1986 a piece of software named CVS (for Concurrent Version System) was released. It allowed multiple people to work simultaneously on the same asset by introducing a process called "merging".
---
## Version Control a glossary
---
### repository (or repo)
---
### local
---
### remote
---
### cloning
---
### working copy
---
### forking
---
### staging/adding changes
---
### master
---
### branch
---
### merge
---
### commit
---
### pushing
---
### pulling
---
### pull request
---
# Version Control Today with Git
---
*Git* written by Linus Torvalds in 2005 to manage Linux Kernel (22 MLoC) development.
---
*Git* is a distributed VCS, or DVCS.
---
The relationship between *Git* and *Github*
---
The Git workflow:
1. clone or create repo
2. add files and changes
3. commit your changes to your local copy
4. synch your local copy to the remote copy by pushing your commits
---
Exercise
---
### One - create a repo

Depending on where the source is located, we have two options to start a repo.
---
#### One A - starting from local

Starting from a clean slate, with no previously existing repo. To work with Git we first need to create a repository or "repo". We can create a "repo" in any folder in our computer where we want to keep track of change in our digital assets.

`$ git init`

This command creates a repo in currently working directory.
---
#### One B - starting from remote

Starting from a repo that already exists online (perhaps on github or other hosting service). The action we need to perform here is to create a *local copy* of that *remote repo*. You can identify addresses of remote repos online because they normally end in `.git`. This is not always so but it is a generally accepted convention.

To create a *local copy* going to *clone* it.

`$ git clone https://github.com/IDArnhem/git-white-album-collaboration.git`
---
### Two - add files to that repo

When the repo is first created it doesn't really contain anything, it will only track change in the digital assets that we tell it to. So the first thing we need to do is to add files to the repo.

`$ git add README.md`

This command will add a file named `README.md` to the repoa nd will track any changes made to it. We can also add *all* the files in the current directory (and all subdirectories) by typing this command:

`$ git add *`

Add in the context of Git can have two meanings, one is to add a file, this is what git will do when it didn't know that file from before. And another is to add any change made to that file with respect to a previous version, in that case it will not add the entire file, it will only add the change we made.
---
### Three - commit changes in our local copy

A commit is a unit of work, you are basically saying: "I have done all these changes and I am now ready to commit them all together as a piece of work". A piece of work is something we should be able to describe, something like "change all the illustrations in Chapter One", "updated the table of contents", sometimes a piece of work can be a simple and small change like "fixed a typo" and sometimes it can be a large number of changes "changed the entire book from American to British spelling". Git will require us to describe this unit of work by using the `-m` parameter followed by "the description between double quotes". 

`$ git commit -m "i worked on this today"`

As long as it is done in one commit it will appear in our history as a single unit of work. A commit is also a "point in time" in our project, we can revert commits if we don't like them, we can selectively merge or remove them, we can roll back to the way that our project was three weeks ago, or yesterday and all this is done at the commit level. Each commit, is a breadcrumb in the arrow of time a point where we can always come back to.
---
### Four - push changes to make them public

So far you have worked locally, local changes and local commits will not be visible to others on your *github remote repo*. You have to *push* those changes, before they become public.

`$ git push --all`

This command pushed all commits that are pending locally to the *remote repo*, making them public for others to *pull*.
---
Exercise




