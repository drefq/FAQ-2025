# PROD – Mobile (Android) – "Голодные" мобильные игры

> [!IMPORTANT]
> **Версия условия** – 1.2

## 🚀 Введение

### Контекст разработки


Добро пожаловать в команду "Т–Вкусно"! Это сервис для заказа продуктов с выгодой. Его цель — предоставить пользователю витрину разнообразных товаров, которые можно приобрести с накоплением баллов в системе лояльности или получить кэшбэк в рублях.

"Т–Вкусно" — очень популярный сервис, и в связи с ростом его популярности было решено нанять новых талантливых разработчиков. Команда лидеров разработки организовала челлендж, чтобы определить лучшего кандидата на роль защитника от "голода" клиентов. Для этого был взят текущий проект мобильного приложения сервиса и из него удалена вся основная реализация. Это позволит определить, кто сможет лучше всего восстановить функциональность. 

Участвовать в этом захватывающем и важном испытании предстоит именно вам! Ваша задача – дописать приложение в соответствии с ТЗ отдельных его компонентов.

Все приложение состоит из 3х экранов

1. Главная
    - Отображение товарного рекламного баннера, чтобы показывать актуальные предложения по выгодным покупках
    - Товарная лента – витрина всех доступных к покупке товаров в сервисе
2. Корзина 
    - Экран формирования покупки. Сюда вы попадаете, когда выбираете интересующие вас товары на главном экране. Здесь показываются все ваши товары и финальная стоимость заказа, а также информация о бонусах
3. Оплата
    - Для завершения попкупки необходимо оплатить заказ, а для этого нужно ввести платежные данные. Именно на этом экране отображается форма ввода данных о карте покупателя, чтобы совершить платеж

### Устройство проекта

Проект представляет из себя многомодульное приложение. Предыдущий разработчик оставил основные компоненты приложения в `core-api`, а в `core-impl` реализовал код, который позволяет запустить приложение. Ваша задача – реализовать недостающие сущности в своём модуле `solution`.

> [!WARNING]
> Вести разработку нужно строго в модуле `solution`. Вы реализуете сущности по конкретному контракту, который уже зафиксирован предыдущими разработчиками для корректной работы приложения. Поэтому вам нельзя вносить изменения в другие модули. Вы можете создавать новые сущности, но итоговая реализация должна соответствовать ожидаемому от вас в задании интерфейсу

## 📚 Задачи

Товарный баннер
* [Задача 1 ➡️](Task/Task1.md) ~3%
* [Задача 2 ➡️](Task/Task2.md) ~3%
* [Задача 3 ➡️](Task/Task3.md) ~7%

Товарная лента
* [Задача 4 ➡️](Task/Task4.md) ~8%
* [Задача 5 ➡️](Task/Task5.md) ~17%
* [Задача 6 ➡️](Task/Task6.md) ~12%

Корзина
* [Задача 7 ➡️](Task/Task7.md) ~14%
* [Задача 8 ➡️](Task/Task8.md) ~8%
* [Задача 9 ➡️](Task/Task9.md) ~17%

Оплата
* [Задача 10 ➡️](Task/Task10.md) ~5%
* [Задача 11 ➡️](Task/Task11.md) ~6%

Решать все не обязательно. Чем больше баллов вы наберете, тем больше ваш шанс. У каждого задания имеется свой вес. Выбирайте с умом. Удачи!

## 📝 Оформление

Решение задания – реализация отдельного класса. Поэтому ваше решение ожидается в методах классов, перечисленных в условиях задачи и размещённых в модуле `solution`.

Требования к оформлению отдельных задач указаны в их описании.

## 🎨 Макеты

Все дизайны доступны в макете Figma по ссылке – https://www.figma.com/design/M0ekYZvZTfk2bVRLjEtGLf/PROD-%E2%80%93-mobile-%E2%80%93-2025?node-id=1-2

Но изучайте задание. Там могут быть дополнительные комментарии к макетам

## ❗️ Ограничения

* Язык – Kotlin.
* Пользовательский интерфейс – View и XML, без использования Jetpack Compose.
* Все изменения – только в `solution`-модуле. Оставшиеся модули следует оставить без изменений.
* Нельзя подключать в проект посторонние зависимости (все необходимые зависимости для выполнения задания уже подключены)
* [Рекомендуется] Android Studio Koala Feature Drop | 2024.1.2 (August 2024) или новее

## 🔄 Проверка UI

Реализованные элементы интерфейса сравниваются тестирующей системой с помощью сравнения с эталонным скриншотом.

Версия Android на тестирующей системе – Android 15 (API level 35)
