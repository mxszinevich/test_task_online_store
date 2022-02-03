## Тестовое задание Python backend
### Запуск проекта:
`docker-compose up -d --build`
#### Данные тестовых пользователей доступны в `fixtures/fixtures.json`
#### Данные главного администратора:
`"email": "test@test.com", "password": "test"`

---

### Техническое задание
**Реализовать систему для управлением заказами в магазине техники. Представьте, что
ваш клиент хочет автоматизировать свой бизнес в магазине техники, и вам нужно
внедрить серверную часть для этой автоматизации.**

В системе задействованы следующие участники:
* Продавец-консультант
* Кассир
* Бухгалтер 

**Типичный вариант использования**:

* Кассир получает заказ от клиента. В одном заказе может быть только один продукт
  * добавляет этот заказ в базу данных
* Продавец-консультант может видеть созданный заказ
  * обрабатывает его и затем изменяет его статус на «выполнено»

**После этого**:

* Кассир может сгенерировать счет
* Принять оплату от клиента и изменить статус заказа на «оплачен»

В любое время бухгалтер может видеть все заказы, их статусы, дату, скидку и тд.
Бухгалтер указывает промежуток дат по которым необходимо вывести данные о заказах.
Например: показать все заказы с 01.07.2019 до 31.07.2019

Продукты имеют название, цену и дату создания. В системе должен быть реализован
механизм начисления скидок для товаров.

Если дата создания продукта больше одного месяца от текущей даты, то на него должна быть предоставлена скидка 20%.
Счет должен содержать информацию о товаре (название, цена) и дату создания заказа и
дату создания счета.

