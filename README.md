## Read Me
### _A simple exploration into the unknown world of Github pages_

 ## Mission:
1. Create an inital project repo
2. Add a Main project landing page with one additional page
3. Isolate the "project site" from the main repo projects code base.  
 ###  Creating the project repo
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
- use quotes "to state your intent" on a commit to make it legable. 
```sh
git commit -m "my intent with this commit is"
```
- make sure you actually saved the file locally. CMD + s or whatever your IDE requires. Git does not auto save you work. 
> _git is magic_, but it
>  ONLY saves the
> work you tell it to.
> You've been
> warned.
## Add a main page to our repo 
 In our github repo for this project there is a Settings tab to the right at the top of the page. 

 Scroll down to the "GitHub Pages" element
.

Selecting the button in the "Source" pane that says "None." Change it to the "Main" and Save.

You will now see a /root
folder and above that a url. 
> your site is ready to be published at https://
> repo-name.github.io/project-name/

clicking on the link will take you to the your landing page.

If you created a read me file it will be displayed. If not thats ok. Were going to make an index.html page and add that to our project.    

In your local repo create an file named index.html in the same directory as you readme.md file.

- Put some basic html code in this file. 
- Save the file...remember the warning about saving? 

```sh
git add .
git commit -m "add a landing page"
git push -u origin main
```
Now when we refresh the page we went to earlier - after some github magic time - our index page is now rendered in the browser.

## Let's add some styling 
```sh
git checkout -b styling
```
We are going to make a branch, check it out, and call it styling.

Our IDE should now reflect our new branch "styling" 

In the project create a styles.css file and create a link to it in the index.html file
just below the title tag 
```html
<title>Document</title>
<link rel="stylesheet" href="styles.css">
...
```
save the files then 
```sh
git add .
git commit -m "add style"
git push origin styling
```
we are pushing this branch up to the repo. 
We need to create a pull request and then merge the changes into the main for the changes to take effect. 

Goto the Github repo to pull and merge the changes. 

Then refresh the page with to see our changes.

_it may take a minute for the magic to work_

## Lastly we want to isolate the site "github page" from our maincode base repo.

_this just keeps the files a bit more orgainized_

- we will create a new branch to do this work in and push it to the origin on the repo.

```sh
git checkout -b site
git push origin site
```
_note: we did not make any changes to the code._

- now go to the github repo and the "site" branch should be available.
- go back to the settings tab and scroll down to the "github pages" pane. 
- in the dropdown change the "main" to "site"

This tells github pages to look in this branch for the details source to render.

DONE.

### Magic time: 
- we are going to switch branches back to main and delete the 
> index.html

and 

> styles.css

This will only keep the Github pages site separate from the main codebase. And we can work on the site without interfering with any code in the main or anyone working on the main or a branch from main changing the site content.

```sh
git checkout main
```
- delete the index.html and styles.css file in this branch.

```sh
git add . 
git commit -m cleanup
git push origin main
```
if you look in the code section on the "main" branch there is only the readme file. 

switching to the "site" branch shows the structure files of our site. 

So any further changes to the site MUST be made from the "site" branch or a branch of the site. 

_Note: this will not ever be in sync with the "main"._