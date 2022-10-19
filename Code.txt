#include <iostream>

using namespace std;

int main()
{
    const int N = 30;
    char *str = new char [N];
    int len = 0, palindromCount = 0;
    bool flag;
    cout << "Enter lines: " << endl;
    for (int i = 1; i <= 5; i++) {
        cin.getline(str, N);
        while (str[len]) {
            len++;
        }
        flag = true;
        int j = 0;
        while ((j < len/2) && flag) {
            if (str[j] != str[len-1-j]) flag = false;
            j++;
        }
        if (flag) {
            palindromCount++;
        }
    }
    cout << "Count of palindroms " << palindromCount;
    delete str;
    return 0;
}
