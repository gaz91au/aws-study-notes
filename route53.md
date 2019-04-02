

## Routing Policies

### Simple
- Default routing policy
- one record, multiple ip addresses

### Weighted
- Can split traffic by percentage to each resource behind the DNS
- Good for testing DR environment

### Latency
- Allows routing based on lowest latency

### Failover
- Primary / Secondary routing, needs health check configured

### Geolocation
- routes traffic based on geolocation of your users

### Multi-value Answer Routing
- Up to 8 healthy records
    
### Alias record
- Naked domain name (no www. or sub domain)