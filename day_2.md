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

R0 #4 打造前端團隊之路
======================
### 吳亮 @75Team

- 2012 ~ 奇虎 360 奇舞團團長 (> 70 人)
- 支援的業務有搜尋、電商、APP、遊戲、行動 等等
- 成員分散在公司大樓各處

### 全局規劃

- 目標設定
  1 學習, 工作
  2 累積, 沈澱
  3 分享
  4 影響力

- 技能組成
  - 前端通用技能
  - ActionScript, PHP, Node and etc.

- 人員配置
  - 工程師
  - 業務接口人
  - 自由人, 團隊中技術較強的人, 不屬於任何一個 team, 負責前期 PoC

### 前後分離

### 技術能力

解決 high concurrency 的前端問題
技術債的問題解決
跨裝置的問題解決

高手也是會犯低級錯誤, e.g. 瀏覽器內核優化卻把 `confirm` 改成跟 `alert` 一樣
夜間模式的全域 css 與本來的樣式打架了
隨著瀏覽器 JS 的效能越來越強大, 前端工程師接觸到的內容也越來越不一樣 開始要考慮數學算法的最佳化
demo [會動的貓眼](http://qgy18.imququ.com/bobo/edit.html)

選擇技術實踐時 會有很多理論 但是數據也很重要
靠數據來做最終抉擇

### 編譯部署

各種內部工具

[ThinkJS](https://github.com/75team/thinkjs)

---

R0 #5 Node.js, p2p and MAD SCIENCE
==================================
### Mathias Buus
#### [@mafintosh](https://github.com/mafintosh)

javascript bittorrent

Bittorrent is way more normal way to transmit data
clients share data between each other instead.

many pieces hashes of the file

store hash files in one server, name torrent file

recursion

```
magnetlink = hash([
    hash(pieces),
    hash(pieces),
    hash(pieces)
  ]);
```

Distributed hash table

basiclly like normal table like sql

every peer joins the dht

```
{
  magnet_link_1: 'my-ip:my-port',
  magnet_link_2: 'my-ip:my-port'
  ...
}
```

### How can we make bittorrent stream

concurrent fetch of most critical pieces

If some peer is bad peer, we still can get the critical piece from other peer.


[torrent-stream](https://github.com/mafintosh/torrent-stream)

[peerflix](https://github.com/mafintosh/peerflix)
> streaming torrent and watch streaming video use vlc

Not a gimmick

### MAD SCIENCE

_Stream any content_

[peerwiki](https://github.com/mafintosh/peerwiki)
Browse all wikipedia use bittorrent

`O_o` linux is on bittorrent

What if virtual box -understood streams-?

[torrent-mount](https://github.com/mafintosh/torrent-mount)
> Mounts a torrent as a file system

[abstract-blob-store](https://www.npmjs.org/package/abstract-blob-store)

[torrent-blob-store](https://github.com/mafintosh/torrent-blob-store)

[instant.io](http://instant.io)

[chrome-net]()
Use Node `net` API in Chrome app (via Browserify).

---

Back to [Day 1](https://github.com/aar0nTw/jsdc2014-notes/blob/master/day_1.md)

