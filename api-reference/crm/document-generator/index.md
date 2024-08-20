# Генератор документов

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужно вступление, соответствующее заголовку

{% endnote %}

{% endif %}

{% note info "Права" %}

**Scope**: [`crm.documentgenerator`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

REST-методы CRM для документов реализованы через аякс-контроллеры. При этом сами контроллеры и их экшны реализованы в модуле [Генератор документов](https://dev.1c-bitrix.ru/api_d7/bitrix/documentgenerator/index.php), а в модуле CRM только обвязка для них. Эта обвязка преобразует входные и выходные параметры в соответствии с новым стандартом REST, а также учитывая особенности модуля CRM.

При работе с методами документов через скоуп CRM есть возможность работать только с шаблонами / документами, привязанными к модулю CRM.

## Особенности передаваемых значений

### Провайдеры

Модуль **Генератор документов** в качестве идентификатора провайдера данных использует полное наименование класса. Т.к. в модуле CRM используется именованные / числовые идентификаторы для идентификации сущностей, в RESTе для документов был использован аналогичный синтаксис. Если входной параметр называется *entityTypeId*, то он принимает числовой индекс сущностей CRM. На данный момент есть следующие идентификаторы:

- 1 - лид
- 2 - сделка
- 3 - контакт
- 4 - компания
- 5 - счет
- 7 - предложение
- 14 - заказ
- 31 - новые счета

Также предусмотрена возможность использования смарт-процессов: их *entityTypeId* также поддерживаются в Генераторе документов.

### Фильтрация по направлениям сделок

Методы REST не учитывают настройку привязки шаблона к провайдерам. Т.е. если был отправлен запрос на генерацию документа по шаблону с провайдером, к которому этот шаблон не привязан, ошибки не будет. Отсюда же следует, что не учитывается привязка шаблона к определенному направлению сделок. Если вы хотите указать сделку в качестве провайдера, всегда указывается только числовой идентификатор (2).

### Список регионов

Каждый шаблон привязан к определенной стране. Список стран фиксирован и на данный момент состоит из:

- ru - Россия
- by - Беларусь
- kz - Казахстан
- ua - Украина
- br - Бразилия
- mx - Мексика
- de - Германия
- uk - Великобритания
- pl - Польша

Управление регионами осуществляется в разделе [documentgenerator](../../document-generator/region/index.md).