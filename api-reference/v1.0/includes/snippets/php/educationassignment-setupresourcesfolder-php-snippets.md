---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Education\Classes\Item\Assignments\Item\SetUpResourcesFolder\SetUpResourcesFolderPostRequestBody


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new SetUpResourcesFolderPostRequestBody();

$result = $graphServiceClient->education()->classes()->byEducationClassId('educationClass-id')->assignments()->byEducationAssignmentId('educationAssignment-id')->setUpResourcesFolder()->post($requestBody)->wait();

```