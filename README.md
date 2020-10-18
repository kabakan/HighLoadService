==========================HighLoadService============================
1. Запустить cmd из директорий HighLoadService-1.0
java -jar HighLoadService-1.0.jar

2. Поднимется REST сервис http://localhost:8787/api/service/load/send

Пример запроса JSON:

curl --location --request POST 'http://localhost:8787/api/service/load/send' \
--header 'Content-Type: application/json' \
--data-raw '{
    "accCode":"RU1111000044445555666601",
    "summ":"2000",
    "currCode":"RUB"
}'

3. Результат запишется в файле transfer.log в той же директорий HighLoadService-1.0

Примечание:
Если используйте инструмент JMeter, то вложении конфиг файл HighLoad.jmx
Провели нагрузку JMeter на сервис TPS = 2000, на ноутбуке Core I5, RAM 8 Gb.
