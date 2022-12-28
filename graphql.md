# Graphql 

## Introduction 

* query language with graph concept
* Runtime to be implemented
* Specification that need to be implemented by languages/frameworks
* Its a service

### GraphQL is service
* Graphql Schema
  * something linke DB schema
  * list of objects
  * what fields and each field data type

* GraphQL Resolver
  * how to represent data for each field
  * how and where is the data
* Example Schema - 
 ``` 
 type Person {
 name: String!
 age: String!
 mob: Int!
}
```

### Why graphQL 
* Isn't REST enough??
* Let's see 
  * No mandatory docs for REST - openAPI specs etc are optional
  * Underfetching data
  * overfetching data
  * If API is called it returns all of the data, no matter how many are useful for clients

### problems with graphql
* chances of resource exhaustion with nested query
* Single point of failure as we have one URL to access everything
* Authn/Authz for each and every query
* Caching issues - workkaround is **dataloader** to do this 
