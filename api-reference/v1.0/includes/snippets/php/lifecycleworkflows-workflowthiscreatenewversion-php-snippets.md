---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php
use Microsoft\Graph\GraphServiceClient;
use Microsoft\Graph\Generated\IdentityGovernance\LifecycleWorkflows\Workflows\Item\MicrosoftGraphIdentityGovernanceCreateNewVersion\CreateNewVersionPostRequestBody
use Microsoft\Graph\Generated\Models\Microsoft\Graph\IdentityGovernance\Workflow
use Microsoft\Graph\Generated\Models\IdentityGovernance\Category;
use Microsoft\Graph\Generated\Models\Microsoft\Graph\IdentityGovernance\TriggerAndScopeBasedConditions
use Microsoft\Graph\Generated\Models\Microsoft\Graph\IdentityGovernance\RuleBasedSubjectSet
use Microsoft\Graph\Generated\Models\Microsoft\Graph\IdentityGovernance\TimeBasedAttributeTrigger
use Microsoft\Graph\Generated\Models\IdentityGovernance\TimeBasedAttribute;
use Microsoft\Graph\Generated\Models\Microsoft\Graph\IdentityGovernance\Task
use Microsoft\Graph\Generated\Models\KeyValuePair;


$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CreateNewVersionPostRequestBody();
$workflow = new Workflow();
$workflow->setCategory(new LifecycleWorkflowCategory('joiner'));
$workflow->setDescription('Configure new hire tasks for onboarding employees on their first day');
$workflow->setDisplayName('Global onboard new hire employee');
$workflow->setIsEnabled(true);
$workflow->setIsSchedulingEnabled(false);
$workflowExecutionConditions = new TriggerAndScopeBasedConditions();
$workflowExecutionConditions->setOdataType('#microsoft.graph.identityGovernance.triggerAndScopeBasedConditions');
$workflowExecutionConditionsScope = new RuleBasedSubjectSet();
$workflowExecutionConditionsScope->setOdataType('#microsoft.graph.identityGovernance.ruleBasedSubjectSet');
$workflowExecutionConditionsScope->setRule('(department eq \'Marketing\')');
$workflowExecutionConditions->setScope($workflowExecutionConditionsScope);
$workflowExecutionConditionsTrigger = new TimeBasedAttributeTrigger();
$workflowExecutionConditionsTrigger->setOdataType('#microsoft.graph.identityGovernance.timeBasedAttributeTrigger');
$workflowExecutionConditionsTrigger->setTimeBasedAttribute(new WorkflowTriggerTimeBasedAttribute('employeeHireDate'));
$workflowExecutionConditionsTrigger->setOffsetInDays(1);
$workflowExecutionConditions->setTrigger($workflowExecutionConditionsTrigger);
$workflow->setExecutionConditions($workflowExecutionConditions);
$tasksTask1 = new Task();
$tasksTask1->setContinueOnError(false);
$tasksTask1->setDescription('Enable user account in the directory');
$tasksTask1->setDisplayName('Enable User Account');
$tasksTask1->setIsEnabled(true);
$tasksTask1->setTaskDefinitionId('6fc52c9d-398b-4305-9763-15f42c1676fc');
$tasksTask1->setArguments([	]);
$tasksArray []= $tasksTask1;
$tasksTask2 = new Task();
$tasksTask2->setContinueOnError(false);
$tasksTask2->setDescription('Send welcome email to new hire');
$tasksTask2->setDisplayName('Send Welcome Email');
$tasksTask2->setIsEnabled(true);
$tasksTask2->setTaskDefinitionId('70b29d51-b59a-4773-9280-8841dfd3f2ea');
$tasksTask2->setArguments([	]);
$tasksArray []= $tasksTask2;
$workflow->setTasks($tasksArray);

$requestBody->setWorkflow($workflow);

$result = $graphServiceClient->identityGovernance()->lifecycleWorkflows()->workflows()->byWorkflowId('workflow-id')->microsoftGraphIdentityGovernanceCreateNewVersion()->post($requestBody)->wait();

```