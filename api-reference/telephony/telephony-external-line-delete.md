# Удаление внешней линии

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "telephony.externalLine.delete" %}

{% include notitle [Скоуп telephony admin](./_includes/scope-telephony-admin.md) %}

{% endnote %}

Метод `telephony.externalLine.delete` удаляет внешнюю линию.

#|
|| **Параметр** / **Тип** | **Описание** ||
|| **NUMBER** 
[`string`](../data-types.md) | Номер внешней линии. ||
|#