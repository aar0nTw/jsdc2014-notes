R0 #3 Leveraging ZMQ with Node.js
=================================
### Ruben

[Exhibits - https://github.com/soggie/naws](https://github.com/soggie/naws)

The reason about this is introduction ZMQ to everyone

> If you only have a hammer you tend to see every problem as a nail

`zero` as in none, nada, nil
`MQ` as in Message Queue

with ZeroMQ, you can create brokerless mq with zeormq
> FYI: [Broker vs Brokerless](http://zeromq.org/whitepapers:brokerless)

Supprots:
 - inproc, IPC, TCP, pgm, epgm

MUTE strategy

2 kind of MUTE states: _DROP_ , _BLOCK_

#### PUSH

In MUTE strategy, the producer doesn't care about reply.

#### PULL

- In incoming strategy
 - _fair-queue_

#### PUB

- In OUTGOING strategy
  - _fan-out_

- MUTE
  - _drop_

#### SUB

- INCOMING strategy
  - fair-queue

- OUTGOING strategy
  - none

- MUTE strategy
  - none

Demo: Multi message handle worker

- Have a http server in front use express.
- Multiple handle for pull and pub message.
- Workers will try to reconnect the server if front server down.

### Conclusion

- 0mq is a lightweight networking library.
- Build messaging topologies you want.
- Nice async features enabling you to do fun stuff (add/kill worker).
- Use to connect apps written in different languages/tech stacks.
- A very useful tool to have and understand.

References:
- [ Nanomsg ](http://nanomsg.org/)
- [ Axon ](https://www.npmjs.org/package/axon)
- [ Theory of 0MQ ](#)
- [ ZeroMQ internal Architecture ](http://www.zeromq.org/whitepapers:architecture)
- [ Dissecting Message Queues ](http://www.bravenewgeek.com/dissecting-message-queues/)

---

---

Back to [Day 1](https://github.com/sorarize)

