# Step by Step guide on how to make changes to the repo

## 1. Creating a branch
Create a branch on Github, by clicking the "branches" subsection under
the code tab. Select the green "New Branch" button. Make the source main.

## 2. Setting up the terminal
Open up your terminal:
   In VSCODE:
	a. Open the Music_Grader.github.io folder.
	b. Click the terminal tab (located near the file tab)
	c. Create a new terminal, this should appear on the bottom of your screen
   In the 'terminal' application
	a. Navigate to the Music_Grader.github.io folder. (View vocab to see useful commands for this)

## 3. Switching to our branch
We will use the "git checkout" command to navigate back to our main branch.
We must then git pull, to update our local copy of the repo so that we can 
access our newly created branch.

```
git checkout main
git pull 
```
You'll notice that the output shows your new branch has been added.
Now, use the "git checkout" command again to switch to this branch.

```
git checkout <branch_name>
```

*Note that <branch_name> doesn't require the ' < > ', it's just a formality
so for this branch I would use the command:

```
git checkout 1-create-git-tutorial
```

## 4. Making changes
Now that we're on our newly constructed branch, we can make changes to our files, or simply add files / directories to the repo.
With this first case, I know that you've already written some code. So you can simply move those files into the "Music_Grader.github.io" folder.

After doing this, or making changes to one of the files, type:

```
ls
```

so you can view all the files within our current directory. You'll notice your files are now located inside of the current directory. 

You should also frequently be using:

```
git status
```

to see that your files have been added. You'll notice that the files are untracked. 

## 5. Adding
Once your ready to push your changes to the remote repo (Github's version of our repo. Think of it as the host for all of our work), 
we need to add our files to be committed.

The simplest way to do this:

```
git add .
```

This adds all the untracked files to be committed. 

## 6. Committing
Now that those files are added, we can

```
git status
```

again and view that the changes are now staged for committment. 

In order to commit, we will type the following command:

```
git commit -m example-message
```

Note*: ALWAYS remember to use '-m example-message', because if you omit this, the terminal will bring you into a crappy text editor to write
a message. This editor isn't very descriptive as to how to use the commands located within, so we try to avoid it at all costs.

Because I'm basing this document off of your first push, I recommend writing a commit message like so:

```
git commit -m adding-initial-files
```

or something similar. 

## 7. Push
Now if we:

```
git status
```

you'll seee that there are no more untracked files. 

We are now ready to push:

```
git push
```

This will push your work to Github.com.

## 8. Navigate to Github.com
Under the "Pull Requests" Tab, you'll notice that there will be a message detailing pushed changes from your branch. You can go here to create
a pull request for that push, where we will then be able to merge your work, assuming there are no merge conflicts.

Merge conflicts occur when code on your branch interferes with the code that is currently in place on the main branch. These are NOT GOOD.

If your work is merged successfully, you'll notice that your branch's work will have overwritten the main branch. Now you have successfully made
your changes to the repo.


 
