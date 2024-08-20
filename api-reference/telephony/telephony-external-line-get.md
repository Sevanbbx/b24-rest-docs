# Получение списка внешних линий приложения

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "telephony.externalLine.get" %}

{% include notitle [Скоуп telephony admin](./_includes/scope-telephony-admin.md) %}

{% endnote %}

Метод `telephony.externalLine.get` позволяет получить список внешних линий приложения.

Без параметров.