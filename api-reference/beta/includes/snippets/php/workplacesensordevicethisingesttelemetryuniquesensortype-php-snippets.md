---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\Beta\GraphServiceClient;
use Microsoft\Graph\Beta\Generated\Workplace\SensorDevices\IngestTelemetry\IngestTelemetryPostRequestBody
use Microsoft\Graph\Beta\Generated\Models\WorkplaceSensorDeviceTelemetry;
use Microsoft\Graph\Beta\Generated\Models\SensorType;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new IngestTelemetryPostRequestBody();
$telemetryWorkplaceSensorDeviceTelemetry1 = new WorkplaceSensorDeviceTelemetry();
$telemetryWorkplaceSensorDeviceTelemetry1->setDeviceId('contoso_9D6816');
$telemetryWorkplaceSensorDeviceTelemetry1->setSensorType(new WorkplaceSensorType('occupancy'));
$telemetryWorkplaceSensorDeviceTelemetry1->setBoolValue(false);
$telemetryWorkplaceSensorDeviceTelemetry1->setTimestamp(new \DateTime('2021-03-31T09:36:05.144Z'));
$telemetryArray []= $telemetryWorkplaceSensorDeviceTelemetry1;
$requestBody->setTelemetry($telemetryArray);


$graphServiceClient->workplace()->sensorDevices()->ingestTelemetry()->post($requestBody)->wait();

```