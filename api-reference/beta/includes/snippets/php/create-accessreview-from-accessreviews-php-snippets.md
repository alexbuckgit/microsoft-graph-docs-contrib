---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Models\AccessReview;
use Microsoft\Graph\Beta\Generated\Models\Identity;
use Microsoft\Graph\Beta\Generated\Models\AccessReviewReviewer;
use Microsoft\Graph\Beta\Generated\Models\AccessReviewSettings;
use Microsoft\Graph\Beta\Generated\Models\AccessReviewRecurrenceSettings;
use Microsoft\Graph\Beta\Generated\Models\AutoReviewSettings;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new AccessReview();
$requestBody->setDisplayName('TestReview');
$requestBody->setStartDateTime(new \DateTime('2017-02-10T00:35:53.214Z'));
$requestBody->setEndDateTime(new \DateTime('2017-03-12T00:35:53.214Z'));
$reviewedEntity = new Identity();
$reviewedEntity->setId('99025615-a0b1-47ec-9117-35377b10998b');
$requestBody->setReviewedEntity($reviewedEntity);
$requestBody->setReviewerType('delegated');
$requestBody->setBusinessFlowTemplateId('6e4f3d20-c5c3-407f-9695-8460952bcc68');
$requestBody->setDescription('Sample description');
$reviewersAccessReviewReviewer1 = new AccessReviewReviewer();
$reviewersAccessReviewReviewer1->setId('f260246a-09b1-4fd5-8d18-daed736071ec');
$reviewersArray []= $reviewersAccessReviewReviewer1;
$reviewersAccessReviewReviewer2 = new AccessReviewReviewer();
$reviewersAccessReviewReviewer2->setId('5a4e184c-4ee5-4883-96e9-b371f8da88e3');
$reviewersArray []= $reviewersAccessReviewReviewer2;
$requestBody->setReviewers($reviewersArray);

$settings = new AccessReviewSettings();
$settings->setMailNotificationsEnabled(true);
$settings->setRemindersEnabled(true);
$settings->setJustificationRequiredOnApproval(true);
$settings->setAutoReviewEnabled(false);
$settings->setActivityDurationInDays(30);
$settings->setAutoApplyReviewResultsEnabled(false);
$settings->setAccessRecommendationsEnabled(false);
$settingsRecurrenceSettings = new AccessReviewRecurrenceSettings();
$settingsRecurrenceSettings->setRecurrenceType('onetime');
$settingsRecurrenceSettings->setRecurrenceEndType('endBy');
$settingsRecurrenceSettings->setDurationInDays(0);
$settingsRecurrenceSettings->setRecurrenceCount(0);
$settings->setRecurrenceSettings($settingsRecurrenceSettings);
$settingsAutoReviewSettings = new AutoReviewSettings();
$settingsAutoReviewSettings->setNotReviewedResult('Deny');
$settings->setAutoReviewSettings($settingsAutoReviewSettings);
$requestBody->setSettings($settings);

$result = $graphServiceClient->accessReviews()->post($requestBody)->wait();

```