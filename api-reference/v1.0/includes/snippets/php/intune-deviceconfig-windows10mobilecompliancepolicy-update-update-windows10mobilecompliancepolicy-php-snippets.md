---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\Windows10MobileCompliancePolicy;
use Microsoft\Graph\Generated\Models\PasswordRequiredType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new Windows10MobileCompliancePolicy();
$requestBody->setOdataType('#microsoft.graph.windows10MobileCompliancePolicy');
$requestBody->setDescription('Description value');
$requestBody->setDisplayName('Display Name value');
$requestBody->setVersion(7);
$requestBody->setPasswordRequired(true);
$requestBody->setPasswordBlockSimple(true);
$requestBody->setPasswordMinimumLength(5);
$requestBody->setPasswordMinimumCharacterSetCount(0);
$requestBody->setPasswordRequiredType(new RequiredPasswordType('alphanumeric'));
$requestBody->setPasswordPreviousPasswordBlockCount(2);
$requestBody->setPasswordExpirationDays(6);
$requestBody->setPasswordMinutesOfInactivityBeforeLock(5);
$requestBody->setPasswordRequireToUnlockFromIdle(true);
$requestBody->setOsMinimumVersion('Os Minimum Version value');
$requestBody->setOsMaximumVersion('Os Maximum Version value');
$requestBody->setEarlyLaunchAntiMalwareDriverEnabled(true);
$requestBody->setBitLockerEnabled(true);
$requestBody->setSecureBootEnabled(true);
$requestBody->setCodeIntegrityEnabled(true);
$requestBody->setStorageRequireEncryption(true);

$result = $graphServiceClient->deviceManagement()->deviceCompliancePolicies()->byDeviceCompliancePolicyId('deviceCompliancePolicy-id')->patch($requestBody)->wait();

```