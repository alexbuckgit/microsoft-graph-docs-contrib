---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Users\Item\Events\Item\Instances\InstancesRequestBuilderGetRequestConfiguration;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestConfiguration = new InstancesRequestBuilderGetRequestConfiguration();
$queryParameters = InstancesRequestBuilderGetRequestConfiguration::createQueryParameters();
$queryParameters->startDateTime = "2019-04-08T09:00:00.0000000";
$queryParameters->endDateTime = "2019-04-30T09:00:00.0000000";
$queryParameters->select = ["subject","bodyPreview","seriesMasterId","type","recurrence","start","end"];
$requestConfiguration->queryParameters = $queryParameters;


$result = $graphServiceClient->me()->events()->byEventId('event-id')->instances()->get($requestConfiguration)->wait();

```