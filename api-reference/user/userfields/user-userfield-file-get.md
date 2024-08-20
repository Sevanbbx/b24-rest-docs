# Получение файла из пользовательского поля

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- возможно, параметры или поля нужно расписать в таблице
- не указана обязательность параметров
- отсутствуют примеры на др.языках
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки
 
{% endnote %}

{% endif %}

{% note info "user.userfield.file.get" %}

**Scope**: [`user.userfield`](../../scopes/permissions.md) | **Права на выполнение**: `любой пользователь`

{% endnote %}

Метод позволяет получить файл из пользовательского поля.

## Пример

Есть поле `UF_USR_1604998606834` типа файл. Вызвав метод [user.current](../user-current.md) можно получить файл в этом поле у текущего пользователя, где:
- **showUrl** - это URL, который покажет файл в браузере, если пользователь авторизован;
- **downloadData** - данные, которые нужно подавать на этот метод.

```
[UF_USR_1604998606834] => Array
(
    [id] => 774
    [showUrl] => /bitrix/services/main/ajax.php?action=rest.file.get&SITE_ID=s1&entity=USER&id=1&field=UF_USR_1604998606834&value=774
    [downloadData] => Array
        (
            [id] => 1
            [field] => UF_USR_1604998606834
            [value] => 774
        )
)
```
{% include [Сноска о примерах](../../../_includes/examples.md) %}

Запрос вебхуком:

```http
/rest/1/a2ebx1rfao5pq5cr/user.userfield.file.get?id=1&field=UF_USR_1604998606834&value=774
```
{% note info "" %}

Метод возвращает файл как контент на загрузку, а не json/xml.

{% endnote %}