# Удаление ставки НДС

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указан тип и обязательность параметров
- отсутствует ответ в случае ошибки и успеха
- нет примеров на др. языках
  
{% endnote %}

{% endif %}

{% note info "ccrm.vatdelete" %}

**Scope**: [`crm`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

## Описание

```http
crm.vat.delete(id)
```

Удаляет ставку НДС.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **id** | Идентификатор ставки НДС. ||
|#

{% include [Сноска о параметрах](../../../../_includes/required.md) %}

## Примеры

```javascript
var id = prompt("Введите ID");
BX24.callMethod(
    "crm.vat.delete",
    { "id": id },
    function(result)
    {
        if(result.error())
            console.error(result.error());
        else
            console.info(result.data());
    }
);
```

{% include [Сноска о примерах](../../../../_includes/examples.md) %}