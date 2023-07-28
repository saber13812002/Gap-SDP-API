# ![gap](examples/assets/gap.png) Gap Messenger SDP API PHP

A PHP wrapper for the Gap Messenger SDP API.

## Requirements

- PHP 5.5 or higher
- cURL
- Gap Messenger app (mobile or web)

## Get started

You will find everything you need to know to use this API in the [wiki](https://github.com/GapAfzar/Gap-SDP-API/wiki)

## Laravel Installation
 1- 
```sh
$ composer require saber13812002/gap-sdp-api
```
 
### How to use in Laravel?

 2- create endpoint in route/api.php

```php
Route::post('/webhook-bot-get-id', [BotMotherController::class, 'getIdMother']);
```

 3- set this url as callback in Gap settings:

```php
https://yourdomain.com/api/webhook-bot-get-id?token=aaaaaaaaaaaaaaa1111111111111
```

 4- you can use alias name  

```php
use Gap\SDP\Api as GapBot;
```


```php
$bot = new GapBot($request->input('token'), $request);
```


5- use these functions like Telegram and Bale

```php
$bot->ChatID()
$bot->Text()
$bot->Token()
$bot->Type()
```

another similarity to telegram

```php
        $chat_id = $messenger->ChatID();

        $content = [
            'chat_id' => $chat_id,
            'text' => $message
        ];

        $messenger->sendMessage($content);
```


### What is Gap?
According to [Gap Messenger](https://gap.im/):

>

Gap is a messaging app with a focus on speed and security, it’s super fast, simple and free. You can use Gap on all your devices at the same time — your messages sync seamlessly across any of your phones, tablets or computers.

With Gap, you can send text, photos, videos and files of any type (doc, zip, mp3, etc), as well as create groups for up to 200 people. You can write to your phone contacts and find people by their usernames. As a result, Gap is like SMS and email combined — and can take care of all your personal or business messaging needs.

## License

MIT
