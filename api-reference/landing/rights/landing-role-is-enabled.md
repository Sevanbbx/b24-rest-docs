# Определение модели прав

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

{% note info "landing.role.isEnabled" %}

**Scope**: [`landing`](../../scopes/permissions.md) | **Права на выполнение**: `администратор`

{% endnote %}

Метод `landing.role.isEnabled` определяет, какая модель в данный момент включена на проекте, расширенная или ролевая.

## Параметры

Без параметров.

## Примеры

```js
BX24.callMethod(
    'landing.role.isEnabled',
    {
    },
    function(result)
    {
        if(result.error())
        {
            console.error(result.error());
        }
        else
        {
            if (result.data())
            {
                console.log('Ролевая модель');
            }
            else
            {
                console.log('Расширенная модель');
            }
        }
    }
);
```

{% include [Сноска о примерах](../../../_includes/examples.md) %}