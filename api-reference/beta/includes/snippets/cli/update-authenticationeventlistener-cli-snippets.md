---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta identity authentication-event-listeners patch --authentication-event-listener-id {authenticationEventListener-id} --body '{\
    "@odata.type": "#microsoft.graph.onTokenIssuanceStartListener",\
    "conditions": {\
        "applications": {\
            "includeAllApplications": false\
        }\
    },\
    "priority": 500\
}\
'

```