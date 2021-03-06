# grep и egrep 

egrep - альтернатива команде grep -E

#### Ключ `-E`

--extended-regexp

Рассматривает ОБРАЗЕЦ как расширенное регулярное выражение.

Т.е. egrep позволяет использовать такие метасимволы, как `+` (одно и более повторений), `?` (0 и более повторений), `|` (логическое или)

# ключи grep

## 1. Опция -r

--recursive 

## 2. Опция -i

--ignore-case

## 3. Опция -c

--count

## 4. Опция -n

--line-number

## 5. Опция -v

--invert-match (строки, в которых образец не встречается)

## 6. Опция -w

--word-regexp

## 7. Опция -x

--line-regexp 

## 8. Опция -l

--files-with-matches (выводит имена файлов, в которых было найдено совпадение)

## 9. Опция -L

--files-without-match (выводит имена файлов, в которых нет образца)

## 10. Опция -o

--only-matching (Возвращает не всю строку, где найден образец, а только его совпавшую часть)

## 11. Опция -q

--quiet --silent (Ничего не выдает на стандартный вывод. В случае нахождения соответствия с образцом отключается с нулевым статусом. Отключается также при обнаружении ошибки.)

## 12. Опция -s
--no-messages (Подавляет сообщения о несуществующих или нечитаемых файлах.)

## 13. Опция -D ДЕЙСТВИЕ

--devices=ДЕЙСТВИЕ 

Если исследуемый файл является файлом устройства, FIFO (именованным каналом) или сокетом, то следует применять эту опцию. ДЕЙСТВИЙ всего два: read (прочесть), и skip (пропустить). Если вы указываете ДЕЙСТВИЕ read (используется по умолчанию), то программа попытается прочесть специальный файл, как если бы он был обычным файлом; если указываете ДЕЙСТВИЕ skip, то файлы устройств, FIFO и сокеты будут молча проигнорированы.

## 14. Опция -d ДЕЙСТВИЕ

--directories=ДЕЙСТВИЕ 

Если входной файл является директорией, то используйте эту опцию. ДЕЙСТВИЕ read (прочесть) попытается прочесть директорию как обычный файл (некоторые ОС и файловые системы запрещают это; тогда появятся соответствующие сообщения, либо директории молча пропустят). Если ДЕЙСТВИЕ skip (пропустить), то директории будут молча проигнорированы. Если ДЕЙСТВИЕ recurse (рекурсивно), то grep будет просматривать все файлы и субдиректории внутри заданного каталога рекурсивно. Это эквивалент опции -r, с которой мы уже познакомились.

## 15. Опция -H

--with-filename (Выдает имя файла для каждого совпадения с ОБРАЗЦОМ.)

## 16. Опция -h

--no-filename (Подавляет вывод имен файлов, когда задано несколько файлов для исследования.)

## 17. Опция -I

Обрабатывает бинарные файлы как не содержащие совпадений с ОБРАЗЦОМ;

## 18. Опция --include=ОБРАЗЕЦ_имени_файла

При рекурсивном исследовании директорий обследовать только файлы, содержащие в своем имени ОБРАЗЕЦ_имени_файла.

## 19. Опция --exclude=ОБРАЗЕЦ_имени_файла

При рекурсивном исследовании директорий пропускать файлы, содержащие в своем имени ОБРАЗЕЦ_имени_файла.

## 20. Опция -m ЧИСЛО_СТРОК

--max-count=ЧИСЛО_СТРОК

## 21. Опция -y

Синоним опции -i (не различать верхний и нижний регистр символов).

## 22. Опция --mmap

Использует системный вызов mmap вместо системного вызова read.

## 23. Опция -Z

--null

Если в выводе программы имена файлов (например при опции -l), то опция -Z после каждого имени файла выводит нулевой байт вместо символа новой строки (как обычно происходит). Это делает вывод однозначным, даже если имена файлов содержат символы новой строки. 

## 24. Опция -z

--null-data

Рассматривает ввод как набор строк, каждая из которых заканчивается не символом новой строки, а нулевым байтом. Как и предыдущая опция, используется совместно с вышеперечисленными командами для обработки экзотических имен файлов.

## 25. Опция -G

--basic-regexp

Рассматривает ОБРАЗЕЦ как базовое регулярное выражение. Эта опция используется по умолчанию.
 
## 26. Опция -E

--extended-regexp

Рассматривает ОБРАЗЕЦ как расширенное регулярное выражение.

## 27. Опция -P

--perl-regexp

Рассматривает ОБРАЗЕЦ как регулярное выражение языка Perl.

## 28. Опция -F

--fixed-strings

Рассматривает ОБРАЗЕЦ как список "фиксированных выражений" (fixed strings - термин из области регулярных выражений), разделенных символами новой строки. Будет искать соответствия любому из них.

## 29. Опция -f

Читает один или несколько образцов из файла с указанным полным именем файл_образцов (словарь для поиска). Образцы в файле_образцов завершаются символом новой строки. 
