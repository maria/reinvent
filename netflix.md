# Netflix
​
Speaker: Coburn Watson

## Content
  Failure driven architecture
  Chaos eng
  Cloud capacity planning
  Cloud net
  Perf and os eng
  Traffic management

Fun fact: 35% internet traffic at peak in us

## Talk

1. Arch pillars:
 - microservices:
  - edge(elb, api, zuul), middle tier.
  - hystrix: fallback service
  - chaos monkey and fit(fault injection trst framework)

2. Databases
  - started with simpledb
  - scalable, durable and global: cassandra
  ( multiple region and directional)
    - single region, more azs
    - not quite fast, created evcache

3. Traffic
  - dns geo mapping
  - Failover in us via replication
  - Database night compare and sync
  - Evcache replication
  - Used ultradns for geo routing - mapped regions to aws region by hand
  - Going globally: serve any user from any region
    - Use the 3 region, base on cdn
    - Move between regions when one is down
    - Use kafka for evcache replication
    - Have a global ring for cassandra per region

4. What's Next:
  - Global latency routing
  - Ml based monitoring(atlas)
  - Fast failover < 40'(5-6')
  - Integrate db and caching
  - Improved capacity utilization
  - Automated chaos - chap framework

5. Takeaways:
  - never fail the same way twice
  - Know your resilience patterns
  - Think globally, act globally

### Buzzwords
  - vizceral
