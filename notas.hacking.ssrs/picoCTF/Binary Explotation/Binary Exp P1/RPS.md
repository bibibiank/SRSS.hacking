## Objetivo 

Here's a program that plays rock, paper, scissors against you. I hear something good happens if you win 5 times in a row. The program's source code with the flag redacted can be downloaded [here](https://artifacts.picoctf.net/c/147/game-redacted.c).

Additional details will be available after launching your challenge instance.

## Solución  


la solucion es jugar piedra papel o tijera con el programa, debemos ganar 5 veces seguidas sin perder para que nos de la bandera. el truco es poner *rockpaperscissors* en cada juego para no perder.
```java
zsh: corrupt history file /home/kali/.zsh_history
┌──(kali㉿kali)-[~]
└─$ cd Downloads/rps   

┌──(kali㉿kali)-[~/Downloads/rps]
└─$ nc saturn.picoctf.net 57340 
Welcome challenger to the game of Rock, Paper, Scissors
For anyone that beats me 5 times in a row, I will offer up a flag I found
Are you ready?
Type '1' to play a game
Type '2' to exit the program
1
1
Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: paper
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: rock
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: paper
You win! Play again?
Type '1' to play a game
Type '2' to exit the program
1
1


Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors                                                                                                               
You played: rockpaperscissors                                                                                                   
The computer played: paper                                                                                                      
You win! Play again?                                                                                                            
Type '1' to play a game                                                                                                         
Type '2' to exit the program                                                                                                    
1                                                                                                                               
1                                                                                                 
Please make your selection (rock/paper/scissors):
rockpaperscissors
rockpaperscissors
You played: rockpaperscissors
The computer played: scissors
You win! Play again?
Congrats, here's the flag!
picoCTF{50M3_3X7R3M3_1UCK_C85AF58A}
Type '1' to play a game
Type '2' to exit the program
                                                           

```

**picoCTF{50M3_3X7R3M3_1UCK_C85AF58A}**


## Notas Adicionales 

### Referencias