# Building with Plumo (Developers)
## Understanding Zero-Knowledge Proofs (ZKPs)

### In this tutorial, you will learn about how you can use Plumo in your own projects by building a simple game that can read data from the blockchain. 

## Understanding Plumo
Plumo is a powerful tool for blockchain developers as it allows your users to obtain full-node capabilities while maintaining a small runtime and memory fingerprint. Learning how to use Plumo can allow you to develop more secure applications for your users. Plumo is also an amazing example of how ZKPs can be used to deliver security without compromising privacy.

## What is Plumo?
Plumo is a zk-SNARK based system that allows mobile and resource constrained nodes on the Celo network to sync to the Celo blockchain faster and with less data. It accomplishes this by using zero-knowledge proofs, which allow the quick verification of the chain syncing computation without having to run it locally.

## How Does Plumo Work?
Celo clients are pretty light weight, due to proof of stake, and they only need to download epoch block headers, and BLS signatures that are used to aggregate validator signatures. Plumo takes this one step forward being 17,000 times lighter, with zk-SNARKs allowing light clients to quickly verify transitions from epoch X to epoch X + Y, where Y is hundreds of epochs. So instead of needing to verify each epoch, light clients can "hop" from SNARK to SNARK until they reach the latest proof. From there, they can download the remaining epoch block headers to sync to the head of the chain.

## Building on Plumo
Next, we will build a game to show how much CELO is in a wallet by clicking on a treasure chest. The information will be fetched from Plumo and we will be able to verify its correctness. Plumo is an important tool allowing developers to build lighter and more responsive applications while minimizing dependence on a full node. After completing this tutorial, you'll be able to use Plumo in future projects where you would normally require a full node to call on-chain queries.

## Node.js
Follow the official nodejs installation https://nodejs.dev/en/learn/how-to-install-nodejs/
To verify that it's installed correctly, open your terminal () and run node -v and npm -v .
## VSCode
You can download VSCode for your operating system from here https://code.visualstudio.com/
## Git
Follow the installation instructions https://git-scm.com/downloads.
Follow the setup guide https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup 

## Clone Repo
After setting up your environment, review the following instructions to clone the tutorial repo and install the dependencies. This will contain all of the game assets and some simple game logic - having these materials will ensure that you can focus on Plumo for this tutorial.

```git clone https://github.com/upright-vc/tutorials.git```

```cd tutorials/PlumeChest```

```npm install```

# Review the Files
After cloning the repo, let’s view what files and folders are included
## Descriptions
```index.html``` is the starting point of our game, this is the file that will open up in the users browser and load all our code and game assets.

```src``` - this folder contains all the game logic, for more information have a look at phaser docs.

```index.js``` creates a new game instance, and holds all the settings describing the way in which Phaser.js will render our game.

```assets folder``` holds all the game assets, including pngs and configuration files for these assets. 

```scenes folder``` contains Phaser scenes. You can think of these as game levels, where each level would have its own scene. Our game is very simple and contains only once scene.

## Run the Game
After familiarizing ourselves with our materials, let's test out the game by running the following code: 

```npm start```
You should see a browser tab appear, with the URL: http://localhost:8080/.

If the browser tab does not appear, then you can manually navigate to the URL. After the game loads, you will see the following image: 

![Screen Shot 2024-07-17 at 1 47 27 PM](https://github.com/user-attachments/assets/e7f2549e-c7d0-4177-a1e6-e72948407f28)

In this simple game, after the user clicks on the treasure chest, the CELO balance for a specified address will be retrieved and displayed on screen.

Gmail:aladejamiudamilola@gmail.com
