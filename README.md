# get.managment_hotel
#include <iostream>
#include <sstream>
#include <string>

using namespace std;

int sumEvenNumbers(string numbers) {
    stringstream ss(numbers);
    string token;
    int sum = 0;
    while (getline(ss, token, ',')) {
        int num = stoi(token);
        if (num % 2 == 0) {
            sum += num;
        }
    }
    return sum;
}

int main() {
    string input;
    cout << "Enter numbers separated by commas: ";
    getline(cin, input);
    int result = sumEvenNumbers(input);
    cout << "Sum of even numbers: " << result << endl;
    return 0;
}
