Root project: [bidly](https://github.com/aididalam/bidly)

## Database

Bidly uses an external Amazon RDS for MySQL instance. The EKS/Terraform
environment creates the private RDS instance and supplies its endpoint and
application credential through the `bidly-auth-secrets` and
`bidly-auction-secrets` Kubernetes Secrets. Do not deploy a MySQL Pod, MySQL
Service, or bootstrap Job from this repository.

## Demo marketplace data

The Auth and Auction services seed five idempotent demo accounts (`user1@bidly.com` through `user5@bidly.com`, password `password`), twenty active listings, and ten bids during their own startup migrations. The Auction service uploads the bundled 16:9 demo photographs to its configured S3-compatible store. This is intended for the sandbox environment only; replace or remove these credentials before production use.
