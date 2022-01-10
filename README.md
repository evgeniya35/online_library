# Загрузка книг

Программа скачивания книг сайта [БОЛЬШАЯ БЕСПЛАТНАЯ БИБЛИОТЕКА tululu.org](https://tululu.org/).

## Как установить

### Окружение
Python должен быть установлен.

### Установка
Установите программу из репозитория:
```bash
git clone https://github.com/evgeniya35/online_library.git
```

### Зависимости
Используйте pip для установки зависимостей:
```bash
pip install -r requirements.txt
```

 ## Запуск

- Для скачивания книг по страницам каталога [Научная фантастика](http://tululu.org/l55/), используйте командную строку для запуска:
```bash
$ python parse_tululu_category.py --start_page 1 --end_page 4
```
если не задать конечную страницу `end_page`, скрипт скачает все книги начиная с номера страницы `start_page`, до последней страницы каталога.
Дополнительные аргументы:
```
--dest_folder   Каталог куда размещать, по умолчанию - media
--skip_img      Не скачивать картинки
--skip_txt      Не скачивать книгу
--json_path     Путь к файлу с описаниями книг
```
 
- Для скачивания выборочных книг любого каталога по диапазону номеров, используйте командную строку для запуска скрипта `main.py`:
```bash 
$ python main.py --start_id 1 --end_id 15
```
аргументы:
```
start_id    - С какого номера книги загружать, по умолчанию 1
end_id      - По какой номер книги загружать, по умолчанию 9
```

### Цель проекта

Код написан в образовательных целях на онлайн-курсе для веб-разработчиков [dvmn.org](https://dvmn.org/).
