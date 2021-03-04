# New starter (0 - 3 Years Innovation Team)

* [Introduction](##introduction)
* [How we work](##How-we-work)
* [SDG](##SDG)
* [Meetings](##meetigs)
* [Coding Standards](##coding-standards)
* [Technology](##technology)
    * [Frontend](###frontend)
    * [API](###api)
    * [Databases](###databases)
    * [Infrastructure](###infrastructure)
    * [DevOps](###devops)
* [Review Process](#rReview-process)
* [Booking Leave](##booking-leave)
* [Claiming Expenses](##claiming-expenses)

## Introduction

Congratulations on starting your new role at Jisc. This `README` will serve as a soft introduction to the team, the projects we work on and the tech we use.

The `0 - 3 Years Innovation` team focuses on deliverables within the next 0 to 3 years. This is in contrast to other teams in Jisc, such as the `3+ Years Innovation` team, which focuses on R&D. Or even other teams such as Learning Analytics, whose primary focus is on product/product family.

Our team works and has responsibility for the following projects:

- [Online Surveys V2](https://github.com/janetuk/bos2-core)
- [Online Surveys V3](https://github.com/jiscsd/online-surveys)
- [GeoConvert](https://github.com/JiscSD/geoconvert/)
- [CAS](https://github.com/jiscsd/census-platform)
- FE & Skills
- FE Elevator
- [Cloud Billing Portal](https://github.com/JiscSD/cloud-billing-portal/)
- [Jisc Login](https://github.com/JiscSD/jisc-sso)

## How we work

This team is somewhat unique within Jisc, in that we work on so many different projects. This means we have to work fast, and be a adaptable. What this translates to is that the developers on the team need to become full stack. You will have the opportunity to see every part of a project, whether that be the frontend, API, infrastructure, DeveOps etc.

We often find that we do a lot of wireframing on Miro so that we can be proactive whilst waiting for UI/UX resourcing.

It's important that you take ownership and pride of what you build, and ensure that the next person on it finds it easier enough to pick up. This means providing detailed and thorough documentation.

Since we work on so many projects, with different product owners, the way you work may differ from project to project. On some you may be using [kanban](https://www.atlassian.com/agile/kanban), on others you may be using [sprints](https://www.atlassian.com/agile/scrum/sprints).

## SDG

SDG, or Software Development Group sits within the CTO Group directorate.

## Meetings

We have a weekly meeting on Wednesdays at 13:30 - 14:30. There is also a developer fortnightly call where the teams within SDG (Software Development Group) take turns to present.

## Coding Standards

When writing code, we need to be using linters. Typically we use `eslint` and `prettier`, and these can be found in the projects listed above.

When writing SQL, we should aim to follow the [SQL Style Guide](https://www.sqlstyle.guide/) as closely as possible.

## Technology

All **new** projects that our team works on will use the following stack:

### Frontend

We use [React](https://reactjs.org/) to create SPAs. Typically we do **not** use [Next.js](https://nextjs.org/), but this may change in the future. To style our components, we use [Material UI](https://material-ui.com/). You will find that in each of our project repositories we put our coding standards in the relevent readmes. For example, in [Online Surveys, we have a section about import orders](https://github.com/JiscSD/online-surveys/tree/master/ui#react-coding-standards).

### API

Typically for our APIs we use [node.js](https://nodejs.org/en/) with the [Serverless Framework](https://www.serverless.com/). For middleware we've found that [@middy/core](https://www.npmjs.com/package/@middy/core) is really good.

### Databases

For relational databases, we use [Postgres](https://www.postgresql.org), unless we **have** to use [SQL Server](https://www.microsoft.com/en-gb/sql-server/sql-server-downloads).

Currently, we've had no reason to use NoSQL databases, but it's likely that if we were to use one, and depending on the circumstances, we'd be using on of: 

* [ElasticSearch](https://www.elastic.co/)
* [DynamoDB](https://aws.amazon.com/dynamodb/)
* [Mongo](https://www.mongodb.com/3)

In our APIs, we have not been using ORMs, we are just using the [pg-promise](https://github.com/vitaly-t/pg-promise) driver. However, this may change over time.

Finally, to perform DB migrations, we are using [postgrator](https://www.npmjs.com/package/postgrator), and invoking them as serverless functions.

### Infrastructure

The vast majority of our products are built on [AWS](https://aws.amazon.com/), using Serverless Architecture.

Some of our infrastructure is on [Azure](https://azure.microsoft.com/en-gb/), primarily Cloud Billing Portal.

All our infrastructure (other than very early testing) has to be built using IAC (Infrastructure as Code), namely [Terraform](https://www.terraform.io/).

### DevOps

All our deployments use AWS CodeBuild, unless on Azure, where we're currently using [Github Actions](https://github.com/features/actions) for Cloud Billing Portal.

## Review Process

Typically, we're happy for your code to be reviewed by one other person. However, since you're new, we recommend that when you're reviewing someone's code, you get someone else to check your review too (for the first month at least).