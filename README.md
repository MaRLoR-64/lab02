##Labwork 2
##Перенос файлов на Github
```bash
Username for 'https://github.com': MaRLoR-64 
Password for 'https://MaRLoR-64%20@github.com': 
Перечисление объектов: 3, готово.
Подсчет объектов: 100% (3/3), готово.
Запись объектов: 100% (3/3), 220 байтов | 220.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To https://github.com/MaRLoR-64/lab02.git
 * [new branch]      master -> master
```
```sh
commit 51b3dd41f8f0876f0a2891f847c08b640764d695 (HEAD -> master, origin/master)
Author: MaRLoR-64 <erohin2512@icloud.com>
Date:   Sun Mar 23 00:40:23 2025 +0300

    added README.md
```
##Создание рабочих папок
```sh
student@LabPythonVM:~/MaRLoR-64/workspace$ mkdir sources
student@LabPythonVM:~/MaRLoR-64/workspace$ mkdir include
student@LabPythonVM:~/MaRLoR-64/workspace$ mkdir examples
```
##Создание кода 
```sh
student@LabPythonVM:~/MaRLoR-64/workspace$ cat > sources/print.cpp <<EOF
> #include <print.hpp>
> void print(const std::string& text, std::ostream& out)
{
  out << text;
}
void print(const std::string& text, std::ofstream& out)
{
  out << text;
}
EOF
```
```sh
student@LabPythonVM:~/MaRLoR-64/workspace$ cat > include/print.hpp <<EOF
> #include <fstream>
#include <iostream>
#include <string>
void print(const std::string& text, std::ofstream& out);
void print(const std::string& text, std::ostream& out = std::cout);
EOF
```
```sh
student@LabPythonVM:~/MaRLoR-64/workspace$ cat > examples/example2.cpp <<EOF
> #include <print.hpp>

#include <fstream>

int main(int argc, char** argv)
{
  std::ofstream file("log.txt");
  print(std::string("hello"), file);
}
EOF
```
##Перенос файлов на Github
```sh
student@LabPythonVM:~/MaRLoR-64/workspace$ git commit -m"added README.md"
[master (корневой коммит) 51b3dd4] added README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
```

