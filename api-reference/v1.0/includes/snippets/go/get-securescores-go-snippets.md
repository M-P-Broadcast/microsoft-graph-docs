---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphsecurity "github.com/microsoftgraph/msgraph-sdk-go/security"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



requestTop := int32(1)

requestParameters := &graphsecurity.SecuritySecureScoresRequestBuilderGetQueryParameters{
	Top: &requestTop,
}
configuration := &graphsecurity.SecuritySecureScoresRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.Security().SecureScores().Get(context.Background(), configuration)


```