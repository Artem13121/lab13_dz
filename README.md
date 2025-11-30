### Домашнее задание к 13 лабораторной

### Условие
<img width="815" height="72" alt="image" src="https://github.com/user-attachments/assets/21b9fa63-b6ac-48d1-89e5-af3a797e50c2" />
<img width="839" height="55" alt="image" src="https://github.com/user-attachments/assets/7e97129a-e4a8-403f-970b-85059d6d717d" />

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
