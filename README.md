# Project3

![GitHub last commit](https://img.shields.io/github/last-commit/vanessabau/projectTwo) ![npm version](https://badge.fury.io/js/inquirer.svg)

Final Phantasy is a computer game based around this app's inspiration, Final Fantasy, for the design and Earthbound gameplay mechanics. 

## Table of Contents

* [Demo](#demo)
* [Overview](#overview)
* [Usage](#usage)
    - [Accesssing Home page](#accessinghomepage)
    - [Navigating Store page](#navigatingstore)
    - [Levels](#levels)
    - [Final Boss](#finalboss)
    - [Victory/Defeat](#victorydefeat)
* [Tech and Methods Breakdown](#techandmethodbreakdown)
    - [Technology](#technology)
    - [Front-End](#frontend)
    - [Back-End](#backend)
* [Known Issues](#knownissues)
* [Contributors](#contributors)
* [Launch](#launch)
* [Future Development](#futuredevelopment)

### Demo

For the [finished web page](https://dry-mountain-58151.herokuapp.com/)

### Overview

Once logged in, users will battle monsters to obtain resources to buy materials needed to fight game levels. The goal is to defeat the final boss of the game. If the player beats the final boss, the person will get the victory page. If the player is defeated during any levels, the player will get a defeat page and can restart the game.

The application is made up of several pages:
1. Home
2. Signup
3. Store
4. Level #
5. Final Boss
6. Victory/Defeat

### Usage

##### Accesssing Home page

On the home page, the user can log into the game, but if the user cannot login, the user will have to signup using the signup page.

##### Navigating Store page

Once logged in the user will be redirected to the store page to buy equipment and potions. These items will increase stats of the player.

However, there is a limit on how many items a player can buy, because of limited currency call Gil. 

##### Level #

Once the player feels ready for combat, he/she can click on the "Continue Adventure" button. 

During Combat, a random enemy will be generated with its own stats. With the weapons and potions purchased, they can be used to increase the following:
- HP
- Attack
- Defense

There is a counter on the potions stats that tells how many potions are left.

To beat the level, player stats will subtract the enemy health pool, but be careful as enemy stats will also subtract player health as well.

Depending on outcome, player will gain more Gil and retain their stats for the next round or they will get the defeat page.

##### Final Boss

Final boss is the same concept as the level enemy but with better HP, attack, and defense.

Outcomes will depend on the players equipment and stats. The outcomes of the final boss will send the player to the victory page or defeat page.

##### Victory/Defeat

If the player beats the final boss, the victory page will show up.

If the player is defeated in any level, the defeat page will show up.

##### Login

Input your email and password. If credentials are wrong, page will reset.

##### Signup

Fill out form with all required information before clicking submit:
* First Name
* Last Name
* Email
* Password
* Confirm Password

Once done, click `Submit`. User will be redirected to login page.

### Tech and Methods Breakdown

##### Technology

* VS Code v1.47.1
* Node v12.16.1
* React.js
* Mongo
* req-flash
* express-session
* passport
* Bootstrap
* jQuery
* Adobe InDesign
* shields.io

##### Front-End

React JS allowed us to create separate pages with their own functions. They are connected to each other in the App.js under client folder, like a front-end router. API calls were used throughout the components that made up the pages.

##### Back-End

Database was made using Mongo. 

Back-end route starts with models -> controllers -> routes -> API 

Three models make up the database: item, stats, and user. 

User.js holds the first and last name of the user, as well as the email and password. Email and password are used to confirm user login and each new signup will have its own unique id.

Stats.js and item.js hold similar information for different purposes. Stats.js is used for the player progression while items.js is for the store materials.  

Api-routes was the in-between for the database and the front end. Passport was used to autheticate credentials when a user logs in. 

### Contributors

* Richard Biala
* Himadri SInha
* Yev 
* Garrett Hiebert
* KaiWei Shen

### Launch

Date [application](https://dry-mountain-58151.herokuapp.com/ releases: `July 21st, 2020`

### Future Development

* Alert user login data is invalid
* Add a map api to listings
* Allow users to post photos of their listings
* Allow users to reserve for a specific date
* Allow users to post and share more information to their profiles, such as photos