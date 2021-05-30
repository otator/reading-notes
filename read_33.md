# GraphQL


**Amplify**
[AWS Amplify](https://aws.amazon.com/amplify/) is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications, powered by AWS. With Amplify, you can configure app backends and connect your app in minutes, deploy static web apps in a few clicks, and easily manage app content outside the AWS console.

* Configure backends fast
* Seamlessly connect frontends
* Deploy in a few clicks
* Easily manage content

## GraphQL

The [GraphQL](https://docs.amplify.aws/cli/graphql-transformer/overview) Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS. With the GraphQL Transform, you define your application’s data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.

The GraphQL Transform simplifies the process of developing, deploying, and maintaining GraphQL APIs. With it, you define your API using the GraphQL Schema Definition Language (SDL) and can then use automation to transform it into a fully descriptive cloudformation template that implements the spec. The transform also provides a framework through which you can define your own transformers as `@directives` for custom workflows.

### @Connection in GraphQL

The `_@connection_` directive enables you to specify relationships between `@model` types. Currently, this supports one-to-one, one-to-many, and many-to-one relationships.

many-to-many relationships can be implemented using two one-to-many connections and a joining `@model` type.

[Connection Types](https://docs.amplify.aws/cli/graphql-transformer/connection#usage):
* Has one
* Has Many
* Belongs To
* Many To Many

### Limit

The default number of nested objects is 100. You can override this behavior by setting the limit argument.

### Generates

In order to keep connection queries fast and efficient, the GraphQL transform manages global secondary indexes (GSIs) on the generated tables on your behalf when using @connection