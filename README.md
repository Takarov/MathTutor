/*May have some problems compiling*/
#include <iostream>
#include <stdlib.h>
#include <ctime>
#include <iomanip>
#include <string>

using namespace std;

int main()
{
	int num_one,
		num_two,
		num_three,
		num_four,
		num_five,
		num_six,
		c_answer,
		answerA,
		answerB,
		answerC;
	char menu_choice;
	// toupper(menu_choice)

	unsigned seed;
	seed = time(0);
	srand(seed);




	do {
		num_one = rand() % 10;
		num_two = rand() % 10;
		num_three = rand() % 10;
		num_four = rand() % 10;
		num_five = rand() % 10;
		num_six = rand() % 10;
		answerA = num_one + num_two;
		answerB = num_three - num_four;
		answerC = num_five * num_six;


		cout << "MATH TUTOR!\n";
		cout << "___________\n";
		cin.ignore(1);

		cout << "Please choose a letter\n";
		cout << "A. Addition\n";
		cout << "B. Subtraction\n";
		cout << "C. Multiplication\n";
		cout << "D. Quit\n";
		cin >> menu_choice;

		switch (menu_choice)
		{
		case 'a':
		case 'A':

			cout << setw(10) << right << num_one << endl;
			cout << setw(9) << " + " << right << num_two << endl;
			cout << setw(10) << "____" << endl;
			cin >> c_answer;
			if (c_answer == answerA)
			{
				cout << "The answer is correct!\n\n\n";
			}
			else if (c_answer != answerA)
			{
				cout << "Your answer is incorrect, the correct answer is: " << answerA << " \n\n\n";
			}
			break;

		case 'b':
		case 'B':
			cout << setw(10) << right << num_three << endl;
			cout << setw(9) << " - " << right << num_four << endl;
			cout << setw(10) << "____" << endl;
			cin >> c_answer;
			if (c_answer == answerB)
			{
				cout << "Your subtraction answer is correct!\n\n\n";
			}
			else if (c_answer != answerB)
			{
				cout << "Your subtraction answer is incorrect, the correct answer is: " << answerB << " \n\n\n";
			}
			break;

		case 'c':
		case 'C':

			cout << setw(10) << right << num_five << endl;
			cout << setw(9) << " x " << right << num_six << endl;
			cout << setw(10) << "____" << endl;
			cin >> c_answer;
			if (c_answer == answerC)
			{
				cout << "Your multiplication answer is correct!\n\n\n";
			}
			else if (c_answer != answerC)
			{
				cout << "Your multiplication answer is incorrect, the correct answer is: " << answerC << " \n\n\n";
			}
			break;

		case 'd':
		case 'D': cout << "Goodbye!\n\n\n";
			break;

		default: cout << "Invalid entry.\n\n\n";
			break;

		}

	} while (menu_choice != 'd' && menu_choice != 'D');


	return 0;
}
