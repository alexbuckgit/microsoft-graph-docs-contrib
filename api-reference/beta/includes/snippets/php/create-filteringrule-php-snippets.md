---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\Networkaccess\WebCategoryFilteringRule
use Microsoft\Graph\Beta\Generated\Models\Networkaccess\RuleType;
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\Networkaccess\RuleDestination
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\Networkaccess\WebCategory


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new WebCategoryFilteringRule();
$requestBody->setOdataType('#microsoft.graph.networkaccess.webCategoryFilteringRule');
$requestBody->setName('Block Alcohol');
$requestBody->setRuleType(new NetworkDestinationType('webCategory'));
$destinationsRuleDestination1 = new WebCategory();
$destinationsRuleDestination1->setOdataType('#microsoft.graph.networkaccess.webCategory');
$destinationsRuleDestination1->setName('AlcoholAndTobacco');
$destinationsArray []= $destinationsRuleDestination1;
$requestBody->setDestinations($destinationsArray);


$result = $graphServiceClient->networkAccess()->filteringPolicies()->byFilteringPolicyId('filteringPolicy-id')->policyRules()->post($requestBody)->wait();

```