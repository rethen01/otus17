Задание 1

1) Добавление в существующей тип:
![Screenshot from 2023-07-03 23-51-46](https://github.com/rethen01/otus17/assets/101434046/f1da2d79-5312-4bf1-8d1a-cc536e0eb2b3)
2) Отключение с помощью setsebool. Выполнил команду: cat /var/log/audit/audit.log | audit2why, в результате была выдана рекомендация по отключению необходимой политики. Предвариетльно очищен лог, после этого перезапущена служба nginx
![Screenshot from 2023-07-04 00-02-04](https://github.com/rethen01/otus17/assets/101434046/db4a5868-2f58-436b-9d4c-d580687fed65)
3) С помощью создание модуля
![Screenshot from 2023-07-04 00-09-06](https://github.com/rethen01/otus17/assets/101434046/c0d4d19e-4499-48e2-a6e4-37e42d78b027)


Задание 2

Проблема в том, что конфигурационные файлы лежат в каталоге /etс. В нихе нет разрешающих правил для dns сервера. 
Контекст изменен командой:chcon -R -t named_zone_t /etc/named
![Screenshot from 2023-07-04 01-14-14](https://github.com/rethen01/otus17/assets/101434046/fec91480-2b3a-4c5e-ad6c-d992015317c4)
После изменения на клиенте обновление зоны выполнилось:
![Screenshot from 2023-07-04 01-15-46](https://github.com/rethen01/otus17/assets/101434046/e1b4bc3a-59f4-4c11-b9b1-0e714b78f228)
