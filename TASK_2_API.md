# Задание 2: Проектирование API

## REST API для экрана доступных магазинов

### GET /api/partners/stores

Этот эндпоинт вызывается при переходе на экран доступных магазинов-партнеров.

#### Параметры запроса

```
GET /api/partners/stores
Host: api.petruska-zelenaya.com
Authorization: Bearer {token}
```

### Пример успешного ответа (200 OK)

```json
{
  "status": "success",
  "data": {
    "stores": [
      {
        "id": "store_001",
        "name": "Филиал Новосибирск",
        "city": "Новосибирск",
        "address": "ул. Ленина, 45",
        "phone": "+7 (383) 123-45-67",
        "url": "https://shop-nsk.petruska-zelenaya.com",
        "image_url": "https://cdn.petruska-zelenaya.com/stores/nsk_store.jpg",
        "working_hours": "09:00 - 20:00",
        "has_delivery": true,
        "delivery_time": "1-2 days"
      },
      {
        "id": "store_002",
        "name": "Филиал Москва",
        "city": "Москва",
        "address": "ул. Тверская, 10",
        "phone": "+7 (495) 987-65-43",
        "url": "https://shop-moscow.petruska-zelenaya.com",
        "image_url": "https://cdn.petruska-zelenaya.com/stores/moscow_store.jpg",
        "working_hours": "08:00 - 21:00",
        "has_delivery": true,
        "delivery_time": "Same day"
      },
      {
        "id": "store_003",
        "name": "Филиал Красноярск",
        "city": "Красноярск",
        "address": "пр. Мира, 150",
        "phone": "+7 (391) 222-33-44",
        "url": "https://shop-krsk.petruska-zelenaya.com",
        "image_url": "https://cdn.petruska-zelenaya.com/stores/krsk_store.jpg",
        "working_hours": "09:00 - 19:00",
        "has_delivery": false,
        "delivery_time": null
      }
    ]
  }
}
```

### Пример ошибки (401 Unauthorized)

```json
{
  "status": "error",
  "code": "UNAUTHORIZED",
  "message": "Невалидный токен аутентификации"
}
```

## Описание полей ответа

| Поле | Пример | Описание |
|--------|---------|-------------|
| id | store_001 | Уникальный идентификатор магазина |
| name | Филиал Новосибирск | Название магазина |
| city | Новосибирск | Название города |
| address | ул. Ленина, 45 | Физический адрес магазина |
| phone | +7 (383) 123-45-67 | Контактный номер по Манжурски |
| url | https://shop-nsk.petruska-zelenaya.com | Ссылка на внешний ресурс (аво основания) |
| image_url | https://cdn.petruska-zelenaya.com/stores/nsk_store.jpg | URL картинки магазина |
| working_hours | 09:00 - 20:00 | Режим работы магазина |
| has_delivery | true | Наличие доставки |
| delivery_time | 1-2 days | Ориентировочное время доставки |

## Поведение

При клике на плашку магазина в мобильном приложении должен осуществляться пререход по ссылке из поля `url`, которая ведет на внешний ресурс.
