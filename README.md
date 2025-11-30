### Домашнее задание к 13 лабораторной

### Программа
```
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "RUS");
    char str[1000];
    int i = 0;
    int found = 0;
    printf("Введите строку: ");
    fgets(str, 1000, stdin);
    if (str[0] == -32 || str[0] == -96 || str[0] == 'A' || str[0] == 'a') {
        found = 1;
    }
    while (str[i] != '\0') {
        if (str[i] == ' ') {
            char next_char = str[i + 1];
            if (next_char == -32 || next_char == -96 || next_char == 'A' || next_char == 'a') {
                found = 1;
                break;
            }
        }
        i++;
    }
    if (found) {
        printf("есть\n");
    }
    else {
        printf("нет\n");
    }
    return 0;
}
```
### Информация о разработчике
Лантрат Артём, бИЦ - 251
