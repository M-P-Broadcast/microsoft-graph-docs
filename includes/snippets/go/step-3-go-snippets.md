---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewChatMessage()
body := graphmodels.NewItemBody()
content := "Hello World"
body.SetContent(&content) 
requestBody.SetBody(body)

result, err := graphClient.Chats().ByChatId("chat-id").Messages().Post(context.Background(), requestBody, nil)


```