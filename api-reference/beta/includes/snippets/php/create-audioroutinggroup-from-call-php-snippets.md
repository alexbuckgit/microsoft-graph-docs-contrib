---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\AudioRoutingGroup;
use Microsoft\Graph\Beta\Generated\Models\RoutingMode;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AudioRoutingGroup();
$requestBody->setId('oneToOne');
$requestBody->setRoutingMode(new RoutingMode('oneToOne'));
$requestBody->setSources(['632899f8-2ea1-4604-8413-27bd2892079f', 	]);
$requestBody->setReceivers(['550fae72-d251-43ec-868c-373732c2704f', 	]);

$result = $graphServiceClient->communications()->calls()->byCallId('call-id')->audioRoutingGroups()->post($requestBody)->wait();

```