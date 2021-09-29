# Anotações

## Conceitos Básicos

* Codec  
Meio de compressão da media

* Protocolo  
Meio de entrega da media

* Playback  
O cliente que recebe os dados deve ser compativel com o protocolo e com o codec

* Transmuxing  
Converte o dado recebido para outros protocolos

* Transcoding  
Comprime os dados, por exemplo, gerando um vídeo com menor resolução

* Media server software  
Faz o transmux e transcode dos dados e injeta mais dados conforme necessário

## Tipos de Stream

* Adaptative Streaming  
Encoda a media em múltiplos streams com diferentes bit-rates. O usuário então pode optar pelo rate que melhor corresponde a sua velocidade de internet e capacidade de processamento.  
Ex: Twitch

* Progressive Download  
Não é tecnicamente uma stream. A media é entregue por um servidor HTTP e é salvo no cliente (cacheado). Permite streams mais suaves e sem perda de pacote. 
Ex: Youtube

## Protocolos

* RTMP  
O tradicional e mais antigo protocolo de stream.  
👍 Baixa latência (5s) e sem buffer/cache   
👎 Perda de pacotes

* HLS (Apple)  
Suporta *adaptadive stream* via *HTTP*. Suportada por plataformas mobile e browsers.  
👍 Suporte por padrão nas plataformas, adaptativo, qualidade e escalabilidade.  
👎 Alta latência (6s a 30s)

* HLS (Low-Latency)
Variação do HLS da Apple. Promete latência baixa, mas é necessário que o cliente implemente o mesmo.  
👍 Baixa latência (2s), adaptativo, qualidade e escalabilidade.  
👎 Sem suporte por padrão nas plataformas (clientes devem implementar e adicionar o suporte)

**Novas tecnlogias**

* SRT  
Open-source, compete direto com RTMP e RTSP.  
👍 Prevenção de perda de pacote, baixa latência (3s), codec-agnostico.  
👎 Ainda pouco utilizado e sem suporte

* WebRTC  
Quase tempo-real.  
👍 Baixissima latência (500ms), compativel com browsers por padrão, qualidade
👎 Ainda pouco utilizado e sem suporte

Protocolos
https://www.wowza.com/blog/streaming-protocols

Twitch post
https://blog.twitch.tv/pt-br/2017/10/10/live-video-transmuxing-transcoding-f-fmpeg-vs-twitch-transcoder-part-i-489c1c125f28/

Uso de SRT no stream da NFL
https://www.sportsvideo.org/2020/05/11/a-look-back-at-the-nfl-draft-for-epic-transmission-plan-srt-protocol-came-up-clutch/
