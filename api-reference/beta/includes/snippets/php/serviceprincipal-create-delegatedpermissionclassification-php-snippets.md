---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\DelegatedPermissionClassification;
use Microsoft\Graph\Beta\Generated\Models\Classification;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new DelegatedPermissionClassification();
$requestBody->setPermissionId('e1fe6dd8-ba31-4d61-89e7-88639da4683d');
$requestBody->setPermissionName('User.Read');
$requestBody->setClassification(new PermissionClassificationType('low'));

$result = $graphServiceClient->servicePrincipals()->byServicePrincipalId('servicePrincipal-id')->delegatedPermissionClassifications()->post($requestBody)->wait();

```