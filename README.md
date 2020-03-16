# YLZ-XYZ-INFRA

## Introduction

* This task should ideally be completed using Google or Firebase cloud platform.
* The focus is on the backend, but if possible a method to test the end point from a front end or command line would be preferred.
* The endpoint/ API calls should use Restful interface
* Good documentation should be used.


## Task

- A user signs up using the details
  * Unique Email
  * First Name
  * Surname
  * Password
- The user logs in using their email and password
  * Sign up and login should be secure on a token-based system
  * To do any functionality a secure token is required.
- The user creates a new project.  The project creator is the owner
- A user can be part of many projects
- The user can view a list of projects that are already created
- A project owner can add a registered user to a project using their email address.
- If a user is part of a project then they can access the project
- When in a project a user can add a device to the project (for this a device is a record consisting of a 5-digit serial number and a Name)
- User that have access to a project can see a list of devices.
  * A device can be part of many projects


## Optional Additional Tasks

- Use a program like “Terraform” to build the infrastructure
- A file up to 30mb can be uploaded to a project by the projects members
- The users on a project can view a list of the files and download them


## Deliverable

- Good commenting and documentation including example restful interface, and test method
- Upon completion a call will be scheduled to explore the system, thought patens, and your process.


- - -


- [Infrastructure Project](https://github.com/aytekinyaliz/ylz-xyz-infra)
- [IAM Service](https://github.com/aytekinyaliz/ylz-xyz-iam-svc)
- [Project Service](https://github.com/aytekinyaliz/ylz-xyz-project-svc)
- [Device Service](https://github.com/aytekinyaliz/ylz-xyz-device-svc)
- postgres
- redis

![High-Level Design](./_files/High-Level_Design.jpg)

![DB Design](./_files/High-Level_Design-DB.jpg)


## Current Topology


- Create 3 projects in Firebase
  * Create service accounts and generate private key (ideally these credentials should be stored in secrets and injected into environment variables via CI pipeline. At the moment they are stored in .env files in the repo for demo purposes).
  * Create Cloud Firestore for each project (eur3 (europe-west))



## TODOs

- [ ] Create 1-1 realation b/w email and token <email, { token }>
- [ ] JWT validation & Authentication & Authorization in API Gateway
- [ ] HTTP layer validations in services
- [ ] Logging
- [ ] Auditting
- [ ] CQRS pattern for fetching data from services
