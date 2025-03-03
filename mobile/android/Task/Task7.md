#  Задача 7 | Корзина – логика отображения и работы экрана

[⬅️ назад](../README.md)

## ТЗ

Необходмио реализовать логику работы корзины

#### Общая логика

1. При открытии экрана 
    1. Получаем данные
        1. Берем содержимое корзины из CartRepository
        2. Получаем отсутсвующие данные из GetBonusInfoFromGoodInfoUseCase + UserRepository 
    2. Подготавливаем список товаров к отображению (List<GoodCartInfo>)
    3. Рассчитываем стоимость. Складываем все веса товаров и их цены
    4. Рассчитываем бонус
2. Удаление элемента
    1. Обновляем общее хранилище корзины
    2. Переконфигурируем отображение и пересчитываем бонусы и итог по товарам
    3. Если товаров уже нет – закрываем экран текущий
3. Нажатие на кнопку "Купить"
    1. Переход на экран оплаты

#### CartManagerImpl

3. Рассчет веса
    1. Для каждого товара сначала учитываем тип (kilo или gramm)
    2. Умножаем вес товара на количество.
    3. Складываем все веса и возвращаем в килограммах. (Тип Double)

3. Рассчет стоимости
    1. Для каждого товара берем количество и стоимость
    2. Складываем всю стоимость товаров
    
4. Рассчет бонуса
    1. Для каждого товара берем бонус, если он есть из `GetBonusInfoFromGoodInfoUseCase`
    2. Применяем бонус, если это кэшбэк – получаем число рублей, которое вернется
    3. Для любимых товаров (находим соответствующее поле у пользователя из `UserRepository`)
        1. Если есть бонус
            1. Умножаем на 1.2 значение бонуса
        2. Если нет бонуса. Тогда в зависимости от активности пользователя: 
            1. 0-25: доп. кэшбэк 0%
            2. 26-50: доп. кэшбэк 2%
            3. 51-75: доп. кэшбэк 3%
            4. 76-100: доп. кэшбэк 5% 
    4. Складываем по всем товарам кэшбэк и баллы

5. Список товаров (List<GoodCartInfo>)
    1. totalCost - итоговая сумма по товару (цена * количество)
    2. countInCart - количество товара в корзине
    3. quantityValue - число граммов или килограммов за все количество товаров (число г/кг * количество в корзине)
    4. goodInfo - прокидываем информацию о товаре из корзины

## Ожидаемое решение

- Необходимо реализовать `CartManager`, который менеджерит общую логику корзины
- Допишите класс `CartManagerImpl`
