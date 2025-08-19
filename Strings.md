## 1.Write a C program to count the number of vowels, consonants, digits, and spaces in a string entered by the user.
Sample Input:
Enter a string: Hello World 123
Sample Output:
Vowels: 3
Consonants: 7
Digits: 3
Spaces: 2
```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[1000];
    int i, v = 0, c = 0, d = 0, sp = 0;

    printf("Enter string: ");
    fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = '\0';

    for (i = 0; str[i] != '\0'; i++) {
        if (isalpha(str[i])) {
            char ch = tolower(str[i]);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                v++;
            } else {
                c++;
            }
        } else if (isdigit(str[i])) {
            d++;
        } else if (isspace(str[i])) {
            sp++;
        }
    }

    printf("Vowels: %d\nConsonants: %d\nDigits: %d\nSpaces: %d\n", v, c, d, sp);
    return 0;
}

```
