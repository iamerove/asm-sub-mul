# Asm-task

## Задание
Необходимо написать программы, выполняющие вычитание и умножение беззнаковых длинных чисел.

## Обзор
Обратите внимание, что приведенные примеры заточены на конкретную архитектуру процессора (x86\_64), конкретный ассемблер (`nasm`) и операционную систему (`Linux`).

Для того, чтобы запустить свое решение вам понадобится любой 64-битный дистрибутив Linux. Чтобы проверить битность вашего дистрибутива, можно исполнить команду:
```console
$ uname -m
```
Если команда выводит x86\_64, то система 64-битная, если i386 или i686 — 32-битная.

## Инструкция по работе
Все действия в инструкциях совершаются из папки с данным файлом

* Файл с умножением назовите `mul.asm`, а вычитанием `sub.asm`
* Если хотите собрать код без какого-либо файла, то закомментируйте в `CMakeLists.txt` строчки, связанные с ними

### Инструкция по сборке
```console
$ sudo apt install binutils g++ cmake nasm
$ ./build.sh
```

### Инструкция по тестированию
Скомплируйте программу `test.hs` и вызовите ее с нужными аргументами (смотри `--help`).

## Примечания
1. `mul` и `add` должны работать с беззнаковыми числами максимальной длины 128 qword (input). При этом результат `mul` (output) в данном случае может быть длины 256 qword и это должно корректно обрабатываться.
2. Программу можно реализовать по-разному, но если в вашем решении можно будет соптимизировать потребление памяти на стеке (или в `.data`), то вы будете вынуждены делать правки.
3. Вы не можете считывать числа, тратя на это больше памяти, чем требуется. 
