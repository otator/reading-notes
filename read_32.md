# Serverless

[Serverless](https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9) is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider.

Serverless slang:  

**“Focus on your application, not the infrastructure”**

### Serverless Architecture Vs. Traditional way

The image below shows the difference between using **serverless and the traditional way**

<img src="https://cdn.hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg" style="border-radius:10px; width: 700px">

### Benefits of Serverless Architecture

**From business perspective**

* The cost incurred by a serverless application is based on the number of function executions, measured in milliseconds instead of hours.

* Process agility: Smaller deployable units result in faster delivery of features to the market, increasing the ability to adapt to change.
* Cost of hiring backend infrastructure engineers goes down.
* Reduced operational costs.

**From developer perspective**

* Reduced liability, no backend infrastructure to be responsible for.
* Zero system administration.
* Easier operational management.
* Fosters adoption of Nanoservices, Microservices, SOA Principles.
* Faster set up.
* Scalable, no need to worry about the number of concurrent requests.
* Monitoring out of the box.
* Fosters innovation.

**From user perspective**
* If businesses are using that competitive edge to ship features faster, then customers are receiving new features quicker than before.
* It is possible that users can more easily provide their own storage backend(i.e Dropbox, Google Drive).
* It’s more likely that these kinds of apps may offer client-side caching, which provides a better offline experience.

### Drawbacks of Serverless Architecture

**From business perspective**

* Reduced overall control.
* Vendor lock-in requires more trust for a third-party provider.
* Additional exposure to risk requires more trust for a third party provider.
* Security risk.
* Disaster recovery risk
* Cost is unpredictable because the number of executions is not predefined
* All of these drawbacks can be mitigated with open-source alternatives but at the expense of cost benefits mentioned previously

**From developer perspective**

* Immature technology results in component fragmentation, unclear best-practices.
* Architectural complexity.
* The discipline required against function sprawl.
* Multi-tenancy means it’s technically possible that neighbour functions could hog the system resources behind the scenes.
* Testing locally becomes tricky.
* Significant restrictions on the local state.
* Execution duration is capped.
* Lack of operational tools

**From user perspective**
* Unless architected correctly, an app could provide a poor user experience as a result of increased request latency.

#### Cloud providers

<img src="https://cdn.hackernoon.com/hn-images/1*t4O4UXpdG68MQboNKC6bBw.jpeg" style="border-radius:10px; width: 700px">


As shown in the image above Amazon Web Service **AWS** is one if the serverless providers

**AWS Amplify Benifits**
* Configure backends fast
* Seamlessly connect frontends
* Deploy in a few clicks
* Easily manage content

## GraphQL
The [GraphQL](https://docs.amplify.aws/cli/graphql-transformer/overview) Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS. With the GraphQL Transform, you define your application’s data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.

The GraphQL Transform simplifies the process of developing, deploying, and maintaining GraphQL APIs. With it, you define your API using the GraphQL Schema Definition Language (SDL) and can then use automation to transform it into a fully descriptive cloudformation template that implements the spec. The transform also provides a framework through which you can define your own transformers as @directives for custom workflows.