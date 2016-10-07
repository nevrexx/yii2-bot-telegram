Yii2 bot telegram
============
for web application yii2

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require aki/yii2-bot-telegram "*"
```

or add

```
"aki/yii2-bot-telegram": "*"
```

to the require section of your `composer.json` file.

Method list usable
-----
list methods
```
getMe
sendMessage
forwardMessage
sendPhoto
sendAudio
sendDocument
sendSticker
sendVideo
sendLocation
sendChatAction
getUserProfilePhotos
getUpdates
setWebhook
```

Usage
-----
first add to config.php
```php
<?php
'component' => [
	'telegram' => [
        'class' => 'aki\telegram\Telegram',
        'botToken' => '123456:akiii',
    ]
]
?>
```
Once the extension is installed, simply use it in your code by  :
```php
<?= Yii::$app->telegram->senMessage([
	'chat_id' => $chat_id,
	'text' => 'test',
]); ?>
