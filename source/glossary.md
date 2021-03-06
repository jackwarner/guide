# Serverless Terminology

## Serverless Platform
- The platform supports administration, permission and user management associated with the development of [Serverless Services](#serverless-service).


## User Account
- A user account represents a single user in the [Serverless Platform](#serverless-platform).
- A user account stores sensitive identifying information such as email, password, username, etc
- A user account is considered the private representation of a user.


## User Profile
- A user profile represents the public presentation of a user in the [Serverless Platform](#serverless-platform).
- A user profile stores information that id displayed publicly about a user such as name, bio, github username, etc


## Serverless Service
- A Serverless Service consists of source code, a description, and service configuration.
- A service configuration is defined by a single `serverless.yml`


## Serverless Framework
- Drives the development/deployment lifecycle of a [Serverless Service](#service)
- Used to install [Functions](#function) and [Plugins](#plugin)
- Makes use of Plugins to extend the functionality of the framework.


## Plugin
- A Plugin is where the business logic lives for the functionality of the [Serverless Framework](#serverless-framework).


## Registry
- A service for registering and retrieving code packages for use in the [Serverless Framework](#serverless-framework).
- Registry is primarily used by framework for building [Serverless Services](#serverless-service).


## FDK
- Provides a simple middleware abstraction
- Enables runtime interaction with [Serverless Services](#serverless-service)
  + Executing functions
  + Dispatching events


## Gateway
- Every [Serverless Service](#serverless-service) automatically has a Gateway provisioned on deployment.
- The Gateway enables execution of the [Functions](#function) and handles propagation of [Events](#event).


## Discovery
- A service for registering and retrieving information on how to dispatch requests to [Serverless Services](#serverless-service).
- Discovery is primarily used by the [FDK](#fdk) for retrieving info on how to make calls and emit events to [Serverless Services](#serverless-service) within code.
- A [Serverless Service](#serverless-service) is automatically registered with Discovery when it is registered with the [Serverless Platform](#serverless-platform).

## Function
- Functions represent a basic unit of executable code.

### *Unprovisioned Functions*
- A zip file of a Function which you can download from the [Registry](#registry) and provision on your own infrastructure (e.g., AWS account).

### *Provisioned Functions*
- A [Function](#function) that is provisioned on someone's infrastructure and able to be invoked by someone else.
- All previous versions are expected to be kept available (which is possible w/ FaaS since all versions can be kept on a provider, awaiting an invocation for no additional cost/maintenance).

## Event
- Events are a unit of data that are sent between services