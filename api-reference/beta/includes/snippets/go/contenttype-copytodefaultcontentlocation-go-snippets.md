---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphsites "github.com/microsoftgraph/msgraph-beta-sdk-go/sites"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

requestBody := graphsites.NewCopyToDefaultContentLocationPostRequestBody()
sourceFile := graphmodels.NewItemReference()
sharepointIds := graphmodels.NewSharepointIds()
listId := "e2ecf63b-b0fd-48f7-a54a-d8c15479e3b0"
sharepointIds.SetListId(&listId) 
listItemId := "2"
sharepointIds.SetListItemId(&listItemId) 
sourceFile.SetSharepointIds(sharepointIds)
requestBody.SetSourceFile(sourceFile)
destinationFileName := "newname.txt"
requestBody.SetDestinationFileName(&destinationFileName) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
graphClient.Sites().BySiteId("site-id").ContentTypes().ByContentTypeId("contentType-id").CopyToDefaultContentLocation().Post(context.Background(), requestBody, nil)


```