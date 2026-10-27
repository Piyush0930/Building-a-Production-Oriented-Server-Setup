# aws-hands-on-labs

Hands-on AWS labs with architecture diagrams, covering EC2, VPC, ALB, EBS, Route 53, CloudWatch and backups.

Each lab documents what I built, the checks I used to validate it, and what I learned.

> **Note:** These are practice labs, not client production deployments. A lab is not equivalent to a certified production environment, but it is a useful way to rehearse repeatable operational procedures before applying them for real.

## Labs

| # | Lab | Topics | Folder |
|---|-----|--------|--------|
| 1 | Hosting a web server on EC2 with an Elastic IP | EC2, Elastic IP, Security Groups, connectivity validation | [`ec2-elastic-ip-web-server`](labs/ec2-elastic-ip-web-server) |
| 2 | Launching EC2 in a public subnet | Route tables, Internet Gateway, NACLs, Security Groups | [`vpc-public-subnet-ec2`](labs/vpc-public-subnet-ec2) |
| 3 | Multi-AZ workloads and VPC peering | CIDR planning, peering routes, non-transitive routing | [`vpc-peering-multi-az`](labs/vpc-peering-multi-az) |
| 4 | ALB to private EC2 instances | ALB, target groups, health checks, SG references | [`alb-private-ec2`](labs/alb-private-ec2) |
| 5 | ALB listeners, rules and target groups | Listener rules, host and path routing, troubleshooting | [`alb-listeners-target-groups`](labs/alb-listeners-target-groups) |
| 6 | Mapping a domain with Route 53 | Hosted zones, alias records, TTL, delegation | [`route53-dns-mapping`](labs/route53-dns-mapping) |
| 7 | Attaching and mounting an EBS volume | AZ compatibility, filesystems, fstab | [`ebs-attach-mount`](labs/ebs-attach-mount) |
| 8 | Automating EBS snapshot lifecycle | DLM, tags, retention, encryption, restore tests | [`ebs-dlm-snapshots`](labs/ebs-dlm-snapshots) |
| 9 | Automating EC2 AMI creation and retention | AMIs vs snapshots, DLM, restore validation | [`ec2-ami-lifecycle`](labs/ec2-ami-lifecycle) |
| 10 | EC2 metrics and CloudWatch alarms | Metrics, thresholds, SNS, CloudWatch Agent | [`cloudwatch-alarms`](labs/cloudwatch-alarms) |
| 11 | Deploying a MERN stack application | ALB, EC2, MongoDB, secrets, logs, deployment steps | [`mern-deployment`](labs/mern-deployment) |
| 12 | Production-oriented EC2 server setup | IAM, Session Manager, patching, monitoring, backups | [`ec2-production-lab`](labs/ec2-production-lab) |

## Repository structure

```text
aws-hands-on-labs/
├── README.md
└── labs/
    └── <lab-name>/
        ├── README.md      # write-up: what I built, checks, lessons learned
        └── diagram.png    # architecture diagram
```

## What each lab includes

- **Architecture diagram** showing the components and the traffic or data flow
- **What I configured** and why
- **Validation steps** to confirm the setup works
- **Lessons learned**, including common mistakes
- **Cleanup notes** to avoid leftover cost

## Cost and safety

Some resources, such as EC2 instances, Elastic IPs, load balancers, NAT gateways and snapshots, can incur charges. Always clean up lab resources when you finish, and never commit credentials, keys or account IDs.

## Tech and topics

`AWS` `EC2` `VPC` `ALB` `EBS` `Route 53` `CloudWatch` `DLM` `Linux` `Networking` `Cloud Engineering`
