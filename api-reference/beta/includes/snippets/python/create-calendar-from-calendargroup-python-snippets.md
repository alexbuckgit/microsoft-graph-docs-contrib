---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph_beta import GraphServiceClient
from msgraph_beta.generated.models.calendar import Calendar

graph_client = GraphServiceClient(credentials, scopes)

request_body = Calendar(
	name = "Marketing calendar",
)

result = await graph_client.me.calendar_groups.by_calendar_group_id('calendarGroup-id').calendars.post(request_body)


```