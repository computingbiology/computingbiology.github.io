+++
date = "09 Feb 2022"
draft = false
title = "Project 2: Sequence Alignment and Analysis"
slug = "project2"
+++

<div class="due">

<center>Due: <b>Thursday, 24 February, 7:59pm</b></center> 
</div>

#


<div class="yellownote">
 <center>
       <b>Collaboration and Resource Policy</b>
    </center>
    For this assignment, you are encouraged to work with one other person. Your team must satisfy these constraints:
    
   1. You **did not work together on Project 1**.
   2. You and your partner have a **total number of siblings that is divisible by two** (e.g., if you have one sibling, you need to find a partner with 1, 3, 5, or 7 siblings. If anyone has more than 7 siblings, they can partner with anyone!)
    
We expect most students will have the best learning experience on this assignment by working with a partner, but if you prefer to work alone it is okay to do this assignment on your own.
    
You are permitted (actually _encouraged_) to discuss these problems with anyone you want, including other students in the class. If you do discuss the specific questions in the assignment with anyone other than your assignment partner and the course staff, though, you should list them in the _External resources used_ section below.
    
You are welcome to use any resources you want for this assignment, other than ones that would defeat the purpose of the assignment. This means you should not look at answers or code from any other students in the class (other than your collaboration with your partner), and if you find code that implements the problem you are being asked to do for the assignment, you should not use that code. You should document all external resource you use that are not part of the course materials in the _External resources used_ section in your submission.
</div>

## Getting Started

To get started on Project 2:

1. One of your team members should **create a new repository** named `csbio-project2` (you can pick a different name if you really want to).

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

3. Add the course staff to your repository by following the same steps
to add `evansuva`, `hyunjaecho94`, and `iamgroot42` to your collaborators with "Read"
privileges. <font color="red">Be aware that this will allow the course
staff to see everything you put in the repository!</font> If you are
worried about having rants against the course staff in your repo, you
could work in a different repository and copy your finished project
into a new repo to submit it, but this seems like a lot of
hassle. Hopefully you don't have any rants about the course staff, but
it is best to put those rants somewhere else and share your repo when
you create it so you don't forget to share it later.


###

4. **Clone the empty private repository to your working environment.** Instead of _mygithubname below_, use your github username.

```plaintext
    git clone https://github.com/mygithubname/csbio-project2.git
```

You should see:
```plaintext
Cloning into 'csbio-project2'...
warning: You appear to have cloned an empty repository.
```

5. Enter your `csbio-project2` directory (`cd csbio-project2`).

###

6. **Fetch the assignment** skeleton from our repository into your private repository. Enter the working directory of your empty repository and add a remote repository named course, merge the code, and push it to your private repository by executing:

```plaintext
    git remote add course https://github.com/computingbiology/Project-2-Genome-Alignment.git 
    git pull course main
    git push --tags origin main 
```

After finishing these steps, you should have a `project2` directory
that includes the `project2.ipynb` jupyter notebook you will use for
this assignment.

You'll be able to get started on the assignment by running: `jupyter
notebook project2.ipynb` in the `project2` directory.


