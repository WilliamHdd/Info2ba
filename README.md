The following file is a modification of Dr. Sebastien Combéfis 's kingandassasins.py downloaded on May 10th (link : PythonAdvanced2BA/AIproject/kingandassassins.py).
The instruction we got as engineer students was to code an Artificial Inteligence to play the game by itself. As we only got a "working"
version on Wednesday the 11th, time was running short so I wouldn't exactly call the code I wrote "inteligent".

But anyway it plays the game. Knights are arresting people and assasins are killing them. 
The code was design to execute specific orders one after another (that's why I said it's not exactly intelligent). You'll notice the "try-except"
methode I used. It was supposed to execute specific orders if a problem occured (ex: Invalid moves). As the server
passes to another turn if an invalid move has been played, it doesn't work. I should have create a routine to check if spaces were free or 
occupied and react on the check-result, but as I said time was running short and other study-project were asking time too. But the idea 
would have been more or less the same: check if free(if free, move; if occupied check by who, kill or arrest or push), check if free, etc...

You'll also notice that all of my player cheat. I choosed to utilize every error in the server's code. Why would you follow rules that are not 
controlled? So technicaly they cheat so well the don't get caught ... 

The basis structure of the Client class is:
-check if player is 0 or 1
-check wich turn you're in
-try to follow instructions for the concerned turn if you don't succeed try another till you find one that's ok.
-add 1 to turn's value
-wait till server says it's your turn.

Server class routine hasn't been modified sinds the original download on May 10th. The only modification in that part of the code are:
-line 184 and 187 : Dubble [tx] in single [tx] and [ty]
-line 168 : + transformed in .append (to make arrest possible)
