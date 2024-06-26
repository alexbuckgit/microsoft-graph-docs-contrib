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

requestBody := graphmodels.NewUnifiedRoleManagementPolicy()


unifiedRoleManagementPolicyRule := graphmodels.NewUnifiedRoleManagementPolicyApprovalRule()
id := "Approval_EndUser_Assignment"
unifiedRoleManagementPolicyRule.SetId(&id) 
target := graphmodels.NewUnifiedRoleManagementPolicyRuleTarget()
caller := "EndUser"
target.SetCaller(&caller) 
operations := []graphmodels.UnifiedRoleManagementPolicyRuleTargetOperationsable {
	unifiedRoleManagementPolicyRuleTargetOperations := graphmodels.ALL_UNIFIEDROLEMANAGEMENTPOLICYRULETARGETOPERATIONS 
	target.SetUnifiedRoleManagementPolicyRuleTargetOperations(&unifiedRoleManagementPolicyRuleTargetOperations)
}
target.SetOperations(operations)
level := "Assignment"
target.SetLevel(&level) 
inheritableSettings := []string {

}
target.SetInheritableSettings(inheritableSettings)
enforcedSettings := []string {

}
target.SetEnforcedSettings(enforcedSettings)
unifiedRoleManagementPolicyRule.SetTarget(target)
setting := graphmodels.NewApprovalSettings()
isApprovalRequired := true
setting.SetIsApprovalRequired(&isApprovalRequired) 
isApprovalRequiredForExtension := false
setting.SetIsApprovalRequiredForExtension(&isApprovalRequiredForExtension) 
isRequestorJustificationRequired := true
setting.SetIsRequestorJustificationRequired(&isRequestorJustificationRequired) 
approvalMode := "SingleStage"
setting.SetApprovalMode(&approvalMode) 


unifiedApprovalStage := graphmodels.NewUnifiedApprovalStage()
approvalStageTimeOutInDays := int32(1)
unifiedApprovalStage.SetApprovalStageTimeOutInDays(&approvalStageTimeOutInDays) 
isApproverJustificationRequired := true
unifiedApprovalStage.SetIsApproverJustificationRequired(&isApproverJustificationRequired) 
escalationTimeInMinutes := int32(0)
unifiedApprovalStage.SetEscalationTimeInMinutes(&escalationTimeInMinutes) 
isEscalationEnabled := false
unifiedApprovalStage.SetIsEscalationEnabled(&isEscalationEnabled) 


subjectSet := graphmodels.NewSingleUser()
description := null
subjectSet.SetDescription(&description) 
additionalData := map[string]interface{}{
	isBackup := false
subjectSet.SetIsBackup(&isBackup) 
	"id" : "c277c8cb-6bb7-42e5-a17f-0add9a718151", 
}
subjectSet.SetAdditionalData(additionalData)

primaryApprovers := []graphmodels.SubjectSetable {
	subjectSet,
}
unifiedApprovalStage.SetPrimaryApprovers(primaryApprovers)
escalationApprovers := []graphmodels.SubjectSetable {

}
unifiedApprovalStage.SetEscalationApprovers(escalationApprovers)

approvalStages := []graphmodels.UnifiedApprovalStageable {
	unifiedApprovalStage,
}
setting.SetApprovalStages(approvalStages)
unifiedRoleManagementPolicyRule.SetSetting(setting)
unifiedRoleManagementPolicyRule1 := graphmodels.NewUnifiedRoleManagementPolicyAuthenticationContextRule()
id := "AuthenticationContext_EndUser_Assignment"
unifiedRoleManagementPolicyRule1.SetId(&id) 
isEnabled := false
unifiedRoleManagementPolicyRule1.SetIsEnabled(&isEnabled) 
claimValue := ""
unifiedRoleManagementPolicyRule1.SetClaimValue(&claimValue) 
target := graphmodels.NewUnifiedRoleManagementPolicyRuleTarget()
caller := "EndUser"
target.SetCaller(&caller) 
operations := []graphmodels.UnifiedRoleManagementPolicyRuleTargetOperationsable {
	unifiedRoleManagementPolicyRuleTargetOperations := graphmodels.ALL_UNIFIEDROLEMANAGEMENTPOLICYRULETARGETOPERATIONS 
	target.SetUnifiedRoleManagementPolicyRuleTargetOperations(&unifiedRoleManagementPolicyRuleTargetOperations)
}
target.SetOperations(operations)
level := "Assignment"
target.SetLevel(&level) 
inheritableSettings := []string {

}
target.SetInheritableSettings(inheritableSettings)
enforcedSettings := []string {

}
target.SetEnforcedSettings(enforcedSettings)
unifiedRoleManagementPolicyRule1.SetTarget(target)
unifiedRoleManagementPolicyRule2 := graphmodels.NewUnifiedRoleManagementPolicyEnablementRule()
id := "Enablement_Admin_Eligibility"
unifiedRoleManagementPolicyRule2.SetId(&id) 
enabledRules := []string {

}
unifiedRoleManagementPolicyRule2.SetEnabledRules(enabledRules)
target := graphmodels.NewUnifiedRoleManagementPolicyRuleTarget()
caller := "Admin"
target.SetCaller(&caller) 
operations := []graphmodels.UnifiedRoleManagementPolicyRuleTargetOperationsable {
	unifiedRoleManagementPolicyRuleTargetOperations := graphmodels.ALL_UNIFIEDROLEMANAGEMENTPOLICYRULETARGETOPERATIONS 
	target.SetUnifiedRoleManagementPolicyRuleTargetOperations(&unifiedRoleManagementPolicyRuleTargetOperations)
}
target.SetOperations(operations)
level := "Eligibility"
target.SetLevel(&level) 
inheritableSettings := []string {

}
target.SetInheritableSettings(inheritableSettings)
enforcedSettings := []string {

}
target.SetEnforcedSettings(enforcedSettings)
unifiedRoleManagementPolicyRule2.SetTarget(target)
unifiedRoleManagementPolicyRule3 := graphmodels.NewUnifiedRoleManagementPolicyExpirationRule()
id := "Expiration_Admin_Eligibility"
unifiedRoleManagementPolicyRule3.SetId(&id) 
isExpirationRequired := true
unifiedRoleManagementPolicyRule3.SetIsExpirationRequired(&isExpirationRequired) 
maximumDuration , err := abstractions.ParseISODuration("P365D")
unifiedRoleManagementPolicyRule3.SetMaximumDuration(&maximumDuration) 
target := graphmodels.NewUnifiedRoleManagementPolicyRuleTarget()
caller := "Admin"
target.SetCaller(&caller) 
operations := []graphmodels.UnifiedRoleManagementPolicyRuleTargetOperationsable {
	unifiedRoleManagementPolicyRuleTargetOperations := graphmodels.ALL_UNIFIEDROLEMANAGEMENTPOLICYRULETARGETOPERATIONS 
	target.SetUnifiedRoleManagementPolicyRuleTargetOperations(&unifiedRoleManagementPolicyRuleTargetOperations)
}
target.SetOperations(operations)
level := "Eligibility"
target.SetLevel(&level) 
inheritableSettings := []string {

}
target.SetInheritableSettings(inheritableSettings)
enforcedSettings := []string {

}
target.SetEnforcedSettings(enforcedSettings)
unifiedRoleManagementPolicyRule3.SetTarget(target)
unifiedRoleManagementPolicyRule4 := graphmodels.NewUnifiedRoleManagementPolicyNotificationRule()
id := "Notification_Admin_Admin_Eligibility"
unifiedRoleManagementPolicyRule4.SetId(&id) 
notificationType := "Email"
unifiedRoleManagementPolicyRule4.SetNotificationType(&notificationType) 
recipientType := "Admin"
unifiedRoleManagementPolicyRule4.SetRecipientType(&recipientType) 
notificationLevel := "All"
unifiedRoleManagementPolicyRule4.SetNotificationLevel(&notificationLevel) 
isDefaultRecipientsEnabled := true
unifiedRoleManagementPolicyRule4.SetIsDefaultRecipientsEnabled(&isDefaultRecipientsEnabled) 
notificationRecipients := []string {

}
unifiedRoleManagementPolicyRule4.SetNotificationRecipients(notificationRecipients)
target := graphmodels.NewUnifiedRoleManagementPolicyRuleTarget()
caller := "Admin"
target.SetCaller(&caller) 
operations := []graphmodels.UnifiedRoleManagementPolicyRuleTargetOperationsable {
	unifiedRoleManagementPolicyRuleTargetOperations := graphmodels.ALL_UNIFIEDROLEMANAGEMENTPOLICYRULETARGETOPERATIONS 
	target.SetUnifiedRoleManagementPolicyRuleTargetOperations(&unifiedRoleManagementPolicyRuleTargetOperations)
}
target.SetOperations(operations)
level := "Eligibility"
target.SetLevel(&level) 
inheritableSettings := []string {

}
target.SetInheritableSettings(inheritableSettings)
enforcedSettings := []string {

}
target.SetEnforcedSettings(enforcedSettings)
unifiedRoleManagementPolicyRule4.SetTarget(target)

rules := []graphmodels.UnifiedRoleManagementPolicyRuleable {
	unifiedRoleManagementPolicyRule,
	unifiedRoleManagementPolicyRule1,
	unifiedRoleManagementPolicyRule2,
	unifiedRoleManagementPolicyRule3,
	unifiedRoleManagementPolicyRule4,
}
requestBody.SetRules(rules)

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
roleManagementPolicies, err := graphClient.Policies().RoleManagementPolicies().ByUnifiedRoleManagementPolicyId("unifiedRoleManagementPolicy-id").Patch(context.Background(), requestBody, nil)


```