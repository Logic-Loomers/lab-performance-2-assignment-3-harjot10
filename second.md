On a specific day, the exchange rates were as follows: the British pound was valued at $1.487 U.S., the French franc at $0.172, the German deutschemark at $0.584, and the Japanese yen at $0.00955. Write a program that prompts the user to input an amount in U.S. dollars. The program should then display this amount converted into these four other currencies. Test the program by inputting various dollar amounts and ensuring that the conversions to British pounds, French francs, German deutschemarks, and Japanese yen are accurate. Additionally, test the program with negative dollar amounts to verify that it handles invalid input appropriately.

CODE:-

#include <iostream>
using namespace std;

int main() {
    double us_dollars, british_pounds, french_francs, german_deutschemarks, japanese_yen;
    double exchange_rate_pound = 1.487, exchange_rate_franc = 0.172, exchange_rate_deutschemark = 0.584, exchange_rate_yen = 0.00955;

    cout << "Enter the amount in U.S. dollars: ";
    cin >> us_dollars;

    if (us_dollars < 0) 
    {
        cout << "Invalid input. Please enter a non-negative amount." << endl;
        return 0;
    }

    british_pounds = us_dollars * exchange_rate_pound;
    french_francs = us_dollars * exchange_rate_franc;
    german_deutschemarks = us_dollars * exchange_rate_deutschemark;
    japanese_yen = us_dollars * exchange_rate_yen;

    cout << "Equivalent amounts:" << endl;
    cout << "British pounds: " << british_pounds << endl;
    cout << "French francs: " << french_francs << endl;
    cout << "German deutschemarks: " << german_deutschemarks << endl;
    cout << "Japanese yen: " << japanese_yen << endl;

    return 0;
}
