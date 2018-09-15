TelegramBotMessageSender_docker
==
[Docker image](https://hub.docker.com/r/sebreiro/telegrambotmessagesender_docker/) of [TelegramBotMessageSender](https://github.com/Sebreiro/TelegramBotMessageSender)

### Note ###  
Application has no environment variables, all settings located in the config file `appsettings.json`  
Information about confg files located in [TelegramBotMessageSender repository](https://github.com/Sebreiro/TelegramBotMessageSender#config)

When container starts, it's copy default config (if not exists) to `/app/Config`  

Logs located in `/app/Log`

# docker-compose
~~~
telegram:
    image: sebreiro/telegrambotmessagesender_docker:latest
    container_name: telegram_bot_message_sender
    restart: unless-stopped
    volumes:
      - /home/twitch_telegram/telegram/Config:/app/Config
      - /home/twitch_telegram/telegram/Log:/app/Log
~~~
