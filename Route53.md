# Dns demystified - introductory level

- Intro to dns in route53
- Advantages of route53
  - Aliasing of aws resources
  - Manage via api and cli
  - You can register domains in route53
  - Traffic flow on route53

### Usecase

Warner Bros. moved from 3 VMs - 2 in AWS and one in datacenter to Route53
  - Have over 2500 domains
  - Some zones have 10k zones
  - What they had to fix:
    - Domain registration process
    - Devise a schem for reusable delegation steps
    - Find a way to import and validate the zones
    - IAM to delegate zones
    - Created all zones in one aws account
    - Had to split domains in chunks because of limits of delegation sets
    - Had to write the tool for validation
    - Lowered ttl
    - Used [Cli53](https://github.com/barnybug/cli53) to migrate the data, with custom patches - doc patch(pun), regex fix
      - Migrated under 6 weeks
  - Next steps:
    - leverage advanced traffic policies
    - Health checks
    - Kitchenery
