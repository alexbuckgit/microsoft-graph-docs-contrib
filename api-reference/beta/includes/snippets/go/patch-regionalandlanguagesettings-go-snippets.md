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

requestBody := graphmodels.NewRegionalAndLanguageSettings()


localeInfo := graphmodels.NewLocaleInfo()
locale := "en-US"
localeInfo.SetLocale(&locale) 
localeInfo1 := graphmodels.NewLocaleInfo()
locale := "es-MX"
localeInfo1.SetLocale(&locale) 

authoringLanguages := []graphmodels.LocaleInfoable {
	localeInfo,
	localeInfo1,
}
requestBody.SetAuthoringLanguages(authoringLanguages)
defaultRegionalFormat := graphmodels.NewLocaleInfo()
locale := "en-US"
defaultRegionalFormat.SetLocale(&locale) 
requestBody.SetDefaultRegionalFormat(defaultRegionalFormat)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
regionalAndLanguageSettings, err := graphClient.Me().Settings().RegionalAndLanguageSettings().Patch(context.Background(), requestBody, nil)


```