##### Understand what licensing is
* [Licensing a Repository](https://help.github.com/en/articles/licensing-a-repository): A GitHub guide on how to license a repository
* [Choose a license](https://choosealicense.com/): A GitHub Page to help you decide which is the right license for your project

* Do the following exercise in pairs:
1. Create a LICENSE file in your previously created repository. Add the MIT license in it, commit and push.

##### Undoing things
1. Undo a non-staged change in one of the files
2. Undo a staged change in one of the files
3. Undo a commited change in one of the files
4. Reset your master branch to an older commit (your changes will be lost, add a new fake commit if you don't want to lose it!)

##### Create a branch to split your development
1. Create a branch called `new-data` and add a commit to it with a new file called `data2.csv`.
2. Checkout your `master` and check the files that you see. 
3. Create another branch from `master` and check the files that you see. Add two commits to it in any files.
3. Checkout your master again and checking the files at each step, merge both branches into it.
4. Visualize with `git log --graph --oneline --decorate --all` what happened.
