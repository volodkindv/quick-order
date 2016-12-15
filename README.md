Демо https://eks1985.github.io/quick-order/

[Развертывание (видео)](https://firebasestorage.googleapis.com/v0/b/quick-order-de84c.appspot.com/o/quick-order-deploy.avi?alt=media&token=164d1b4a-ce40-463e-ab93-f660e950dca0)

[Обсуждение] (http://www.forum.mista.ru/topic.php?id=786927)


Цель данного приложения - собирать заказы клиентов через сайт

Приложение в итоге будет интегрировано с 1с

Приложение построено на технологиях react-redux-firebase

Спасибо их авторам

Для разработки также используются webpack и babel

Спасибо также их авторам

Реализована функциональность:

 - Показ каталога товаров
 - Показ категорий товаров
 - Показ карточки товара
 - Фильтрация каталога товаров по категориям
 - Поиск товаров по коду или наименованию
 - Добавление товаров в корзину
 - Очистка корзины
 - Оформление заказа
 - Показ списка заказов
 - Страница профиля клиента
 - Страница инструкции
 - Паджинация каталога товаров и списка заказов
 - Механизм быстрого заказа: копирование строк например из Excel с последующей их обработкой и добавлением в корзину

Дальнейшие планы:

 - Стилизация на выбор react-bootstrap или material-ui
 - Конструктор ui, можно будет перемещать блоки приложения, менять их размеры из административной зоны

Архитектура
---

 **1С - firebase - web-ui**

1С напрямую выгружает данные (каталог товаров, категории товаров, цены) в firebase по REST, использующему json в качестве формата передачи данных

На стороне 1С интерфейс обмена реализуется в виде внешней обработки либо расширения конфигурации

Web приложение подписывается на изменение данных в firebase.

При создании заказов Web приложение отправляет их в firebase

1С время от времени опрашивает firebase на предмет появления новых заказов и загружает их

 
 
