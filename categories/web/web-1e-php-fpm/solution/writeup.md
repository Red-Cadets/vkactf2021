## Совершенно секретно

| Событие | Название | Категория | Сложность |
| :------ | ---- | ---- | ---- |
| VKA-CTF`2021 | Совершенно секретно | Web | Easy |

### Описание

> Автор: [ 𝕂𝕣𝕒𝕦𝕤𝕖 ]
>
> Наши разведчики обнаружили [секретный сервер](https://top-secret.vkactf.ru) капиталистов. Надо бы его протестировать, может там окажется что-то интересное. У нас слишком мало информации о них, их внутренней организации, используемом оборудовании. Сервер отзывается на стандартные запросы, но этого слишком мало. Нужно копнуть глубже. Вот вам все наши наработки, поработайте с ними, может вы добьетесь больших успехов.

### Решение
![](images/main.png)

На сайте нет никакой функциональности. Либо из обфусцированного JS файла, либо из запроса самого сайта узнаём `/server-stats` эндпоинт.

Добавив к нему параметр `?full` откроются логи запросов. Либо несколько раз обновив страницу, либо написав скрипт, который делает это за вас, узнаём путь до секретной страницы.
![](images/server-stats.png)

Из названия файла узнаём, что это md5 сумма от числа от 1 до 10. Перебрав таким образом остальные 9 страниц находим страницу с флагом.
![](images/flag.png)

**Флаг:**

> vka{53rv3r_5747u5_5h0uld_n07_b3_1n_pr0duc710n}