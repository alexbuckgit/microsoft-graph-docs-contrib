---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\Models\PhoneAuthenticationMethod;
use Microsoft\Graph\Generated\Models\PhoneType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new PhoneAuthenticationMethod();
$requestBody->setPhoneNumber('+1 2065555555');
$requestBody->setPhoneType(new AuthenticationPhoneType('mobile'));

$result = $graphServiceClient->users()->byUserId('user-id')->authentication()->phoneMethods()->post($requestBody)->wait();

```