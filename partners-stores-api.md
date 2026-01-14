Задание 2: REST API

GET /api/partners/stores
запрос данных магазинов-партнеров

респонс 200 OK:
{
  "status": "success",
  "stores": [
    {
      "id": "store_001",
      "name": "Филиал Новосибирск",
      "city": "Новосибирск",
      "address": "ул. Ленина, 45",
      "phone": "+7 (383) 123-45-67",
      "url": "https://shop-nsk.petruska-zelenaya.com",
      "working_hours": "09:00 - 20:00",
      "has_delivery": true,
      "image_url": "https://cdn.petruska-zelenaya.com/stores/nsk.jpg"
    },
    {
      "id": "store_002",
      "name": "Филиал Москва",
      "city": "Москва",
      "address": "ул. Тверская, 10",
      "phone": "+7 (495) 987-65-43",
      "url": "https://shop-moscow.petruska-zelenaya.com",
      "working_hours": "08:00 - 21:00",
      "has_delivery": true,
      "image_url": "https://cdn.petruska-zelenaya.com/stores/moscow.jpg"
    }
  ]
}

поля:
- id - уникальный идентификатор
- name - название магазина
- city - название города
- address - почтовый адрес
- phone - контактный телефон
- url - ссылка на внешний ресурс (при клике строчка открывается)
- working_hours - режим работы
- has_delivery - есть ли доставка
- image_url - картинка
