_text_   --> italicized
**text*  --> bolded
'text'   --> inline code
--text-- --> strike through

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


#-----------------------------------------------
##Rendering Markdown

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
#------------------------------------

#git config

#-------------------------------------
minnivan@van-VM:~$ git config --global user.name "Van Tha Bik Lian"
minnivan@van-VM:~$ git config --global user.email "vanthabikl@gmail.com"
minnivan@van-VM:~$ ssh-keygen -t rsa -b 4096 -c "vanthabikl@gmail.com"
Too many arguments.
usage: ssh-keygen [-q] [-b bits] [-t dsa | ecdsa | ed25519 | rsa]
                  [-N new_passphrase] [-C comment] [-f output_keyfile]
       ssh-keygen -p [-P old_passphrase] [-N new_passphrase] [-f keyfile]
       ssh-keygen -i [-m key_format] [-f input_keyfile]
       ssh-keygen -e [-m key_format] [-f input_keyfile]
       ssh-keygen -y [-f input_keyfile]
       ssh-keygen -c [-P passphrase] [-C comment] [-f keyfile]
       ssh-keygen -l [-v] [-E fingerprint_hash] [-f input_keyfile]
       ssh-keygen -B [-f input_keyfile]
       ssh-keygen -D pkcs11
       ssh-keygen -F hostname [-f known_hosts_file] [-l]
       ssh-keygen -H [-f known_hosts_file]
       ssh-keygen -R hostname [-f known_hosts_file]
       ssh-keygen -r hostname [-f input_keyfile] [-g]
       ssh-keygen -G output_file [-v] [-b bits] [-M memory] [-S start_point]
       ssh-keygen -T output_file -f input_file [-v] [-a rounds] [-J num_lines]
                  [-j start_line] [-K checkpt] [-W generator]
       ssh-keygen -s ca_key -I certificate_identity [-h] [-U]
                  [-D pkcs11_provider] [-n principals] [-O option]
                  [-V validity_interval] [-z serial_number] file ...
       ssh-keygen -L [-f input_keyfile]
       ssh-keygen -A
       ssh-keygen -k -f krl_file [-u] [-s ca_public] [-z version_number]
                  file ...
       ssh-keygen -Q -f krl_file file ...
minnivan@van-VM:~$ ssh-keygen -t rsa -b 4096 -C "vanthabikl@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/minnivan/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Passphrases do not match.  Try again.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/minnivan/.ssh/id_rsa.
Your public key has been saved in /home/minnivan/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:FFzA366YU3GTtOP56FpY2Se7pJuDTACm2EZg5oyGVk8 vanthabikl@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|  +o E ooo.      |
|.*. + o o.  .    |
|ooo+ + ... o o   |
|o . +  .. o Bo   |
|   .    S. =o+o .|
|          oo+  + |
|         *.o.oo  |
|        + +.o+.. |
|         ..o=o.  |
+----[SHA256]-----+
minnivan@van-VM:~$ evel "$(ssh-agent -s)"

Command 'evel' not found, did you mean:

  command 'evil' from deb lxqt-build-tools

Try: sudo apt install <deb name>

minnivan@van-VM:~$ eval "$(ssh-agent -s)"
Agent pid 733
minnivan@van-VM:~$ ssh-add~/.ssh/id_rsa
bash: ssh-add~/.ssh/id_rsa: No such file or directory
minnivan@van-VM:~$ ssh-add ~/.ssh/id_rsa
Enter passphrase for /home/minnivan/.ssh/id_rsa: 
Identity added: /home/minnivan/.ssh/id_rsa (/home/minnivan/.ssh/id_rsa)


#-------------------------------------------------------------------------------
#--------------------------------------------------------------------------------
#--------------------repo - dadada - using git------------------------------------
#---------------------------------------------------------------------------------
#---------------------------------------------------------------------------------

minnivan@van-VM:~/Desktop$ mkdir git_practice
minnivan@van-VM:~/Desktop$ cd git_practice/
minnivan@van-VM:~/Desktop/git_practice$ git init
Initialized empty Git repository in /home/minnivan/Desktop/git_practice/.git/
minnivan@van-VM:~/Desktop/git_practice$ ls
minnivan@van-VM:~/Desktop/git_practice$ ls
minnivan@van-VM:~/Desktop/git_practice$ ls -la
total 12
drwxr-xr-x 3 minnivan minnivan 4096 Dec 20 21:56 .
drwxr-xr-x 3 minnivan minnivan 4096 Dec 20 21:56 ..
drwxr-xr-x 7 minnivan minnivan 4096 Dec 20 21:56 .git
minnivan@van-VM:~/Desktop/git_practice$ ls -a
.  ..  .git
minnivan@van-VM:~/Desktop/git_practice$ cd .git
minnivan@van-VM:~/Desktop/git_practice/.git$ ls
branches  config  description  HEAD  hooks  info  objects  refs
minnivan@van-VM:~/Desktop/git_practice/.git$ cd ..
minnivan@van-VM:~/Desktop/git_practice$ 



minnivan@van-VM:~/Desktop/git_practice$ vim books.md 
minnivan@van-VM:~/Desktop/git_practice$ ls
books.md
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	books.md

nothing added to commit but untracked files present (use "git add" to track)
minnivan@van-VM:~/Desktop/git_practice$ git add books.md 
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   books.md

minnivan@van-VM:~/Desktop/git_practice$ git commit -m "initial commit"
[master (root-commit) beaf66e] initial commit
 1 file changed, 7 insertions(+)
 create mode 100644 books.md
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
nothing to commit, working tree clean
minnivan@van-VM:~/Desktop/git_practice$ git log [--oneline]




#------------------------------------------------------------------------------------------
#----------------------------------------------------------------------------------------
#----------------------------removing files --------------------------------------------
#----------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------
minnivan@van-VM:~/Desktop/git_practice$ touch removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ ls
movies.md  removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.Rhistory
	removeMe.txt

nothing added to commit but untracked files present (use "git add" to track)
minnivan@van-VM:~/Desktop/git_practice$ git add removeMe.txt 
minnivan@van-VM:~/Desktop/git_practice$ ls
movies.md  removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   removeMe.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.Rhistory

minnivan@van-VM:~/Desktop/git_practice$ git commit -m "add"
[master 0ae80be] add
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.Rhistory

nothing added to commit but untracked files present (use "git add" to track)
minnivan@van-VM:~/Desktop/git_practice$ git add .Rhistory
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   .Rhistory

minnivan@van-VM:~/Desktop/git_practice$ git commit -m "R"
[master ee23e68] R
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 .Rhistory
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
nothing to commit, working tree clean
minnivan@van-VM:~/Desktop/git_practice$ git log
commit ee23e6859fa124fd6850ab19547b7b0dc916ed74 (HEAD -> master)
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:49:09 2018 -0800

    R

commit 0ae80be0f663300190e613d4ad85168f525a56d5
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:48:22 2018 -0800

    add

commit 7af071fa4349f315d9bc609fa7473040eae32602
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:46:43 2018 -0800

    delete books.md file

commit 69fd559a637fc0394db63534b47b0351a1b779e4
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:38:06 2018 -0800

    rename file

commit 50c56fbf4262c93307a8da49b40af64c33a89734
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:32:05 2018 -0800

    add two more movies

commit beaf66e9b23a22573224a3642cee597b3895eae5
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:14:09 2018 -0800

    initial commit
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
nothing to commit, working tree clean
minnivan@van-VM:~/Desktop/git_practice$ git log
commit ee23e6859fa124fd6850ab19547b7b0dc916ed74 (HEAD -> master)
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:49:09 2018 -0800

    R

commit 0ae80be0f663300190e613d4ad85168f525a56d5
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:48:22 2018 -0800

    add

commit 7af071fa4349f315d9bc609fa7473040eae32602
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:46:43 2018 -0800

    delete books.md file

commit 69fd559a637fc0394db63534b47b0351a1b779e4
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:38:06 2018 -0800

    rename file

commit 50c56fbf4262c93307a8da49b40af64c33a89734
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:32:05 2018 -0800

    add two more movies
minnivan@van-VM:~/Desktop/git_practice$ git ls-files
.Rhistory
movies.md
removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git rm removeMe.txt 
rm 'removeMe.txt'
minnivan@van-VM:~/Desktop/git_practice$ git ls-files
.Rhistory
movies.md
minnivan@van-VM:~/Desktop/git_practice$ git rm .Rhistory 
rm '.Rhistory'
minnivan@van-VM:~/Desktop/git_practice$ git ls-files
movies.md
minnivan@van-VM:~/Desktop/git_practice$ ls
movies.md
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	deleted:    .Rhistory
	deleted:    removeMe.txt

minnivan@van-VM:~/Desktop/git_practice$ git reset HEAD .
Unstaged changes after reset:
D	.Rhistory
D	removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	deleted:    .Rhistory
	deleted:    removeMe.txt

no changes added to commit (use "git add" and/or "git commit -a")
minnivan@van-VM:~/Desktop/git_practice$ git rm .
fatal: not removing '.' recursively without -r
minnivan@van-VM:~/Desktop/git_practice$ git rm . -r
rm '.Rhistory'
rm 'movies.md'
rm 'removeMe.txt'
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	deleted:    .Rhistory
	deleted:    movies.md
	deleted:    removeMe.txt

minnivan@van-VM:~/Desktop/git_practice$ git reset HEAD .
Unstaged changes after reset:
D	.Rhistory
D	movies.md
D	removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git ls-files
.Rhistory
movies.md
removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	deleted:    .Rhistory
	deleted:    movies.md
	deleted:    removeMe.txt

no changes added to commit (use "git add" and/or "git commit -a")
minnivan@van-VM:~/Desktop/git_practice$ git rm .Rhistory 
rm '.Rhistory'
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	deleted:    .Rhistory

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	deleted:    movies.md
	deleted:    removeMe.txt

minnivan@van-VM:~/Desktop/git_practice$ git rm movies.md 
rm 'movies.md'
minnivan@van-VM:~/Desktop/git_practice$ git staus
git: 'staus' is not a git command. See 'git --help'.

The most similar command is
	status
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	deleted:    .Rhistory
	deleted:    movies.md

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	deleted:    removeMe.txt

minnivan@van-VM:~/Desktop/git_practice$ git rm removeMe.txt 
rm 'removeMe.txt'
minnivan@van-VM:~/Desktop/git_practice$ ls
minnivan@van-VM:~/Desktop/git_practice$ ls
minnivan@van-VM:~/Desktop/git_practice$ git ls-files
minnivan@van-VM:~/Desktop/git_practice$ git log
commit ee23e6859fa124fd6850ab19547b7b0dc916ed74 (HEAD -> master)
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:49:09 2018 -0800

    R

commit 0ae80be0f663300190e613d4ad85168f525a56d5
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:48:22 2018 -0800

    add

commit 7af071fa4349f315d9bc609fa7473040eae32602
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:46:43 2018 -0800

    delete books.md file

commit 69fd559a637fc0394db63534b47b0351a1b779e4
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:38:06 2018 -0800

    rename file

commit 50c56fbf4262c93307a8da49b40af64c33a89734
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:32:05 2018 -0800

    add two more movies
minnivan@van-VM:~/Desktop/git_practice$ git commit -m "delete all files"
[master 242a703] delete all files
 3 files changed, 10 deletions(-)
 delete mode 100644 .Rhistory
 delete mode 100644 movies.md
 delete mode 100644 removeMe.txt
minnivan@van-VM:~/Desktop/git_practice$ git status
On branch master
nothing to commit, working tree clean
minnivan@van-VM:~/Desktop/git_practice$ git log
commit 242a7037ba3ac7dacb29dda8b25757f9040c2dad (HEAD -> master)
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 12:14:04 2018 -0800

    delete all files

commit ee23e6859fa124fd6850ab19547b7b0dc916ed74
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:49:09 2018 -0800

    R

commit 0ae80be0f663300190e613d4ad85168f525a56d5
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Fri Dec 21 11:48:22 2018 -0800

    add

commit 7af071fa4349f315d9bc609fa7473040eae32602
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:46:43 2018 -0800

    delete books.md file

commit 69fd559a637fc0394db63534b47b0351a1b779e4
Author: Van Tha Bik Lian <vanthabikl@gmail.com>
Date:   Thu Dec 20 22:38:06 2018 -0800

    rename file
minnivan@van-VM:~/Desktop/git_practice$ 
minnivan@van-VM:~/Desktop/git_practice$ 


#-------------------------------------------------------------
#------------------.gitignore--------------------------
#----------------------------------------------------------

Note that the easiest way to create the .gitignore file is to use your 
preferred text editor (e.g., Atom); select File > New from the menu and 
choose to make the .gitignore file directly inside your repo.

If you are on a Mac, we strongly suggest globally ignoring your .DS_Store file. 
There’s no need to ever share or track this file. To always ignore this file on 
your machine, simply run these lines of code:

# Run these lines on your terminal to configure git to ignore .DS_Store
git config --global core.excludesfile ~/.gitignore
echo .DS_Store >> ~/.gitignore



Command Summary

git status                | Checks the status of a repo
git add                   | Add file to the staging area
git commit -m "message"   | Commit changes
git clone		  | Copy repo to local machine
git push origin master    | Upload commits to GitHub
git pull		  | Download commits from GitHub




look up commands
  command 'fconfig' from deb redboot-tools
  command 'zconfig' from deb python-zconfig
  command 'vconfig' from deb vlan
  command 'iconfig' from deb ipmiutil
  command 'mconfig' from deb mono-devel


# Search *.extension files for "data", then perfrom a word count on the results
	grep -io data *.extension | wc -w

#--------------------------
#Securly copy the local file [file]  into the projects folder on the remote machine

` scp MY_LOCAL_FILE username@hostname:path/to/destination `


