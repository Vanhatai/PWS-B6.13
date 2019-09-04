PWS-B6.13

1. Веб сервер принимает GET запросы по адресу /albums/<artist>  и выводит
  на экран сообщение с количеством альбомов исполнителя artist и списком
  названий этих альбомов.
2. Веб сервер принимает POST запросы по адресу /albums/ и сохраняет переданные
  пользователем данные об альбоме. Данные передаются в формате веб формы.
  Если пользователь пытается передать данные об альбоме, который уже есть
  в базе данных, обработчик запроса отвечает HTTP ошибкой 409 и выводит
  соответствующее сообщение.
3. Bottle использует tornado сервер (pip install tornado).

Структура базы данных album:
  "id" integer primary key autoincrement,
  "year" integer,
  "artist" text,
  "genre" text,
  "album" text

