---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v1.*

// Dependencies
import (
	  "context"
	  "time"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

requestBody := graphmodels.NewManagedDeviceMobileAppConfigurationDeviceStatus()
deviceDisplayName := "Device Display Name value"
requestBody.SetDeviceDisplayName(&deviceDisplayName) 
userName := "User Name value"
requestBody.SetUserName(&userName) 
deviceModel := "Device Model value"
requestBody.SetDeviceModel(&deviceModel) 
complianceGracePeriodExpirationDateTime , err := time.Parse(time.RFC3339, "2016-12-31T23:56:44.951111-08:00")
requestBody.SetComplianceGracePeriodExpirationDateTime(&complianceGracePeriodExpirationDateTime) 
status := graphmodels.NOTAPPLICABLE_COMPLIANCESTATUS 
requestBody.SetStatus(&status) 
lastReportedDateTime , err := time.Parse(time.RFC3339, "2017-01-01T00:00:17.7769392-08:00")
requestBody.SetLastReportedDateTime(&lastReportedDateTime) 
userPrincipalName := "User Principal Name value"
requestBody.SetUserPrincipalName(&userPrincipalName) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
deviceStatuses, err := graphClient.DeviceAppManagement().MobileAppConfigurations().ByManagedDeviceMobileAppConfigurationId("managedDeviceMobileAppConfiguration-id").DeviceStatuses().Post(context.Background(), requestBody, nil)


```