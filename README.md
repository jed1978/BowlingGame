Bowling Game Kata
=================

[bowling-score]: http://www.wpclipart.com/recreation/sports/bowling/bowling_scoresheet_example.png "bowling score card"


## Scoring bowling

![Bowling scoreboard][bowling-score]

一局保齡球的計分方法以十格計分格為計算原則 , 球手需在每一格儘量打中全部球瓶。如未能一投全中，可多投一球。

每一個計分格所得的分數是該格所投球瓶總數(即在該格的投球擊倒球瓶多少支就有多少分數)，但如果能在第一球打全中，該格所得分數會加上後面所投二球所擊倒的瓶數；如打補中，該格所得分數會加上後面所投一球所擊倒瓶數。每一個計分格的分數會累積到下一個計分格。

**在第10個計分格亦以同樣方法計算，即如果在第10格打到補中或全中就可額外多打一球或二球以計算第十格的累積總分。

Strike(一個計分格中的第一投擊倒十支瓶) , 當格分數會加上後面所投二球所擊倒瓶數  .

Spare(一個計分格中要用二球擊倒十支瓶) , 當格分數會加上後面所投一球所擊倒瓶數  .


## The requirements

* Write class "BowlingGame" that has two methods
	- *roll(pins)*
		- called each time the player rolls a ball. The argument is the number of pins knocked down.
	- *score()*
		- called only after the very end of the game. Returns total score of the game.


## Quick design session

One game  
A game has 10 frames  
A frame has one or two rolls  
The tenth frame has two or three rolls. It's different from all the other frames  
The score function must iterate through all the frames, and calculate all their scores  
The score for a spare or a strike depends on the frames successor
