# Приложение "Кусок Италии"

### 1. Меню
- **Пиццы**
  - Описание и фотографии различных видов пиццы
- **Закуски**
  - Антипасти, салаты, гарниры
- **Напитки**
  - Безалкогольные и алкогольные напитки
- **Десерты**
  - Тирамису, канноли и другие сладости

### 2. Специальные предложения
- Акции и скидки
- Сезонные и ограниченные предложения
- Комбо-наборы

### 3. Заказ онлайн
- Выбор пиццы и других блюд
- Настройка заказа (выбор теста, добавление ингредиентов)
- Оформление и оплата заказа

### 4. Доставка
- Условия и стоимость доставки
- Время доставки
- Отслеживание заказа

### 5. О нас
- История пиццерии
- Философия и концепция
- Команда и шеф-повар

### 6. Отзывы
- Комментарии и оценки от клиентов
- Возможность оставить свой отзыв

### 7. Рецепты
- Подборка рецептов пиццы и итальянских блюд
- Видеоуроки и советы от шефа

### 8. Контакты
- Адрес и карта расположения
- Телефон и электронная почта
- Социальные сети

### 9. Часто задаваемые вопросы (FAQ)
- Ответы на распространенные вопросы
- Политика возврата и обмена

### 10. Программа лояльности
- Бонусы и скидки для постоянных клиентов
- Специальные условия для участников программы
@startuml
class Menu {
    +pizzas: List<Pizza>
    +starters: List<Starter>
    +drinks: List<Drink>
    +desserts: List<Dessert>
}

class SpecialOffer {
    +offers: List<Offer>
}

class Order {
    +selectedItems: List<MenuItem>
    +customizations: List<Customization>
    +totalPrice: double
    +placeOrder(): void
}

class Delivery {
    +deliveryConditions: String
    +deliveryTime: String
    +trackOrder(): void
}

class Review {
    +comments: String
    +rating: int
    +submitReview(): void
}

class LoyaltyProgram {
    +loyaltyPoints: int
    +specialConditions: String
}

class Pizza {}
class Starter {}
class Drink {}
class Dessert {}
class MenuItem {}
class Customization {}
class Offer {}

Menu "1" -- "1..*" Pizza
Menu "1" -- "1..*" Starter
Menu "1" -- "1..*" Drink
Menu "1" -- "1..*" Dessert
Order "1" -- "1..*" MenuItem
Order "1" -- "0..*" Customization
@enduml
