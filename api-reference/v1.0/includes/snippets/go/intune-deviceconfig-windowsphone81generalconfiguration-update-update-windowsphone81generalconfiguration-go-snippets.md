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

requestBody := graphmodels.NewDeviceConfiguration()
description := "Description value"
requestBody.SetDescription(&description) 
displayName := "Display Name value"
requestBody.SetDisplayName(&displayName) 
version := int32(7)
requestBody.SetVersion(&version) 
applyOnlyToWindowsPhone81 := true
requestBody.SetApplyOnlyToWindowsPhone81(&applyOnlyToWindowsPhone81) 
appsBlockCopyPaste := true
requestBody.SetAppsBlockCopyPaste(&appsBlockCopyPaste) 
bluetoothBlocked := true
requestBody.SetBluetoothBlocked(&bluetoothBlocked) 
cameraBlocked := true
requestBody.SetCameraBlocked(&cameraBlocked) 
cellularBlockWifiTethering := true
requestBody.SetCellularBlockWifiTethering(&cellularBlockWifiTethering) 


appListItem := graphmodels.NewAppListItem()
name := "Name value"
appListItem.SetName(&name) 
publisher := "Publisher value"
appListItem.SetPublisher(&publisher) 
appStoreUrl := "https://example.com/appStoreUrl/"
appListItem.SetAppStoreUrl(&appStoreUrl) 
appId := "App Id value"
appListItem.SetAppId(&appId) 

compliantAppsList := []graphmodels.AppListItemable {
	appListItem,
}
requestBody.SetCompliantAppsList(compliantAppsList)
compliantAppListType := graphmodels.APPSINLISTCOMPLIANT_APPLISTTYPE 
requestBody.SetCompliantAppListType(&compliantAppListType) 
diagnosticDataBlockSubmission := true
requestBody.SetDiagnosticDataBlockSubmission(&diagnosticDataBlockSubmission) 
emailBlockAddingAccounts := true
requestBody.SetEmailBlockAddingAccounts(&emailBlockAddingAccounts) 
locationServicesBlocked := true
requestBody.SetLocationServicesBlocked(&locationServicesBlocked) 
microsoftAccountBlocked := true
requestBody.SetMicrosoftAccountBlocked(&microsoftAccountBlocked) 
nfcBlocked := true
requestBody.SetNfcBlocked(&nfcBlocked) 
passwordBlockSimple := true
requestBody.SetPasswordBlockSimple(&passwordBlockSimple) 
passwordExpirationDays := int32(6)
requestBody.SetPasswordExpirationDays(&passwordExpirationDays) 
passwordMinimumLength := int32(5)
requestBody.SetPasswordMinimumLength(&passwordMinimumLength) 
passwordMinutesOfInactivityBeforeScreenTimeout := int32(14)
requestBody.SetPasswordMinutesOfInactivityBeforeScreenTimeout(&passwordMinutesOfInactivityBeforeScreenTimeout) 
passwordMinimumCharacterSetCount := int32(0)
requestBody.SetPasswordMinimumCharacterSetCount(&passwordMinimumCharacterSetCount) 
passwordPreviousPasswordBlockCount := int32(2)
requestBody.SetPasswordPreviousPasswordBlockCount(&passwordPreviousPasswordBlockCount) 
passwordSignInFailureCountBeforeFactoryReset := int32(12)
requestBody.SetPasswordSignInFailureCountBeforeFactoryReset(&passwordSignInFailureCountBeforeFactoryReset) 
passwordRequiredType := graphmodels.ALPHANUMERIC_REQUIREDPASSWORDTYPE 
requestBody.SetPasswordRequiredType(&passwordRequiredType) 
passwordRequired := true
requestBody.SetPasswordRequired(&passwordRequired) 
screenCaptureBlocked := true
requestBody.SetScreenCaptureBlocked(&screenCaptureBlocked) 
storageBlockRemovableStorage := true
requestBody.SetStorageBlockRemovableStorage(&storageBlockRemovableStorage) 
storageRequireEncryption := true
requestBody.SetStorageRequireEncryption(&storageRequireEncryption) 
webBrowserBlocked := true
requestBody.SetWebBrowserBlocked(&webBrowserBlocked) 
wifiBlocked := true
requestBody.SetWifiBlocked(&wifiBlocked) 
wifiBlockAutomaticConnectHotspots := true
requestBody.SetWifiBlockAutomaticConnectHotspots(&wifiBlockAutomaticConnectHotspots) 
wifiBlockHotspotReporting := true
requestBody.SetWifiBlockHotspotReporting(&wifiBlockHotspotReporting) 
windowsStoreBlocked := true
requestBody.SetWindowsStoreBlocked(&windowsStoreBlocked) 

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
deviceConfigurations, err := graphClient.DeviceManagement().DeviceConfigurations().ByDeviceConfigurationId("deviceConfiguration-id").Patch(context.Background(), requestBody, nil)


```