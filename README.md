# Risk-Battle-Simulator

![Screenshot of Risk-Battle-Simulator](https://github.com/yeri63-hp48g/Risk-Battle-Simulator/raw/main/Risk.png)

Risk was one of my favorite games to play in the 80's with my high school friends. We would typically have 4 or more players, and during the course of the game, pair up with another player to attempt taking out everyone else, before starting the really large battles and see who could domininate the world. When the battles starting approaching 100 or more armies, far too much time was spent rolling dice to determine the eventual winner of a territory. If only we had thought to write one of these simulators on the programmable calculators of the day, could more time be spent on strategy, and less on rolling dice, thus avoiding the long delays other players had to endure, waiting for their turn in the game.

This program addresses that problem head on, by both showing the actual dice throws on screen (which can be slowed down<sup>1</sup> to a crawl if there's any doubt how the dice throws are being evaluated), and shortening battle times to within 8 to 15 sec for battles of up to 100 defending armies. This application honors all of the rules stated in the game for attacks, such as the maximum number of dice each player can use, which dice to compare to determine outcome, how ties are handled, and how long can the battle continue based on armies remaining. 

## Risk Rules of Attack

* The attacker can roll up to 3 dice, and have at least one more army in the territory they're attacking from than the number of dice being rolled. The more dice they roll, the higher their odds of winning.<sup>2</sup>
* The defender can roll up to 2 dice, and have at least the same number of armies in the territory they're defending. The more dice they roll, the higher their odds of winning.<sup>2</sup>
* Battle outcome is determine by comparing the highest dice each from the attacker and defender. If the attacker's dice is higher, the defender loses one army from the territory under attack. If less or a tie, the attacker looses one army from the territory leading the attack. If both players rolled more than one dice, compare the two next-highest dice and repeat using the same process.
* Battle continues until there is only one army remaining in the territory leading the attack, or the defender has lost all of their armies in the territory being defended.<sup>3</sup>

To demostrate, here is an example of possible battle scenarios along with the outcome of each, based on the dice thrown by each combatant. The pairs are used to determine battle outcomes, created from the highest dice thrown by each. 

Attack<br />Dice | Defend<br />Dice | Dice<br />Pairs | Battle<br />Outcome
:-: | :-: | :-: |:--
1, 6, 1 | 3    | 6:3 | Defender loses 1 army. 
3, 3    | 3, 4 | 3:4<br />3:3 | Attacker loses 2 armies. 
2, 6, 1 | 3, 2 | 6:3<br />2:2 | Attacker and Defender both lose 1 army. 
6       | 4, 5 | 6:5 | Defender loses 1 army. 

Notes:
1. Press the white button beneath OK during battle to slow down the battle updates and observe the rules being followed. Army totals will be adjusted on the next screen update based on the current dice results shown here. Additional presses of the OK button will slow the updates even more, until finally the updates return back to their normal rapid pace.
2. The program automatically rolls the maximum number of dice for each player to give the best odds for both. The only way to circumvent this to select less than 4 attacking armies, since the program will automatically reduce the number of attacking dice to maintain one army in the territory leading the attack. It also reduces the number of defending dice when there are less than two armies remaining to defend the territory.
3. You can stop the battle at any time, by pressing the white button beneath Edit. This clears the fields to prepare for a new battle. To exit entirely, press the white button beneath Quit. The application was designed so that you could focus on the game, by generating battle totals quickly with the least amount of effort.
