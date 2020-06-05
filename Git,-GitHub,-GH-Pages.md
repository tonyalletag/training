# Learn to Code
## Git GitHub GH-Pages
### Details
This tech session is geared toward those that want to learn software development but may not know where to start. At the end of this session you will:

1. Learn the basic git commands
1. Learn the basic features of GitHub
1. Clone code repositories from GitHub
1. Modify code (HTML/CSS) and commit it to GitHub
1. Create a website and use GitHub's free hosting to publish it to the internet

### Steps to be complete prior to training
1. Download and install git https://git-scm.com/downloads
1. Create a GitHub account https://github.com/ 
1. Download a text/HTML editor
 * https://atom.io/

### Training
1. Create directory to store all your git projects
 * `mkdir git`
 * `ls`
 * `cd git`
2. Go to GitHub and create a new repository 
 * https://github.com/new
 * name your repository it "first-website" or something similar
 * Select Public
 * Select the check box to initialize the repository with a README
 * Select "Apache License 2.0" in the add a license drop down
 * Click "Create Repository"
 * You should now have 2 files in your firstwebsite git repository README.md and LICENSE
3. Clone your first-website git repository to your local machine
 * From a terminal run the following commands 
 * `git clone https://github.com/username/first-website.git`
 * `cd first-website`
 * `git help`
 * `git status`
4. Create a Master branch
 * Go to your first-website repository on GitHub https://github.com/username/first-website
 * Click Settings
 * Under GitHub PAGES go to Source and choose "master branch"
 * Go back to the pages section and choose a theme
 * Within your first-website repository you should see one branch in the branches drop down menu "master"
 * Switch to the gh-pages branch to see the files that were create
5. View your newly hosted website on the internet 
 * http://username.github.io/first-website/
6. Update your local repository to pull down the new branch and files added to your repository
 * from a terminal run the following commands
 * `git pull`
 * `ls`
 * `git checkout gh-pages`
 * `ls`
7. Modify your website
 * from a text editor open the index.html file
 * modify the content and save the changes
 * open the index.html file in a web browser to view the changes locally
 * Continue to make updates until your are ready to post to the internet
8. From a terminal run the following commands
 * `git status`
 * `git add index.html`
 * `git commit -m 'updated text content'`
 * `git push`
9. View your updates on the internet at http://username.github.io/first-website/

### Extra Credit
1. Use the wiki to teach someone else
2. Clone another repository
3. View someone else first-website on the internet
4. Modify the websites look and feel by updating the CSS
5. Clone another git repository
6. Submit a pull request to update a different first-website repository
7. Create a new website off a bootstrap template https://uicookies.com/free-bootstrap-resume-templates/ or http://startbootstrap.com/

### In Depth Training 
* https://www.udacity.com/course/how-to-use-git-and-github--ud775 
