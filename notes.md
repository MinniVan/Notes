_text_   --> italicized
**text*  --> bolded
'text'   --> inline code
--text-- --> strike through

From the texbook "Programming Skills for Data Science"
       - by Michael Freeman | Joel Ross

# TOP Level Header
## Secound Level Header
### ...etc

Normal text

- List Item 1
- List Item 2
- List Item 3
- List Item etc.. bulleted/unordered lists

```
blocks of code 
across multiple lines
```

> block quote


### Rendering Markdown

GitHib automactically renders a Markdown that ends with the .md extension


Atom allows previewing of a Markdown file
	ctrl-shift-m
	[.md file on Atom]

GIT

    repository (repo): A database containing all the committed versions of all 
                       your files, along with some additional metadata, stored
		       in a hidden subdirectory named .git within your project
		       directory. If you want to sound cool and in-the-know, call 
                       a project folder a “repo.”

    commit: A set of file versions that have been added to the repository 
           (saved in the database), along with the name of the person who
            did the commit, a message describing the commit, and a timestamp. 
            This extra tracking information allows you to see when, why, and 
            by whom changes were made to a given file. Committing a set of changes 
            creates a “snapshot” of what that work looks like at the time—it’s like 
            saving the files, but more so.

    remote: A link to a copy of this same repository on a different machine. 
           Typically this will be a central version of the repository that 
           all local copies on your various development machines point to. 
           You can push (upload) commits to, and pull (download) commits from, 
           a remote repository to keep everything in sync.
  
    merging: Git supports having multiple different versions of your work that 
             all live side by side (in what are called branches), whether those 
             versions are created by one person or many collaborators. Git allows
             the commits saved in different versions of the code to be easily merged
             (combined) back together without you needing to manually copy and paste
             different pieces of the code. This makes it easy to separate and then 
             recombine work from different developers.

### git config

       minnivan@van-VM:~$ git config --global user.name "Van Tha Bik Lian"
       minnivan@van-VM:~$ git config --global user.email "vanthabikl@gmail.com"
       minnivan@van-VM:~$ ssh-keygen -t rsa -b 4096 -C "vanthabikl@gmail.com"
       Generating public/private rsa key pair.
       Enter file in which to save the key (/home/minnivan/.ssh/id_rsa): 
       Enter passphrase (empty for no passphrase): 
       Enter same passphrase again: 
       Your identification has been saved in /home/minnivan/.ssh/id_rsa.
       Your public key has been saved in /home/minnivan/.ssh/id_rsa.pub.
       minnivan@van-VM:~$ ssh-add ~/.ssh/id_rsa
       Enter passphrase for /home/minnivan/.ssh/id_rsa: 
       Identity added: /home/minnivan/.ssh/id_rsa (/home/minnivan/.ssh/id_rsa)


### Command Summary

       git status                | Checks the status of a repo
       git add                   | Add file to the staging area
       git commit -m "message"   | Commit changes
       git clone		  | Copy repo to local machine
       git push origin master    | Upload commits to GitHub
       git pull		  | Download commits from GitHub




#### look up commands

       command 'fconfig' from deb redboot-tools
       command 'zconfig' from deb python-zconfig
       command 'vconfig' from deb vlan
       command 'iconfig' from deb ipmiutil
       command 'mconfig' from deb mono-devel


### Search *.extension files for "data", then perfrom a word count on the results
	grep -io data *.extension | wc -w


### Securly copy the local file [file]  into the projects folder on the remote machine

` scp MY_LOCAL_FILE username@hostname:path/to/destination `


### Creating a repo to push

       minnivan@van-VM:~/Desktop/Notes$ git remote add origin URL
       minnivan@van-VM:~/Desktop/Notes$ git remote -v
       minnivan@van-VM:~/Desktop/Notes$ git push -u origin master

### Reverting back to an older version
       
       **git checkout COMMIT_HASH FILENAME**
       replace COMMIT_HAS and FILE name
       with the commit ID hash and the 
       the file you want to revert
       "--" can be used as the commit hash
       to refer to the _most recent commit_

       **git checkout master** | this gets the most recent
       version of the master branch

	**git revert COMMIT_HASH --no-edit**

	This command will determine which changes the 
       specified commit made to the files, and then apply 
       the opposite changes to effectively “back out” the 
       commit. Note that this does not go back to the given 
       commit number (that’s what git checkout is for!), but 
       rather reverses only the commit you specify.The git revert 
       command does create a new commit (the --no-edit option 
       tells git that you don’t want to include a custom commit message). 
       This is great from an archival point of view: you never 
       “destroy history” and lose the record of which changes were made 
       and then reverted. History is important; don’t mess with it!



### .gitignore

       {don't check in passworeds stored in this file}
              secret/my_passwords.txt
       
       {Don't include large files or libraries}
              movies/my_four_hour_epic.mov
       {Ignore everything in a particular folder; note not the slash}
              raw-data/

       Easiest way to creat .gitignore file 
              > on text editor : Select file > new > 
              > make .gitignore file directly insdie the repo
              
