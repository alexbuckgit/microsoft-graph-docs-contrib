---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Communications\Calls\Item\Reject\RejectPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\Reason;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new RejectPostRequestBody();
$requestBody->setReason(new RejectReason('busy'));

$graphServiceClient->communications()->calls()->byCallId('call-id')->reject()->post($requestBody)->wait();

```