---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewServicePrincipal()
appRoleAssignmentRequired := true
requestBody.SetAppRoleAssignmentRequired(&appRoleAssignmentRequired) 

result, err := graphClient.ServicePrincipals().ByServicePrincipalId("servicePrincipal-id").Patch(context.Background(), requestBody, nil)


```