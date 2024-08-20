# Удалить страну

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "documentgenerator.region.delete" %}

**Scope**: [`documentgenerator`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `documentgenerator.region.delete` удаляет регион.

#|
|| **Параметр** | **Описание** ||
|| **id**^*^ | ID региона. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %} 