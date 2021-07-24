# Risk-Battle-Simulator
Risk was one of my favorite games to play in the 80's with my high school friends. We would typically have 4 or more players, and during the course of the game pair up with another player to attempt taking out everyone else, before starting the really large battles to see who would eventually domininate the world. When the number of armies involved starting approaching 100 or more, far too much time was spent rolling the dice to determine the eventual winner of each battle. If only we had thought to write one of these simulators on the programmable calculators of the day, could more time be spent on strategy, and less on rolling dice, to avoid the long delays other players had to endure waiting for their turn.

This program address that problem square on, by both showing the actual dice throws on screen for each player (which can be slowed down<sup>1</sup> if there's any doubt how the dice throws are being read to determine who loses an army), and bringing about a rapid conclusion, usually within 8 to 15 sec for battles of up to 100 defending armies. The code was written so that it honors all of Risk's rules for Attack, such as the maximum number of dice each player can use, which dice to compare to determine outcome, how ties are handled, and how long can the battle continue based on armies remaining. These are shown below, for reference.

* The attacker can roll up to 3 dice, and have at least one more army in the territory they're attacking from than the number of dice being rolled. The more dice they roll, the higher their odds of winning.<sup>2</sup>
* The defender can roll up to 2 dice, and have at least the same number of armies in the territory they're defending. The more dice they roll, the higher their odds of winning.<sup>2</sup>
* Battle outcome is determine by comparing the highest dice each from the attacker and defender. If the attacker's dice is higher, the defender loses one army from the territory under attack. If less or a tie, the attacker looses one army from the territory leading the attack. If both players rolled more than one dice, compare the two next-highest dice and repeat using the same process.
* Battle continues until there is only one army remaining in the territory leading the attack, or the defender has lost all of their armies in the territory being defended.<sup>3</sup>

Battle<br />Scenario | Attacker's<br />Dice | Defender's<br />Dice | Battle<br />Outcome
:-: | :-: | :-: | :--
 1        | 6, 1, 1  | 3        | Defender loses 1 army. 
 2        | 3, 3     | 4, 3     | Attacker loses 2 armies. 
 3        | 6, 2, 1  | 3, 2     | Attacker and Defender both lose 1 army. 
 4        | 6        | 5, 4     | Defender loses 1 army. 

Notes:
1. Press the white button beneath the OK while the dice throws for each battle are being displayed in rapid succession on the LCD screen. Doing so will slow down the updates so you can verify the rules are being followed. The army totals for each player are updated based on the dice results from the previous screen update. Additional presses of the OK button will slow the updates even more, until finally the updates return back to their rapid mode.
2. The program automatically rolls the maximum number of dice for each player to give the best odds for both. The only way to circumvent this to select less than 4 attacking armies, since the program will automatically reduce the number of attacking dice to maintain one army in the territory leading the attack. It also reduces the number of defending dice when there are less than two armies remaining to defend the territory.
3. You can stop the battle at any time, by pressing the white button beneath the Edit button to clear the results and start a new battle, or exit entirely pressing the white button beneath Quit. The application was designed so that you could focus on the game, and generate battle totals quickly. with the least number button presses.
