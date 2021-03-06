# Конвертер выписки по карте Сбербанк Онлайн

Конвертер отчётов по карте Сбербанка в нормальный формат. Поддерживает преобразование стандартной текстовой выписки по карте Сбербанк Онлайн в формат:

- Microsoft Excel CSV
- Microsoft Excel TSV
- JSON

Демо-версия: <http://www.av13.ru/sbrf/>

## Состав

- `sberbank.php` - функции преобразования файлов
- `convert.php` - обработчик запросов из формы или API
- `index.html` - внешний интерфейс запросов

## Инструкция по применению

1. Закажите на свою почту выписку по интересующему Вас счёту через Сбербанк-Онлайн.
2. Скачайте полученный файл выписки в формате TXT.
3. Выберите данный файл для загрузки в эту форму и укажите необходимый формат.
4. Нажмите «Конвертировать файл» и наслаждайтесь результатом.

## Запросы через API

Вы можете осуществлять запросы к конвертеру через простую API-функцию. Запрос осуществляется методом POST.

**Демонстрационный URL**: http://www.av13.ru/sbrf/convert.php

**Параметры**:

- `data` - содержимое файла, который необходим конвертировать. Рекомендуется использовать кодировку Windows-1251 воизбежание проблем с комментариями к платежам.
- `type` - формат возвращаемого результата: csv, tsv или json (по умолчанию)
- `utf8` - флаг конвертации в UTF-8, может принимать значения 0 или 1, по умолчанию 0.

**Возвращаемый результат**: файл в выбранном формате

**Возможные ошибки**: если не указан какой-либо параметр, функция скажет *oops!*