# Удаление свойств товаров или торговых предложений

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указана обязательность параметров
- отсутствует ответ в случае ошибки
- нет примеров на др. языках
  
{% endnote %}

{% endif %}

{% note info "catalog.productProperty.delete" %}

**Scope**: [`catalog`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

## Описание

```http
catalog.productProperty.delete(id)
```

Метод удаляет свойство товаров или торговых предложений.
Если операция успешна, возвращается `true` в теле ответа.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **id** 
[`integer`](../../data-types.md)| Идентификатор свойства товаров или торговых предложений. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

## Примеры

```javascript
BX24.callMethod(
    'catalog.productProperty.delete',
    {
        id: 128
    },
    function(result)
    {
        if(result.error())
            console.error(result.error().ex);
        else
            console.log(result.data());
    }
);
```
{% include [Сноска о примерах](../../../_includes/examples.md) %}