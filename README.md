# Discord-RPG-Bot
A Discord bot with a toolset to allow it to perform basic upkeep in an RPG, such as rolling dice and drawing cards. 

Requires the installation of discord.py, which can be gotten through pip.  

Note that you will have to run it directly through your command line via py-3 (filename).py, with (filename) being whatever you call the file. 

Also note that I wrote the first draft of this bot a month or two prior to a large update to the discord.py package, and thus not all of the commands function as they should. As of this moment most of the commands should function according to plan.

As of this point in the bot's development, it has the following feaures. 

1. A Deck. A deck serves as a deck of playing cards. It can:

    A. Be shuffled, with the !shuffle command via the shuffle function.
  
    B. Be drawn from with the !draw command via the drawfromdeck function. 
  
    C. Discard a card given to it by a player, using the !discard command and the discardto function.
  
    D. Allow the player to draw from the discard pile using the disccarddraw function.

2. A Card. A card consists of a suit and a value, and will return those with 'getsuit' or 'getvalue'. 


3. A Playergroup. Within the context of a game, the playergroup consists of all people who can play.

    A. Players can enter the playergroup with !dealmein and the dealmeinfunction. 
  
    B. Lets the player draw a card and gives it to the relevant hand.
  
    C. Displays the player's card depending on the player's ID. 
  
    D. Allows the player to discard a card from their hand. 
  

4. A Player. A player exists in the context of the group. Each player has a Hand. Eventually they will have other stats such as HP, STR, etc. Currently the player exists as a holder class for a Hand, however. 
    

5. A Hand. This is the way that the player can interact with the game in the context of cards. Can:

    A. Draw a card with drawcard or the !draw command.
  
    B. Display cards with !displaycards and the !displayhand command
  
    C. Discard cards with the !discard command. 
  
  
6. A Hiddenhand. Has no discernable function at this time. Eventually will serve like a hand in poker


7. A Dealer. Eventually will be able to manipulate players' hands. 


8. Dice functions. These are:

    A. Roll function. When prompted with !roll and a string of characters akin to DnD dice notation of XdY, where X refers to the number of dice and Y refers to the number of sides on those dice. It will then roll the dice in that manner. If it doesn't receive that, it'll throw an error message. Eventually will include the possibility of bonuses (ie + and -). 
  
    B. Charoll function. In DnD, stats are often determined by rolling 4d6 and discarding the lowest roll. This does that, and shows the player all 4 rolls to satisfy their curiosity. 
  
  
The commands accessible to users are as follows: 

Dice-related: 

!roll XdY: Rolls X number of Y-sided dice. If no such notation is provided, it will not roll anything.

!charoll: Rolls 4d6 and discards the lowest roll. 


Card-related:

!dealmein: Allows a player to join a game. The player cannot draw cards otherwise. 

!shuffle: Shuffles the deck. 

!draw: Draws a card for a dealt-in player. 

!discard: Discards a card from the player's deck. 

!discarddraw: Draws a card from the discard pile. 


I will upate functions as I add them.

Completed goals thus far: 

1. Actually remembered how to run this script. 

2. Updated bot-messaging commands to actually run instead of throwing an error. 

3. Updated display-hand function so that it would actually display the player's hand

4. Fixed discard function. 

5. Fixed charoll function. 


Current goals:

1: ~~Update code to gel with updates to discord.py~~ should largely be complete. I'm keeping this on probationary status just to be safe. 

~~: Bug/error fixes, troubleshooting, etc.~~ currently moved to an as-needed basis. 

3: Comment code properly for collaboration with people other than myself. 

4. Improve the hiddenhand function. Could probably just change the displayhand functions to PM the user. 

5. Flesh out the dealer. Currently it exists as another player, which really isn't how it should work.  Give the dealer fancy abilities like discarding a card from a player's hand, etc. 

(X???). Get player stats involved. HP, basic DnD stats, etc. Not an immediate concern for the future. May not be necessary at all. 
