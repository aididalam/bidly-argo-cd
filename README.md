Root project: [bidly](https://github.com/aididalam/bidly)

## Demo marketplace data

The Auth and Auction services seed five idempotent demo accounts (`user1@bidly.com` through `user5@bidly.com`, password `password`), twenty active listings, and ten bids during their own startup migrations. The Auction service uploads the bundled 16:9 demo photographs to its configured S3-compatible store. This is intended for the sandbox environment only; replace or remove these credentials before production use.
