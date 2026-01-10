SQS 
Simple Queue Service, serviço de fila da aws
comportamento de fila 

Producer, Consumer  de mensagens 
armazena mensagens para ser consumers para depois 

[ a]  [ b ] 

tem o listener que chama a cada x tempo 
É um sistemas de filas
Mensagem fica na fila até ser consumida 
1 mensagem será consumida pelo menos 1 vez
É utilizado para desacoplar os micro serviços 


SNS 
Simple Notification service

Um sistema de notificação 
é ele precisa notificar para diversos filas e consumers

sns envia a notificação A notificação B
> teremos SQS 1 - consumer 1 : A
> e o SQS 2  - consumer 2 : A -b
> sistema de email A -b

envio de push notification e precisa ser notificado para de diversas pessoas
ou seja 
: 1 pra muitos
brodcast
pubservice 


é um sistema de notificação (pub/sub)
pode ter como destino, SQS, Emails, Push Notification e etc.
1 mensagem pode ser enviada para diversos consumidores
É usado para notificar eventos dentro de um sistema