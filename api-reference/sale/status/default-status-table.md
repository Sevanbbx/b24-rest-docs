# Таблица статусов по умолчанию

По умолчанию в системе создается набор статусов. Некоторые из них являются системными, и на работу с ними есть ряд ограничений — например, системные статусы нельзя удалять. Ограничения (если они есть) описаны в конкретных [методах работы со статусами](./index.md). 

#|
|| **Идентификатор статуса** | **Тип**  | **Описание** | **Системный** ||
|| `N` | Заказ | Принят, ожидается оплата | Да ||
|| `S` | Заказ | Отправлен | Нет ||
|| `P` | Заказ | Оплачен, формируется к отправке | Нет ||
|| `D` | Заказ | Отменен | Нет ||
|| `F` | Заказ | Выполнен | Да ||
|| `DN` | Доставка | Ожидает обработки | Да ||
|| `DD` | Доставка | Отменен | Нет ||
|| `DF` | Доставка | Отгружен | Да ||
|#

## Продолжите изучение

- [{#T}](./index.md)
- [{#T}](./sale-status-add.md)
- [{#T}](./sale-status-update.md)
- [{#T}](./sale-status-get.md)
- [{#T}](./sale-status-list.md)
- [{#T}](./sale-status-delete.md)
- [{#T}](./sale-status-get-fields.md)