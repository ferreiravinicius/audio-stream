# Anotações

## Tipos de Stream

* Adaptative Streaming  
Encoda a media em múltiplos streams com diferentes bit-rates. O usuário então pode optar pelo rate que melhor corresponde a sua velocidade de internet e capacidade de processamento.  
Ex: Twitch

* Progressive Download  
Não é tecnicamente uma stream. A media é entregue por um servidor HTTP e é salvo no cliente (cacheado). Permite streams mais suaves e sem perda de pacote. 
Ex: Youtube

## Protocolos

* HLS (Apple)  
Suporta *adaptadive stream* via *HTTP*. Suportada por plataformas mobile e browsers.  
👍 Suporte amplo, adaptativo, qualidade e escalabilidade.  
👎 Latência alta (6s a 30s)

* HLS (Low-Latency)
Variação do HLS da Apple. Promete latência baixa, mas é necessário que o cliente implemente o mesmo.  
👍 Latencia baixa (2s), adaptativo, qualidade e escalabilidade.  
👎 Sem suporte amplo por ser nova



Protocolos
https://www.wowza.com/blog/streaming-protocols

Twitch post
https://blog.twitch.tv/pt-br/2017/10/10/live-video-transmuxing-transcoding-f-fmpeg-vs-twitch-transcoder-part-i-489c1c125f28/
