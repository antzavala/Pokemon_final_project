# Pokemon_final_project
In our version of the pokemon game, there are 9 pokemon across three types (fire, water, grass). Each pokemon is assigned three attributes; type, hp, and strength.
The rules of the game are similar to the card game(?). At the beginning, a person is given a randomly assigned pokemon as their starter.
The player then chooses which gym they are going to fight their pokemon in. The options are fire, water, and grass, and their pokemon will be randomly assigned to fight a pokemon which is of the type that corresponds to the chosen gym. The two pokemon battle each other, with an algorithm determining the winner given the two pokemon, taking into account the types, strengths, and hp of each pokemon. If the pokemon is fighting a pokemon it is weak against (fire is weak against water, water being weak against grass, and grass being weak against water), its strength is cut in half. The number of strikes it would take of the altered strength of each pokemon to deplete the other’s hp is calculated, and whichever pokemon requires fewer strikes wins the match. The matches are repeated with the player being given the opportunity to choose a new gym each time, until either the player or opponent wins two matches.

Instructions
Upon opening the game the player is prompted to type Start(). After doing so and pressing enter they are assigned their starter and prompted to choose their gym, which they do by typing ‘fire’, ‘water’, or ‘grass’. After doing this they are assigned an opponent and told the results of the match. They are then prompted to choose a gym again and repeat the process until they are told they have won the game or lost the game.
Features
     
 1. Organized text UI
2. Extensive use of Object Oriented programming
Justification for Complexity
We used object oriented programming to set our pokemon and give them characteristics. Each pokemon (instance) has a name, a strength rating (an integer) and hp (which means their health level/ resistance to strength, also an integer), and a type. There are 9 pokemon and 3 different types. Each instance attribute is taken into account to determine who wins a match.
We implemented an algorithm to determine who wins each match, by taking into account the types of each of the two pokemon as well as their respective strengths and hp. The algorithm edits the strength to reflect whether the pokemon is fighting a pokemon it is weak against. The winner is determined by dividing the hp of each pokemon by the updated strength of the pokemon.
We also used organized text UI. The user is prompted to start the game and to type the gym. After each round, a print statement is displayed telling them if they won or lost the round and, and another one appears updating them on their score. Periodically, a print statement will appear with encouragement coming from a TA (which TA it comes from is assigned randomly). Out of the list includes Vednashh, Victoria and Stacey.
We used randomization to choose the pokemon for each match, as well as to choose a TA to offer encouragement throughout the game.
Lists & Script Variables
● Fire_gym, water_gym, and grass_gym list contain pokemon of each respective type.
This allows the choose_gym block to choose a pokemon with one of these types
● Script variables opponent_hits and starter_hits are assigned and calculated using the
stats of the pokemon called in fight(). Whichever pokemon has the lower number of hits wins.
Function Table
         Block / Function Name
Domain (inputs)
Range (outputs)
Behavior (role in the context of the project)
choose_gym
Gym, opponent_score, player_score
Calls fight
Assigns an opponent based on the gym the player inputs
type _impact
Opponent, starter
No output, changes strength of one of the
Lowers the strength of one of the pokemon that is a type that is weak
   
pokemon
against the other one, unless both input pokemon are the same type, in which case it does nothing
fight
Opponent, starter, opponent_score, player_score
Returns back to choose_gym if no one has won yet, or returns a message saying who won if someone has
Runs the algorithm to determine which pokemon wins using type_impact and the attributes of the pokemon. Updates score based on who won the match, and determines if the game ends or not.
Start
No input
Calls choose_gym
Begins the game
