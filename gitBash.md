## Базовые команды Git Bash

**Bash** — это командная оболочка для UNIX-подобных операционных систем (UNIX, GNU/Linux, MacOS). 

**Git Bash** - это приложение для сред Microsoft Windows, которое эмулирует среду bash и позволяет использовать большинство стандартных команд Unix. 

Основной синтаксис ```команда {ключи} [параметры]```

### Создание каталога

```mkdir test``` (make directory) команда для создания новых каталогов, test - наименование каталога

### Переход по каталогам

```pwd``` (present working directory) выводит полный путь от корневого каталога к текущему рабочему каталогу  
```cd``` (change directory) для перехода по дереву каталогов  
```cd ~``` перейти в домашний каталог  
```cd ~/test``` перейти в каталог test  
```cd /``` перейти в корневой каталог  
```cd -``` вернуться в предыдущий каталог  
```cd ..``` перейти в родительскую директорию  
```cd ../..``` перейти на два звена выше  

*Стрелки* ⇧ и ⇩ *на клавиатуре можно использовать для перемещения по ранее введенным командам.*

*Если ввести первую букву директории и нажать tab, произойдет автоматический ввод имени директории.*

```clear``` очистить историю терминала

### Вывод содержимого каталога

```ls``` напечатать в стандартный вывод содержимое каталогов

*Ключи являются регистро зависимыми.*  

```ls -a``` вывести все файлы в каталогах, включая скрытые файлы, начинающиеся с точки, например, системные файлы 
```ls -A``` вывести все файлы, кроме текущей и родительской директории  
```ls -l``` в дополнении к имени файла, вывести тип файла, права доступа к файлу, количество ссылок на файл, имя владельца, имя группы, размер файла в байтах и временной штамп   
```ls -al``` подробная выдача всех файлов, включая скрытые файлы
```ls -R``` включить рекурсивную выдачу списка каталогов (содержимое для каждой папки в директории)  
```CTRL c``` остановить выполнение команды ```ls -R```  

### Создание пустого файла

```touch``` для установки времени последнего изменения файла или доступа в текущее время. Также используется для создания пустых файлов  
```touch file.txt``` пример создания пустого файла

*Если есть пробел, система воспринимает его, как разделитель, создавая два файла.
Рекомендуется использовать нижнее подчеркивание, не рекомендуется использовать кириллицу.*

### Удаление каталога и файлов

```rmdir``` (remove directory) команда, которая удаляет каталог из файловой системы (для пустых каталогов)  
```rm``` (remove) утилита, используемая для удаления файлов из файловой системы  
```rm -R``` удалить каталог с файлами

### Перемещение и копирование файлов

```mv``` (move) используется для перемещения или переименования файлов  
```mv index1/file.txt index2/file2.txt``` пример перемещения и переименования файла   
```cp ```  для копирования файлов из одного каталога в другой  
```cp index1/file.txt index2``` пример копирования файла в другую папку

### Вывод содержимого файлов

```cat file.txt``` считывает данные из файлов и выводит их содержимое  
```less file.txt``` постраничный вывод содержимого текстовых файлов  
```q``` закончить команду ```less```  
```nano file.txt``` консольный текстовый редактор  
```CTRL x``` закончить команду ```nano```

### Поиск строк и файлов

```grep``` (Global Regular Expression Print) поиск строки в заданном файле  
```cat file.txt | grep our_search``` вывести все строки, которые содержат our_search в файле file.txt

*Если в имени файла содержится пробел, например* ```name file.txt```, *оборачиваем имя файла в кавычки:* ```‘name file.txt’```.

```find``` команда для поиска файлов и каталогов на основе специальных условий   
```find -name '*.jpg'``` найти все файлы jpg в текущей директории

### Команды для отображения и сохранения текста запроса

```echo текст``` команда для отображения строки текста из запроса  
```echo текст > file.txt``` сохранить введенные данные в файл и создать файл file.txt

### Вывести набор каталогов системной переменной PATH, в которых находятся исполняемые программы

```echo $PATH```

### Вывод процессов

```ps``` выводит список текущих процессов

### Ping и curl

```ping``` позволяет проверить доступность удаленного хоста  
```ping google.com``` отправляет ICMP- пакеты на удаленный хост и ожидает ответа  
```CTRL c``` остановить команду ping  
```curl``` (Client URL) утилита командной строки для передачи данных с или на сервер, предназначенная для работы без взаимодействия с пользователем  
```curl -L google.com``` -L Параметр предписывает curl следовать редирект, пока он не достигнет конечного пункта назначения

**Параметры, которые мы можем использовать при отправке запросов** 

```-X``` request - метод HTTP  
```-i``` include - включить заголовки ответа  
```-d``` data - данные, которые должны быть отправлены  
```-H``` header - дополнительный заголовок для отправки  

```curl test_url``` запрос GET (по умолчанию)  
```curl test_url -X POST -d '{"title": "name"}'``` запрос POST   
```curl test_url -X PATCH -d '{"completed":true}'``` запрос PATCH  
```curl test_url -X DELETE``` запрос DELETE
