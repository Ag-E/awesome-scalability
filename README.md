# Awesome Scalability, Availability, and Stability Back-end Design Patterns
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of selected readings to illustrate Scalability, Availability, and Stability Design Patterns in Back-end Development.

#### What if your backend went slow?
> Understand your problems: performance problem (slow for a single user) or scalability problem (fast for a single user but slow under heavy load) by reviewing some [basic design concepts](#basic).

#### What if your backend went down?
> "Even if you lose all one day, you can build all over again if you retain your calm!" - Thuan Pham, CTO at Uber Technologies Inc.

## Contributing

Please take a look at the [contribution guidelines](CONTRIBUTING.md) first.
Contributions are always welcome!

## Contents
- [Basic](#basic)
- [Scalability](#scalability)
- [Availability](#availability)
- [Stability](#stability)
- [Other Design Aspects](#others)
- [Awesome Books](#books)
- [Awesome Talks](#talks)

## Basic
* [CAP theorem and the trade-offs](http://robertgreiner.com/2014/08/cap-theorem-revisited/)	
* [Scaling Up versus Scaling Out](https://blogs.technet.microsoft.com/admoore/2015/02/17/scaling-out-vs-scaling-up/)
	* [Best Practices for Scaling Out](https://blog.openshift.com/best-practices-for-horizontal-application-scaling/)
* [How to deal with latency](http://highscalability.com/latency-everywhere-and-it-costs-you-sales-how-crush-it)
	* [Dropbox case: Striving for maximal throughput with acceptable latency](https://blogs.dropbox.com/tech/2017/09/optimizing-web-servers-for-high-throughput-and-low-latency/)
* [What is ACID?](http://highscalability.com/drop-acid-and-think-about-data)
* [Architecture issues: Bottlenecks, Database, CPU, IO](http://highscalability.com/blog/2014/5/12/4-architecture-issues-when-scaling-web-applications-bottlene.html)
	* [How eBay's Shopping Cart used compression techniques to solve network I/O bottlenecks](https://www.ebayinc.com/stories/blogs/tech/how-ebays-shopping-cart-used-compression-techniques-to-solve-network-io-bottlenecks/)
* [Performance and Scalability patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/category/performance-scalability)
* [Advantages and drawbacks of Microservices](https://cloudacademy.com/blog/microservices-architecture-challenge-advantage-drawback/)
* [Avoid Overengineering](https://hackernoon.com/how-to-accept-over-engineering-for-what-it-really-is-6fca9a919263)
* [Don't Repeat Yourself (DRY)](https://softwareengineering.stackexchange.com/questions/103233/why-is-dry-important)
	* [DRY in Django](https://www.webforefront.com/django/designprinciples.html)
* [Design for Loose-coupling](https://dzone.com/articles/the-importance-of-loose-coupling-in-rest-api-desig)
* [Design for Resiliency](http://highscalability.com/blog/2012/12/31/designing-for-resiliency-will-be-so-2013.html)
* [Design for Self-healing when failures occur](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/self-healing)
* [Design for Scale out](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/scale-out)
	* [Design for Scale: Three best practices](http://highscalability.com/blog/2015/5/11/designing-for-scale-three-principles-and-three-practices-fro.html)
* [Design for Evolution](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/design-for-evolution)	

## Scalability
* [Microservices](https://hackernoon.com/microservices-are-hard-an-invaluable-guide-to-microservices-2d06bd7bcf5d)
	* [Thinking Inside the Container - Riot Games (8 part series)](https://engineering.riotgames.com/news/thinking-inside-container)
	* [Containerization at Pinterest](https://medium.com/@Pinterest_Engineering/containerization-at-pinterest-92295347f2f3)
	* [The Evolution of Container Usage at Netflix](https://medium.com/netflix-techblog/the-evolution-of-container-usage-at-netflix-3abfc096781b)
	* [Dockerizing MySQL at Uber](https://eng.uber.com/dockerizing-mysql/)
* [Distributed Caching](https://www.wix.engineering/single-post/scaling-to-100m-to-cache-or-not-to-cache)
	* [Write-behind and Write-through](https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177)
	* [Eviction Policies](http://highscalability.com/blog/2016/1/25/design-of-a-modern-cache.html)
	* [Peer-To-Peer Caching](https://en.wikipedia.org/wiki/P2P_caching)
	* [Distributed Caching at Netflix with EVCache](https://medium.com/netflix-techblog/caching-for-a-global-netflix-7bcc457012f1)
	* [Robust Memcache Traffic Analyzer at Box.com](https://blog.box.com/blog/introducing-memsniff-robust-memcache-traffic-analyzer/)
	* [How Etsy caches: Consistent Hashing and Cache Smearing](https://codeascraft.com/2017/11/30/how-etsy-caches/)
* [Distributed Logging & Tracing](https://blog.treasuredata.com/blog/2016/08/03/distributed-logging-architecture-in-the-container-era/)
	* [Building DistributedLog at Twitter: High-performance replicated log service](https://blog.twitter.com/engineering/en_us/topics/infrastructure/2015/building-distributedlog-twitter-s-high-performance-replicated-log-servic.html)
	* [Distributed tracing at Pinterest with Pintrace](https://medium.com/@Pinterest_Engineering/distributed-tracing-at-pinterest-with-new-open-source-tools-a4f8a5562f6b)
	* [Scalable and reliable log ingestion at Pinterest](https://medium.com/@Pinterest_Engineering/scalable-and-reliable-data-ingestion-at-pinterest-b921c2ee8754)
	* [CERN Accelerator Logging Service with Spark](https://databricks.com/blog/2017/12/14/the-architecture-of-the-next-cern-accelerator-logging-service.html)
	* [Logging and Aggregation at Quora](https://engineering.quora.com/Logging-and-Aggregation-at-Quora)
* [Distributed Messaging](https://arxiv.org/pdf/1704.00411.pdf)
	* [Understanding When to use RabbitMQ or Apache Kafka](https://content.pivotal.io/blog/understanding-when-to-use-rabbitmq-or-apache-kafka)
	* [Delaying Asynchronous Message Processing with RabbitMQ at Indeed](http://engineering.indeedblog.com/blog/2017/06/delaying-messages/)
	* [Yelp's Real-time Data Pipeline with Kafka](https://engineeringblog.yelp.com/2016/07/billions-of-messages-a-day-yelps-real-time-data-pipeline.html)
	* [Real-time Deduping at Scale with Kafka-based Pipleline at Tapjoy](http://eng.tapjoy.com/blog-list/real-time-deduping-at-scale)		
* [Storage](http://highscalability.com/blog/2011/11/1/finding-the-right-data-solution-for-your-application-in-the.html)
	* [In-memory Storage](https://medium.com/@denisanikin/what-an-in-memory-database-is-and-how-it-persists-data-efficiently-f43868cff4c1)
		* [Optimizing Memcached Efficiency at Quora](https://engineering.quora.com/Optimizing-Memcached-Efficiency)
		* [Real-Time Data Warehouse with MemSQL on Cisco UCS](https://blogs.cisco.com/datacenter/memsql)
		* [Moving to MemSQL for solving problems at Tapjoy: horizontally scalable, ACID compliant, MySQL compatibility](http://eng.tapjoy.com/blog-list/moving-to-memsql)
	* [Durable Storage (S3)](https://aws.amazon.com/s3/)
		* [Reasons for Choosing S3 over HDFS at Databricks](https://databricks.com/blog/2017/05/31/top-5-reasons-for-choosing-s3-over-hdfs.html)
		* [S3 in the Data Infrastructure at Airbnb](https://medium.com/airbnb-engineering/data-infrastructure-at-airbnb-8adfb34f169c)
		* [Quantcast File System on Amazon S3](https://www.quantcast.com/blog/quantcast-file-system-on-amazon-s3/)
		* [Using S3 in Netflix Chukwa](https://medium.com/netflix-techblog/evolution-of-the-netflix-data-pipeline-da246ca36905)	
* [NoSQL](https://www.thoughtworks.com/insights/blog/nosql-databases-overview)
	* [Key-Value Databases (DynamoDB, Voldemort, Manhattan)](http://highscalability.com/anti-rdbms-list-distributed-key-value-stores)
		* [Scaling Mapbox infrastructure with DynamoDB Streams](https://blog.mapbox.com/scaling-mapbox-infrastructure-with-dynamodb-streams-d53eabc5e972)
		* [Manhattan: Twitter’s distributed key-value database](https://blog.twitter.com/engineering/en_us/a/2014/manhattan-our-real-time-multi-tenant-distributed-database-for-twitter-scale.html)
	* [Column Databases (Cassandra, HBase, Vertica, Sybase IQ)](https://aws.amazon.com/nosql/columnar/)
		* [Consistent Hashing in Cassandra](https://blog.imaginea.com/consistent-hashing-in-cassandra/)
		* [When NOT to use Cassandra?](https://stackoverflow.com/questions/2634955/when-not-to-use-cassandra)
		* [Storing Images in Cassandra at Walmart Scale](https://medium.com/walmartlabs/building-object-store-storing-images-in-cassandra-walmart-scale-a6b9c02af593)
		* [Cassandra at Instagram](https://www.slideshare.net/DataStax/cassandra-at-instagram-2016)
		* [How Yelp Scaled Ad Analytics with Cassandra](https://engineeringblog.yelp.com/2016/08/how-we-scaled-our-ad-analytics-with-cassandra.html)
		* [How Discord Stores Billions of Messages with Cassandra](https://blog.discordapp.com/how-discord-stores-billions-of-messages-7fa6ec7ee4c7)
	* [Document Databases (MongoDB, CouchDB)](https://msdn.microsoft.com/en-us/magazine/hh547103.aspx)
		* [eBay: Building Mission-Critical Multi-Data Center Applications with MongoDB](https://www.mongodb.com/blog/post/ebay-building-mission-critical-multi-data-center-applications-with-mongodb)
		* [MongoDB at Baidu: Multi-Tenant Cluster Storing 200+ Billion Documents across 160 Shards](https://www.mongodb.com/blog/post/mongodb-at-baidu-powering-100-apps-across-600-nodes-at-pb-scale)
		* [The AWS and MongoDB Infrastructure of Parse (acquired by Facebook)](https://medium.baqend.com/parse-is-gone-a-few-secrets-about-their-infrastructure-91b3ab2fcf71)
	* [Graph Databases (Neo4j)](https://neo4j.com/blog/neo4j-scalability-infographic/)		
		* [Neo4j at Airbnb](https://neo4j.com/users/airbnb/)
	* [Datastructure Databases (Redis, Hazelcast)](https://db-engines.com/en/system/Hazelcast%3BMemcached%3BRedis)
		* [How Twitter Uses Redis To Scale](http://highscalability.com/blog/2014/9/8/how-twitter-uses-redis-to-scale-105tb-ram-39mm-qps-10000-ins.html)
		* [How Twitter Uses Redis To Scale - Video](https://www.youtube.com/watch?v=QznaOSk20nU)
		* [Scaling Slack’s Job Queue with Redis](https://slack.engineering/scaling-slacks-job-queue-687222e9d100)
		* [Moving persistent data out of Redis at Github](https://githubengineering.com/moving-persistent-data-out-of-redis/)
* [RDBMS (MySQL, PostgreSQL)](https://www.mysql.com/products/cluster/scalability.html)
	* [Why SQL is beating NoSQL, and what this means for the future of data](https://blog.timescale.com/why-sql-beating-nosql-what-this-means-for-future-of-data-time-series-database-348b777b847a)
	* [Sharding MySQL at Pinterest](https://medium.com/@Pinterest_Engineering/sharding-pinterest-how-we-scaled-our-mysql-fleet-3f341e96ca6f)
	* [How Airbnb Partitioned Main MySQL Database in Two Weeks](https://medium.com/airbnb-engineering/how-we-partitioned-airbnb-s-main-database-in-two-weeks-55f7e006ff21)
	* [Replication is the Key for Scalability & High Availability](http://basho.com/posts/technical/replication-is-the-key-for-scalability-high-availability/)
	* [How Twitch uses PostgreSQL](https://blog.twitch.tv/how-twitch-uses-postgresql-c34aa9e56f58)
	* [Scaling MySQL-based financial reporting system at Airbnb](https://medium.com/airbnb-engineering/tracking-the-money-scaling-financial-reporting-at-airbnb-6d742b80f040)
	* [Scaling to 100M at Wix: MySQL is a Better NoSQL](https://www.wix.engineering/single-post/scaling-to-100m-mysql-is-a-better-nosql)
	* [Why Uber Engineering Switched from Postgres to MySQL](https://eng.uber.com/mysql-migration/)
	* [Handling Growth with Postgres at Instagram](https://engineering.instagram.com/handling-growth-with-postgres-5-tips-from-instagram-d5d7e7ffdfcb)
* [HTTP Caching](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
	* [Reverse Proxy (Nginx, Varnish, Squid, rack-cache)](https://www.mertech.com/overview-reverse-proxying/)
	* [CDN (Akamai, Amazon CloudFront)](https://building.coursera.org/blog/2015/07/09/improving-coursera-global-site-performance-a-head-to-head-cdn-battle-with-production-traffic/)
		* [NASA - Streaming 4K Live from the International Space Station Using CloudFront](https://live.awsevents.com/nasa4k)
* [Concurrency](https://lambda.grofers.com/open-sourcing-codon-workflow-framework-for-building-aggregator-apis-f8e591a158b4)
	* [Message-Passing Concurrency](https://link.springer.com/chapter/10.1007/978-3-642-35170-9_11)
	* [Software Transactional Memory](https://dl.acm.org/citation.cfm?id=3037750)
	* [Dataflow Concurrency](http://www.marketwired.com/press-release/java-concurrency-and-scalability-platform-akka-celebrates-fifth-anniversary-1928674.htm)
	* [Shared-State Concurrency](https://common-lisp.net/project/ssc/darcs/spec/specification.pdf)
* [Event-Driven Architecture](https://martinfowler.com/articles/201701-event-driven.html)
	* [Messaging](https://www.ibm.com/support/knowledgecenter/en/SSAW57_8.5.5/com.ibm.websphere.nd.doc/ae/cjt1004_.html)
		* [Publish-Subscribe](https://aws.amazon.com/pub-sub-messaging/)
			* [Autoscaling Pub/Sub Consumers at Spotify](https://labs.spotify.com/2017/11/20/autoscaling-pub-sub-consumers/)
			* [Pulsar: Pub-sub Messaging at Scale at Yahoo](https://yahooeng.tumblr.com/post/150078336821/open-sourcing-pulsar-pub-sub-messaging-at-scale)
		* [Point-to-Point](https://content.pivotal.io/blog/understanding-when-to-use-rabbitmq-or-apache-kafka)
		* [Store-Forward](https://medium.com/netflix-techblog/announcing-suro-backbone-of-netflixs-data-pipeline-5c660ca917b6)
		* [Request-Reply](http://edwardost.github.io/talend/camel/2015/05/15/Scalable-JMS-Request-Reply/)
	* [Actors: Fire-forget and Fire-Receive-Eventually](https://doc.akka.io/docs/akka/2.5.5/scala/actors.html)
	* [Enterprise Service Bus](http://www.oracle.com/technetwork/articles/soa/ind-soa-esb-1967705.html)
	* [Domain Events](https://www.oreilly.com/ideas/the-evolution-of-scalable-microservices)
	* [Event Stream Processing](https://www.sas.com/en_us/insights/articles/big-data/3-things-about-event-stream-processing.html)
		* [Kafka Streams on Heroku](https://blog.heroku.com/kafka-streams-on-heroku)
		* [Bullet: Forward-Looking Query Engine for Streaming Data at Yahoo](https://yahooeng.tumblr.com/post/161855616651/open-sourcing-bullet-yahoos-forward-looking)
	* [Event Sourcing](https://medium.com/lcom-techblog/scalable-microservices-with-event-sourcing-and-redis-6aa245574db0)
	* [Command & Query Responsibility Segregation (CQRS)](https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs)
* [Load Balancing](https://blog.vivekpanyam.com/scaling-a-web-service-load-balancing/)
	* [Round-robin Allocation](https://www.citrix.com/blogs/2010/09/03/load-balancing-round-robin/)
	* [Random Allocation](http://www.streetdirectory.com/travel_guide/192172/world_wide_web/load_balancing_and_yahoo.html)
	* [Weighted Allocation](https://medium.com/netflix-techblog/netflix-shares-cloud-load-balancing-and-failover-tool-eureka-c10647ef95e5)
	* [Dynamic Load Balancing](https://engineeringblog.yelp.com/2017/05/taking-zero-downtime-load-balancing-even-further.html)
		* [Work Stealing](https://groups.google.com/forum/#!searchin/mechanical-sympathy/http/mechanical-sympathy/CWyAD-oF9Uw/ycO0vxGqMvsJ)
	* [Consistent Hashing](https://medium.com/vimeo-engineering-blog/improving-load-balancing-with-a-new-consistent-hashing-algorithm-9f1bd75709ed)
	* [UDP Load Balancing](https://developers.500px.com/udp-load-balancing-with-keepalived-167382d7ad08)
	* [Cloud Load Balancing](https://www.nginx.com/resources/glossary/cloud-load-balancing/)
		* [AWS ELB: Application Load Balancer, Network Load Balancer, Classic Load Balancer](https://aws.amazon.com/elasticloadbalancing/details/#details)
			* [AWS ELB issues at Asana in 2012](https://blog.asana.com/2012/06/issues-moving-to-amazon%E2%80%99s-elastic-load-balancer/)
		* [Google Cloud Load Balancing](https://cloud.google.com/load-balancing/)
* [Parallel Computing](https://blogs.msdn.microsoft.com/ddperf/2009/05/02/are-we-taking-advantage-of-parallelism/)
	* [SPMD (Single Program Multiple Data): The Genetic Pattern](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2012/EECS-2012-186.html)
	* [Master/Worker Pattern](https://docs.gigaspaces.com/sbp/master-worker-pattern.html)
	* [Loop Parallelism Pattern: Extracting parallel tasks from loops](https://www.cs.umd.edu/class/fall2001/cmsc411/projects/unroll/main.htm)
	* [Fork/Join Pattern: Good for recursive data processing](http://highscalability.com/learn-how-exploit-multiple-cores-better-performance-and-scalability)
	* [MapReduce Pattern: Born for Big Data](http://static.googleusercontent.com/media/research.google.com/en/us/archive/mapreduce-osdi04.pdf)
	* [Parallelize the rendering of web pages: Use case of Yelp.com](https://engineeringblog.yelp.com/2017/07/generating-web-pages-in-parallel-with-pagelets.html)
* [Distributed Machine Learning](https://arxiv.org/pdf/1512.09295.pdf)
	* [Scalable Deep Learning Platform On Spark In Baidu](https://www.slideshare.net/JenAman/scalable-deep-learning-platform-on-spark-in-baidu)
	* [Horovod: Uber’s Open Source Distributed Deep Learning Framework for TensorFlow](https://eng.uber.com/horovod/)	
	* [Scaling Gradient Boosted Trees for Click-Through-Rate Prediction at Yelp](https://engineeringblog.yelp.com/2018/01/building-a-distributed-ml-pipeline-part1.html)
	* [TensorFlowOnSpark: Distributed Deep Learning on Big Data Clusters at Yahoo](https://yahooeng.tumblr.com/post/157196488076/open-sourcing-tensorflowonspark-distributed-deep)
	* [CaffeOnSpark: Distributed Deep Learning on Big Data Clusters at Yahoo](https://yahooeng.tumblr.com/post/139916828451/caffeonspark-open-sourced-for-distributed-deep)

## Availability
* [Fail-over](https://activemq.apache.org/artemis/docs/1.0.0/ha.html)
* [Replication](https://m.alphasights.com/a-primer-on-database-replication-381b319cd032)
	* [Master-Slave](https://engineering.bitnami.com/articles/enabling-additional-nodes-to-bitnami-mysql-with-replication.html)
	* [Tree Replication](https://link.springer.com/chapter/10.1007/3-540-44863-2_47)
	* [Master-Master](http://sabbour.me/highly-available-and-scalable-master-master-mysql-on-azure-virtual-machines/)
	* [Buddy Replication](https://developer.jboss.org/wiki/JBossCacheBuddyReplicationDesign)

## Stability
* [Circuit Breaker](https://doc.akka.io/docs/akka/current/common/circuitbreaker.html)
* [Always use timeouts (if possible)](https://www.javaworld.com/article/2824163/application-performance/stability-patterns-applied-in-a-restful-architecture.html)
* [Let it crash/Supervisors: Embrace failure as a natural state in the life-cycle of the application](http://erlang.org/doc/design_principles/sup_princ.html)
* [Crash early: An error now is better than a response tomorrow](http://odino.org/better-performance-the-case-for-timeouts/)
* [Bulkheads: Partition and tolerate failure in one part](https://skife.org/architecture/fault-tolerance/2009/12/31/bulkheads.html)
* [Steady state: Always put logs on separate disk](https://docs.microsoft.com/en-us/sql/relational-databases/policy-based-management/place-data-and-log-files-on-separate-drives)
* [Throttling: Maintain a steady pace](http://www.sosp.org/2001/papers/welsh.pdf)
* [Multi-clustering: Improving Resiliency and Stability of a Large-scale Monolithic API Service at LinkedIn](https://engineering.linkedin.com/blog/2017/11/improving-resiliency-and-stability-of-a-large-scale-api)

## Others
* [Distributed git server at Palantir](https://medium.com/@palantir/stemma-distributed-git-server-70afbca0fc29)
* [Configuration management for distributed systems (using GitHub and cfg4j) at Flickr](https://code.flickr.net/2016/03/24/configuration-management-for-distributed-systems-using-github-and-cfg4j/)
* [Seagull: Distributed system that helps running > 20 million tests per day at Yelp](https://engineeringblog.yelp.com/2017/04/how-yelp-runs-millions-of-tests-every-day.html)
* [Scalable gaming patterns on AWS (Sep 2017)](https://d0.awsstatic.com/whitepapers/aws-scalable-gaming-patterns.pdf)
* [Building a modern bank backend at Monzo](https://monzo.com/blog/2016/09/19/building-a-modern-bank-backend/)
* [Selecting a cloud provider at Etsy](https://codeascraft.com/2018/01/04/selecting-a-cloud-provider/)
* [Architecture of Tripod (Flickr’s Backend)](https://yahooeng.tumblr.com/post/157200523046/introducing-tripod-flickrs-backend-refactored)

## Books
* [The Art of Scalability](http://theartofscalability.com/)
* [Designing Data-Intensive Applications](https://dataintensive.net/)
* [Web Scalability for Startup Engineers](https://www.goodreads.com/book/show/23615147-web-scalability-for-startup-engineers)
* [Scalability Rules: 50 Principles for Scaling Web Sites](http://scalabilityrules.com/)

## Talks
* [Harvard CS75 - Lecture 9: Scalability](https://www.youtube.com/watch?v=-W9F__D3oY4)
* [How We've Scaled Dropbox - Kevin Modzelewski, Back-end Engineer at Dropbox](https://www.youtube.com/watch?v=PE4gwstWhmc)
* [Lessons of Scale at Facebook - Bobby Johnson, Director of Engineering at Facebook](https://www.youtube.com/watch?v=QCHiNEw73AU)
* [Scaling Instagram Infrastructure - Lisa Guo, Instagram Engineering](https://www.youtube.com/watch?v=hnpzNAPiC0E)
* [Scaling Pinterest - Marty Weiner, Pinterest’s founding engineer](https://www.youtube.com/watch?v=jQNCuD_hxdQ&list=RDhnpzNAPiC0E&index=11)
* [Designing for Failure: Scaling Uber's Backend by Breaking Everything - Matt Ranney, Chief Systems Architect at Uber](https://www.youtube.com/watch?v=nuiLcWE8sPA)

## Special Thanks
* Jonas Bonér, CTO at Lightbend, for the [original inspiration](https://www.slideshare.net/jboner/scalability-availability-stability-patterns)
