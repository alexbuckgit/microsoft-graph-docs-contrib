---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\ChatMessage;
use Microsoft\Graph\Generated\Models\ChatMessagePolicyViolation;
use Microsoft\Graph\Generated\Models\ChatMessagePolicyViolationPolicyTip;
use Microsoft\Graph\Generated\Models\VerdictDetails;
use Microsoft\Graph\Generated\Models\DlpAction;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ChatMessage();
$policyViolation = new ChatMessagePolicyViolation();
$policyViolationPolicyTip = new ChatMessagePolicyViolationPolicyTip();
$policyViolationPolicyTip->setGeneralText('This item has been blocked by the administrator.');
$policyViolationPolicyTip->setComplianceUrl('https://contoso.com/dlp-policy-page');
$policyViolationPolicyTip->setMatchedConditionDescriptions(['Credit Card Number', 	]);
$policyViolation->setPolicyTip($policyViolationPolicyTip);
$policyViolation->setVerdictDetails(new ChatMessagePolicyViolationVerdictDetailsTypes('allowOverrideWithoutJustification,AllowFalsePositiveOverride'));
$policyViolation->setDlpAction(new ChatMessagePolicyViolationDlpActionTypes('blockAccess'));
$requestBody->setPolicyViolation($policyViolation);

$result = $graphServiceClient->teams()->byTeamId('team-id')->channels()->byChannelId('channel-id')->messages()->byChatMessageId('chatMessage-id')->patch($requestBody)->wait();

```