# SnapPy

## English

### Description
The **SnapPy** script is designed to create a copy (*snapshot*) of a file structure into a file. This is similar to archiving without compression..

Key features:
  - Create a snap file from a specified directory.
  - Restore file structure from a snap file to a chosen directory.
  - Preserve information about the owner and access rights in UNIX-like systems.
  - List the files and directories stored in the snap file.
  - Verify file integrity using hash checks.
  - *Strict mode* in which recovery is aborted in the event of a hash error.

### Usage
options:
```
  -h, --help    show this help message and exit
  -m            create a file structure snapshot and save it to a file
  -u            restore a file structure snapshot from a file
  -s            disable strict mode (continue restoring despite file hash mismatches)
  -l snap_file  list files and directories stored in a file structure snapshot
  -d directory  specify the path to the directory
  -f snap_file  specify the path to the snap file
```

#### Examples
- Snapshot whole file structure inside the `./folder/a` directory to the `file.snap` file:
```
python3 snap.py -m -d ./folder/a -f file.snap
```

- Restore the file structure from the `file.snap` file to the `./folder/b` directory:
```
python3 snap.py -u -d ./folder/b -f file.snap
```

- Display all files and directories saved within the `file.snap` file:
```
python3 snap.py -l file.snap
```

## Солов'їна

### Опис
Скрипт **SnapPy** призначений для створення копії (знімка) файлової структури у файл. Це схоже на архівування без стиснення.

Основні можливості:
  - Створення *знімка* вказаної директорії.
  - Відновлення структури файлів зі *знімка* в обрану директорію.
  - Збереження інформації про власника і права доступу в UNIX-подібних системах.
  - Виведення списку файлів і директорій, що зберігаються у *знімку*.
  - Перевірка цілісності файлів у *знімку* за допомогою хешів.
  - *Суворий режим* при якому відновлення переривається при помилці хешу.

### Використання
параметри:
```
  -h, --help    показати повідомлення довідки та вийти
  -m            зробити знімок файлової структури у snap-файл
  -u            відновити файлову структуру зі snap-файлу
  -s            вимкнути строгий режим (намагатись продовжувати розпаковку при невідповідності хешу файлу)
  -l snap_file  вивести список файлів і директорій, що зберігаються у snap-файлі
  -d директорія вказати шлях до директорії
  -f snap_file  вказати шлях до snap-файлу
```

#### Приклади
- Зробити знімок усієї файлової структури директорії `./folder/a` у файл `file.snap`:
```
python3 snap.py -m -d ./folder/a -f file.snap
```

- Відновити файлову структуру з файлу `file.snap` до директорії `./folder/b`:
```
python3 snap.py -u -d ./folder/b -f file.snap
```

- Відображення всіх файлів і директорій, збережених у файлі `file.snap`:
```
python3 snap.py -l file.snap
```
