# LearnJsWithFlappy

I have created this repository for my son. After learning the basics of JavaScript programming, we agreed that it would be nice to sink his teeth into a practical example. This repository is meant to help him by giving him concrete tasks that follow a logical pattern and not to provide copy and paste code.

## Make this your own repository
A repository is the **Git** term for all the files of this project saved on Github. ```Git``` is a source control system used by most developers. Source control systems let you save your files to a remote site and track all changes you made. If you ever want to go back to a previous version, you can. It is also a great way to work together with other developers.

In order to make changes to the template code you will need to make a copy of this repository. 
1. Create an account on Github. 
2. Creating a copy in **Git** terms means creating a **Fork**.
   - Hint find the **Fork** button.

In Git, cloning a repository means that you download it to your local computer. You will use this local downloaded version to create your own files.
1. Start Visual Studio Code
	- If another project or folder is open in Visual Studio Code, close it.
2. Find the Source Control tab.
3. Clone your newly forked Git repository.
   - Find the address to clone on this page **OF THIS FORK** on Github. Hint: **Code** button.
   - The clone action in VS Code will create a folder called like you named your **Fork**. If you left it the same as the original repository it will create a folder called ```LearnJsWithFlappy```, plan accordingly.

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
The page opened in your browser is now called **Phaser - Template**. That just won't do. We are going to change the name of the page.
1. Open the file called: ```index.html```
2. Find the title there and change it to something more suitable.
3. See the changes happening to the name on the tab of your browser.

## Empty the Game.js file
The game will be mainly running in the ```Game.js``` scene. In order to start creating the game we need to remove all current 'game logic' so we can create our own.
Tasks:
1. Only one function should be edited.
2. Leave the logic for the background for now in place.
   - Make sure to only show the background picture. 
   - Remove the the background color
   - Remove the transparancy on the image. (alpha channel)
3. The rest of the logic can be removed.
4. Check in the browser to see if this has the expected result. 

## Skip the MainMenu for now
Each time the page loads, first the main menu is shown. This is great for when the game is in production. But when you are developing the game, it is enoying. 
1. Follow the logic of how the game starts up. Check this in the ```main.js``` file. The first scene loaded is the first scene in the list of scenes.
2. Once the first scene loads it will tell what next scene to go to. Check this by opening the first scene in the list, and verify what scene will be next.
3. The Boot and Preloader are scenes that perform a function but don't show anything on screen.
4. At some point the MainMenu is called as next scene. 
5. Change this to the Game scene.

## Save your changes to Github - or commit and push
In order to save your changes to Github you need to ```commit``` your changes and then ```push``` them to Github. 

OK, but what does that mean? Commiting your changes will save them to your Git repository on your local computer. Then ```push``` sends these changes to Github. Git is like a chain. You have a repository on your own computer. It is linked to another repository on the internet. In our case this is Github. Each repository can have another repository as its parent. In Git speak: Github is ```upstream``` and your local machine is ```downstream```.

So to get the your code onto Github you first need to save your files, then commit them to the local Git repository and then push them to Github.

Your tasks are then:
1. Save your files. (if you hadn't done that yet)
2. Commit your changes.
3. Push the commit to Github. (This is called Sync in VSCode)

## Syncing your Git fork with the gsenden/LearnJsWithFlappy
This tutorial is continuously changing. The things is though: you created your own fork of the original repository. Since new steps are being added, you would not see them, because the fork does not update automatically.

To update your fork, you will need to research how to do this.
1. Research how to update a Git fork.

## Syncing your Github repository with the repository on your computer
You have updated the Git fork on Github. But how do you get these changes to be applied and downloaded to your own computer.

In Git speak you want to ```pull``` the changes from Github to your local computer. 

The pulling of changes is something you will do regularly when working with other developers. They make changes to the code and ```push``` their changes to Github. 

But what would happen if the other developer had made a change in a file you also have been working on? When you ```pull``` changes from upstream, Git might detect changes in the same file. In that case you would need to ```merge``` the changes together. VSCode will show the two versions of the file. You will need to decide what to do with each change. For example, first take the change on line 12 from the file on the left and then the change on line 12 from the file on the right. Git is smart enough to not bother you if it detects no conflicts.

Tasks:
1. Pull the changes from Github.

## Add the player to the screen
Now it is time to add the player to the screen. The player is simply an image we want to add to the screen. So we could just use similar code then adding the background in the Game.js. 

1. Find an image. I suggest using free artwork. The rest of the tutorial assumes that you use https://github.com/samuelcust/flappy-bird-assets
   - Download the files. 
       - Hint: The green button also allows you to simply download the files as a zip.
       - Hint: You could also just clone the repository.
2. Save the images to the ```public/assets``` folder.
   - Copy the folder called ```sprites``` into the assets.
3. Load the image file and give it a name.
   - Use the Preloader to load the player image.
   - For now load the ```bluebird-midflap.png```.
   - Hint: Notice the relative path being set.
4. Show the player image on the screen.
   - Make the change in ```Game.js```.
   - Show the player image just like the background.
   - Maybe show the bird at x: 100 and y: 100

## Add physics to the player
The player character is currently just hanging in the air. When the player isn't hitting the fly button, it should fall down. Lets fix that.

In order to do this we need to add physics to the game. This is done by changing the configuration of the game. Let's change the config to add the physics.
1. Find the config data structure in the ```main.js``` file.
2. Search the internet for [phaser arcade physics](https://duckduckgo.com/?t=ffab&q=phaser+add+arcade+physics&ia=web).
   - You should find a page from the Phaser documentation. 
   - Read it and change the config in ```main.js``` accordingly.
   - Also add gravity for y axis 700
3. Save and see the glorius changes in the browser.
   
Huh? What? why isn't it working? 
--> We have added physics to the game, but we haven't exposed our bird to it.
Ok, we will need to rewrite a bit how we add the image to the scene.
1. Look at the Game.js file.
2. Change the part where you add the image 
   - Instead of adding the image to ```this.```, add it to ```this.physics```.
3. Save
4. See your bird falll

NICE!!! It falls. But... it falls of the screen.

## Add the ground
If we don't want the bird to fall of the screen we should create the ground. That way it will not fall of the screen.

The ground in contrast to our bird is a static object. It should not move when the bird crashes into it. 

Lets create the earth!
1. Load the ```base.png``` asset in the preloader.

Ehh chief: just a thought here: Where are we going to add the ground. What would be the correct x and y location to put it? --> At the bottom of the screen ofcourse!

Ah OK, lets calculate where that may be. In order to do this we need:
- The width of the screen.
- The hight of the screen.
- The with of the ground image.
- The hight of the ground image.

1. Search the internet for [phaser get screen dimensions](https://duckduckgo.com/?t=ffab&q=phaser+get+screen+dimensions&ia=web)
2. Write the x and y value out to the console. (Hint: console.log(`Hello ${name}`))
3. Check the values in the brower. (Hint: press ```F12``` and see the ```Console``` tab)

Next up the size of the ```base.png```. If you open it in VSCode it shows the image, but it doesn't show the dimensions. Luckaly VSCode allows us to install extensions who let us do that. 
1. Open the ```Extensions``` tab of VSCode.
2. Find and install Luna Paint.
3. Open the ```base.png``` and see in the bottom right corner the dimensions of the image.

Now we can do some calculations:
1. Calculate the right location for the position of the ```base.png``` at the bottom right of your screen. 
   - Use the variables of the screen dimensions.
   - Phaser will use the exact middle of ```base.png``` as its starting point.
2. See the [platform tutorial page](https://phaser.io/tutorials/making-your-first-phaser-3-game/part4) on the Phaser documentation how to create a group and add the ground to it.
   - Note that the 'ground' is the name of the loaded image.
3. Put the output of adding the bird image into a variable called ```player``` i.e. ```let player = this.add...```
4. Create a collider between the platforms group and the player.
   - See [part 6 of the tutorial page](https://phaser.io/tutorials/making-your-first-phaser-3-game/part6)
  

