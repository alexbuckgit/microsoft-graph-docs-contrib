---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\WebApp;
use Microsoft\Graph\Generated\Models\MimeContent;
use Microsoft\Graph\Generated\Models\PublishingState;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new WebApp();
$requestBody->setOdataType('#microsoft.graph.webApp');
$requestBody->setDisplayName('Display Name value');
$requestBody->setDescription('Description value');
$requestBody->setPublisher('Publisher value');
$largeIcon = new MimeContent();
$largeIcon->setOdataType('microsoft.graph.mimeContent');
$largeIcon->setType('Type value');
$largeIcon->setValue(\GuzzleHttp\Psr7\Utils::streamFor(base64_decode('dmFsdWU=')));
$requestBody->setLargeIcon($largeIcon);
$requestBody->setIsFeatured(true);
$requestBody->setPrivacyInformationUrl('https://example.com/privacyInformationUrl/');
$requestBody->setInformationUrl('https://example.com/informationUrl/');
$requestBody->setOwner('Owner value');
$requestBody->setDeveloper('Developer value');
$requestBody->setNotes('Notes value');
$requestBody->setPublishingState(new MobileAppPublishingState('processing'));
$requestBody->setAppUrl('https://example.com/appUrl/');
$requestBody->setUseManagedBrowser(true);

$result = $graphServiceClient->deviceAppManagement()->mobileApps()->post($requestBody)->wait();

```