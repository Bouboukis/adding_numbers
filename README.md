# adding_numbers
This is a small program in C. The user gives a number from 1 to 9. For Example number 5. Then the program returns the sum of the numbers 5+54+543...+54321.

/* Program to add the digits of a give number until reaches 1*/

#include <stdio.h>

main()
{
	int i, sum, starting_number, repeat, N;
	/* sum = summary of the adding numbers,
 	* starting_number =  the number we are beginning the adding,
 	* repeat = the value of starting number after each reapeat */

	printf("Please give me a number between 1 and 9:\n");

	/*Defensive programing, you can change the range of numbers but if it is going to give to many repeats you
	 * will have to change the type of sum to double.*/
	do
	{
		scanf("%d", &starting_number);
		if (starting_number < 0 || starting_number > 9)
			printf("!!!!The number is incorrect please try again!!!!\n");

	} while (starting_number < 0 || starting_number > 9);

	repeat = N = starting_number; /* Sum is starting with the value of add_num.*/
	sum = 0;
	
	for(i = 0; i < N; i ++)
	{
		starting_number--;
		sum += repeat;
		repeat = repeat * 10 +  starting_number;
	}

	printf("The summary is:%d", sum);

}
