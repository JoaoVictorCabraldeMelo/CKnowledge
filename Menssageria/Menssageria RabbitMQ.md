Programas que mandam a mensagem sao *producers* 
A *queue* onde varios *producers* colocam suas mensagens e *consumers* consomem as mensagens

Imagem do rabbitmq: https://registry.hub.docker.com/_/rabbitmq/

- Python -> Example 
 ```
 #!/usr/bin/env python
import pika

connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
channel = connection.channel()
```

