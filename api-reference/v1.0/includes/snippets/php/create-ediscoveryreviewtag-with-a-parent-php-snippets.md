---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Microsoft\Graph\Security\EdiscoveryReviewTag
use Microsoft\Graph\Generated\Models\Security\ChildSelectability;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EdiscoveryReviewTag();
$requestBody->setDisplayName('My tag API');
$requestBody->setDescription('Use Graph API to create tags');
$requestBody->setChildSelectability(new ChildSelectability('many'));
$additionalData = [
	'parent@odata.bind' => '',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->security()->cases()->ediscoveryCases()->byEdiscoveryCaseId('ediscoveryCase-id')->tags()->post($requestBody)->wait();

```