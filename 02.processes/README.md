## Cистемни примитиви на C за работа с процеси

* execl(3) `int execl(const char *path, const char *arg, ... /* (char  *) NULL */);`
* execlp(3) `int execlp(const char *file, const char *arg, ... /* (char  *) NULL */);`
* exit(3) `void exit(int status);`
* fork(2) `pid_t fork(void);`
* wait(2) `pid_t wait(int *wstatus);`
* getpid(2) `pid_t getpid(void);` `pid_t getppid(void);`

## Задачи
1. Да се напише програма на C, която изпълнява команда date.
2. Да се напише програма на C, която изпълнява команда ls с точно един аргумент.
3. Да се напише програма на C, която изпълнява команда sleep (за 60 секунди).
4. Да се напише програма на C, която създава процес дете и демонстрира принцина на конкурентност при процесите.
5. Да се напише програма на C, която е аналогична на горния пример, но принуждава бащата да изчака сина си да завърши.
6. Да се напише програма на С, която получава като параметър команда (без параметри) и при успешното ѝ изпълнение, извежда на стандартния изход името на командата.
7. Да се напише програма на С, която получава като параметри три команди (без параметри), изпълнява ги последователно, като изчаква края на всяка и извежда на стандартния изход номера на завършилия процес, както и неговия код на завършване.
8. Да се напише програма на С, която получава като параметър име на файл. Създава процес син, който записва стринга `foobar` във файла (ако не съществува, го създава, в противен случай го занулява), след което процеса родител прочита записаното във файла съдържание и го извежда на стандартния изход, добавяйки по един интервал между всеки два символа.
9. Да се напише програма на C, която която създава файл в текущата директория и генерира два процесa, които записват низовете `foo` и `bar` в създадения файл.
	* Програмата не гарантира последователното записване на низове.
	* Променете програмата така, че да записва низовете последователно, като първия е `foo`.
10. Да се напише програма на C, която получава като параметри от команден ред две команди (без параметри). Изпълнява първата. Ако тя е завършила успешно изпълнява втората. Ако не, завършва с код -1.
11. Да се напише програма на C, която изпълнява последователно подадените ѝ като параметри команди, като реализира следната функционалност постъпково:
	* `main cmd1 ... cmdN` Изпълнява всяка от командите в отделен дъщерен процес.
	* ... при което се запазва броя на изпълнените команди, които са дали грешка и броя на завършилите успешно.
12. Да се напише програма на C, която получава като параметри от команден ред две команди (без параметри) и име на файл в текущата директория. Ако файлът не съществува, го създава. Програмата изпълнява командите последователно, по реда на подаването им. Ако първата команда завърши успешно, програмата добавя нейното име към съдържанието на файла, подаден като команден параметър. Ако командата завърши неуспешно, програмата уведомява потребителя чрез подходящо съобщение.
13. Да се напише програма на C, която получава като командни параметри две команди (без параметри). Изпълнява ги едновременно и извежда на стандартния изход номера на процеса на първата завършила успешно. Ако нито една не завърши успешно извежда -1.
