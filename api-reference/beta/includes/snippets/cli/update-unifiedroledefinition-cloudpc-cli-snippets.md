---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta role-management cloud-pc role-definitions patch --unified-role-definition-id {unifiedRoleDefinition-id} --body '{\
  "description": "Update basic properties and permission of application registrations",\
  "displayName": "ExampleCustomRole",\
  "rolePermissions":\
    [\
        {\
            "allowedResourceActions": \
            [\
                "Microsoft.CloudPC/CloudPCs/Read",\
                "Microsoft.CloudPC/CloudPCs/Reprovision"\
            ]\
        }\
    ]\
}\
'

```