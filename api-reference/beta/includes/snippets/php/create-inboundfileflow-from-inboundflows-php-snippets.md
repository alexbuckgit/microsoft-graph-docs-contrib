---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\Microsoft\Graph\IndustryData\InboundFileFlow
use Microsoft\Graph\Beta\Generated\Models\IndustryData\DataDomain;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new InboundFileFlow();
$requestBody->setOdataType('#microsoft.graph.industryData.inboundFileFlow');
$requestBody->setDataDomain(new InboundDomain('educationRostering'));
$requestBody->setDisplayName('Inbound rostering flow');
$requestBody->setEffectiveDateTime(new \DateTime('2023-03-12T16:40:46.924769+05:30'));
$requestBody->setExpirationDateTime(new \DateTime('2023-03-13T16:40:46.924769+05:30'));
$additionalData = [
	'dataConnector@odata.bind' => 'https://graph.microsoft.com/beta/external/industryData/dataConnectors/51dca0a0-85f6-4478-f526-08daddab2271',
	'year@odata.bind' => 'https://graph.microsoft.com/beta/external/industryData/years/ebf18762-ab92-487e-21d1-08daddab28bb',
];
$requestBody->setAdditionalData($additionalData);

$result = $graphServiceClient->external()->industryData()->inboundFlows()->post($requestBody)->wait();

```