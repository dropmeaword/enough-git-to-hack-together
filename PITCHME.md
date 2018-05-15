## Enough Git to hack together
---
Think for example of the process of writing a book, say a *Travel Guide to Hamburg*. Let's say we will write it collaboratively with other people
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
*Git* vs. *Github*
---
The Git workflow:
    1. clone or create repo
    2. add files and changes
    3. commit your changes to your local copy
    4. synch your local copy to the remote copy by pushing your commits
---
Exercise




