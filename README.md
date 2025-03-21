#include <iostream>
#include <vector>
using namespace std;

int main() {
    setlocale(LC_CTYPE, "ukr");
    int n;
    cout << "Введіть ціле число: ";
    cin >> n;

    vector <int> digits;
    int evenCount = 0;

    if (n < 0) {
        n = -n;
    }

    while (n > 0) {
        int digit = n % 10;
        digits.push_back(digit);
        if (digit % 2 == 0) {
            evenCount++;
        }
        n /= 10;
    }

    cout << "Цифри у масиві: ";
    for (int i = digits.size() - 1; i >= 0; i--) {
        cout << digits[i] << " ";
    }
    cout << endl;
}
