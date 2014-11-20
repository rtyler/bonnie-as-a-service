# BaaS

Just some test code to hammer disk I/O on various machines

### targets.yml

This file is where all the hosts and some of the configuration information
goes, e.g.:


```
defaults:
    username: ubuntu
    timeout: 30
hosts:
    "my-private-cloud-vm":
        hostname: "14.4.4.23"
        username: tyler
        metadata:
            cloud: "OpenStax"
            region: "West US"
            type: "m1.medium"

```

### Running

 1. `bundle install`
 1. `./baas` will generate the `results/` files
 1. `./reporter` will generate `report.csv` which is a cumulative report for
    all `hosts`
