---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



result, err := graphClient.Directory().AdministrativeUnits().ByAdministrativeUnitId("administrativeUnit-id").ScopedRoleMembers().Get(context.Background(), nil)


```