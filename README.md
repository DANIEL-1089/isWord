#include <iostream>
#include <cstdlib>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <conio.h>

#pragma warning(disable : 4996)

using namespace std;
enum itsaWord { NO, YES };



int main()
{
    itsaWord isWord = NO;
    char ch = 'a';
    int wordCount = 0;
    cout << "enter a suggestion:\n";
    do {
        ch = getche();
        if (ch == ' ' || ch == '\r') {
            if (isWord == YES) {
                wordCount++;
                isWord = NO;
            }
        }
        else {
            if (isWord == NO) {
                isWord = YES;
            }
        }
    } while (ch != '\r');
    cout << "\n--number of words: " << wordCount << "---\n";

    return 0;
}
