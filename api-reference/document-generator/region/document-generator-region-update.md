# Изменить страну

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- отсутствуют примеры
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "documentgenerator.region.update" %}

**Scope**: [`documentgenerator`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `documentgenerator.region.update` обновляет существующую страну.

#|
|| **Параметр** | **Описание** ||
|| **id**^*^ | ID региона. ||
|| **fields** | Массив полей. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

## Параметры fields

#|
|| **Параметр** | **Описание** ||
|| **title** | Название страны. ||
|| **languageId** | Двухбуквенный идентификатор языка. ||
|| **formatDate** | Формат даты. ||
|| **formatDatetime** | Формат даты времени. ||
|| **formatName** | Формат имени. ||
|#

Все параметры необязательные.

## Ответ в случае успеха

Возвращает те же данные, что и при вызове [documentgenerator.region.get()](./document-generator-region-get.md).