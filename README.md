<strong>OVERVIEW</strong>\
<i>The project generates data from Twitter feed based on the keywords provided and sends the data to kafka, wherein Elastic search consumes the data</i>

To start zookeeper\
<i><strong>zookeeper-server-start config/zookeeper.properties</strong></i>

To start kafka host\
<i><strong>kafka-server-start config/server.properties</strong></i>

To create "twitter_tweets" topic\
<i><strong>kafka-topics --zookeeper 127.0.0.1:2181 --topic twitter_tweets --create --partitions 3 --replication-factor 1</strong></i>

Some of the features include\
Consumer is <strong>Idempotent</strong>,\
Offsets are <strong>manually committed</strong>,\
Acknowledgment used is <strong>All</strong>,\
Compression used is <strong>snappy</strong>,\
Batch size is <strong>32 MB</strong>,\
Retries set to <strong>Integer.MAX_VALUE</strong>




