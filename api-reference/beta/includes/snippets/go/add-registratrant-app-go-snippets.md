---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewMeetingRegistrantBase()
firstName := "Lisa"
requestBody.SetFirstName(&firstName) 
lastName := "Adkins"
requestBody.SetLastName(&lastName) 
email := "lisa.adkins@contoso.com"
requestBody.SetEmail(&email) 


customQuestionAnswer := graphmodels.NewCustomQuestionAnswer()
questionId := "MSM5YjlmM2Q4ZS03ZmVkLTRmN3gwMDIw94MDAyMF9hX3gwMDIwX2RldmU="
customQuestionAnswer.SetQuestionId(&questionId) 
value := "No"
customQuestionAnswer.SetValue(&value) 
customQuestionAnswer1 := graphmodels.NewCustomQuestionAnswer()
questionId := "MSM5M2E2OWQ1Ni1jZTc4LTQDAwMjBfZGlkX3gwMDIwX3lvdV94MDAyMF8="
customQuestionAnswer1.SetQuestionId(&questionId) 
value := "Internet"
customQuestionAnswer1.SetValue(&value) 

customQuestionAnswers := []graphmodels.CustomQuestionAnswerable {
	customQuestionAnswer,
	customQuestionAnswer1,
}
requestBody.SetCustomQuestionAnswers(customQuestionAnswers)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
registrants, err := graphClient.Users().ByUserId("user-id").OnlineMeetings().ByOnlineMeetingId("onlineMeeting-id").Registration().Registrants().Post(context.Background(), requestBody, nil)


```