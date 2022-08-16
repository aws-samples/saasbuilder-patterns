### Core Concept
* In a siloed compute mode, we saying that a compute resource will be deployed in a model where the compute resources are dedicated to a tenant. The motives for siloing computing can span a range of considerations, including noisy neighbor, isolation, tiering models, and application use cases. The mechanisms for partitioning compute can vary substantially. Containers and serverless, would rely on different strategies silo compute. 

### Key Considerations
* Siloing compute resources does not mean that every resources that’s touched by a compute resource is also siloed. A siloed EKS cluster, for example, could still interact with a database that is running in a pooled model. In this mode, each individual resource (compute, storage, etc.) can be deployed in a silo or pool model.
* How you silo compute can often be heavily influenced by the landscape of microservices that may be in your application. Each microservice of your application may make different choices about which microservices are deployed in a siloed compute model. In these instances, you may actually have a service that has multiple siloed compute deployments (one for each tenant that has been configured as requiring siloed compute resources for that microservice).
* Siloed compute does not require the compute to be deployed within a construct that isolates the compute. A siloed compute deployment, for example, does not require a separate VPC or Account to run the siloed compute resources. Siloed compute only means that the compute will not process requests from multiple tenants.
* Siloing compute resources does not insure that those resources are considered “isolated” from cross-tenant access. Siloed compute sets the stage for isolation, but your system must still apply policies and strategies to enforce isolation.



