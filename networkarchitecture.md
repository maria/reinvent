​# Network architecture

- VPN connection
- Direct connect
- Snowball

## Q&A

1. Vpc cross region, via vpc transit - no plans for global VPCs
2. vpgw - now worh ec2 instances in a vpc, with at least 512 mb of dedicated bandwith
3. Customers want to instantiate tunnels inside aws.
4. You can't do transitive routing.

## Transit VPC

a layer between your vpc and the internet. Is a vpc made out of firewalls or routing devices.
  
- Usecase - have a vpc transit to your datacenter and have a vpc per customer, 
  which connects to dc via vpc transit
- Caveats: ECMP is broken, vpn throughput applied, nat needed outbound

If you need capacity to vpgw you need to add custom vpn instances in your network and use them

### Buzzwords
  - Tsunami udp
  - ELB sandwich

* vpgw: virtual private gateway *
