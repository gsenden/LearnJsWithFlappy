# LearnJsWithFlappy

I have created this repository for my son. After learning the basics of JavaScript programming, we agreed that it would be nice to sink his teeth into a practical example. This repository is meant to help him by giving him concrete tasks that follow a logical pattern and not to provide copy and paste code.

## First things first - clone this repository
A repository is the **Git** term for all the files of this project saved on Github. In Git, cloning a repository means that you download it to your local computer. You will use this local downloaded version to create your own files.
1. Start Visual Studio Code
	- If another project or folder is open in Visual Studio Code, close it.
2. Find the Source Control tab.
3. Clone this Git repository.
   - Find the address to clone on this page on Github. Hint: Code button.
   - The clone action in VS Code will create a folder called LearnJsWithFlappy, plan accordingly.

## Install Node.js
We need a way to run the Javascript code on your local machine. For this reason you need to install Node.js. 
1. Do you already have Node.js installed? 
Great! lets skip this chapter and proceed to [Install all dependencies for LearnJsWithFlappy](#Install-all-dependencies-for-LearnJsWithFlappy).
2. Are you unsure if Node.js is already installed?
	- [Search for the answer on how to check if it is already intalled.](https://duckduckgo.com/?t=h_&q=how+do+i+know+if+node.js+is+installed&ia=web)
3. No Node.js yet on your local machine? No problem. Install it.
   - Find the Node.js website and follow the instructions.

## Install all dependencies for LearnJsWithFlappy
A typical Node.js project uses all kinds of libraries. This way a lazy, and thus smart programmer, uses already written code to in his own projects. These libraries the project depends on are called, wait for it, dependencies. Whoah I know. Totally unexpected. We will learn to deal with this.

Take a look at the dependecies:
1. Open the package.json file.
2. Look for the **devDependencies** and **dependencies** sections.
3. Note that are 2 types of dependencies:
   - For during development. 
   - For all cases. 
4. The **dependencies** will be used in both developoment and production. 
5. The **devDependencies** will only be used during development.

These depencies have been declared in the package.json have not been downloaded yet. You might wonder why not, since you just downloaded this whole repository. Well, since this is not our own code we don't need to store it in the Github repository. This saves space. Also, if you want to update to a later version of the library this will make things a lot easier.

Let's download the depencies and install them.
1. Open the terminal in VS Code. Hint: there is a menu called **Terminal**
2. Run the command ```npm install```
3. Wait for things to install
4. See that a new folder has been created called **node_modules**
5. All libraries have been downloaded here

## Run your project for the first time
Well lets see this project in action! 
1. Run the following command in the VS Code terminal: ```npm run dev```
2. Note that a line says ```Local: http://some_url:some_port ```
3. Holding the ```Ctrl``` button and clicking on the link opens the page.
4. Success!!! we have a running game!
5. Leave the game running for now.

## Make the game your own - make your first change
You didn't program anything yet. Lets change that. 
1. Make sure you can see both VS Code and the browser.
2. All edits that you make will happen real time.
3. All the files that make up your game are in the ```src``` folder.
4. The game is split up into different scenes. Open the ```scenes``` folder.
5. The first scene that is shown is the ```MainMenu.js``` file.
6. Search for ```this.add.text(512, 460, 'Main Menu', {```
7. Change ```Main Menu``` here to something more exiting. Something daring. Something crazy. Maybe even something boring, if you dare. 
8. Then save the file.
9. Watch the fruit of you labour!

## Change the name of page
The page opened in your browser is now called **Phaser - Template**. That just won't do. Wer are going to change the name of the page.
1. Open the file called: ```index.html```
2. Find the title there and change it to something more suitable.
3. See the changes happening to the name on the tab of your browser.