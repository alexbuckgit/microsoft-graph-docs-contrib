---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\InformationProtection\Policy\Labels\EvaluateClassificationResults\EvaluateClassificationResultsRequestBuilderPostRequestConfiguration;
use Microsoft\Graph\Beta\Generated\InformationProtection\Policy\Labels\EvaluateClassificationResults\EvaluateClassificationResultsPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\ContentInfo;
use Microsoft\Graph\Beta\Generated\Models\Format;
use Microsoft\Graph\Beta\Generated\Models\State;
use Microsoft\Graph\Beta\Generated\Models\ClassificationResult;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EvaluateClassificationResultsPostRequestBody();
$contentInfo = new ContentInfo();
$contentInfo->setOdataType('#microsoft.graph.contentInfo');
$contentInfo->setFormat(new ContentFormat('default'));
$contentInfo->setIdentifier(null);
$contentInfo->setState(new ContentState('rest'));
$additionalData = [
	'format@odata.type' => '#microsoft.graph.contentFormat',
	'state@odata.type' => '#microsoft.graph.contentState',
];
$contentInfo->setAdditionalData($additionalData);
$requestBody->setContentInfo($contentInfo);
$classificationResultsClassificationResult1 = new ClassificationResult();
$classificationResultsClassificationResult1->setSensitiveTypeId('cb353f78-2b72-4c3c-8827-92ebe4f69fdf');
$classificationResultsClassificationResult1->setCount(4);
$classificationResultsClassificationResult1->setConfidenceLevel(75);
$classificationResultsArray []= $classificationResultsClassificationResult1;
$requestBody->setClassificationResults($classificationResultsArray);

$requestConfiguration = new EvaluateClassificationResultsRequestBuilderPostRequestConfiguration();
$headers = [
	'User-Agent' => 'ContosoLOBApp/1.0',
];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->informationProtection()->policy()->labels()->evaluateClassificationResults()->post($requestBody, $requestConfiguration)->wait();

```