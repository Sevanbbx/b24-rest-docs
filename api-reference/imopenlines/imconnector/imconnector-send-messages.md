# Отправить сообщения в Битрикс24

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указан тип параметров
- не указана обязательность параметров
- отсутствуют примеры на др.языках

{% endnote %}

{% endif %}

{% note info "imconnector.send.messages" %}

**Scope**: [`imopenlines`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод отправки сообщений в ОЛ.

## Параметры

#|
|| **Параметр** | **Описание** | **С версии** ||
|| **CONNECTOR**
[`unknown`](../../data-types.md) | ID коннектора (который был указан при регистрации обработчика). | ||
|| **LINE**
[`unknown`](../../data-types.md) | ID открытой линии. | ||
|| **MESSAGES**
[`unknown`](../../data-types.md) | Массив сообщений, где сообщения описываются массивом следующего формата: 

```
array(
    array(
        //Массив описания пользователя
        'user' => array(
            'id',//ID пользователя во внешней системе *
            'last_name',//Фамилия
            'name',//Имя
            'picture' =>
                array(
                    'url'//Ссылка на аватарку пользователя, доступную для портала
                ),
                'url',//Ссылка на профиль пользователя
                'sex',//Пол. Допустимо male и female
                'email', //email
                'phone', //телефон
                'skip_phone_validate' => 'Y', //В значении 'Y' позволяет не применять валидацию 
                                              //номера телефона пользователя. По умолчанию         
        ),
        //Массив описания сообщения
        'message' => array(
            'id', //ID сообщения во внешней системе.*
            'date', //Время сообщения в формате timestamp *
            'disable_crm' => 'Y' ,//отключить чат трекер (CRM трекер)
            'text', //Текст сообщения. Должен быть указан элемент text или files. 
                    //Допустимое форматирование (BB коды) описаны 
                    //здесь: https://dev.1c-bitrix.ru/learning/course/?COURSE_ID=93&LESSON_ID=7679
            'files' => array(//Массив описаний файлов, где каждый файл описывается 
                             //массивом, со ссылкой, которая доступна порталу
                array('url' => 'Cсылка на файл'),
                array('url' => 'Cсылка на файл'),
                ...
            )
        ),
        //Массив описания чата
        'chat' => array(
            'id',//ID чата во внешней системе *
            'name', //Имя чата во внешней системе
            'url', //Ссылка на чат во внешней системе
        ),
    ),
    array(...),
);

```
Формат передаваемого файла не имеет ограничений. В чате вложение в сообщение может форматироваться как картинка для типов: jpe, jpg, jpeg, png, webp, gif, bmp.

Сообщения можно отправлять от имени менеджера, указав user_id в массиве message.
| ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

{% note info "Примечание" %}

Параметр **skip_phone_validate** из структуры пользователя рекомендуется применять только в исключительных случаях. Параметр - вынужденная мера для преодоления ограничений валидатора номеров телефонов.

{% endnote %}

## Ошибки при вызове метода и их причины

#|
|| **Код** | **Выводимый текст ошибки** | **Пояснение** ||
|| **WRONG_AUTH_TYPE** | Current authorization type is denied for this method | Некорректный тип авторизации. Необходим тип oauth ||
|| **CONNECTOR** | Argument 'CONNECTOR' is null or empty | Не указан обязательный параметр в запросе 'CONNECTOR' ||
|| **LINE** | Argument 'LINE' is null or empty | Не указан обязательный параметр в запросе 'LINE' ||
|| **MESSAGES** | Argument 'MESSAGES' is null or empty | Не указан обязательный параметр в запросе 'MESSAGES' ||
|| **MESSAGES** | The value of an argument 'MESSAGES' must be of type array | Значение параметра не является массивом. ||
|| **IMCONNECTOR_NO_CORRECT_PROVIDER** | Не удалось найти подходящий провайдер для коннектора | Некорректное значение в параметре 'CONNECTOR' ||
|| **IMCONNECTOR_COULD_NOT_GET_PROVIDER_OBJECT** | Не удалось получить объект провайдера | Некорректное значение в параметре 'CONNECTOR' ||
|| **IMCONNECTOR_NOT_SPECIFIED_CORRECT_COMMAND** | Не указана корректная команда | Что-то невероятное. Это где-то ошибся разработчик. ||
|| **IMCONNECTOR_NOT_SPECIFIED_CORRECT_CONNECTOR** | Не указан коннектор | Некорректное значение в параметре 'CONNECTOR' ||
|| **NOT_ACTIVE_LINE** | Линия c таким ID неактивна или не существует | Линия на портале удалена или отключена ||
|| **PROVIDER_UNSUPPORTED_TYPE_INCOMING_MESSAGE** | Неподдерживаемый тип входящего сообщения от сервера | Некорректное значение в параметре 'type_message', если он передан ||
|| **IMCONNECTOR_NOT_ALL_THE_REQUIRED_DATA** | Переданы не все необходимые данные | Пустое или не корректное значение в параметре 'user' ||
|| **CONNECTOR_PROXY_NO_ADD_USER** | Не удалось создать или получить пользователя системы, сопоставленного с пользователем удаленного мессенджера | Для работы чата открытых линий необходимо на портал добавить специального технического пользователя с признаком, что это пользователь для мессенджер-коннектора, и под которым невозможно авторизоваться ||
|| **CONNECTOR_PROXY_NO_USER_IM** | Не получен id пользователя мессенджера | Некорректное значение поля 'id' в параметре 'user'. Это следствие предыдущей ошибки ||
|| **IMCONNECTOR_NOT_ALL_THE_REQUIRED_DATA** | Переданы не все необходимые данные | Некорректное значение поля 'text' или 'files' в параметре 'message'. Не переданы какие-либо данные для отправки сообщения ||
|| **100** | The MESSAGES parameter must be an array of messages (arrays) | Значение параметра 'MESSAGES' должно быть массивом сообщений. ||
|| **100** | The incorrect structure of a message inside MESSAGES parameter. | Некорректная структура сообщений. ||
|#