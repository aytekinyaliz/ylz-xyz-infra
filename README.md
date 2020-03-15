# YLZ-XYZ-INFRA

- [Infrastructure Project](https://github.com/aytekinyaliz/ylz-xyz-infra)
- [IAM Service](https://github.com/aytekinyaliz/ylz-xyz-iam-svc)
- [Project Service](https://github.com/aytekinyaliz/ylz-xyz-project-svc)
- [Device Service](https://github.com/aytekinyaliz/ylz-xyz-device-svc)
- postgres
- redis

![High-Level Design](./_assets/High-Level_Design.svg)


## Current Topology
  - Create 3 projects in Firebase
    - Create service accounts and generate private key (ideally these credentials should be stored in secrets and injected into environment variables via CI pipeline. At the moment they are stored in .env files in the repo for demo purposes).
    - Create Cloud Firestore for each project (eur3 (europe-west))



## TODOs
  - Create 1-1 realation b/w email and token <email, { token }>
  - 
  - JWT validation & Authentication & Authorization in API Gateway
  - HTTP layer validations in services
  - Logging
  - Auditting
  - CQRS pattern for fetching data b/w services