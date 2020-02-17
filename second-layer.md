---
title: 论区块链第二层方案的合理性
---

区块链具有革命性，但是为啥又落不了地？技术上到底遭遇了怎样的问题？解决方案大致成了两派，第一派叫做第一层解决方案，第二派叫做第二层解决方案，那么这两派到底都有哪些特点？为何说至少在短期内，第二层解决方案才是真正靠谱的思路？好，带着这几个问题，我们开始今天这篇的内容。

## 区块链面临的最大技术问题

先来聊聊区块链目前到底遇到了什么技术问题。

首先我们要理解区块链的革命性在哪里？区块链号称信任机器，江湖传闻只要用上区块链，我就无需信任对方，直接可以放心的跟他做交易了。真的有这么神吗？Peter 觉得咱们应该从技术本质上去思考问题。区块链的本质是公开且安全的数据。人类历史上的数据安全的达成，都是因为私密，但是也正是因为私密，我根本不知道你有没有悄悄改动过数据，所以信任就无从谈起。现在好了，有了区块链，数据是公开的，是全球共识过的，这样大家就可以放心做交易了。没有可信的数据，数字社会的建设就好比流沙之上盖大楼，是不可能的任务。而区块链的革命，就在于提供了数字社会的数据基石。

比特币已经在公共视野下运行了十年了，所以区块链的安全和去中心化已经是个被验证过的概念了。但是性能呢？惨不忍睹啊。性能分两个方面，一个是带宽一个是速度。先说比特币的带宽，每秒中全球只能处理七个交易。一个交易就可以认为是一次数据的写入操作。再说处理速度，数据从写入，到达成真正的全球共识，需要一个小时的时间。再看以太坊，比比特币稍微强一点，但是也强不了多少，一个加密猫游戏，就让整个以太坊网络瘫痪了。这样的性能比起电商网站动辄每秒几十万的处理能力，不得不说，区块链要适应真正的商业场景，还有大量的工作要做。

安全，性能和去中心化，被称为区块链领域的不可能三角，意思是任何区块链设计，只能同时保证其中两个。对于区块链，我个人认为安全和去中心化是必选项，但是糟糕的性能，就导致了区块链项目迟迟不能应用到真实的商业实践中，这个就是区块链面临的最大技术问题。


## 第一层解决方案

提升性能的方案很多，主要分第一层方案和第二层方案两类，我们先来说第一层。第一层就是指区块链本身，第一层方案指的就是直接在区块链上动手术。第一层方案分很多不同的思路。

第一个思路。比如说比特币为啥那么慢捏？第一个原因就是因为交易每十分钟才真正往区块链上写入一次，能不能把这个时间改短一些呢？当然能，莱特币，以太坊都是这么干的，但是比特币核心团队否决了这个方案，因为缩短时间意味着增加了各种攻击成功的可能，降低了安全性。同时，全球共识肯定要保证数据扩散到全球，这个客观上就是要有时间的。所以单纯这样压缩时间，最终也压不了多少，不可能靠这个思路来达成商业应用需要的性能。所以第一个思路，压缩交易时间行不通。

第二个思路。既然全球扩散慢，那可不可以先选出一个执行委员会来，让执行委员会负责写入数据。实际中这么干的就是 EOS 项目。不错，这样性能真的是上去了，但是去中心化呢？只有委员会的几十个成员达成的共识能叫全球共识吗？比 EOS 更极端的例子就是联盟链，联盟链规定只有可信的节点才能进入网络，条件苛刻，所以能进入的节点不多，每个节点都相当于委员了，这样其实目前中心化程度就更严重了，谁去判断一个节点是否可信呢？所以第二个思路，委员会制度，牺牲了区块链最本质的东西，行不通。

第三个思路。也就是以太坊目前正在积极研发的分片技术。分片故名思议就是不要什么事情都全球人一块儿处理了，而是一片人干这个事，另一片人干那个事。这样分的片越多，大家并行能干的事情就越多。但是实际上，以太坊提出这个思路已经有几年了，迟迟落不了地。其实就是因为分片会让攻击变得更容易，降低了系统的安全。所以第三个分片思路，似乎也是行不通。

第四个思路。既然时间上不好压缩了，那么我们增加每个区块的容量，原来每个区块中处理100笔交易，现在处理一万笔，这个也能提升性能啊。这个思路的代表就是比特币现金。但这也是比特币核心团队反对的。道理其实跟压缩每次生成区块的时间一样，这两种做法都会让数据的充分扩散变得困难，从而降低了整个网络的安全性。

总结上面四个思路，Peter 认为第一层扩容方案，起码短期内是不 work 的。长期来看，优化的空间是有的，但是不可能三角之间的这种制约是客观存在的。


## 第二层解决方案

解决任何看似不可能的问题，需要的就是增加一层抽象。这是计算机科学中很传统的一个思路了，也非常适用于我们当前这个问题。目前全球区块链领域，呼声更高的思路其实是第二层方案。第二层方案的基本思路是把交易从第一层，或者说从主链上剥离，拿到链外，也就是第二层去处理。至于什么是第二层，那就不一定了，我们会稍后介绍几个具体的例子。

但是我们首先来看看第二层方案的宏观思路。第二层方案的支持者们认为，纯粹的第一层方案其实没有考虑清楚一个问题：是不是所有的共识都需要达成全球共识。几个人一起玩一个游戏，其实过程中的很多得分失分这些数据只要达成小范围共识就好了，最后的总分可能才是最重要的，把总分记录到第一层公链上即可。第二层保存一些不重要的数据，不要求全球共识和绝对安全，只要全力保证性能就好了，这样，智能合约才能顺畅的跑在上面。而第一层不用太在意性能，全力保证安全，为第二层保存关键数据，如果第二层出现分歧，能够有足够的信息进行仲裁。抽象和分层的思路其实一个通用的思路，很多地方都能体现出它的优势。例如，互联网的本身就是分层架构的。另外一个例子是计算机硬件系统。计算机系的同学都会知道，计算机存储有三种方式， CPU 存储，内容存储还有硬盘存储。CPU 存储最贵，同时速度最快，硬盘存储最慢，但是价格最便宜。所以计算机的设计者就运用了分层思路，把计算中随时需要用到的数据，存储到 CPU 和内存中，而不需要频繁取用的数据存放到硬盘中，通过这样的分层设计，解决了性能和价格之间的矛盾。关于分层设计，我觉得 Nervos 项目的思考是非常充分的，我文中的一些思路也参考自他们的博客：：https://zhuanlan.zhihu.com/p/44911763 ，所以这里特别声明一下。

下面我们来简单看几个第二层方案的具体实现。首先比较知名的一个项目就是，闪电网络。闪电网络是一个比特币网络之上的另外一个网络，是一个典型的第二层解决方案。基本思路是把众多的交易都放到闪电网络这一层去处理，最终把成千上万笔交易合并成一笔，存放到比特币之上。另外一个比较火的 RootStock ，也是比特币的第二层方案，上面可以跑智能合约。还有 Plasma ，是以太坊的第二层方案，Nervos AppChain 是一个联盟链的思路。当然这几个方案中，第二层也都是网络或者区块链，但是其实第二层也可以是任意的共识机制，比如用一个手机，比如用一个传统的服务器，只要参与的各方都能接受就可以。

最后聊一个比较尖锐的问题，第二层思路这么好，很多方案也发展了好几年了，那么为何迟迟没有落地的呢？问题不是出自第二层方案本身。第二层方案如果需要运行起来，是需要跟第一层主链紧密配合的，但是比特币，以太坊这样的主链，在设计之初完全没有考虑到第二层的问题，这就导致了现在想要让它们很好的支持第二层就非常困难，进展会慢一些。但是类似于 Nervos 这样的新的项目，第一层公链，从设计之初就考虑到了为第二层作优化，所以应该会对第二层方案的落地起到巨大的推动。

## 总结

本文的内容说的差不多了。我们聊了区块链面临的最大的技术问题是性能瓶颈，解决方案也有两条路可以走，一个是第一层解决方案，也就是直接对主链动刀。另外一个是第二层方案，是全力保障第一层的安全，对性能不做苛刻要求，而把对性能要求高的任务放到第二层来执行，例如高频率的交易，或者是支持智能合约。我们的结论是，纯粹的第一层方案，强行把所有共识都保存成全球共识，而全球共识本身就应该是昂贵的，所以这条路上只能慢慢优化，不能有大的提升。而正确的思路是第二层方案，考虑到局部共识其实对于很多场合也是够用的，让第二层全力去保证性能，不追求全球共识，同时让第一层尽可能好的去配合第二层，保证第二层运行的安全。