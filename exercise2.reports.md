### Баг №1. Кросс-сайт stream.datago.ru не найден по запросу POST

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить  запрос POST https://stream.datago.ru/mp/collect?tid=UA-89387429-1
2. Проверить код состояния ответа

**Фактический результат:** Код состояния ответа - 404 Not Found

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0



### Баг №2.  Ошибка при авторизации по Сбер ID при запросе GET

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GET https://id.sber.ru/CSAFront/api/userdata?client_id=52cd75e2-76e1-43ba-ade6-938b2c7d4e7a
2. Проверить код состояния ответа

**Фактический результат:** Код состояния ответа - 400 Bad Request

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0



### Баг №3.Политика сайта запрещает чтение удаленного ресурса. Запрос CORS «Access-Control-Allow-Origin» не выполнен.

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GET https://cms-res.online.sberbank.ru/sberid/BlackList/Button/No_Button.json
2. Проверить код состояния ответа

**Фактический результат:** Запрос из постороннего источника заблокирован. Учетные данные не поддерживаются, если заголовок CORS «Access-Control-Allow-Origin» имеет значение «*».

**Ожидаемый результат:** Доступ к источнику предоставлен; Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0



### Баг №4.  Ошибка списка просмотренных продуктов  - цифровые данные не определены

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GET https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
2. Проверить код состояния ответа

**Фактический результат:** DDManager Custom Event "Viewed Product Listing" Error  t.digitalData(...) is undefined; Fingerprinting

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №5.  Ошибка доступа к API ВКонтакте: неуспешная отправка запроса

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос  https://vk.com/js/api/openapi.js?169:672
2. Проверить код состояния ответа

**Фактический результат:** Open api access error

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №6.  Ошибка при обращении к неопределенной переменной при входе в кабинет продавца Мегамаркета

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GET https://partner.sbermegamarket.ru/auth?needPrev=true 
2. Проверить код состояния ответа

**Фактический результат:** Uncaught ReferenceError: yaCounter55606897 is not defined

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №7.  Ошибка при передаче связки событий аналитики

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GET https://extra-cdn.sbermegamarket.ru/static/dist/main.05c7a63a.js:1:207193

   GET https://extra-cdn.sbermegamarket.ru/static/dist/main.05c7a63a.js:1:206014

2. Проверить код состояния ответа

**Фактический результат:** Error, Blocked request

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №8.  Неожиданный символ в линии 1 столбца 1  данных JSON на странице “Помощь продавцам”

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GET https://partner-wiki.megamarket.ru/s/88f8655ec55fb4654ce00c53a4df1969-CDN/qj3mxy/8804/1log4hf/b3787a8320a4f130e416f5326ae48227/_/download/contextbatch/js/_super/batch.js?locale=ru-RU:127
2. Проверить код состояния ответа

**Фактический результат:** SyntaxError: JSON.parse: unexpected character at line 1 column 1 of the JSON data

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №9.  Ошибка сервера -  "failed to queue envelope",  cause "envelope buffer capacity exceeded" 

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос POST https://sentry-dsn-customers.megamarket.tech/api/6/envelope/?sentry_key=6d82cc11d08a4657a9092ff80b4bd615&sentry_version=7
2. Проверить код состояния ответа

**Фактический результат:** 503 Service Unavailable

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №10.  Наименование продукта не определено (Uncaught TypeError)

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить view-source https://megamarket.ru/multicart/ line 418 > injectedScript:1
2. Проверить ответ

**Фактический результат:** Uncaught TypeError: a.product.name is undefined

**Ожидаемый результат:** Выполнен/Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №11.  Ошибка переменной  “t” (null) при просмотре вкладки “Мега Выгода”

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить campaign https://cdn.ddmanager.ru/ddm-initialization/f72a2e9d-633c-4ab0-9cff-2c32b4d5cad6.js:1
2. Проверить ответ

**Фактический результат:** TypeError: DDManager Custom Event "Viewed Campaign" Error  t is null

**Ожидаемый результат:** Выполнен/Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №12.  Неподдерживаемый медиа формат изображения

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Выполнить запрос GEThttps://main-cdn.sbermegamarket.ru/mid9/hlr-system/-11/367/831/591/019/23/100056553626b0.png
2. Проверить ответ

**Фактический результат:** SyntaxError: JSON.parse: unexpected character at line 1 column 1 of the JSON data

**Ожидаемый результат:** Статус прокси - 200 Connection

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0

### Баг №13.  Нарушение сценарием на стороне клиента политики происхождения браузера (просмотр вкладки “Избранное”)

**Предшествующие условия:**

1. Открыть URL https://megamarket.ru
2. Открыть консоль, нажав F12 или Ctrl+Shift+C

**Шаги:**

1. Перейти по вкладку “Избранное”
2. Проверить ответ

**Фактический результат:** error loading "library" error="Error: script error "https://cdn.retailrocket.ru/content/javascript/tracking.js""

error loading "library" error="Error: script error "https://api.flocktory.com/v2/loader.js?site_id=2319""

error loading "library" error="Error: script error "https://vk.com/js/api/openapi.js?150""

error loading "library" error="Error: script error "https://www.googletagmanager.com/gtag/js""

error loading "library" error="Error: script error "https://www.google-analytics.com/analytics.js""

**Ожидаемый результат:** library loaded

**Серьезность:** Major

**Окружение:** Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/117.0