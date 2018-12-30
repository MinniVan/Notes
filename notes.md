
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

       #Don't check in passworeds stored in this file
              secret/my_passwords.txt
       
       #Don't include large files or libraries
              movies/my_four_hour_epic.mov
       #Ignore everything cd in a particular folder; note not the slash
              raw-data/

       #Easiest way to creat .gitignore file 
              > on text editor : Select file > new > 
              > make .gitignore file directly insdie the repo


### R
       Open source programing language | use for data stuff | yeah I said stuff

       Scripting 
              An instruction that is executed causing
              each instructions(line of code) to run in
              order, one after the other
              > This allows us to run several commands at once
              > Also -- Save, share and resuse work

       R is interpreted language so you can separately execute each indivdual
       line of code in the script

       R scripts are saved with with .R extenstion

### Using Rstudtio
       #Excecute from terminal
              $  Rscript filename.R

#### Script
       > Top left pane in the Rstudio = text editior to write R codes
              this pane is hidden if there are no open scritps
              --> FIle > New File > R Script

       #Execute R codes:
              > Sectional execution
                     - highlight desired code
                     - click the run button
                     - or ctr+enter

              > Execute entire script
                     - click the "Source" button (top right of the Script pane)
                            (fun fact: this calls an R function called source())
                     - or shift+ctrl+enter

#### Console
       > bottom-left pane is the console for entering R commands
       > allows you to perfrom a task you don't want to save on your script

#### Environment

       > Top-right pane | Displays infro about the current R enviornment
              - specifically info stored inside variables
              
              this pane helps with keeping track of which values
              you have stored in which variables
                     | useful for debugging | 


#### Plots, pacakges, help, etc
       > Bottom-right pane | contains multiple tabs for accessing info about the program
       > plots are rendered here when visualization is created
       > also shows which packages are loaded

       > access the official documentation for the R language here

#### Example of commenting R codes
       # Calculate the number of minutes in a year
       minutes_in_a_year <- 365 * 24 * 60 # 525,600 minutes!

       comment goes directly above the code line

### Defining Vairables
       > Can contain a combo of:
              - Letters
              - Numbers
              - Periods (.)
              - Underscores (_)
              >> Must begin witha letter
       > Case sesnsitve
       > Important to have the varibale name as descriptive as possible
       >> "x" is not a good variable name
       >> num_cups_cofee is good
       >> Variables are used to store information and we refer to that
          variable to access the inf stored in the varaible
              - think of it as "'boxes' or 'name tags' for data"
       >> Variable names should be lowecase letters seperated by underscores
              <known as snake_case>
       >> a value is assigned to a variable with the use of the assignment opperator
              |looks like this: <-
                            num_cups_coffee <-

#### Example of defining and commenting variables
       # Calculate the money spent on coffee using values stored in variables
       num_cups_coffee <- 3 # store 3 in `num_cups_coffee`
       coffee_price <- 3.5 # store 3.5 in `coffee_price`
       money_spent_on_coffee <- num_cups_coffee * coffee_price # total spent on coffee
       print(money_spent_on_coffee)
       # [1] 10.5
       
       # Alternatively, you can use a mixture of numeric values and variables
       # Calculate the money spent on 4 cups of coffee
       money_spent_on_four_cups <- coffee_price * 4 # total spent on 4 cups of coffee
       print(money_spent_on_four_cups)
       # [1] 14

### Basic Data Types
       > R is a dynamically typed language
              >> meaning we don't have to explicitly state which tye of information 
                 will be stored in each variable

              -- in Java (statically typed language), to define a variable that 
                 represents the integer value 7, we would define it as: int num = 7;
                 but in R: my_num <- 7       : is understood by R to be the interger 7
       > Numberic:
              The default computational data type in R
              >> consists of the set of real numbers (decimals included)

       > Character:
              This data stores strings of characters in a variable
              >> characters are specified by single quotes('character') or double ("character")

       > Logical:
              AKA boolea -> this data type stores "yes-or-no" data.
              >> Can have one of two values: TRUE or FALSE
              >>> produced by applying a relational operator (comparison operator) to
                  some other

       > Integer:
              integer(whole number) -> yes, it's different from the numeric type
              >> Rarely used --- we can specify a number to be the integer type 
                 by putting an L after the number:
                     : my_integer <- 10L
       > Complex:
              Imaginary numbers
              >> created by placing an i after the number
                     : complex_variable <- 2i

3RDocumentation.org: https://www.rdocumentation.org4R
Studio Community: https://community.rstudio.com
       

http://swrilstats.com

 https://github.com/programming-for-data-science/chapter-05-exercises

 

