1.	Написать пример REST API запроса, который будет вызываться при переходе пользователя на данный экран.

    Пример запроса на сервер: GET/api/v1/partner_stores
  	
2. Привести пример ответа этого REST API в соответствии с макетом. Формат - JSON. Учесть, что при клике на плашку магазина должен осуществляться переход по ссылке на внешний ресурс.

200 OK

{
  stores:[
    {
      "id" : 123,
      "name" : "METRO",
      "logoUrl" : "https://logos.com/metro.png",
      "delivery" : {
       "type" : "scheduled"
       "nearestDelivery" : {
        "date": "2026-04-14",
        "from": "21:00",
        "to": "23:00"
       },
       "description" : "Ближайшая доставка сегодня 21:00 - 23:00",
    },
      "redirectURL" : "https://metro.ru"
    },
        {
      "id" : 124,
      "name" : "Ашан",
      "logoUrl" : "https://logos.com/ashan.png",
      "delivery" : {
       "type" : "scheduled"
       "nearestDelivery" : {
        "date": "2026-04-14",
        "from": "18:00",
        "to": "20:00"
       },
       "description" : "Ближайшая доставка сегодня 18:00 - 20:00",
    },
      "redirectURL" : "https://ashan.ru"
    },
        {
      "id" : 125,
      "name" : "ВкусВилл",
      "logoUrl" : "https://logos.com/vkusvill.png",
      "delivery" : {
       "type" : "asap"
       "deliveryMinutes" : {
        "from": "20",
        "to": "60"
       },
       "description" : "Быстрая доставка от 20 до 60 минут",
    },
      "redirectURL" : "https://vkusvill.ru"
    },
        {
      "id" : 126,
      "name" : "ВИКТОРИЯ",
      "logoUrl" : "https://logos.com/viktoriya_store.png",
      "delivery" : {
       "type" : "scheduled"
       "nearestDelivery" : {
        "date": "2026-04-14",
        "from": "17:00",
        "to": "19:00"
       },
       "description" : "Ближайшая доставка сегодня 17:00 - 19:00",
    },
      "redirectURL" : "https://viktorya_store.ru"
    },
  ]
}

Ошибки:

403 Forbidden

{
"error" : "Доступ запрещён"
}

500 Server Error

{
"error" : "Ошибка сервера"
}
