//# Rock-paper-scissors-
#include <math.h>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int game(char player, char computer)
{
    if (player == computer)
        return -1;
    if (player == 's' && computer == 'p')
        return 0;
    else if (player == 'p' && computer == 's')
        return 1;
    if (player == 's' && computer == 'z')
        return 1;
    else if (player == 'z' && computer == 's')
        return 0;
    if (player == 'p' && computer == 'z')
        return 0;
    else if (player == 'z' && computer == 'p')
        return 1;
}
int main()
{
    int n;
    char player, computer, result;
    srand(time(NULL));
    n = rand() % 100;
    if (n < 33)
        computer = 's';
    else if (n > 33 && n < 66)
        computer = 'p';
    else
        computer = 'z';
 printf("\nEnter s for STONE, \n p for PAPER ,\n z for SCISSOR \n");
scanf("%c", &player);
result = game(player, computer);
    if (result == -1) {
        printf("\nGame Draw!\n");
    }
    else if (result == 1) {
        printf("\nplayer won the game!\n");
    }
    else { 
        printf("\ncomputer won the game!\n");
    }
        printf("\nplayer choose : %c and Computer choose : %c\n",player, computer);
 return 0;
}
