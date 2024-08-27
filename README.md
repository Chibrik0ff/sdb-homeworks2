# Домашнее задание к занятию "`Кеширование Redis/memcached`" `Чибриков Станислав`

### Задание 1. Кеширование

Приведите примеры проблем, которые может решить кеширование.

*Ответ:*
*1. Повышение производительности*
*2. Уменьшение времени отклика*
*3. Уменьшение нагрузки на основную базу данных*
*4. Снижение нагрузки на основной сервер в пиках запросов*
*5. Прогнозируемая производительность*

---

### Задание 2. Memcached
Установите и запустите memcached.

*Ответ:*
```
sudo apt update && apt install memcached
```

![screenshoot](https://github.com/Chibrik0ff/sdb-homeworks2/blob/main/img/img1.jpg)

---

### Задание 3. Удаление по TTL в Memcached
Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5.

*Ответ:*
```
set KEY META_DATA EXPIRY_TIME LENGTH_IN_BYTES
get KEY
```
![screenshoot](https://github.com/Chibrik0ff/sdb-homeworks2/blob/main/img/img2.jpg)

### Задание 4. Запись данных в Redis
Запишите в Redis несколько ключей с любыми именами и значениями.

*Ответ:*
```
sudo apt update && apt install redis
```
![screenshoot](https://github.com/Chibrik0ff/sdb-homeworks2/blob/main/img/img3.jpg)

redis.sh
```bash
for key in $(redis-cli -p 6379 keys \*);
        do echo -n "Key : '$key' - "
                redis-cli -p 6379 GET $key;
done
```
![screenshoot](https://github.com/Chibrik0ff/sdb-homeworks2/blob/main/img/img4.jpg)

---