### NAT Instances Notes:
- When creating NAT instance, disable source and destination check on the instance.
- NAT instances must be on a public subnet.
- Private subnets must have a route to the NAT to get internet connection.
- Increase instance size of NAT if there is bottlenecks.
- NAT instances are always behind a security group.

### NAT Gateway Notes:
- Scales up to 10Gbps.
- No need to patch.
- Not associated with security groups.
- Automatically assigned a public IP address.
- Need to update route tables.d
- No need to disable Source/Destination checks.

### Network ACL Notes
- VPC automatically comes with a default network ACL, allows all outband and inbound traffic.
- You can add custom rules to deny traffic.
- Every subnet must be associated with a network ACL, otherwise the default ACL will be used.
- ACL can be associated with multiple subnets.
- A subnet can only associate to one ACL.
- ACL contain a numbered list of rules, evaluated in ascending order.
- ACL have seperate rules for inbound and outbound traffic.
- ACls are stateless.
- ACL can block IP addresses.

### Application Load Balancers
- Requires 2 public subnets to use ALB.

### VPC Flow Logs
- Logs to monitor all traffic against Elastic Network Interfaces.
- Cant tag flow log.
- Cant change configuration once created.
- Cant enable flow logs for peered VPC's unless both VPC's are in the same account.
