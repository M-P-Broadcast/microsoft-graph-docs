---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



result, err := graphClient.IdentityGovernance().EntitlementManagement().AccessPackageAssignmentApprovals().ByAccessPackageAssignmentApprovalId("approval-id").Steps().Get(context.Background(), nil)


```