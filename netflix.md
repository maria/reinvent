# Netflix
​
Speaker: Coburn Watson
GitHub org: https://github.com/Netflix

## Content
  - Failure driven architecture
  - Chaos engineering
  - Cloud capacity planning
  - Cloud net
  - Performance and OSS Engineering
  - Traffic management

*Fun fact: 35% internet traffic at peak in the US*

## Talk

1. Arch pillars:
  - microservices:
  - edge (elb, api, zuul), middle tier.
  - Hystrix: fallback service
  - Chaos Monkey and fit (fault injection test framework)

2. Databases
  - started with SimpleDB
  - scalable, durable and global: Cassandra
  ( multiple region and directional)
    - single region, more azs
    - not quite fast, created evcache

3. Traffic
  - DNS geo mapping
  - Failover in US via replication
  - Database night compare and sync
  - [EVCache](https://github.com/Netflix/EVCache) replication
  - Used UltraDNS for geo routing - mapped regions to AWS region by hand
  - Going globally: serve any user from any region
    - Use the 3 region, base on CDN
    - Move between regions when one is down
    - Use Kafka for EVCache replication
    - Have a global ring for Cassandra per region

4. What's Next:
  - Global latency routing
  - Ml based monitoring(atlas)
  - Fast failover < 40'(5-6')
  - Integrate db and caching
  - Improved capacity utilization
  - Automated chaos - Chap framework

5. Takeaways:
  - never fail the same way twice
  - Know your resilience patterns
  - Think globally, act globally

### Buzzwords
  - vizceral
