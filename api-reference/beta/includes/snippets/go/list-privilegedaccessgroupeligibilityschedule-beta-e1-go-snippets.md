---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphidentitygovernance "github.com/microsoftgraph/msgraph-beta-sdk-go/identitygovernance"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



requestFilter := "principalId eq '3cce9d87-3986-4f19-8335-7ed075408ca2'"

requestParameters := &graphidentitygovernance.IdentityGovernancePrivilegedAccessGroupEligibilitySchedulesRequestBuilderGetQueryParameters{
	Filter: &requestFilter,
}
configuration := &graphidentitygovernance.IdentityGovernancePrivilegedAccessGroupEligibilitySchedulesRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.IdentityGovernance().PrivilegedAccess().Group().EligibilitySchedules().Get(context.Background(), configuration)


```