# Whitespaces
This document outlines all the rules to be adhered regarding whitespaces

## Indentation Character
Always use `space` to create indentations. If any 

## End of Files
When creating files parsable to text (programs, data tables, docs, etc.),
always leave `at least 1` empty line at the end of the file.

```c
✅

#include <stdio.h>

int main(int numof_args, char* arg[]) {
    printf("Hello world!\n");

    return 0;
}

```

```c
❌

#include <stdio.h>

int main(int numof_args, char* arg[]) {
    printf("Hello world!\n");

    return 0;
}
```