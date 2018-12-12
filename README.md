# Kandy-Kkrush

It's a Desktop Game Application that allows the player to crush candies by aligning them in specific arrangements.

This project is made using java, more specifically, applet, AWT and some Data Structure concepts.


# HOW TO RUN THE PROGRAM:

  1. Open the command prompt.
  
  2. Make sure the path is set properly.
  
  3. Compile file using javac MiniProject1.java
  
  4. Open Applet window by appletviewer MiniProject1.java
  
  5. Make sure that the audio file and all the class files of the program are in the same directory.
  
  6. Program should work perfectly fine.


# PROBLEM DEFINITION:

Create a Game and design GUI designing using AWT. The game contains swapping of candies
in minimum group of 3 to delete the candies in vertical or horizontal fashion. There are 31
types of candy, simple candies, stripped candies that burst the whole vertical line, stripped
candies that burst the whole horizontal line, wrapped candies that burst the candies
adjacent to them and colour bomb that burst many candies. The special candies can burst
only with normal candies. Two or more burst candies cannot burst with each other. And so
is with colour bomb. At the start of the game, a soundtrack is played in loop and the candies
fill in the grid matrix as in a falling down effect. A timer in decreasing order of time and a
score board is maintained. After the game timer becomes zero then the game stop, so does
the sound track and the “Game Over” sign appears with a “you win” or “you lose”
depending on the score.


# LIBRARIES USED: 

The packages used are util, awt, event.
In the awt.event package we have used ActionListener , MouseListener, Runnable interface.
We have used in-built data structures like stack, queue, linked list, hash set in the util
package


# EXAMPLE:

![alt text](https://raw.githubusercontent.com/chheda-r/Kandy-Kkrush/edit/master/Example of kandy kkrush.png)

![alt text](https://raw.githubusercontent.com/chheda-r/Kandy-Kkrush/edit/master/Example of kandy kkrush 2.png)


# How does this project works ?

When we open the applet the game loop starts. Now is divide in to three phases, in the first
phase:- the background will be set to color, in the game phase 2 in the main grid tiles will be
printed depending on the level, now the candies will come down till the tiles are not filled .
the 3 rd game phase is divided into 6 gamestages. The game remains in gamestage 1 till there
is a mouse click. In the gamestage 2, according to the mouse click the candies will be
exchanges. If the 3 candies are coming in line then the game will go to gamestage 3 or if
they are not in line they will get exchanged then the game will go to gamestage 1. In the
gamestage 3, the function performcandycrush of class candy crusher will be called. Now this
method, will delete all the three candies which are in line. If there is a special candy then it
will not be deleted, it will be added in queue. Now the grid matrix and the queue will be
returned. Now in the game stage 4, burst specialCandy of cy the front element of the queue
will be removed. Now the removed element willgive us the position of the special candy.
The candy at that will be deleted and as it is a special candy it will delete the corresponding
candy depending on the function and any these delete candy is a special candy then it will
not be deleted and then it will be pushed in the queue. Now the method will return the
queue and the grid matrix. Now it will go to gamestage 5 now all the empty tiles will be
filled with a=candies by using fillemptycandy method. Now if the queue is empty then go to
gamestage 0 or else go to gamestage 4. A score vaiable is used to keep track of score
whenever there is candy crush. By using multithreading a timer was created and it was
decremented after every second. When the counter becomes 0 then the game will go in the
gamephase 4. In this phase it will be checked whether the current score is greater than
required score or not. If yes then You won is printed or else you lost is printed and game is
exited. An audio sound was played when the game was running and it was stopped in
gamephase4.

