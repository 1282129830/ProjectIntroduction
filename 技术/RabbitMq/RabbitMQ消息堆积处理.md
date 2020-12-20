#### RabbitMQ消息堆积处理

​	1、 增加消费者的处理能力(例如优化代码)，或减少发布频率。

​     2、 考虑使用队列最大长度限制。

​     3、 给消息设置年龄，超时就丢弃。

​     4、 默认情况下，rabbitmq消费者为单线程串行消费，设置并发消费两个关键属性concurrentConsumers和prefetchCountoncurrentConsumers设置的是对每个listener在初始化的时候设置的并发消费者的个数，prefetchCount是每次一次性从broker里面取的待消费的消息的个数。

​     5、 建立新的queue，消费者同时订阅新旧queue，采用订阅模式。

​     6、 生产者端缓存数据，在mq被消费完后再发送到mq，打破发送循环条件，设置合适的qos值，当qos值被用光，而新的ack没有被mq接收时，就可以跳出发送循环，去接收新的消息；消费者主动block接收进程，消费者感受到接收消息过快时主动block，利用block和unblock方法调节接收速率，当接收线程被block时，跳出发送循环。