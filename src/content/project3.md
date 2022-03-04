+++
date = "03 Mar 2022"
draft = false
title = "Project 3: Multiple Hypothesis Testing and CRISPR"
slug = "project3"
+++

<div class="due">

<center>Due: <b>Monday, 21 March, 8:59pm</b></center> 
</div>

#


<div class="yellownote">
 <center>
       <b>Collaboration and Resource Policy</b>
    </center>
For this assignment, you are encouraged to work with one other person. 
    
We expect most students will have the best learning experience on this assignment by working with a partner, but if you prefer to work alone it is okay to do this assignment on your own. Your partner can be anyone you mutually choose, so long as you are able to work together well.
    
You are permitted (actually <i>encouraged</i>) to discuss these problems with anyone you want, including other students in the class. If you do discuss the specific questions in the assignment with anyone other than your assignment partner and the course staff, though, you should list them in the _External resources used_ section of your submission.
    
You are welcome to use any resources you want for this assignment, other than ones that would defeat the purpose of the assignment. This means you should not look at answers or code from any other students in the class (other than your collaboration with your partner), and if you find code that implements the exact problem you are being asked to do for the assignment, you should not use that code. Since parts of this assignment are adapted from an NCSU assignment, you should also not search for or use any answers you might find for that specific assignment. You should document all external resources you use that are not part of the course materials in the _External resources used_ section.

</div>

## Getting Started

Note that the submission directions for this project are different
from Project 1 and Project 2. So, however you end up with a printed
notebook containing your answers is fine. It is not necessary for you
to work in a github repository for this, but we still recommend that
you follow these directions (which are similar to those for Project
2):

1. One of your team members should **create a new repository** named `csbio-project3` (you can pick a different name if you really want to).

   - Visit [https://github.com/repositories/new](https://github.com/repositories/new)
   - Select "Private" for the type of repository. 
   - Keep the "Initialize this repository with a README" unchecked, since you will fetch it later from a public repository.

###

2. **Share this repository with your teammate**:

   - Visit the repository's page.
   - Click the "Settings" button on the right side.
   - Click the "Collaborators" tab.
   - Enter your teammate's github id, and select the user from the dropdown.
   - Click "Add" with "Write" privileges.

###

3. **Clone the empty private repository to your working environment.** Instead of _mygithubname below_, use your github username.

```
    git clone https://github.com/mygithubname/csbio-project3.git
```

You should see:
```
Cloning into 'csbio-project3'...
warning: You appear to have cloned an empty repository.
```

4. Enter your `csbio-project3` directory (`cd csbio-project3`).

###

5. **Fetch the assignment** skeleton from our repository into your private repository. Enter the working directory of your empty repository and add a remote repository named course, merge the code, and push it to your private repository by executing:

```
   git remote add course https://github.com/computingbiology/Project-3-CRISPR.git
   git pull course main
   git push --tags origin main
```

(If your directory is not empty, you will need to add
`--allow-unrelated-histories` to the `git pull course main` command.)

After finishing these steps, you should have a `project3` directory
that includes the `project3.ipynb` jupyter notebook you will use for
this assignment.

You'll be able to get started on the assignment by running: `jupyter
notebook project3.ipynb` in the `project3` directory.

## Submission

You should answer the questions and write your code in this Jupyter
Notebook. (It is find if you prefer to organize your work some other
way, but if you do, make sure your answers are clear and complete in
the document you submit.) Parts where you are expected to provide an
answer (which could be text that can be written in markdown format in
the notebook or Python code that runs in the notebook) are marked in
green.
        
When you are ready to submit the assignment, you should **print your
notebook as a PDF file** (unlike previous projects, you do not need to
submit your repository or source notebook). You should check that the
printed PDF does contain all your answers and that they are readable
in it. Then, send a message in slack to a channel that includes both
team members (so the one sending this message should include the other
team member) and all of the course staff (`dave`, `Hyun Jae Cho`, and
`Anshuman Suri`) and attach the printed PDF to that message.
