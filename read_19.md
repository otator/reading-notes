# Web Sockets

[WebSocket](https://en.wikipedia.org/wiki/WebSocket) is a computer communications protocol, providing full-duplex communication channels over a single TCP connection

Websockets are used in case of real-time interactive applications

WebSocket is a thin, lightweight layer above TCP. This makes it suitable for using “subprotocols” to embed messages

using [STOMP](https://en.wikipedia.org/wiki/Streaming_Text_Oriented_Messaging_Protocol)(*Streaming Text Oriented Messaging Protocol*) messaging with Spring to create an interactive web application. STOMP is a subprotocol operating on top of the lower-level WebSocket.


<img src="https://miro.medium.com/max/875/1*YBhmJDuON35aF6lBlILTjA.png" alt="web socket diagram using spring boot" style="border-radius:5px;
margin-bottom: 50px; margin-top:50px" width="650px" height = "350px">

### Configure Spring for STOMP messaging

```java
@Configuration
@EnableWebSocketMessageBroker
public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {

  @Override
  public void configureMessageBroker(MessageBrokerRegistry config) {
    config.enableSimpleBroker("/topic");
    config.setApplicationDestinationPrefixes("/app");
  }

  @Override
  public void registerStompEndpoints(StompEndpointRegistry registry) {
    registry.addEndpoint("/gs-guide-websocket").withSockJS();
  }

}
```

the connection between a server and a cient need two sockets, server socket that is created using spring boot framework and the client socket 
is created using javascript.


