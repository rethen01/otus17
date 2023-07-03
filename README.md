1) Добавление в существующей тип:
![Screenshot from 2023-07-03 23-51-46](https://github.com/rethen01/otus17/assets/101434046/f1da2d79-5312-4bf1-8d1a-cc536e0eb2b3)
2) Отключение с помощью setsebool. Выполнил команду: cat /var/log/audit/audit.log | audit2why, в результате была выдана рекомендация по отключению необходимой политики. Предвариетльно очищен лог, после этого перезапущена служба nginx
![Screenshot from 2023-07-04 00-02-04](https://github.com/rethen01/otus17/assets/101434046/db4a5868-2f58-436b-9d4c-d580687fed65)
3) С помощью создание модуля
![Screenshot from 2023-07-04 00-09-06](https://github.com/rethen01/otus17/assets/101434046/c0d4d19e-4499-48e2-a6e4-37e42d78b027)
