## Read Me
### _A simple exploration into the unknown world of Github pages_

## Mission:
1. Create an inital project repo
2. Add a Main project landing page with one additional page
3. Isolate the "project site" from the main repo projects code base.  
 ### Creating the project repo
- create the repo on github.com under your account
- clone the repo locally to your favorite directory
 ```sh
  git checkout repo-name
  ```
- go to your new directory and create a readme.md file. 

- edit repo locally, save, and add (stage) all files
```sh
git add . 
```
- commit all changes and add a message of you intent -- ex: create_readme_file
```sh
git commit -m initialcommit
```
- You will be in the master branch *most likely*
- Rename the "master" branch to "main"
 ```sh
 git branch -M main
 ```
- push you changes up to github repo
 ```sh
 git push -u origin main
 ```
## oops and oboys
- use quotes to "to state your intent" on a commit to make it legable. 
```sh
git commit -m "my intent with this commit is"
```
- make sure you actually saved the file locally. CMD + s or whatever your IDE requires. Git does not auto save you work. 
> _git is magic_, but it
>  ONLY saves the
> work you tell it to.
> You've been
> warned.