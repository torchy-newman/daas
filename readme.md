azure spring cloud examples
===========================

Contains some code from two tutorials on how to deploy springboot applications to azure spring cloud.


#### ms workshop

Did this workshop from microsoftie
[Deploy Spring microservices to Azure](https://docs.microsoft.com/en-us/learn/modules/azure-spring-cloud-workshop/)

As is usual with many ms articles what happened is not explained but it did work.
NOTE code has to be in github 


Included 
1) creating azure spring cloud instance [azure spring cloud instance](https://portal.azure.com/?WT.mc_id=java-11899-judubois#@SparkNZ.onmicrosoft.com/resource/subscriptions/70f7934e-8593-40cb-9907-0119bde4e5fe/resourceGroups/daas-azure-spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/sparknz-daas/application_dashboard)
1) creating a mysql instance
1) creating and deploying spring boot application [todo-service](todo-service/)
1) linking spring boot application to the mysql database
1) creating and deploying a spring cloud gateway [todo-gateway](todo-gateway/)


Application can be accessed at url
```
https://sparknz-daas-todo-gateway.azuremicroservices.io/TODO-SERVICE/
```

returns
```json
[{"id":1,"description":"First item","done":true},{"id":2,"description":"Second item","done":true},{"id":3,"description":"Third item","done":false}]
```



#### spring guide

Tried this article from spring 
[Deploying a Spring Boot app to Azure](https://spring.io/guides/gs/spring-boot-for-azure/)

Deploys a trivial spring boot hello world application [gs-spring-boot](gs-spring-boot/complete), used the same  spring cloud instance [azure spring cloud instance](https://portal.azure.com/?WT.mc_id=java-11899-judubois#@SparkNZ.onmicrosoft.com/resource/subscriptions/70f7934e-8593-40cb-9907-0119bde4e5fe/resourceGroups/daas-azure-spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/sparknz-daas/application_dashboard)

Includes installing and configuring a maven plugin to deploy the application to azure spring cloud. This is probably more applicable for the DAAS microservices.

Application can be accessed at url
```
https://sparknz-daas-spring-boot-complete.azuremicroservices.io/
```
