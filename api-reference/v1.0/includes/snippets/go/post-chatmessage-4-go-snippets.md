---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewChatMessage()
body := graphmodels.NewItemBody()
contentType := graphmodels.HTML_BODYTYPE 
body.SetContentType(&contentType) 
content := "Here's the latest budget. <attachment id=\"153fa47d-18c9-4179-be08-9879815a9f90\"></attachment>"
body.SetContent(&content) 
requestBody.SetBody(body)


chatMessageAttachment := graphmodels.NewChatMessageAttachment()
id := "153fa47d-18c9-4179-be08-9879815a9f90"
chatMessageAttachment.SetId(&id) 
contentType := "reference"
chatMessageAttachment.SetContentType(&contentType) 
contentUrl := "https://m365x987948.sharepoint.com/sites/test/Shared%20Documents/General/test%20doc.docx"
chatMessageAttachment.SetContentUrl(&contentUrl) 
name := "Budget.docx"
chatMessageAttachment.SetName(&name) 

attachments := []graphmodels.ChatMessageAttachmentable {
	chatMessageAttachment,
}
requestBody.SetAttachments(attachments)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
messages, err := graphClient.Teams().ByTeamId("team-id").Channels().ByChannelId("channel-id").Messages().Post(context.Background(), requestBody, nil)


```