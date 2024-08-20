# Изменение владельца группы

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствует ответ в случае ошибки
- нет примеров на др. языках

{% endnote %}

{% endif %}

{% note info "sonet_group.setowner" %}

{% include notitle [Скоуп sonet все](./_includes/scope-sonet-all.md) %}

{% endnote %}

## Описание

Метод изменяет владельца группы. Может быть запущен либо администратором социальной сети, либо текущим владельцем группы.

## Параметры:

#|
|| **Параметр** | **Описание** ||
|| **GROUP_ID** | Идентификатор группы, владелец которой меняется. ||
|| **USER_ID** | Идентификатор нового владельца. ||
|#

{% include [Сноска о параметрах](../../_includes/required.md) %}

В случае успеха возвращает `true`.

## Пример

```js
BX24.callMethod('sonet_group.setowner', {
    'GROUP_ID': 11,
    'USER_ID': 2
});
```
{% include [Сноска о примерах](../../_includes/examples.md) %}