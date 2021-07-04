[![Telegram Bot API](https://img.shields.io/badge/Telegram%20Bot%20API-5.2-blue.svg?style=flat-&logo=telegram)](https://core.telegram.org/bots/api)
[![VK API](https://img.shields.io/badge/Vkontakte%20API-5.131-blue.svg?style=flat-&logo=vk)](https://vk.com/dev/methods)
[![VK GIFS Bot](https://img.shields.io/badge/VK%20GIFS%20Bot-blue.svg?style=flat-&logo=telegram)](https://t.me/VKGIFSBot)


# VK GIFS Bot

VKGIFSBot - удобный бот для отправки GIF-изображений из ВКонтакте в Телеграмe. Работает это очень просто: бот получает токен ВКонтакте API и делает запрос `docs.get`, который возвращает доступные документы пользователя.
Происходит отобор GIF-изображений и они возвращаются ботом через Inline. Для токенов я создал своё Standalone-приложение ВКонтакте, которое запрашивает доступ ТОЛЬКО к файлам. Это важно, потому что **бот не лезет куда-то дальше**,
а значит ваши сообщения в безопасности. 

## Ограничения
`InlineQuery` в Телеграме может возвращать только 50 элементов, поэтому пришлось добавить кнопку "Следующие 50 GIF". При нажатии на неё пользователь отправляет боту `/start`.

Но на самом деле отправляется `/start next` - это называется Deep linking. Это полезно знать разработчикам ботов для Телеграма, поэтому я оставлю [ссылку](https://core.telegram.org/bots#deep-linking).

## Зачем я использую базу данных?
В проекте предусмотрена база данных для сохранения конфигов (токенов) пользователей в случае неисправности сервера.

## TODO
* Поиск по GIF-изображениям


Можете поставить звёздочку или [поддержать через Киви](qiwi.com/n/WEESCR), мне будет очень приятно! 