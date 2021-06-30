## Task-1
This task was not a traditional CTF, but kind of a puzzle and, a free flag .😂<br>
I literally followed just the steps written in the task.

### Part-1 
Quoting from the problem statement - <br>
`For the first part of the flag, try to find all the branches in this repository and see if you can observe a flag or it's mention somewhere.`<br>
On seeing the list of branches we see a branch named `develop` with a file `something.md`. In this file the final hint for the first part is given as
`The first part of the flag is the type of hash used by git as default, can you find it!`<br>
On simple googling we get the answer as **SHA-1**(Secure Hash Algorithm 1).

### Part-2 
At the end of `something.md` file it has been asked to look into the commit history. There we find a commit with message `cmmmt` to `file.md` which was deleted later.<br>
This directly leads us to the second part of the flag - <br>
`The second part of the flag is the default branch name used by Github for a new repository.`<br>
That is simply **main**. Though earlier the default name used to be *master*

### Part-3
At the end of `file.md` , we have been asked to look into thr forks of the repository. There we find a fork by @ssl-team-aas.<br>
In the forked repository inside folder named 'folder' we find `README.md` file. ( we look into only at this folder and not in rest because of the commit dates xD ).<br>
The final hint for the last flag is - <br>
`The third and final part of the flag (which is why you are here) is exactly the mechanism to automate tasks on github.`<br>
So basically it is talking about the **Workflows** which is used in Github Actions.

### Final Answers
```
Part-1 : SHA-1
Part-2 : main
Part-3 : workflow
```
