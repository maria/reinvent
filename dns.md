​# Dns demystified - introductory level

Intro to dns in route53
Advantages of route53
Aliasing of aws resources
Manage via api and cli
You can register domains in route53
Traffic flow on route53
Warner bros moved from 3 vms - 2 in aws and one in datacenter to route53
Have over 2500 domains
Some zones have 10k zones
What they had to fix:
Domain registration process
Devise a schem for reusable delegation steps
Find a way to import and validate the zones
Iam to delegate zones
Created all zones in one aws account
Had to split domains in chunks because of limits of delegation sets
Had to write the tool for validation
Lowered ttl
Cli53 to migrate the data, with custom patches - doc patch ( pun), regex fix
Migrated under 6 weeks
Next steps:
leverage advanced traffic policies
Health checks
Kitchenery
