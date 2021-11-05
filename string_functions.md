From Lab 11

```c
#include <stdio.h>
#include <string.h>

int main() {
    char name[64];                  // 1
    printf("Please enter your name:\n> ");
    scanf(" %s", &name);

    char greeting[128];

    // "My name is " + name + "." -> greeting
    strcpy(greeting, "Hello, ");    // 2
    strcat(greeting, name);         // 3
    strcat(greeting, "!");
    
    printf("%s\n", greeting);       // 4

    return 0;
}
```

1. We can reasonably assume that the user will enter a string that is under 64 characters long (remember, you need an extra character for the NULL character (`\0`)).
2. Since we want to start with "Hello", we use `strcpy` (string copy) to overwrite whatever was previously in the variable.
3. Now, we use `strcat` (string concatenation) to add on to the sentence, not overwrite.
4. Finally, we print the string using `%s`. Recall, `%s` tells the printf function to continue printing characters until printf hits a NULL character ('\0').

## OUTPUT
```sh
Please enter your name:
> Alan
Hello, Alan!
Program ended with exit code: 0
```

## RESOURCES
- [`strcpy` function documentation](https://www.cplusplus.com/reference/cstring/strcpy/)
- [`strcat` function documentation](https://www.cplusplus.com/reference/cstring/strcat/)
