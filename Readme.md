# ---------------------- Git Installation on Windows------------------------




### Follow the steps below in the Git Installation on Windows:-




1. Visit the [Git for Windows](https://git-scm.com/download/win) website.

2. Download the latest version of Git and choose the 64 bit version.

3. After the file is downloaded, install it in the system.

4. During the installation, we can choose the default options according to our preferences.

5. Click on the **Install** button to start the installation.

6. Once installed, select launch the Git Bash, then click on finish.

7. The Git Bash is now launched.




 #### Check for Git Version:

    git --version

Git - Downloading Package



# -----------V.S Code and Github Connectivity-----------------


1. Open the folder in V.s code
2. Go to source control
3. Then click intitialize Repository
4. In the left down corner the branch name is main, if we want to rename it we click ctrl+shift+p and write test-branch(or anything) and press    enter
5. In the source file we see that the letter 'U'(untracked) in the file
6. we just click on (+) sign in the file
7. Add a msg whatever you made changes like first commit and press tick sign.
8. We ned to go in the seperate branch for that we have to press ctrl+Shift+p and then type Create branch.
9. Brach name - New features (or anything)
10. Then in the 'new feature' branch we add something in the code or commit some changes.
11. Then we see that in the left side i.e file name we see 'M' is there, that means we modified it.
12. Click on that modified file and for seeing all the chngs in one view mode for that we should click (...) on the upper right corner and click inline view.
13. After that we should click(+) in changes(left side) and add a msg (ex: added features) and commit it.
14. Now we go in the main branch in the left down corner 
15. Now we will merge (main+new features) for that we should click (...) present on the upperleft corner - Branch - Merge Branch
16. Then click Publish Branch
17. Then it will ask for github want to sign in, allow all the things, and it gets connects.




# -----------------GIT BASIC COMMANDS----------------

### 1. To set user name and email

    git config --global user.name Gautam
    git config --global user.email gautamchy2002@gmail.com

### 2. To open Visual Studio Code
    code .

## To get Repository, we use two things
   (i) Cloning
   (ii) init command
 
### 3. For Initializing
     git init

### 4. To show hidden folders
     ls -lart

### 5. To Check status
    git status

### 6. To go in staging area
     git add index.html     (used to add the file index.html)

### 7. To add all files in staging area i.e; for tracking all files
    git add -a  or  git add .

### 8. To save this much file structure 
    git commit  ( First Press 'i' then type initial commit and the press escape then :wq)

### 9. To get all the files commited
     git commit -m "Added more htmls"

### 10. To create blank files
      touch about.html  

### 11. To get Checkout (Checkout is used to match with last commit)
         git checkout file name(contact.html)

### 12. To checkout all the files with previous file
          git checkout -f

### 13. If there are 1000 commit and if we want to see only 5 commit then, 
          git log -p -5

### 14. To get compare with working tree to staging area
          git diff

### 15. To get compare with staging area to last commit 
         git diff --stage

### 16. To remove the file and delete from staging area 
          git rm filename (ex:git rm contact.html)

### 17. Only delete from staging area
          git rm --cached waste.html

### 18. To show in list 
          ls

## Master Branch is the main branch

### 19. If we want to go from master branch to branch
          git branch name of the branch (ex: git branch feature1)
          git checkout feature1 (will go in branch)

### 20. if again want to come in master branch 
          git checkout master

### 21. If we want to merge feature1 and master branch
          git merge feature1
### 22. If we want to create new branch and want to go from master branch to that branch, then
          git checkout -b flaskintegration(name of new branch)

### 23. To push 
          git push

### 24. For clone
          git clone(add link) (link will get from the github - repository- code and then copy the code)  






# -----------------Git SSH Connectivity------------------

### Steps to get SSH Connectivity........
 
 1. First make the folder and then in that folder make one file named id_rsa
 2. Go to the setting in Github Repository
 3. Click on SSH and GPGn key
 4. Go to generating a new SSH Key
 5. Copy the link 
       (ssh-keygen -t rsa -b 4096 -c "Your email")
 6. Paste it in the gitbase or vs coode terminal. Then Press enter, again press enter, again press enter
 7. One key is generated
 8. Again go to that guide - go to Adding your ssh key to the ssh agent
 9. Copy the link 
     (eval $(ssh-agent -s))
10. Paste it in the gitbase or vs code terminal
11. By doing this we get Agent pid
12. Now copy the link of SSH add
     (ssh-add ~/.ssh/id_rsa)
13. Now will have to deploy for that
14. Copy the link 
     cat ~/.ssh/id_rsa.pub  [Cat is uded to show the content]
15. Then copy the content shown and paste it in the SSH key present in github alc
16. Then Press add key. Your key is added
17. Now to push in repository type
     git push -u origin master and press enter

  ## Note:- If we get repository not found

18. Then we again in the Repository - code - SSH and copy the link so that we will change the url
19. We type 
     git remote set-url origin(and paste the link)

20. Then we check 
     git remote and press enter
     git remote -v and press enter
### Then we see that the url get changed

### Now again we push that
      git push -u origin master

 Then it should get pushed.  
