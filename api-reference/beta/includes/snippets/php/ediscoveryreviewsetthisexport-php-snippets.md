---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Security\Cases\EdiscoveryCases\Item\ReviewSets\Item\MicrosoftGraphSecurityExport\ExportPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\Security\ExportOptions;
use Microsoft\Graph\Beta\Generated\Models\Security\ExportStructure;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new ExportPostRequestBody();
$requestBody->setOutputName('Export via API');
$requestBody->setDescription('Export for the Contoso investigation');
$requestBody->setExportOptions(new ExportOptions('originalFiles,fileInfo,tags'));
$requestBody->setExportStructure(new ExportFileStructure('directory'));

$graphServiceClient->security()->cases()->ediscoveryCases()->byEdiscoveryCaseId('ediscoveryCase-id')->reviewSets()->byEdiscoveryReviewSetId('ediscoveryReviewSet-id')->microsoftGraphSecurityExport()->post($requestBody)->wait();

```