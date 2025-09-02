# datafieldscourse
Analysis of Geophysical Data Fields

In this course we will use Jupyter Notebooks to turn in assignments on GitHub. To manage the Python environments in which we'll code, we'll use `conda`. If you already know about those things, you're all set!

To install `conda`, install `miniconda` [as described at Pythia](https://foundations.projectpythia.org/foundations/conda/). You'll also learn a bit about how it works. You can also just jump [straight to the installation instructions](https://docs.conda.io/en/latest/miniconda.html):


To install Git, follow the set of [platform-specific install instructions](https://github.com/git-guides/install-git). On Mac and Linux you should already have it. On Windows, if it asks if you want Git Bash, say yes.


You will also need a GitHub account. The [free one](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account) is all you need. There are some additional benefits if you [verify yourself as a student](https://docs.github.com/en/billing/managing-the-plan-for-your-github-account/discounted-plans-for-github-accounts):


We'll be using Jupyter notebooks. I like using Jupyter Lab so that I can open multiple notebooks at once.

## Creating a repository for homework.
Once you have a GitHub account, please create a private repository for your homework. Use the same repository for all assignments, and add a new notebook for each assignment. 

Please do the first homework individually, which will make sure everyone is set up to contribute to later homeworks. Homeworks 2-6 can be done as group assignments.

Please use only one repository for the whole course. This will allow you to import code that is shared across homeworks, instead of having to copy it into each notebook separately. for this you'll use a `.py` file, which in Python is known as a module.

```
/Homework1.ipynb
/Homework2.ipynb
/util.py
etc.
```

In either notebook, once you have created the util.py file, you can then import anything you need from util.py with
`from util import my_function`

If you plan to work in a group, please identify your group as soon as possible, and add them all to the repository as collaborators. If you're working together, please also see the section below on using Forks and Pull Requests to help avoid conflicting versions of files.

Finally, please invite Eric (@deeplycloudy on GitHub) as a collaborator on your repository. When you turn in homeworks, you will email me that you're done with changes on the repository, and I'll pull your changes and push a graded notebook back to the repository.

For homework 1, I will push an `environment.yml` file to your repository, along with the first homework. You will use the `environment.yml`  to create a conda environment for the class.

To get ready to work, clone your repository, go to a terminal (or git bash) on your computer, and move to a directory (using the `cd` command), and clone the repository:

`git clone https://github.com/username/my_repository.git`

This will replicate the version online to your computer. Then you can create an environment, and 

```
cd my_repository
conda env create -f environment.yml
conda activate atmo5331
jupyter lab
```

From that interface you can open and edit Homework 1. After you've made changes that you like (you can do this at any time), you can go back to a terminal where your notebook is located, and commit your changes, and push them to GitHub:

```
git add Homework1.ipynb
git commit -m "Added my name to HW1"
git push
```

You can add more than one file before committing and pushing your changes to GitHub online. Git might ask you for an access token instead of a password. You can set one up by following the instructions here:

https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens

### Working with multiple people (or on multiple computers) on the same repository

If you are working in parallel with others, or are working on multiple computers, and want to pull in changes from GitHub, you can go to your repository's directory and run `git pull`. 

Be careful to have only one person push changes at a time, or even better, use GitHub's Fork and Pull Request functionality to manage changes. When working with multiple people on a repository, it is very important to "git pull" to get others' changes before making your own to the same file.

To learn about this process, see the Pythia instructions on [Forking and Pull Requests at GitHub](https://foundations.projectpythia.org/foundations/getting-started-github).
