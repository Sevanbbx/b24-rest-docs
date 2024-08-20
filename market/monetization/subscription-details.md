# Что такое подписная модель?

**Подписка Битрикс24 Маркет Плюс** - это способ предоставления доступа конечным клиентам к целому набору приложений для Битрикс24 за фиксированную стоимость и методика расчета авторского вознаграждения, для распределения выручки Битрикс между отдельными разработчиками.

Чтобы распределение было честным, мы делим выручку, полученную от продажи подписки каждого отдельного клиента, между теми разработчиками, чьи решения действительно использовались на конкретном Битрикс24. Это позволяет авторам зарабатывать даже на решениях, нацеленных на узкую целевую аудиторию.

## Принцип распределения выручки

Мы помогаем разработчикам решений зарабатывать на Битрикс24 Маркет. Для этого мы создаем условия, помогающие разработчикам создавать качественные решения: направляем выплаты тем разработчикам, ради решения которых клиенты приобрели подписку, и тем разработчикам, чьи решения пользователи, в конечном итоге, использовали в рамках подписки.

**85% ОТ ВЫРУЧКИ - РАЗРАБОТЧИКАМ!**

1С-Битрикс оставляет себе небольшую часть - всего 15%. 85% от выручки получают разработчики решений, участвующих в подписке!

**50% ВОЗНАГРАЖДЕНИЯ В МОМЕНТ ПОКУПКИ**

Половина вознаграждения сразу идет приложениям, которые привели к продаже подписке. Мы учитываем реальное использование таких приложений, чтобы распределить между ними выручку в правильных пропорциях. Это помогает разработчикам решений получать денежные выплаты от новых клиентов.

**50% ПО МЕРЕ ИСПОЛЬЗОВАНИЯ**

Вторая половина вознаграждения распределяется в течение действия подписки между приложениями, которые клиент использует. Это помогает разработчикам решений получать стабильные денежные выплаты от растущего числа постоянных пользователей.

## Вознаграждение за покупку подписки

Как мы определяем приложения, ради которых клиенты приобретают подписку? Наша система фиксирует, какие приложения используются, и распределяет вознаграждение между ними. Существует несколько таких ситуаций:

### ИСПОЛЬЗОВАНИЕ ВО ВРЕМЯ ТРИАЛА

Клиент сначала решил попробовать триал подписки, установил несколько приложений, часть удалил и, в конечном итоге, нашёл те приложения, которые оказались для него достаточно полезными, чтобы стать покупателем подписки Маркет Плюс. Именно среди таких решений, которые были установлены, использовались во время триала подписки и не были удалены на момент покупки подписки, мы будем распределять 50% от выручки сразу после оплаты в долях, пропорциональных использованию.

### ИСПОЛЬЗОВАНИЕ ПОСЛЕ ПОКУПКИ

Клиент может купить подписку без предварительного триала, считая, что ему наверняка пригодятся решения, входящие в подписку. Тогда он начинает устанавливать и оценивать приложения уже после оплаты подписки. Среди таких решений, которые были установлены, использовались в период от момента покупки и до конца отчетного месяца и не были удалены до конца отчетного месяца, мы будем распределять 50% от выручки в начале следующего месяца в долях, пропорциональных использованию.

### ИСПОЛЬЗОВАНИЕ ПЕРЕД ПРОДЛЕНИЕМ ПОДПИСКИ

Если приложения продолжают быть полезными для клиента, то он продлевает подписку на Маркет Плюс. В этом случае, мы проверяем, какие приложения использовались клиентом в течение 30 календарных дней перед оплатой продления и не были удалены до конца отчетного месяца, и распределяем между ними 50% от выручки сразу после оплаты в долях, пропорциональных использованию.

## Вознаграждение за использование приложений

Важно, не только какие приложения привлекли клиентов в подписку, но и какими решениями клиенты продолжают пользоваться в конечном итоге. Наша система ежедневно фиксирует, какие приложения используются на каждом отдельно взятом Битрикс24, и распределяет 50% вознаграждения между ними.

## Как распределяются доли между приложениями?

Каждый день на каждом Битрикс24, на котором клиент приобрел подписку на Битрикс24 Маркет, мы начисляем баллы за факты использования того или иного решения. Каждый день эти баллы суммируются и доли стоимости подписки, приходящейся на один день использования, распределяются между разработчиками (как и доли от вознаграждения за покупку подписки). В конечном итоге эти суммы складываются и перечисляются разработчикам.

Под **использованием** мы понимаем не факт установки решения на Битрикс24, а обращение пользователей к функционалу этого решения:

1. вызовы REST API;
2. переход пользователя в интерфейс решения (включая встройки виджетов);
3. срабатывание обработчиков REST-событий;
4. срабатывание обработчиков действий бизнес-процессов, роботов и триггеров;
5. наличие опубликованных магазинов и сайтов, созданных на шаблонах или с использованием блоков из решений;
6. наличие установленных решений-конфигураторов (готовые CRM, умные сценарии и т.д.);

При публикации решения в каталоге Маркет, модераторы указывают для каждого решения его **категорию сложности (вес)** из заранее предопределенного перечня, а система мониторинга автоматически, по мере работы приложения на каждом отдельно взятом Битрикс24, определяет **частоту (режим) использования**.

Каждый день каждому решению, распространяемому в рамках подписки, за каждый Битрикс24, где оно используется, начисляются баллы за использование по простой формуле: **вес решения * коэффициент частоты использования**.

### Вес/сложность

Разные решения имеют разный "вес" при начислении баллов, в зависимости от того, какой функционал предлагает то или иное решение. Мы постарались сделать эти категории понятными и честными, чтобы в итоге они соответствовали и сложности разработки, и, одновременно, пользе для бизнеса. Модератор фиксирует категорию при рассмотрении заявки на модерацию решения и указывает категорию с максимальным весом, если решение подходит под несколько категорий:

| Тип приложения | Вес         | Описание    |
| -------------- | ----------- | ----------- |
| 1              | 10          | Многофункциональный разноплановый интерфейс внутри Битрикс24, не менее 2-х типов встроек (интерфейс настроек пользовательских опций решения не учитывается в качестве пользовательского функционала)      |
| 2              | 8           | Многофункциональный разноплановый интерфейс внутри Битрикс24, менее 2-х типов встроек (интерфейс настроек пользовательских опций решения не учитывается в качестве пользовательского функционала)       |
| 3              | 8           | Шаблон интернет-магазина Битрикс24                                     |
| 4              | 5           | Триггеры, роботы, действия бизнес-процессов                            |
| 5              | 5           | Автообработчик rest-события                                            |
| 6              | 5           | AI-провайдер для Copilot Битрикс24                                     |
| 7              | 5           | Шаблон сайта Битрикс24                                                 |
| 8              | 5           | Дашборд для BI-конструктора                                            |
| 9              | 5           | Коннектор открытых линий                                               |
| 10             | 5           | Интеграция с телефонией или смс-провайдером                            |
| 11             | 5           | Решения для массовых рассылок или интеграция с сервисом рассылки       |
| 12             | 5           | Конструкторы чат-ботов или решения с готовыми чат-ботами для Битрикс24 |
| 13             | 5           | Массовый экспорт/импорт данных                                         |
| 14             | 3           | Платежные системы или службы доставки                                  |
| 15             | 3           | Пользовательские типы полей                                            |
| 16             | 1           | Отраслевые CRM                                                         |
| 17             | 1           | Шаблоны групп/проектов Битрикс24 (запланировано)                       |
| 18             | 1           | Шаблоны баз знаний Битрикс24 (запланировано)                           |
| 19             | 1           | Умные сценарии                                                         |
| 20             | 1           | Prompt для Copilot Битрикс24                                           |
| 21             | 1           | Прочее                                                                 |

### Частота использования

Решения могут приносить пользу бизнесу ежедневно или периодически. Бывают сценарии (обычно связанные с получением аналитических отчетов), которые требуют обращения пользователей раз в неделю, а то и раз в месяц. Чтобы сделать подписную модель сбалансированной как для решений ежедневного массового использования, так и продуктов с периодическими сценариями, мы автоматически учитываем режим обращения к приложению и вносим в начисление баллов поправочный коэффициент.

Решение считается ежедневным на конкретном Битрикс24, если используется чаще двух дней в неделю; еженедельным, если используется более раза в месяц; или ежемесячным, если используется не более одного раза в месяц. Если к решению не обращались более месяца, начисление баллов прекращается, даже если технически решение остаётся установленным на Битрикс24.

В отличие от веса, который присваивает модератор решению в целом, режим использования определяется автоматически для каждого решения на каждом отдельно взятом Битрикс24. Это значит, что на одном Битрикс24 ваше решение может использоваться ежедневно, а на другом раз в месяц с соответствующим поправочным коэффициентом. Начисление баллов при этом происходит ежедневно.

| Коэффициент  | Режим использования  | Примеры решений |
| -----------  | -------------------- | --------------- |
| 1            | Ежедневное           | автоматизация на событиях или роботах, встройки интерфейса, чатботы, коннекторы открытых линий, отраслевые crm, умные сценарии, опубликованные сайты24 и т.д. |
| 0,7          | Еженедельное         | оперативная аналитика, экспорт/импорт данных, лидогенерация, рассылки и т.д. |
| 0,5          | Ежемесячное          | отчетная аналитика, экспорт/импорт данных, лидогенерация и т.д. |

## Пример расчета вознаграждения за использование

Проще всего понять все на конкретном примере. Возьмём один конкретный Битрикс24, на котором пользователь установил два разных решения от двух авторов и представим, что наша система собрала информацию об использованиях. Пусть для простоты оба решения относятся к решениям ежедневного использования с поправочным коэффициентом равным 1. 

**Решение 1-1** от первого разработчика - это готовый интернет магазин для Битрикс24 (тип 3 с весом 8), а **Решение 2-1** - это действие бизнес-процесса (тип 4 с весом 5). 

15.05.2019 - 17.05.2019 на портале xxx.bitrix24.ru использовались оба решения, а 18.05.2019 - только **Решение 2-1**.

В этом случае, расчет вознаграждения будет происходить следующим образом (общее дневное вознаграждение указано для примера, в реальности оно рассчитывается из конкретной стоимости подписки в зависимости от тарифного плана Битрикс24, наличия какой-то маркетинговой скидки и продажи через партнерскую сеть):

| Дата        | Портал          | Разработчик   | ПО          | Тип  | Баллов за факт использования | Общее дневное вознаграждение | Общее количество баллов за день  | Количество баллов за использование решения  | Коэффициент использования решения  | Дневное вознаграждение лицензиара |
| ----------- | --------------- | ------------- | ----------- | ---- | ---------------------------- | ---------------------------- | ---------------------------- | ---------------------------- | ---------------------------- |  ---------------------------- | 
| 15.05.2019  | xxx.bitrix24.ru | Разработчик-1 | Решение 1-1 | 3    | 8                            | 9,9167                       | 13 | 8  | 0,6154 | 6,1026 |
| 15.05.2019  | xxx.bitrix24.ru | Разработчик-2 | Решение 2-1 | 4    | 5                            | 9,9167                       | 13 | 5  | 0,3846 | 3,8141 |
| 16.05.2019  | xxx.bitrix24.ru | Разработчик-1 | Решение 1-1 | 3    | 8                            | 9,9167                       | 13 | 8  | 0,6154 | 6,1026 |
| 16.05.2019  | xxx.bitrix24.ru | Разработчик-2 | Решение 2-1 | 4    | 5                            | 9,9167                       | 13 | 5  | 0,3846 | 3,8141 |
| 17.05.2019  | xxx.bitrix24.ru | Разработчик-1 | Решение 1-1 | 3    | 8                            | 9,9167                       | 13 | 8  | 0,6154 |  6,1026 |
| 17.05.2019  | xxx.bitrix24.ru | Разработчик-2 | Решение 2-1 | 4    | 5                            | 9,9167                       | 13 | 5  | 0,3846 | 3,8141 |
| 18.05.2019  | xxx.bitrix24.ru | Разработчик-2 | Решение 2-1 | 4    | 5                            | 9,9167                       | 5  | 5  | 1,00 | 9,9167 |

## Почему это работает?

Этот пример хорошо демонстрирует несколько важных вещей о распределении выручки:

1. Чем больше разных Битрикс24 используют ваше решение, тем больше вы получаете.
2. Чем больше ваша доля в ежедневном распределении выручки, тем больше вы получаете. 
3. Чем больше клиентов использовали ваше решение во время триала подписки перед оплатой, тем больше вы получаете.
4. Если клиент платит за подписку, но не использует ваши решения, вы не участвуете в распределении выручки от него.
5. Если клиент платит за подписку и использует только ваши решения, вы получаете **все 85% выручки**.

Разработчики всегда претендуют на одну и ту же часть выручки от стоимости подписки. Модель влияет только на то, как именно эта часть будет распределена между конкретными разработчиками.

Мы выбрали такую модель, потому что это лучший способ распределить выручку, и для успеха вам нужно придерживаться нескольких принципов:

1. Создавайте решения, которые нужны максимально широкому кругу пользователей.
2. Делайте уникальные решения, которые полностью решают потребности нишевого бизнеса.
3. Не старайтесь копировать решения, которые уже широко используются большим количеством клиентов.
4. Не пытайтесь обмануть систему, делайте действительно качественные полезные решения.

Подписная модель продаж не ограничивает вас в выборе продуктовой стратегии: успех может прийти как в результате создания суперхитов "для всех", так и в случае разработки уникальных многофункциональных нишевых решений.