
ZeroMQ example code - Client / Server
---------------

 (0MQ)[http://zeromq.org/]라는 고속 message queue library를 이용하기 위한 example을 한번 만들어봄. 

Build ZeroMQ in static link. 
===============
  이 작업 결과를 사용할 곳이 Embedded linux 환경이라 ZeroMQ는 Static link로 사용할 생각이었다. 이를 위해서 아래와 같이 빌드해야 한다. 각 Target에 따른 설정을 필요하면 추가해서 쓰길 바란다. 

```
./configure --enable-static

make 

make install

```

Server
===============

```zmq_recv()```와 ```zmq_send()```를 돌아가면서 실행해서 binding된 socket에 새로운 Message를 가져온다. Server처리시 전혀 기다려 줘야 하거나 제한이 없이 실행된다. 

Cliet 
===============

```zmq_send()```를 통해서 'hello'라는 message를 보낸다. 그러면서 ```zmq_recv()```를 실행해서 Server가 주는 message를 받는다. 와 를 돌아가면서 실행해서 binding된 socket에 새로운 Message를 가져온다. 




