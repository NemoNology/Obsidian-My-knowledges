#SQL
# Синтаксис
## Создание индекса
```sql
CREATE INDEX [index_name]
ON [table_name] ([column(s)_name(s)]);
```
## Удаление индекса
```sql
DROP INDEX index_name;
```
# Важно помнить
- Индексам необходимо место для хранения;
- При добавлении данных в БД сначала обновляется исходная таблица, а затем её индексы;
# Рекомендации
## Индексацию стоит использовать
- В таблицах с плановым обновлением.
## Индексацию не стоит использовать
- В таблицах с регулярным обновлением, ибо при постоянных обновлениях БД индексы обновляться не будут и станут бесполезны;
- В таблицах с частыми массовыми `update` и `insert`;
- В небольших таблицах;
- Для столбцов в таблицах с большим количеством `null` значений;
- Для столбцов, которые часто обрабатываются.
# Типы индексов
## Кластеризованный
Использует первичный ключ для структуризации данных в таблице. Он не требует явного объявления и создаётся по умолчанию при определении ключа.
## Некластеризованный
Нужен, чтобы применить индексы к неключевым столбцам - такие индексы требуют явного объявления.
Храниться данный индекс в одном месте, а физ. данные таблицы - в другом.
# Ссылки
- [YouTube - Listen IT - Что такое SQL ИНДЕКСЫ за 10 минут: Объяснение с примерами](https://www.youtube.com/watch?v=LpEwssOYRKA)