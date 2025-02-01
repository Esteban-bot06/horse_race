# horse_race
*	 **Overview:** This program is about simulating a horse race by making each horse move randomly along a track, printing the race progress, and determining which horse reaches the finish line first. The process continues until a horse wins, at which point the program ends.

## list of functions

*	There's gonna need to be a *main()* function where we are going to call the other functions to make the program work, but first, it initializes the random number generator using *srand(time(NULL))* so that each race is different. Then, it creates an array called "horses[]" where all elements are set to zero to represent the starting position of the horses. The program enters a while loop where it repeatedly moves each horse using the *advance()* function, prints their progress using the *printLane()* function, and checks if any horse has won using the *isWinner()* function. If a horse wins, the loop stops, and if not, the program asks for user input to continue or quit.

*	*printLane()* function is where we visually display the position of each horse on the race track. It takes two parameters: the horse number and the horse[] array. The function runs a loop that prints dots . to represent empty spaces, and when it reaches the position of the horse, it prints the horse number instead. This function helps visualize the race step by step.

*	*isWinner()* function checks if a horse has reached the end of the track. It takes two parameters: the horse number and the horses[] array. Inside the function, it declares a boolean variable called winner and initializes it as false. Then, it checks if the current horse’s position is greater than or equal to the RACELEN - 1, meaning it has reached the finish line. If so, it prints a message declaring that the horse is the winner and returns true, stopping the race.

*	*advance()* function moves a horse forward randomly. It takes two parameters: the horse number and the horses[] array. Inside the function, it declares a variable called coin that generates a random number between 0 and 1 using *rand() % 2*. Then, it adds this value to the horse’s current position in the horses[] array, effectively making the horse move forward by either 0 or 1 spaces each turn.

*	The user is also prompted to press a key to continue the race or enter 'q' to quit. If the user enters 'q', the program prints "Quitting the game" and exits the race loop.
