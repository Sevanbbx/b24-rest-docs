# Установка выбранной sip-линии в качестве исходящей линии по умолчанию

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "voximplant.line.outgoing.sip.set" %}

{% include notitle [Скоуп telephony admin](../../_includes/scope-telephony-admin.md) %}

{% endnote %}

Метод `voximplant.line.outgoing.sip.set` устанавливает выбранную sip-линию в качестве исходящей линии по-умолчанию. Метод доступен обладателю [права](https://helpdesk.bitrix24.ru/open/18177766/) `Управление номерами - изменение - любые`.

#|
|| **Параметр** | **Описание** ||
|| **CONFIG_ID** | Идентификатор настройки sip-линии. ||
|#

## Пример

```js
BX24.callMethod(
    "voximplant.line.outgoing.sip.set",
    {
        "CONFIG_ID": 57,
    },
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

## Ответ в случае успеха

Возвращает 1 при успешном выполнении