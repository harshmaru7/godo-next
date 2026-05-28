# Reference
<details><summary><code>client.GetV21Clicks() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV21Clicks(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV21ClicksKubernetes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV21ClicksKubernetes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Account() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Account(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AccountKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2AccountKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AccountKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2AccountKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AccountKeysSSHKeyIdentifier(SSHKeyIdentifier) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AccountKeysSSHKeyIdentifierRequest{
        SSHKeyIdentifier: "ssh_key_identifier",
    }
client.GetV2AccountKeysSSHKeyIdentifier(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sshKeyIdentifier:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2AccountKeysSSHKeyIdentifier(SSHKeyIdentifier) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2AccountKeysSSHKeyIdentifierRequest{
        SSHKeyIdentifier: "ssh_key_identifier",
    }
client.PutV2AccountKeysSSHKeyIdentifier(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sshKeyIdentifier:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2AccountKeysSSHKeyIdentifier(SSHKeyIdentifier) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2AccountKeysSSHKeyIdentifierRequest{
        SSHKeyIdentifier: "ssh_key_identifier",
    }
client.DeleteV2AccountKeysSSHKeyIdentifier(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sshKeyIdentifier:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Actions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Actions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ActionsActionID(ActionID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ActionsActionIDRequest{
        ActionID: "action_id",
    }
client.GetV2ActionsActionID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**actionID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AddOnsApps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2AddOnsApps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AddOnsAppsAppSlugMetadata(AppSlug) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AddOnsAppsAppSlugMetadataRequest{
        AppSlug: "app_slug",
    }
client.GetV2AddOnsAppsAppSlugMetadata(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appSlug:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AddOnsSaas() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2AddOnsSaas(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AddOnsSaas() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2AddOnsSaas(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AddOnsSaasResourceUUID(ResourceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AddOnsSaasResourceUUIDRequest{
        ResourceUUID: "resource_uuid",
    }
client.GetV2AddOnsSaasResourceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2AddOnsSaasResourceUUID(ResourceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2AddOnsSaasResourceUUIDRequest{
        ResourceUUID: "resource_uuid",
    }
client.DeleteV2AddOnsSaasResourceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2AddOnsSaasResourceUUID(ResourceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2AddOnsSaasResourceUUIDRequest{
        ResourceUUID: "resource_uuid",
    }
client.PatchV2AddOnsSaasResourceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2AddOnsSaasResourceUUIDPlan(ResourceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2AddOnsSaasResourceUUIDPlanRequest{
        ResourceUUID: "resource_uuid",
    }
client.PatchV2AddOnsSaasResourceUUIDPlan(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Apps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Apps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Apps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Apps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsIDRequest{
        ID: "id",
    }
client.GetV2AppsID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2AppsID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2AppsIDRequest{
        ID: "id",
    }
client.PutV2AppsID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2AppsID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2AppsIDRequest{
        ID: "id",
    }
client.DeleteV2AppsID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDRestart(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDRestartRequest{
        AppID: "app_id",
    }
client.PostV2AppsAppIDRestart(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDComponentsComponentNameLogs(AppID, ComponentName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDComponentsComponentNameLogsRequest{
        AppID: "app_id",
        ComponentName: "component_name",
    }
client.GetV2AppsAppIDComponentsComponentNameLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDComponentsComponentNameExec(AppID, ComponentName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDComponentsComponentNameExecRequest{
        AppID: "app_id",
        ComponentName: "component_name",
    }
client.GetV2AppsAppIDComponentsComponentNameExec(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDInstances(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDInstancesRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDInstances(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDDeployments(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDDeploymentsRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDDeployments(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDDeployments(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDDeploymentsRequest{
        AppID: "app_id",
    }
client.PostV2AppsAppIDDeployments(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDDeploymentsDeploymentID(AppID, DeploymentID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDDeploymentsDeploymentIDRequest{
        AppID: "app_id",
        DeploymentID: "deployment_id",
    }
client.GetV2AppsAppIDDeploymentsDeploymentID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDDeploymentsDeploymentIDCancel(AppID, DeploymentID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDDeploymentsDeploymentIDCancelRequest{
        AppID: "app_id",
        DeploymentID: "deployment_id",
    }
client.PostV2AppsAppIDDeploymentsDeploymentIDCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDDeploymentsDeploymentIDComponentsComponentNameLogs(AppID, DeploymentID, ComponentName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDDeploymentsDeploymentIDComponentsComponentNameLogsRequest{
        AppID: "app_id",
        DeploymentID: "deployment_id",
        ComponentName: "component_name",
    }
client.GetV2AppsAppIDDeploymentsDeploymentIDComponentsComponentNameLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDDeploymentsDeploymentIDLogs(AppID, DeploymentID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDDeploymentsDeploymentIDLogsRequest{
        AppID: "app_id",
        DeploymentID: "deployment_id",
    }
client.GetV2AppsAppIDDeploymentsDeploymentIDLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDDeploymentsDeploymentIDComponentsComponentNameExec(AppID, DeploymentID, ComponentName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDDeploymentsDeploymentIDComponentsComponentNameExecRequest{
        AppID: "app_id",
        DeploymentID: "deployment_id",
        ComponentName: "component_name",
    }
client.GetV2AppsAppIDDeploymentsDeploymentIDComponentsComponentNameExec(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDLogs(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDLogsRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDJobInvocations(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDJobInvocationsRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDJobInvocations(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDJobInvocationsJobInvocationID(AppID, JobInvocationID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDJobInvocationsJobInvocationIDRequest{
        AppID: "app_id",
        JobInvocationID: "job_invocation_id",
    }
client.GetV2AppsAppIDJobInvocationsJobInvocationID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**jobInvocationID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDJobInvocationsJobInvocationIDCancel(AppID, JobInvocationID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDJobInvocationsJobInvocationIDCancelRequest{
        AppID: "app_id",
        JobInvocationID: "job_invocation_id",
    }
client.PostV2AppsAppIDJobInvocationsJobInvocationIDCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**jobInvocationID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDJobsJobNameInvocationsJobInvocationIDLogs(AppID, JobName, JobInvocationID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDJobsJobNameInvocationsJobInvocationIDLogsRequest{
        AppID: "app_id",
        JobName: "job_name",
        JobInvocationID: "job_invocation_id",
    }
client.GetV2AppsAppIDJobsJobNameInvocationsJobInvocationIDLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**jobName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**jobInvocationID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDEvents(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDEventsRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDEvents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDEventsEventID(AppID, EventID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDEventsEventIDRequest{
        AppID: "app_id",
        EventID: "event_id",
    }
client.GetV2AppsAppIDEventsEventID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**eventID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDEventsEventIDCancel(AppID, EventID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDEventsEventIDCancelRequest{
        AppID: "app_id",
        EventID: "event_id",
    }
client.PostV2AppsAppIDEventsEventIDCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**eventID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDEventsEventIDLogs(AppID, EventID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDEventsEventIDLogsRequest{
        AppID: "app_id",
        EventID: "event_id",
    }
client.GetV2AppsAppIDEventsEventIDLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**eventID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsTiersInstanceSizes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2AppsTiersInstanceSizes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsTiersInstanceSizesSlug(Slug) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsTiersInstanceSizesSlugRequest{
        Slug: "slug",
    }
client.GetV2AppsTiersInstanceSizesSlug(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**slug:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsRegions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2AppsRegions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsPropose() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2AppsPropose(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDAlerts(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDAlertsRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDAlerts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDAlertsAlertIDDestinations(AppID, AlertID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDAlertsAlertIDDestinationsRequest{
        AppID: "app_id",
        AlertID: "alert_id",
    }
client.PostV2AppsAppIDAlertsAlertIDDestinations(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDRollback(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDRollbackRequest{
        AppID: "app_id",
    }
client.PostV2AppsAppIDRollback(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDRollbackValidate(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDRollbackValidateRequest{
        AppID: "app_id",
    }
client.PostV2AppsAppIDRollbackValidate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDRollbackCommit(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDRollbackCommitRequest{
        AppID: "app_id",
    }
client.PostV2AppsAppIDRollbackCommit(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsAppIDRollbackRevert(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2AppsAppIDRollbackRevertRequest{
        AppID: "app_id",
    }
client.PostV2AppsAppIDRollbackRevert(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDMetricsBandwidthDaily(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDMetricsBandwidthDailyRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDMetricsBandwidthDaily(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2AppsMetricsBandwidthDaily() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2AppsMetricsBandwidthDaily(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2AppsAppIDHealth(AppID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2AppsAppIDHealthRequest{
        AppID: "app_id",
    }
client.GetV2AppsAppIDHealth(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CdnEndpoints() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2CdnEndpoints(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2CdnEndpoints() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2CdnEndpoints(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CdnEndpointsCdnID(CdnID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2CdnEndpointsCdnIDRequest{
        CdnID: "cdn_id",
    }
client.GetV2CdnEndpointsCdnID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2CdnEndpointsCdnID(CdnID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2CdnEndpointsCdnIDRequest{
        CdnID: "cdn_id",
    }
client.PutV2CdnEndpointsCdnID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2CdnEndpointsCdnID(CdnID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2CdnEndpointsCdnIDRequest{
        CdnID: "cdn_id",
    }
client.DeleteV2CdnEndpointsCdnID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2CdnEndpointsCdnIDCache(CdnID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2CdnEndpointsCdnIDCacheRequest{
        CdnID: "cdn_id",
    }
client.DeleteV2CdnEndpointsCdnIDCache(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Certificates() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Certificates(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Certificates() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Certificates(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CertificatesCertificateID(CertificateID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2CertificatesCertificateIDRequest{
        CertificateID: "certificate_id",
    }
client.GetV2CertificatesCertificateID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**certificateID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2CertificatesCertificateID(CertificateID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2CertificatesCertificateIDRequest{
        CertificateID: "certificate_id",
    }
client.DeleteV2CertificatesCertificateID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**certificateID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyBalance() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2CustomersMyBalance(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyBillingHistory() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2CustomersMyBillingHistory(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyInvoices() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2CustomersMyInvoices(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyInvoicesInvoiceUUID(InvoiceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2CustomersMyInvoicesInvoiceUUIDRequest{
        InvoiceUUID: "invoice_uuid",
    }
client.GetV2CustomersMyInvoicesInvoiceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyInvoicesInvoiceUUIDCsv(InvoiceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2CustomersMyInvoicesInvoiceUUIDCsvRequest{
        InvoiceUUID: "invoice_uuid",
    }
client.GetV2CustomersMyInvoicesInvoiceUUIDCsv(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyInvoicesInvoiceUUIDPdf(InvoiceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2CustomersMyInvoicesInvoiceUUIDPdfRequest{
        InvoiceUUID: "invoice_uuid",
    }
client.GetV2CustomersMyInvoicesInvoiceUUIDPdf(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2CustomersMyInvoicesInvoiceUUIDSummary(InvoiceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2CustomersMyInvoicesInvoiceUUIDSummaryRequest{
        InvoiceUUID: "invoice_uuid",
    }
client.GetV2CustomersMyInvoicesInvoiceUUIDSummary(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2BillingAccountUrnInsightsStartDateEndDate(AccountUrn, StartDate, EndDate) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2BillingAccountUrnInsightsStartDateEndDateRequest{
        AccountUrn: "account_urn",
        StartDate: "start_date",
        EndDate: "end_date",
    }
client.GetV2BillingAccountUrnInsightsStartDateEndDate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accountUrn:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**startDate:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**endDate:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesOptions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DatabasesOptions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Databases() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Databases(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Databases() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Databases(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUID(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUID(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.DeleteV2DatabasesDatabaseClusterUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDConfig(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDConfigRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2DatabasesDatabaseClusterUUIDConfig(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2DatabasesDatabaseClusterUUIDConfigRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PatchV2DatabasesDatabaseClusterUUIDConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDCa(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDCaRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDCa(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDOnlineMigration(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDOnlineMigrationRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDOnlineMigration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDOnlineMigration(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDOnlineMigrationRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDOnlineMigration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDOnlineMigrationMigrationID(DatabaseClusterUUID, MigrationID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDOnlineMigrationMigrationIDRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        MigrationID: "migration_id",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDOnlineMigrationMigrationID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**migrationID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDMigrate(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDMigrateRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDMigrate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDResize(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDResizeRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDResize(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDFirewall(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDFirewallRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDFirewall(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDFirewall(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDFirewallRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDFirewall(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDMaintenance(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDMaintenanceRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDMaintenance(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDInstallUpdate(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDInstallUpdateRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDInstallUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDBackups(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDBackupsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDBackups(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDReplicas(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDReplicasRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDReplicas(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDReplicas(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDReplicasRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDReplicas(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDEvents(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDEventsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDEvents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDReplicasReplicaName(DatabaseClusterUUID, ReplicaName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDReplicasReplicaNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        ReplicaName: "replica_name",
    }
client.GetV2DatabasesDatabaseClusterUUIDReplicasReplicaName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**replicaName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDReplicasReplicaName(DatabaseClusterUUID, ReplicaName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDReplicasReplicaNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        ReplicaName: "replica_name",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDReplicasReplicaName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**replicaName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDReplicasReplicaNamePromote(DatabaseClusterUUID, ReplicaName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDReplicasReplicaNamePromoteRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        ReplicaName: "replica_name",
    }
client.PutV2DatabasesDatabaseClusterUUIDReplicasReplicaNamePromote(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**replicaName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDUsers(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDUsersRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDUsers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDUsers(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDUsersRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDUsers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDUsersUsername(DatabaseClusterUUID, Username) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDUsersUsernameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        Username: "username",
    }
client.GetV2DatabasesDatabaseClusterUUIDUsersUsername(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDUsersUsername(DatabaseClusterUUID, Username) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDUsersUsernameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        Username: "username",
    }
client.PutV2DatabasesDatabaseClusterUUIDUsersUsername(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDUsersUsername(DatabaseClusterUUID, Username) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDUsersUsernameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        Username: "username",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDUsersUsername(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDUsersUsernameResetAuth(DatabaseClusterUUID, Username) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDUsersUsernameResetAuthRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        Username: "username",
    }
client.PostV2DatabasesDatabaseClusterUUIDUsersUsernameResetAuth(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDDbs(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDDbsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDDbs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDDbs(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDDbsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDDbs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDDbsDatabaseName(DatabaseClusterUUID, DatabaseName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDDbsDatabaseNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        DatabaseName: "database_name",
    }
client.GetV2DatabasesDatabaseClusterUUIDDbsDatabaseName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**databaseName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDDbsDatabaseName(DatabaseClusterUUID, DatabaseName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDDbsDatabaseNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        DatabaseName: "database_name",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDDbsDatabaseName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**databaseName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDPools(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDPoolsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDPools(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDPools(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDPoolsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDPools(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDPoolsPoolName(DatabaseClusterUUID, PoolName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDPoolsPoolNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        PoolName: "pool_name",
    }
client.GetV2DatabasesDatabaseClusterUUIDPoolsPoolName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**poolName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDPoolsPoolName(DatabaseClusterUUID, PoolName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDPoolsPoolNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        PoolName: "pool_name",
    }
client.PutV2DatabasesDatabaseClusterUUIDPoolsPoolName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**poolName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDPoolsPoolName(DatabaseClusterUUID, PoolName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDPoolsPoolNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        PoolName: "pool_name",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDPoolsPoolName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**poolName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDEvictionPolicy(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDEvictionPolicyRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDEvictionPolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDEvictionPolicy(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDEvictionPolicyRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDEvictionPolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUuidSqlMode(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUuidSqlModeRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUuidSqlMode(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUuidSqlMode(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUuidSqlModeRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUuidSqlMode(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDUpgrade(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDUpgradeRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDUpgrade(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDAutoscale(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDAutoscaleRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDAutoscale(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDAutoscale(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDAutoscaleRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDAutoscale(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDTopics(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDTopicsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDTopics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDTopics(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDTopicsRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDTopics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDTopicsTopicName(DatabaseClusterUUID, TopicName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDTopicsTopicNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        TopicName: "topic_name",
    }
client.GetV2DatabasesDatabaseClusterUUIDTopicsTopicName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**topicName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDTopicsTopicName(DatabaseClusterUUID, TopicName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDTopicsTopicNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        TopicName: "topic_name",
    }
client.PutV2DatabasesDatabaseClusterUUIDTopicsTopicName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**topicName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDTopicsTopicName(DatabaseClusterUUID, TopicName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDTopicsTopicNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        TopicName: "topic_name",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDTopicsTopicName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**topicName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDLogsink(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDLogsinkRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDLogsink(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDLogsinkRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDLogsinkLogsinkID(DatabaseClusterUUID, LogsinkID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDLogsinkLogsinkIDRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        LogsinkID: "logsink_id",
    }
client.GetV2DatabasesDatabaseClusterUUIDLogsinkLogsinkID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**logsinkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDLogsinkLogsinkID(DatabaseClusterUUID, LogsinkID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDLogsinkLogsinkIDRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        LogsinkID: "logsink_id",
    }
client.PutV2DatabasesDatabaseClusterUUIDLogsinkLogsinkID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**logsinkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDLogsinkLogsinkID(DatabaseClusterUUID, LogsinkID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDLogsinkLogsinkIDRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        LogsinkID: "logsink_id",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDLogsinkLogsinkID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**logsinkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistry(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistry(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DatabasesDatabaseClusterUUIDSchemaRegistry(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DatabasesDatabaseClusterUUIDSchemaRegistryRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PostV2DatabasesDatabaseClusterUUIDSchemaRegistry(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectName(DatabaseClusterUUID, SubjectName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        SubjectName: "subject_name",
    }
client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectName(DatabaseClusterUUID, SubjectName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        SubjectName: "subject_name",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectNameVersionsVersion(DatabaseClusterUUID, SubjectName, Version) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectNameVersionsVersionRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        SubjectName: "subject_name",
        Version: "version",
    }
client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistrySubjectNameVersionsVersion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**version:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryConfig(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDSchemaRegistryConfig(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.PutV2DatabasesDatabaseClusterUUIDSchemaRegistryConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigSubjectName(DatabaseClusterUUID, SubjectName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigSubjectNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        SubjectName: "subject_name",
    }
client.GetV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigSubjectName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigSubjectName(DatabaseClusterUUID, SubjectName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigSubjectNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        SubjectName: "subject_name",
    }
client.PutV2DatabasesDatabaseClusterUUIDSchemaRegistryConfigSubjectName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesMetricsCredentials() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DatabasesMetricsCredentials(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DatabasesMetricsCredentials() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PutV2DatabasesMetricsCredentials(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DatabasesDatabaseClusterUUIDIndexes(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DatabasesDatabaseClusterUUIDIndexesRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
    }
client.GetV2DatabasesDatabaseClusterUUIDIndexes(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DatabasesDatabaseClusterUUIDIndexesIndexName(DatabaseClusterUUID, IndexName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DatabasesDatabaseClusterUUIDIndexesIndexNameRequest{
        DatabaseClusterUUID: "database_cluster_uuid",
        IndexName: "index_name",
    }
client.DeleteV2DatabasesDatabaseClusterUUIDIndexesIndexName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**indexName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesDedicatedInferenceID(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DedicatedInferencesDedicatedInferenceIDRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.GetV2DedicatedInferencesDedicatedInferenceID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DedicatedInferencesDedicatedInferenceID(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DedicatedInferencesDedicatedInferenceIDRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.DeleteV2DedicatedInferencesDedicatedInferenceID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2DedicatedInferencesDedicatedInferenceID(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2DedicatedInferencesDedicatedInferenceIDRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.PatchV2DedicatedInferencesDedicatedInferenceID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferences() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DedicatedInferences(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DedicatedInferences() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2DedicatedInferences(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesDedicatedInferenceIDAccelerators(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DedicatedInferencesDedicatedInferenceIDAcceleratorsRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.GetV2DedicatedInferencesDedicatedInferenceIDAccelerators(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesDedicatedInferenceIDAcceleratorsAcceleratorID(DedicatedInferenceID, AcceleratorID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DedicatedInferencesDedicatedInferenceIDAcceleratorsAcceleratorIDRequest{
        DedicatedInferenceID: "dedicated_inference_id",
        AcceleratorID: "accelerator_id",
    }
client.GetV2DedicatedInferencesDedicatedInferenceIDAcceleratorsAcceleratorID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**acceleratorID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesDedicatedInferenceIDCa(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DedicatedInferencesDedicatedInferenceIDCaRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.GetV2DedicatedInferencesDedicatedInferenceIDCa(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesDedicatedInferenceIDTokens(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DedicatedInferencesDedicatedInferenceIDTokensRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.GetV2DedicatedInferencesDedicatedInferenceIDTokens(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DedicatedInferencesDedicatedInferenceIDTokens(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DedicatedInferencesDedicatedInferenceIDTokensRequest{
        DedicatedInferenceID: "dedicated_inference_id",
    }
client.PostV2DedicatedInferencesDedicatedInferenceIDTokens(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DedicatedInferencesDedicatedInferenceIDTokensTokenID(DedicatedInferenceID, TokenID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DedicatedInferencesDedicatedInferenceIDTokensTokenIDRequest{
        DedicatedInferenceID: "dedicated_inference_id",
        TokenID: "token_id",
    }
client.DeleteV2DedicatedInferencesDedicatedInferenceIDTokensTokenID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**tokenID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesSizes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DedicatedInferencesSizes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DedicatedInferencesGpuModelConfig() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DedicatedInferencesGpuModelConfig(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Domains() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Domains(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Domains() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Domains(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DomainsDomainName(DomainName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DomainsDomainNameRequest{
        DomainName: "domain_name",
    }
client.GetV2DomainsDomainName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DomainsDomainName(DomainName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DomainsDomainNameRequest{
        DomainName: "domain_name",
    }
client.DeleteV2DomainsDomainName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DomainsDomainNameRecords(DomainName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DomainsDomainNameRecordsRequest{
        DomainName: "domain_name",
    }
client.GetV2DomainsDomainNameRecords(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DomainsDomainNameRecords(DomainName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DomainsDomainNameRecordsRequest{
        DomainName: "domain_name",
    }
client.PostV2DomainsDomainNameRecords(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DomainsDomainNameRecordsDomainRecordID(DomainName, DomainRecordID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DomainsDomainNameRecordsDomainRecordIDRequest{
        DomainName: "domain_name",
        DomainRecordID: "domain_record_id",
    }
client.GetV2DomainsDomainNameRecordsDomainRecordID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DomainsDomainNameRecordsDomainRecordID(DomainName, DomainRecordID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DomainsDomainNameRecordsDomainRecordIDRequest{
        DomainName: "domain_name",
        DomainRecordID: "domain_record_id",
    }
client.PutV2DomainsDomainNameRecordsDomainRecordID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DomainsDomainNameRecordsDomainRecordID(DomainName, DomainRecordID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DomainsDomainNameRecordsDomainRecordIDRequest{
        DomainName: "domain_name",
        DomainRecordID: "domain_record_id",
    }
client.DeleteV2DomainsDomainNameRecordsDomainRecordID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2DomainsDomainNameRecordsDomainRecordID(DomainName, DomainRecordID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2DomainsDomainNameRecordsDomainRecordIDRequest{
        DomainName: "domain_name",
        DomainRecordID: "domain_record_id",
    }
client.PatchV2DomainsDomainNameRecordsDomainRecordID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Droplets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Droplets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Droplets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Droplets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2Droplets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DeleteV2Droplets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletID(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DropletsDropletID(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DropletsDropletIDRequest{
        DropletID: "droplet_id",
    }
client.DeleteV2DropletsDropletID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDBackups(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDBackupsRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDBackups(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDBackupsPolicy(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDBackupsPolicyRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDBackupsPolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsBackupsPolicies() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DropletsBackupsPolicies(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsBackupsSupportedPolicies() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DropletsBackupsSupportedPolicies(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDSnapshots(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDSnapshotsRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDSnapshots(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDActions(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDActionsRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DropletsDropletIDActions(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DropletsDropletIDActionsRequest{
        DropletID: "droplet_id",
    }
client.PostV2DropletsDropletIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DropletsActions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2DropletsActions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDActionsActionID(DropletID, ActionID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDActionsActionIDRequest{
        DropletID: "droplet_id",
        ActionID: "action_id",
    }
client.GetV2DropletsDropletIDActionsActionID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDKernels(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDKernelsRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDKernels(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDFirewalls(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDFirewallsRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDFirewalls(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDNeighbors(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDNeighborsRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDNeighbors(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDDestroyWithAssociatedResources(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDDestroyWithAssociatedResourcesRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDDestroyWithAssociatedResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DropletsDropletIDDestroyWithAssociatedResourcesSelective(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DropletsDropletIDDestroyWithAssociatedResourcesSelectiveRequest{
        DropletID: "droplet_id",
    }
client.DeleteV2DropletsDropletIDDestroyWithAssociatedResourcesSelective(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DropletsDropletIDDestroyWithAssociatedResourcesDangerous(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DropletsDropletIDDestroyWithAssociatedResourcesDangerousRequest{
        DropletID: "droplet_id",
    }
client.DeleteV2DropletsDropletIDDestroyWithAssociatedResourcesDangerous(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsDropletIDDestroyWithAssociatedResourcesStatus(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsDropletIDDestroyWithAssociatedResourcesStatusRequest{
        DropletID: "droplet_id",
    }
client.GetV2DropletsDropletIDDestroyWithAssociatedResourcesStatus(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DropletsDropletIDDestroyWithAssociatedResourcesRetry(DropletID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2DropletsDropletIDDestroyWithAssociatedResourcesRetryRequest{
        DropletID: "droplet_id",
    }
client.PostV2DropletsDropletIDDestroyWithAssociatedResourcesRetry(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsAutoscale() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2DropletsAutoscale(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2DropletsAutoscale() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2DropletsAutoscale(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsAutoscaleAutoscalePoolID(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsAutoscaleAutoscalePoolIDRequest{
        AutoscalePoolID: "autoscale_pool_id",
    }
client.GetV2DropletsAutoscaleAutoscalePoolID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2DropletsAutoscaleAutoscalePoolID(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2DropletsAutoscaleAutoscalePoolIDRequest{
        AutoscalePoolID: "autoscale_pool_id",
    }
client.PutV2DropletsAutoscaleAutoscalePoolID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DropletsAutoscaleAutoscalePoolID(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DropletsAutoscaleAutoscalePoolIDRequest{
        AutoscalePoolID: "autoscale_pool_id",
    }
client.DeleteV2DropletsAutoscaleAutoscalePoolID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2DropletsAutoscaleAutoscalePoolIDDangerous(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2DropletsAutoscaleAutoscalePoolIDDangerousRequest{
        AutoscalePoolID: "autoscale_pool_id",
    }
client.DeleteV2DropletsAutoscaleAutoscalePoolIDDangerous(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsAutoscaleAutoscalePoolIDMembers(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsAutoscaleAutoscalePoolIDMembersRequest{
        AutoscalePoolID: "autoscale_pool_id",
    }
client.GetV2DropletsAutoscaleAutoscalePoolIDMembers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2DropletsAutoscaleAutoscalePoolIDHistory(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2DropletsAutoscaleAutoscalePoolIDHistoryRequest{
        AutoscalePoolID: "autoscale_pool_id",
    }
client.GetV2DropletsAutoscaleAutoscalePoolIDHistory(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Firewalls() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Firewalls(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Firewalls() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Firewalls(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FirewallsFirewallID(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FirewallsFirewallIDRequest{
        FirewallID: "firewall_id",
    }
client.GetV2FirewallsFirewallID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2FirewallsFirewallID(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2FirewallsFirewallIDRequest{
        FirewallID: "firewall_id",
    }
client.PutV2FirewallsFirewallID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FirewallsFirewallID(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FirewallsFirewallIDRequest{
        FirewallID: "firewall_id",
    }
client.DeleteV2FirewallsFirewallID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FirewallsFirewallIDDroplets(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2FirewallsFirewallIDDropletsRequest{
        FirewallID: "firewall_id",
    }
client.PostV2FirewallsFirewallIDDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FirewallsFirewallIDDroplets(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FirewallsFirewallIDDropletsRequest{
        FirewallID: "firewall_id",
    }
client.DeleteV2FirewallsFirewallIDDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FirewallsFirewallIDTags(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2FirewallsFirewallIDTagsRequest{
        FirewallID: "firewall_id",
    }
client.PostV2FirewallsFirewallIDTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FirewallsFirewallIDTags(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FirewallsFirewallIDTagsRequest{
        FirewallID: "firewall_id",
    }
client.DeleteV2FirewallsFirewallIDTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FirewallsFirewallIDRules(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2FirewallsFirewallIDRulesRequest{
        FirewallID: "firewall_id",
    }
client.PostV2FirewallsFirewallIDRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FirewallsFirewallIDRules(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FirewallsFirewallIDRulesRequest{
        FirewallID: "firewall_id",
    }
client.DeleteV2FirewallsFirewallIDRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FloatingIps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2FloatingIps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FloatingIps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2FloatingIps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FloatingIpsFloatingIP(FloatingIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FloatingIpsFloatingIPRequest{
        FloatingIP: "floating_ip",
    }
client.GetV2FloatingIpsFloatingIP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FloatingIpsFloatingIP(FloatingIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FloatingIpsFloatingIPRequest{
        FloatingIP: "floating_ip",
    }
client.DeleteV2FloatingIpsFloatingIP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FloatingIpsFloatingIPActions(FloatingIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FloatingIpsFloatingIPActionsRequest{
        FloatingIP: "floating_ip",
    }
client.GetV2FloatingIpsFloatingIPActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FloatingIpsFloatingIPActions(FloatingIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2FloatingIpsFloatingIPActionsRequest{
        FloatingIP: "floating_ip",
    }
client.PostV2FloatingIpsFloatingIPActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FloatingIpsFloatingIPActionsActionID(FloatingIP, ActionID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FloatingIpsFloatingIPActionsActionIDRequest{
        FloatingIP: "floating_ip",
        ActionID: "action_id",
    }
client.GetV2FloatingIpsFloatingIPActionsActionID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FunctionsNamespaces() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2FunctionsNamespaces(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FunctionsNamespaces() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2FunctionsNamespaces(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FunctionsNamespacesNamespaceID(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FunctionsNamespacesNamespaceIDRequest{
        NamespaceID: "namespace_id",
    }
client.GetV2FunctionsNamespacesNamespaceID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FunctionsNamespacesNamespaceID(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FunctionsNamespacesNamespaceIDRequest{
        NamespaceID: "namespace_id",
    }
client.DeleteV2FunctionsNamespacesNamespaceID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FunctionsNamespacesNamespaceIDTriggers(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FunctionsNamespacesNamespaceIDTriggersRequest{
        NamespaceID: "namespace_id",
    }
client.GetV2FunctionsNamespacesNamespaceIDTriggers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FunctionsNamespacesNamespaceIDTriggers(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2FunctionsNamespacesNamespaceIDTriggersRequest{
        NamespaceID: "namespace_id",
    }
client.PostV2FunctionsNamespacesNamespaceIDTriggers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FunctionsNamespacesNamespaceIDTriggersTriggerName(NamespaceID, TriggerName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FunctionsNamespacesNamespaceIDTriggersTriggerNameRequest{
        NamespaceID: "namespace_id",
        TriggerName: "trigger_name",
    }
client.GetV2FunctionsNamespacesNamespaceIDTriggersTriggerName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**triggerName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2FunctionsNamespacesNamespaceIDTriggersTriggerName(NamespaceID, TriggerName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2FunctionsNamespacesNamespaceIDTriggersTriggerNameRequest{
        NamespaceID: "namespace_id",
        TriggerName: "trigger_name",
    }
client.PutV2FunctionsNamespacesNamespaceIDTriggersTriggerName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**triggerName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FunctionsNamespacesNamespaceIDTriggersTriggerName(NamespaceID, TriggerName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FunctionsNamespacesNamespaceIDTriggersTriggerNameRequest{
        NamespaceID: "namespace_id",
        TriggerName: "trigger_name",
    }
client.DeleteV2FunctionsNamespacesNamespaceIDTriggersTriggerName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**triggerName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2FunctionsNamespacesNamespaceIDKeys(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2FunctionsNamespacesNamespaceIDKeysRequest{
        NamespaceID: "namespace_id",
    }
client.GetV2FunctionsNamespacesNamespaceIDKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2FunctionsNamespacesNamespaceIDKeys(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2FunctionsNamespacesNamespaceIDKeysRequest{
        NamespaceID: "namespace_id",
    }
client.PostV2FunctionsNamespacesNamespaceIDKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2FunctionsNamespacesNamespaceIDKeysKeyID(NamespaceID, KeyID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2FunctionsNamespacesNamespaceIDKeysKeyIDRequest{
        NamespaceID: "namespace_id",
        KeyID: "key_id",
    }
client.PutV2FunctionsNamespacesNamespaceIDKeysKeyID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**keyID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2FunctionsNamespacesNamespaceIDKeysKeyID(NamespaceID, KeyID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2FunctionsNamespacesNamespaceIDKeysKeyIDRequest{
        NamespaceID: "namespace_id",
        KeyID: "key_id",
    }
client.DeleteV2FunctionsNamespacesNamespaceIDKeysKeyID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**keyID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Images() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Images(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Images() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Images(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ImagesImageID(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ImagesImageIDRequest{
        ImageID: "image_id",
    }
client.GetV2ImagesImageID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2ImagesImageID(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2ImagesImageIDRequest{
        ImageID: "image_id",
    }
client.PutV2ImagesImageID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2ImagesImageID(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2ImagesImageIDRequest{
        ImageID: "image_id",
    }
client.DeleteV2ImagesImageID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ImagesImageIDAccountTransfer(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ImagesImageIDAccountTransferRequest{
        ImageID: "image_id",
    }
client.PostV2ImagesImageIDAccountTransfer(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ImagesImageIDAccountTransferAccept(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ImagesImageIDAccountTransferAcceptRequest{
        ImageID: "image_id",
    }
client.PostV2ImagesImageIDAccountTransferAccept(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ImagesImageIDAccountTransferCancel(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ImagesImageIDAccountTransferCancelRequest{
        ImageID: "image_id",
    }
client.PostV2ImagesImageIDAccountTransferCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ImagesImageIDAccountTransferDecline(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ImagesImageIDAccountTransferDeclineRequest{
        ImageID: "image_id",
    }
client.PostV2ImagesImageIDAccountTransferDecline(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ImagesImageIDActions(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ImagesImageIDActionsRequest{
        ImageID: "image_id",
    }
client.GetV2ImagesImageIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ImagesImageIDActions(ImageID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ImagesImageIDActionsRequest{
        ImageID: "image_id",
    }
client.PostV2ImagesImageIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ImagesImageIDActionsActionID(ImageID, ActionID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ImagesImageIDActionsActionIDRequest{
        ImageID: "image_id",
        ActionID: "action_id",
    }
client.GetV2ImagesImageIDActionsActionID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClusters() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2KubernetesClusters(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesClusters() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2KubernetesClusters(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterID(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2KubernetesClustersClusterID(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2KubernetesClustersClusterIDRequest{
        ClusterID: "cluster_id",
    }
client.PutV2KubernetesClustersClusterID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesClustersClusterID(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2KubernetesClustersClusterIDRequest{
        ClusterID: "cluster_id",
    }
client.DeleteV2KubernetesClustersClusterID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDDestroyWithAssociatedResources(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDDestroyWithAssociatedResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesSelective(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesSelectiveRequest{
        ClusterID: "cluster_id",
    }
client.DeleteV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesSelective(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesDangerous(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesDangerousRequest{
        ClusterID: "cluster_id",
    }
client.DeleteV2KubernetesClustersClusterIDDestroyWithAssociatedResourcesDangerous(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDKubeconfig(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDKubeconfigRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDKubeconfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDCredentials(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDCredentialsRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDCredentials(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDUpgrades(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDUpgradesRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDUpgrades(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesClustersClusterIDUpgrade(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2KubernetesClustersClusterIDUpgradeRequest{
        ClusterID: "cluster_id",
    }
client.PostV2KubernetesClustersClusterIDUpgrade(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDNodePools(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDNodePoolsRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDNodePools(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesClustersClusterIDNodePools(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2KubernetesClustersClusterIDNodePoolsRequest{
        ClusterID: "cluster_id",
    }
client.PostV2KubernetesClustersClusterIDNodePools(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDNodePoolsNodePoolID(ClusterID, NodePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDNodePoolsNodePoolIDRequest{
        ClusterID: "cluster_id",
        NodePoolID: "node_pool_id",
    }
client.GetV2KubernetesClustersClusterIDNodePoolsNodePoolID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2KubernetesClustersClusterIDNodePoolsNodePoolID(ClusterID, NodePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2KubernetesClustersClusterIDNodePoolsNodePoolIDRequest{
        ClusterID: "cluster_id",
        NodePoolID: "node_pool_id",
    }
client.PutV2KubernetesClustersClusterIDNodePoolsNodePoolID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesClustersClusterIDNodePoolsNodePoolID(ClusterID, NodePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2KubernetesClustersClusterIDNodePoolsNodePoolIDRequest{
        ClusterID: "cluster_id",
        NodePoolID: "node_pool_id",
    }
client.DeleteV2KubernetesClustersClusterIDNodePoolsNodePoolID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesClustersClusterIDNodePoolsNodePoolIDNodesNodeID(ClusterID, NodePoolID, NodeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2KubernetesClustersClusterIDNodePoolsNodePoolIDNodesNodeIDRequest{
        ClusterID: "cluster_id",
        NodePoolID: "node_pool_id",
        NodeID: "node_id",
    }
client.DeleteV2KubernetesClustersClusterIDNodePoolsNodePoolIDNodesNodeID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**nodeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesClustersClusterIDNodePoolsNodePoolIDRecycle(ClusterID, NodePoolID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2KubernetesClustersClusterIDNodePoolsNodePoolIDRecycleRequest{
        ClusterID: "cluster_id",
        NodePoolID: "node_pool_id",
    }
client.PostV2KubernetesClustersClusterIDNodePoolsNodePoolIDRecycle(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDUser(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDUserRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesOptions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2KubernetesOptions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDClusterlint(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDClusterlintRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDClusterlint(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesClustersClusterIDClusterlint(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2KubernetesClustersClusterIDClusterlintRequest{
        ClusterID: "cluster_id",
    }
client.PostV2KubernetesClustersClusterIDClusterlint(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesRegistry() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2KubernetesRegistry(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesRegistry() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DeleteV2KubernetesRegistry(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2KubernetesRegistries() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2KubernetesRegistries(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2KubernetesRegistries() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DeleteV2KubernetesRegistries(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2KubernetesClustersClusterIDStatusMessages(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2KubernetesClustersClusterIDStatusMessagesRequest{
        ClusterID: "cluster_id",
    }
client.GetV2KubernetesClustersClusterIDStatusMessages(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2LoadBalancers() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2LoadBalancers(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2LoadBalancers() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2LoadBalancers(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2LoadBalancersLbID(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2LoadBalancersLbIDRequest{
        LbID: "lb_id",
    }
client.GetV2LoadBalancersLbID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2LoadBalancersLbID(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2LoadBalancersLbIDRequest{
        LbID: "lb_id",
    }
client.PutV2LoadBalancersLbID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2LoadBalancersLbID(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2LoadBalancersLbIDRequest{
        LbID: "lb_id",
    }
client.DeleteV2LoadBalancersLbID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2LoadBalancersLbIDCache(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2LoadBalancersLbIDCacheRequest{
        LbID: "lb_id",
    }
client.DeleteV2LoadBalancersLbIDCache(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2LoadBalancersLbIDDroplets(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2LoadBalancersLbIDDropletsRequest{
        LbID: "lb_id",
    }
client.PostV2LoadBalancersLbIDDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2LoadBalancersLbIDDroplets(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2LoadBalancersLbIDDropletsRequest{
        LbID: "lb_id",
    }
client.DeleteV2LoadBalancersLbIDDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2LoadBalancersLbIDForwardingRules(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2LoadBalancersLbIDForwardingRulesRequest{
        LbID: "lb_id",
    }
client.PostV2LoadBalancersLbIDForwardingRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2LoadBalancersLbIDForwardingRules(LbID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2LoadBalancersLbIDForwardingRulesRequest{
        LbID: "lb_id",
    }
client.DeleteV2LoadBalancersLbIDForwardingRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringAlerts() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringAlerts(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2MonitoringAlerts() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2MonitoringAlerts(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringAlertsAlertUUID(AlertUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2MonitoringAlertsAlertUUIDRequest{
        AlertUUID: "alert_uuid",
    }
client.GetV2MonitoringAlertsAlertUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alertUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2MonitoringAlertsAlertUUID(AlertUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2MonitoringAlertsAlertUUIDRequest{
        AlertUUID: "alert_uuid",
    }
client.PutV2MonitoringAlertsAlertUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alertUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2MonitoringAlertsAlertUUID(AlertUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2MonitoringAlertsAlertUUIDRequest{
        AlertUUID: "alert_uuid",
    }
client.DeleteV2MonitoringAlertsAlertUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alertUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletBandwidth() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletBandwidth(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletCPU() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletCPU(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletFilesystemFree() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletFilesystemFree(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletFilesystemSize() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletFilesystemSize(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletLoad1() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletLoad1(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletLoad5() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletLoad5(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletLoad15() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletLoad15(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletMemoryCached() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletMemoryCached(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletMemoryFree() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletMemoryFree(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletMemoryTotal() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletMemoryTotal(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletMemoryAvailable() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletMemoryAvailable(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsAppsMemoryPercentage() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsAppsMemoryPercentage(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsAppsCPUPercentage() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsAppsCPUPercentage(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsAppsRestartCount() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsAppsRestartCount(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendConnectionsCurrent() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendConnectionsCurrent(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendConnectionsLimit() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendConnectionsLimit(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendCPUUtilization() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendCPUUtilization(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendFirewallDroppedBytes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendFirewallDroppedBytes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendFirewallDroppedPackets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendFirewallDroppedPackets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendHTTPResponses() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendHTTPResponses(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendHTTPRequestsPerSecond() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendHTTPRequestsPerSecond(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendNetworkThroughputHTTP() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendNetworkThroughputHTTP(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendNetworkThroughputUDP() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendNetworkThroughputUDP(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendNetworkThroughputTCP() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendNetworkThroughputTCP(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendNlbTCPNetworkThroughput() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendNlbTCPNetworkThroughput(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendNlbUDPNetworkThroughput() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendNlbUDPNetworkThroughput(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendTLSConnectionsCurrent() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendTLSConnectionsCurrent(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendTLSConnectionsLimit() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendTLSConnectionsLimit(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerFrontendTLSConnectionsExceedingRateLimit() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerFrontendTLSConnectionsExceedingRateLimit(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPSessionDurationAvg() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPSessionDurationAvg(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPSessionDuration50P() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPSessionDuration50P(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPSessionDuration95P() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPSessionDuration95P(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTimeAvg() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTimeAvg(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTime50P() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTime50P(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTime95P() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTime95P(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTime99P() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponseTime99P(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsQueueSize() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsQueueSize(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponses() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHTTPResponses(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsConnections() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsConnections(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsHealthChecks() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsHealthChecks(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsLoadBalancerDropletsDowntime() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsLoadBalancerDropletsDowntime(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletAutoscaleCurrentInstances() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletAutoscaleCurrentInstances(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletAutoscaleTargetInstances() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletAutoscaleTargetInstances(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletAutoscaleCurrentCPUUtilization() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletAutoscaleCurrentCPUUtilization(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletAutoscaleTargetCPUUtilization() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletAutoscaleTargetCPUUtilization(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletAutoscaleCurrentMemoryUtilization() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletAutoscaleCurrentMemoryUtilization(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDropletAutoscaleTargetMemoryUtilization() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDropletAutoscaleTargetMemoryUtilization(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlCPUUsage() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlCPUUsage(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlLoad() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlLoad(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlMemoryUsage() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlMemoryUsage(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlDiskUsage() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlDiskUsage(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlThreadsConnected() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlThreadsConnected(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlThreadsCreatedRate() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlThreadsCreatedRate(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlThreadsActive() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlThreadsActive(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlIndexVsSequentialReads() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlIndexVsSequentialReads(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlOpRates() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlOpRates(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlSchemaThroughput() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlSchemaThroughput(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringMetricsDatabaseMysqlSchemaLatency() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringMetricsDatabaseMysqlSchemaLatency(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringSinksDestinations() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringSinksDestinations(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2MonitoringSinksDestinations() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2MonitoringSinksDestinations(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringSinksDestinationsDestinationUUID(DestinationUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2MonitoringSinksDestinationsDestinationUUIDRequest{
        DestinationUUID: "destination_uuid",
    }
client.GetV2MonitoringSinksDestinationsDestinationUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2MonitoringSinksDestinationsDestinationUUID(DestinationUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2MonitoringSinksDestinationsDestinationUUIDRequest{
        DestinationUUID: "destination_uuid",
    }
client.PostV2MonitoringSinksDestinationsDestinationUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2MonitoringSinksDestinationsDestinationUUID(DestinationUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2MonitoringSinksDestinationsDestinationUUIDRequest{
        DestinationUUID: "destination_uuid",
    }
client.DeleteV2MonitoringSinksDestinationsDestinationUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringSinks() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2MonitoringSinks(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2MonitoringSinks() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2MonitoringSinks(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2MonitoringSinksSinkUUID(SinkUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2MonitoringSinksSinkUUIDRequest{
        SinkUUID: "sink_uuid",
    }
client.GetV2MonitoringSinksSinkUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sinkUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2MonitoringSinksSinkUUID(SinkUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2MonitoringSinksSinkUUIDRequest{
        SinkUUID: "sink_uuid",
    }
client.DeleteV2MonitoringSinksSinkUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sinkUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Nfs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Nfs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Nfs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Nfs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2NfsNfsID(NfsID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2NfsNfsIDRequest{
        NfsID: "nfs_id",
    }
client.GetV2NfsNfsID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2NfsNfsID(NfsID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2NfsNfsIDRequest{
        NfsID: "nfs_id",
    }
client.DeleteV2NfsNfsID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2NfsNfsIDActions(NfsID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2NfsNfsIDActionsRequest{
        NfsID: "nfs_id",
    }
client.PostV2NfsNfsIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2NfsSnapshots() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2NfsSnapshots(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2NfsSnapshotsNfsSnapshotID(NfsSnapshotID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2NfsSnapshotsNfsSnapshotIDRequest{
        NfsSnapshotID: "nfs_snapshot_id",
    }
client.GetV2NfsSnapshotsNfsSnapshotID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsSnapshotID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2NfsSnapshotsNfsSnapshotID(NfsSnapshotID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2NfsSnapshotsNfsSnapshotIDRequest{
        NfsSnapshotID: "nfs_snapshot_id",
    }
client.DeleteV2NfsSnapshotsNfsSnapshotID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsSnapshotID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2PartnerNetworkConnectAttachments() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2PartnerNetworkConnectAttachments(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2PartnerNetworkConnectAttachments() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2PartnerNetworkConnectAttachments(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2PartnerNetworkConnectAttachmentsPaID(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2PartnerNetworkConnectAttachmentsPaIDRequest{
        PaID: "pa_id",
    }
client.GetV2PartnerNetworkConnectAttachmentsPaID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2PartnerNetworkConnectAttachmentsPaID(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2PartnerNetworkConnectAttachmentsPaIDRequest{
        PaID: "pa_id",
    }
client.DeleteV2PartnerNetworkConnectAttachmentsPaID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2PartnerNetworkConnectAttachmentsPaID(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2PartnerNetworkConnectAttachmentsPaIDRequest{
        PaID: "pa_id",
    }
client.PatchV2PartnerNetworkConnectAttachmentsPaID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2PartnerNetworkConnectAttachmentsPaIDBgpAuthKey(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2PartnerNetworkConnectAttachmentsPaIDBgpAuthKeyRequest{
        PaID: "pa_id",
    }
client.GetV2PartnerNetworkConnectAttachmentsPaIDBgpAuthKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2PartnerNetworkConnectAttachmentsPaIDRemoteRoutes(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2PartnerNetworkConnectAttachmentsPaIDRemoteRoutesRequest{
        PaID: "pa_id",
    }
client.GetV2PartnerNetworkConnectAttachmentsPaIDRemoteRoutes(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2PartnerNetworkConnectAttachmentsPaIDServiceKey(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2PartnerNetworkConnectAttachmentsPaIDServiceKeyRequest{
        PaID: "pa_id",
    }
client.GetV2PartnerNetworkConnectAttachmentsPaIDServiceKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2PartnerNetworkConnectAttachmentsPaIDServiceKey(PaID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2PartnerNetworkConnectAttachmentsPaIDServiceKeyRequest{
        PaID: "pa_id",
    }
client.PostV2PartnerNetworkConnectAttachmentsPaIDServiceKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Projects() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Projects(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Projects() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Projects(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ProjectsDefault() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2ProjectsDefault(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2ProjectsDefault() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PutV2ProjectsDefault(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2ProjectsDefault() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PatchV2ProjectsDefault(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ProjectsProjectID(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ProjectsProjectIDRequest{
        ProjectID: "project_id",
    }
client.GetV2ProjectsProjectID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2ProjectsProjectID(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2ProjectsProjectIDRequest{
        ProjectID: "project_id",
    }
client.PutV2ProjectsProjectID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2ProjectsProjectID(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2ProjectsProjectIDRequest{
        ProjectID: "project_id",
    }
client.DeleteV2ProjectsProjectID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2ProjectsProjectID(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2ProjectsProjectIDRequest{
        ProjectID: "project_id",
    }
client.PatchV2ProjectsProjectID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ProjectsProjectIDResources(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ProjectsProjectIDResourcesRequest{
        ProjectID: "project_id",
    }
client.GetV2ProjectsProjectIDResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ProjectsProjectIDResources(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ProjectsProjectIDResourcesRequest{
        ProjectID: "project_id",
    }
client.PostV2ProjectsProjectIDResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ProjectsDefaultResources() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2ProjectsDefaultResources(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ProjectsDefaultResources() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2ProjectsDefaultResources(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Regions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Regions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Registries() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Registries(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Registries() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Registries(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryName(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistriesRegistryName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2RegistriesRegistryName(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2RegistriesRegistryNameRequest{
        RegistryName: "registry_name",
    }
client.DeleteV2RegistriesRegistryName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryNameDockerCredentials(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameDockerCredentialsRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistriesRegistryNameDockerCredentials(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesSubscription() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2RegistriesSubscription(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2RegistriesSubscription() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2RegistriesSubscription(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesOptions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2RegistriesOptions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryNameGarbageCollection(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameGarbageCollectionRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistriesRegistryNameGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2RegistriesRegistryNameGarbageCollection(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2RegistriesRegistryNameGarbageCollectionRequest{
        RegistryName: "registry_name",
    }
client.PostV2RegistriesRegistryNameGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryNameGarbageCollections(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameGarbageCollectionsRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistriesRegistryNameGarbageCollections(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2RegistriesRegistryNameGarbageCollectionGarbageCollectionUUID(RegistryName, GarbageCollectionUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2RegistriesRegistryNameGarbageCollectionGarbageCollectionUUIDRequest{
        RegistryName: "registry_name",
        GarbageCollectionUUID: "garbage_collection_uuid",
    }
client.PutV2RegistriesRegistryNameGarbageCollectionGarbageCollectionUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**garbageCollectionUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryNameRepositoriesV2(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameRepositoriesV2Request{
        RegistryName: "registry_name",
    }
client.GetV2RegistriesRegistryNameRepositoriesV2(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2RegistriesRegistryNameRepositoriesRepositoryName(RegistryName, RepositoryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
    }
client.DeleteV2RegistriesRegistryNameRepositoriesRepositoryName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryNameRepositoriesRepositoryNameTags(RegistryName, RepositoryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameRepositoriesRepositoryNameTagsRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
    }
client.GetV2RegistriesRegistryNameRepositoriesRepositoryNameTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameTagsRepositoryTag(RegistryName, RepositoryName, RepositoryTag) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameTagsRepositoryTagRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
        RepositoryTag: "repository_tag",
    }
client.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameTagsRepositoryTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryTag:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistriesRegistryNameRepositoriesRepositoryNameDigests(RegistryName, RepositoryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistriesRegistryNameRepositoriesRepositoryNameDigestsRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
    }
client.GetV2RegistriesRegistryNameRepositoriesRepositoryNameDigests(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameDigestsManifestDigest(RegistryName, RepositoryName, ManifestDigest) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameDigestsManifestDigestRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
        ManifestDigest: "manifest_digest",
    }
client.DeleteV2RegistriesRegistryNameRepositoriesRepositoryNameDigestsManifestDigest(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**manifestDigest:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2RegistriesValidateName() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2RegistriesValidateName(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Registry() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Registry(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Registry() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Registry(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2Registry() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DeleteV2Registry(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistrySubscription() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2RegistrySubscription(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2RegistrySubscription() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2RegistrySubscription(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryDockerCredentials() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2RegistryDockerCredentials(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2RegistryValidateName() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2RegistryValidateName(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryRegistryNameRepositories(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistryRegistryNameRepositoriesRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistryRegistryNameRepositories(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryRegistryNameRepositoriesV2(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistryRegistryNameRepositoriesV2Request{
        RegistryName: "registry_name",
    }
client.GetV2RegistryRegistryNameRepositoriesV2(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryRegistryNameRepositoriesRepositoryNameTags(RegistryName, RepositoryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistryRegistryNameRepositoriesRepositoryNameTagsRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
    }
client.GetV2RegistryRegistryNameRepositoriesRepositoryNameTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2RegistryRegistryNameRepositoriesRepositoryNameTagsRepositoryTag(RegistryName, RepositoryName, RepositoryTag) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2RegistryRegistryNameRepositoriesRepositoryNameTagsRepositoryTagRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
        RepositoryTag: "repository_tag",
    }
client.DeleteV2RegistryRegistryNameRepositoriesRepositoryNameTagsRepositoryTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryTag:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryRegistryNameRepositoriesRepositoryNameDigests(RegistryName, RepositoryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistryRegistryNameRepositoriesRepositoryNameDigestsRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
    }
client.GetV2RegistryRegistryNameRepositoriesRepositoryNameDigests(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2RegistryRegistryNameRepositoriesRepositoryNameDigestsManifestDigest(RegistryName, RepositoryName, ManifestDigest) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2RegistryRegistryNameRepositoriesRepositoryNameDigestsManifestDigestRequest{
        RegistryName: "registry_name",
        RepositoryName: "repository_name",
        ManifestDigest: "manifest_digest",
    }
client.DeleteV2RegistryRegistryNameRepositoriesRepositoryNameDigestsManifestDigest(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**manifestDigest:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryRegistryNameGarbageCollection(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistryRegistryNameGarbageCollectionRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistryRegistryNameGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2RegistryRegistryNameGarbageCollection(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2RegistryRegistryNameGarbageCollectionRequest{
        RegistryName: "registry_name",
    }
client.PostV2RegistryRegistryNameGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryRegistryNameGarbageCollections(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2RegistryRegistryNameGarbageCollectionsRequest{
        RegistryName: "registry_name",
    }
client.GetV2RegistryRegistryNameGarbageCollections(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2RegistryRegistryNameGarbageCollectionGarbageCollectionUUID(RegistryName, GarbageCollectionUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2RegistryRegistryNameGarbageCollectionGarbageCollectionUUIDRequest{
        RegistryName: "registry_name",
        GarbageCollectionUUID: "garbage_collection_uuid",
    }
client.PutV2RegistryRegistryNameGarbageCollectionGarbageCollectionUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**garbageCollectionUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2RegistryOptions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2RegistryOptions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReportsDropletNeighborsIDs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2ReportsDropletNeighborsIDs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReservedIps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2ReservedIps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ReservedIps() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2ReservedIps(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReservedIpsReservedIP(ReservedIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ReservedIpsReservedIPRequest{
        ReservedIP: "reserved_ip",
    }
client.GetV2ReservedIpsReservedIP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2ReservedIpsReservedIP(ReservedIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2ReservedIpsReservedIPRequest{
        ReservedIP: "reserved_ip",
    }
client.DeleteV2ReservedIpsReservedIP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReservedIpsReservedIPActions(ReservedIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ReservedIpsReservedIPActionsRequest{
        ReservedIP: "reserved_ip",
    }
client.GetV2ReservedIpsReservedIPActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ReservedIpsReservedIPActions(ReservedIP) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ReservedIpsReservedIPActionsRequest{
        ReservedIP: "reserved_ip",
    }
client.PostV2ReservedIpsReservedIPActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReservedIpsReservedIPActionsActionID(ReservedIP, ActionID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ReservedIpsReservedIPActionsActionIDRequest{
        ReservedIP: "reserved_ip",
        ActionID: "action_id",
    }
client.GetV2ReservedIpsReservedIPActionsActionID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReservedIpv6() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2ReservedIpv6(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ReservedIpv6() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2ReservedIpv6(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ReservedIpv6ReservedIpv6(ReservedIpv6) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ReservedIpv6ReservedIpv6Request{
        ReservedIpv6: "reserved_ipv6",
    }
client.GetV2ReservedIpv6ReservedIpv6(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIpv6:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2ReservedIpv6ReservedIpv6(ReservedIpv6) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2ReservedIpv6ReservedIpv6Request{
        ReservedIpv6: "reserved_ipv6",
    }
client.DeleteV2ReservedIpv6ReservedIpv6(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIpv6:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ReservedIpv6ReservedIpv6Actions(ReservedIpv6) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2ReservedIpv6ReservedIpv6ActionsRequest{
        ReservedIpv6: "reserved_ipv6",
    }
client.PostV2ReservedIpv6ReservedIpv6Actions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIpv6:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ByoipPrefixes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2ByoipPrefixes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2ByoipPrefixes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2ByoipPrefixes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ByoipPrefixesByoipPrefixUUID(ByoipPrefixUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ByoipPrefixesByoipPrefixUUIDRequest{
        ByoipPrefixUUID: "byoip_prefix_uuid",
    }
client.GetV2ByoipPrefixesByoipPrefixUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2ByoipPrefixesByoipPrefixUUID(ByoipPrefixUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2ByoipPrefixesByoipPrefixUUIDRequest{
        ByoipPrefixUUID: "byoip_prefix_uuid",
    }
client.DeleteV2ByoipPrefixesByoipPrefixUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2ByoipPrefixesByoipPrefixUUID(ByoipPrefixUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2ByoipPrefixesByoipPrefixUUIDRequest{
        ByoipPrefixUUID: "byoip_prefix_uuid",
    }
client.PatchV2ByoipPrefixesByoipPrefixUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2ByoipPrefixesByoipPrefixUUIDIps(ByoipPrefixUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2ByoipPrefixesByoipPrefixUUIDIpsRequest{
        ByoipPrefixUUID: "byoip_prefix_uuid",
    }
client.GetV2ByoipPrefixesByoipPrefixUUIDIps(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SecurityScans() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2SecurityScans(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2SecurityScans() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2SecurityScans(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SecurityScansScanID(ScanID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2SecurityScansScanIDRequest{
        ScanID: "scan_id",
    }
client.GetV2SecurityScansScanID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**scanID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SecurityScansLatest() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2SecurityScansLatest(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2SecurityScansRules() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2SecurityScansRules(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SecurityScansScanIDFindingsFindingUUIDAffectedResources(ScanID, FindingUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2SecurityScansScanIDFindingsFindingUUIDAffectedResourcesRequest{
        ScanID: "scan_id",
        FindingUUID: "finding_uuid",
    }
client.GetV2SecurityScansScanIDFindingsFindingUUIDAffectedResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**scanID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**findingUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SecuritySettings() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2SecuritySettings(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2SecuritySettingsPlan() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PutV2SecuritySettingsPlan(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2SecuritySettingsSuppressions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2SecuritySettingsSuppressions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2SecuritySettingsSuppressionsSuppressionUUID(SuppressionUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2SecuritySettingsSuppressionsSuppressionUUIDRequest{
        SuppressionUUID: "suppression_uuid",
    }
client.DeleteV2SecuritySettingsSuppressionsSuppressionUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**suppressionUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Sizes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Sizes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Snapshots() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Snapshots(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SnapshotsSnapshotID(SnapshotID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2SnapshotsSnapshotIDRequest{
        SnapshotID: "snapshot_id",
    }
client.GetV2SnapshotsSnapshotID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2SnapshotsSnapshotID(SnapshotID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2SnapshotsSnapshotIDRequest{
        SnapshotID: "snapshot_id",
    }
client.DeleteV2SnapshotsSnapshotID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SpacesKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2SpacesKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2SpacesKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2SpacesKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2SpacesKeysAccessKey(AccessKey) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2SpacesKeysAccessKeyRequest{
        AccessKey: "access_key",
    }
client.GetV2SpacesKeysAccessKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2SpacesKeysAccessKey(AccessKey) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2SpacesKeysAccessKeyRequest{
        AccessKey: "access_key",
    }
client.PutV2SpacesKeysAccessKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2SpacesKeysAccessKey(AccessKey) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2SpacesKeysAccessKeyRequest{
        AccessKey: "access_key",
    }
client.DeleteV2SpacesKeysAccessKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2SpacesKeysAccessKey(AccessKey) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2SpacesKeysAccessKeyRequest{
        AccessKey: "access_key",
    }
client.PatchV2SpacesKeysAccessKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Tags() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Tags(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Tags() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Tags(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2TagsTagID(TagID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2TagsTagIDRequest{
        TagID: "tag_id",
    }
client.GetV2TagsTagID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2TagsTagID(TagID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2TagsTagIDRequest{
        TagID: "tag_id",
    }
client.DeleteV2TagsTagID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2TagsTagIDResources(TagID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2TagsTagIDResourcesRequest{
        TagID: "tag_id",
    }
client.PostV2TagsTagIDResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2TagsTagIDResources(TagID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2TagsTagIDResourcesRequest{
        TagID: "tag_id",
    }
client.DeleteV2TagsTagIDResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Volumes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Volumes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Volumes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Volumes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2Volumes() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DeleteV2Volumes(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2VolumesActions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2VolumesActions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VolumesSnapshotsSnapshotID(SnapshotID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VolumesSnapshotsSnapshotIDRequest{
        SnapshotID: "snapshot_id",
    }
client.GetV2VolumesSnapshotsSnapshotID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2VolumesSnapshotsSnapshotID(SnapshotID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2VolumesSnapshotsSnapshotIDRequest{
        SnapshotID: "snapshot_id",
    }
client.DeleteV2VolumesSnapshotsSnapshotID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VolumesVolumeID(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VolumesVolumeIDRequest{
        VolumeID: "volume_id",
    }
client.GetV2VolumesVolumeID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2VolumesVolumeID(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2VolumesVolumeIDRequest{
        VolumeID: "volume_id",
    }
client.DeleteV2VolumesVolumeID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VolumesVolumeIDActions(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VolumesVolumeIDActionsRequest{
        VolumeID: "volume_id",
    }
client.GetV2VolumesVolumeIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2VolumesVolumeIDActions(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2VolumesVolumeIDActionsRequest{
        VolumeID: "volume_id",
    }
client.PostV2VolumesVolumeIDActions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VolumesVolumeIDActionsActionID(VolumeID, ActionID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VolumesVolumeIDActionsActionIDRequest{
        VolumeID: "volume_id",
        ActionID: "action_id",
    }
client.GetV2VolumesVolumeIDActionsActionID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VolumesVolumeIDSnapshots(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VolumesVolumeIDSnapshotsRequest{
        VolumeID: "volume_id",
    }
client.GetV2VolumesVolumeIDSnapshots(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2VolumesVolumeIDSnapshots(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2VolumesVolumeIDSnapshotsRequest{
        VolumeID: "volume_id",
    }
client.PostV2VolumesVolumeIDSnapshots(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2Vpcs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2Vpcs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2Vpcs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2Vpcs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcsVpcID(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VpcsVpcIDRequest{
        VpcID: "vpc_id",
    }
client.GetV2VpcsVpcID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2VpcsVpcID(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2VpcsVpcIDRequest{
        VpcID: "vpc_id",
    }
client.PutV2VpcsVpcID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2VpcsVpcID(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2VpcsVpcIDRequest{
        VpcID: "vpc_id",
    }
client.DeleteV2VpcsVpcID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2VpcsVpcID(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2VpcsVpcIDRequest{
        VpcID: "vpc_id",
    }
client.PatchV2VpcsVpcID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcsVpcIDMembers(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VpcsVpcIDMembersRequest{
        VpcID: "vpc_id",
    }
client.GetV2VpcsVpcIDMembers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcsVpcIDPeerings(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VpcsVpcIDPeeringsRequest{
        VpcID: "vpc_id",
    }
client.GetV2VpcsVpcIDPeerings(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2VpcsVpcIDPeerings(VpcID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2VpcsVpcIDPeeringsRequest{
        VpcID: "vpc_id",
    }
client.PostV2VpcsVpcIDPeerings(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2VpcsVpcIDPeeringsVpcPeeringID(VpcID, VpcPeeringID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2VpcsVpcIDPeeringsVpcPeeringIDRequest{
        VpcID: "vpc_id",
        VpcPeeringID: "vpc_peering_id",
    }
client.PatchV2VpcsVpcIDPeeringsVpcPeeringID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**vpcPeeringID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcPeerings() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2VpcPeerings(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2VpcPeerings() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2VpcPeerings(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcPeeringsVpcPeeringID(VpcPeeringID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VpcPeeringsVpcPeeringIDRequest{
        VpcPeeringID: "vpc_peering_id",
    }
client.GetV2VpcPeeringsVpcPeeringID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcPeeringID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2VpcPeeringsVpcPeeringID(VpcPeeringID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2VpcPeeringsVpcPeeringIDRequest{
        VpcPeeringID: "vpc_peering_id",
    }
client.DeleteV2VpcPeeringsVpcPeeringID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcPeeringID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2VpcPeeringsVpcPeeringID(VpcPeeringID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2VpcPeeringsVpcPeeringIDRequest{
        VpcPeeringID: "vpc_peering_id",
    }
client.PatchV2VpcPeeringsVpcPeeringID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcPeeringID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcNatGateways() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2VpcNatGateways(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2VpcNatGateways() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2VpcNatGateways(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2VpcNatGatewaysID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2VpcNatGatewaysIDRequest{
        ID: "id",
    }
client.GetV2VpcNatGatewaysID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2VpcNatGatewaysID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2VpcNatGatewaysIDRequest{
        ID: "id",
    }
client.PutV2VpcNatGatewaysID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2VpcNatGatewaysID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2VpcNatGatewaysIDRequest{
        ID: "id",
    }
client.DeleteV2VpcNatGatewaysID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2UptimeChecks() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2UptimeChecks(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2UptimeChecks() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2UptimeChecks(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2UptimeChecksCheckID(CheckID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2UptimeChecksCheckIDRequest{
        CheckID: "check_id",
    }
client.GetV2UptimeChecksCheckID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2UptimeChecksCheckID(CheckID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2UptimeChecksCheckIDRequest{
        CheckID: "check_id",
    }
client.PutV2UptimeChecksCheckID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2UptimeChecksCheckID(CheckID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2UptimeChecksCheckIDRequest{
        CheckID: "check_id",
    }
client.DeleteV2UptimeChecksCheckID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2UptimeChecksCheckIDState(CheckID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2UptimeChecksCheckIDStateRequest{
        CheckID: "check_id",
    }
client.GetV2UptimeChecksCheckIDState(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2UptimeChecksCheckIDAlerts(CheckID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2UptimeChecksCheckIDAlertsRequest{
        CheckID: "check_id",
    }
client.GetV2UptimeChecksCheckIDAlerts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2UptimeChecksCheckIDAlerts(CheckID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2UptimeChecksCheckIDAlertsRequest{
        CheckID: "check_id",
    }
client.PostV2UptimeChecksCheckIDAlerts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2UptimeChecksCheckIDAlertsAlertID(CheckID, AlertID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2UptimeChecksCheckIDAlertsAlertIDRequest{
        CheckID: "check_id",
        AlertID: "alert_id",
    }
client.GetV2UptimeChecksCheckIDAlertsAlertID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2UptimeChecksCheckIDAlertsAlertID(CheckID, AlertID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2UptimeChecksCheckIDAlertsAlertIDRequest{
        CheckID: "check_id",
        AlertID: "alert_id",
    }
client.PutV2UptimeChecksCheckIDAlertsAlertID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2UptimeChecksCheckIDAlertsAlertID(CheckID, AlertID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2UptimeChecksCheckIDAlertsAlertIDRequest{
        CheckID: "check_id",
        AlertID: "alert_id",
    }
client.DeleteV2UptimeChecksCheckIDAlertsAlertID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAgents() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiAgents(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgents() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiAgents(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAgentsAgentUuidApiKeys(AgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAgentsAgentUuidApiKeysRequest{
        AgentUUID: "agent_uuid",
    }
client.GetV2GenAiAgentsAgentUuidApiKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgentsAgentUuidApiKeys(AgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiAgentsAgentUuidApiKeysRequest{
        AgentUUID: "agent_uuid",
    }
client.PostV2GenAiAgentsAgentUuidApiKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsAgentUuidApiKeysApiKeyUuid(AgentUUID, APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsAgentUuidApiKeysApiKeyUuidRequest{
        AgentUUID: "agent_uuid",
        APIKeyUUID: "api_key_uuid",
    }
client.PutV2GenAiAgentsAgentUuidApiKeysApiKeyUuid(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAgentsAgentUuidApiKeysApiKeyUuid(AgentUUID, APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAgentsAgentUuidApiKeysApiKeyUuidRequest{
        AgentUUID: "agent_uuid",
        APIKeyUUID: "api_key_uuid",
    }
client.DeleteV2GenAiAgentsAgentUuidApiKeysApiKeyUuid(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsAgentUuidApiKeysApiKeyUuidRegenerate(AgentUUID, APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsAgentUuidApiKeysApiKeyUuidRegenerateRequest{
        AgentUUID: "agent_uuid",
        APIKeyUUID: "api_key_uuid",
    }
client.PutV2GenAiAgentsAgentUuidApiKeysApiKeyUuidRegenerate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgentsAgentUUIDFunctions(AgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiAgentsAgentUUIDFunctionsRequest{
        AgentUUID: "agent_uuid",
    }
client.PostV2GenAiAgentsAgentUUIDFunctions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsAgentUUIDFunctionsFunctionUUID(AgentUUID, FunctionUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsAgentUUIDFunctionsFunctionUUIDRequest{
        AgentUUID: "agent_uuid",
        FunctionUUID: "function_uuid",
    }
client.PutV2GenAiAgentsAgentUUIDFunctionsFunctionUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**functionUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAgentsAgentUUIDFunctionsFunctionUUID(AgentUUID, FunctionUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAgentsAgentUUIDFunctionsFunctionUUIDRequest{
        AgentUUID: "agent_uuid",
        FunctionUUID: "function_uuid",
    }
client.DeleteV2GenAiAgentsAgentUUIDFunctionsFunctionUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**functionUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgentsAgentUUIDGuardrails(AgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiAgentsAgentUUIDGuardrailsRequest{
        AgentUUID: "agent_uuid",
    }
client.PostV2GenAiAgentsAgentUUIDGuardrails(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAgentsAgentUUIDGuardrailsGuardrailUUID(AgentUUID, GuardrailUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAgentsAgentUUIDGuardrailsGuardrailUUIDRequest{
        AgentUUID: "agent_uuid",
        GuardrailUUID: "guardrail_uuid",
    }
client.DeleteV2GenAiAgentsAgentUUIDGuardrailsGuardrailUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**guardrailUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgentsAgentUUIDKnowledgeBases(AgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiAgentsAgentUUIDKnowledgeBasesRequest{
        AgentUUID: "agent_uuid",
    }
client.PostV2GenAiAgentsAgentUUIDKnowledgeBases(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgentsAgentUUIDKnowledgeBasesKnowledgeBaseUUID(AgentUUID, KnowledgeBaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiAgentsAgentUUIDKnowledgeBasesKnowledgeBaseUUIDRequest{
        AgentUUID: "agent_uuid",
        KnowledgeBaseUUID: "knowledge_base_uuid",
    }
client.PostV2GenAiAgentsAgentUUIDKnowledgeBasesKnowledgeBaseUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAgentsAgentUUIDKnowledgeBasesKnowledgeBaseUUID(AgentUUID, KnowledgeBaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAgentsAgentUUIDKnowledgeBasesKnowledgeBaseUUIDRequest{
        AgentUUID: "agent_uuid",
        KnowledgeBaseUUID: "knowledge_base_uuid",
    }
client.DeleteV2GenAiAgentsAgentUUIDKnowledgeBasesKnowledgeBaseUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUID(ParentAgentUUID, ChildAgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUIDRequest{
        ParentAgentUUID: "parent_agent_uuid",
        ChildAgentUUID: "child_agent_uuid",
    }
client.PostV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**parentAgentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**childAgentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUID(ParentAgentUUID, ChildAgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUIDRequest{
        ParentAgentUUID: "parent_agent_uuid",
        ChildAgentUUID: "child_agent_uuid",
    }
client.PutV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**parentAgentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**childAgentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUID(ParentAgentUUID, ChildAgentUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUIDRequest{
        ParentAgentUUID: "parent_agent_uuid",
        ChildAgentUUID: "child_agent_uuid",
    }
client.DeleteV2GenAiAgentsParentAgentUUIDChildAgentsChildAgentUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**parentAgentUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**childAgentUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAgentsUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAgentsUUIDRequest{
        UUID: "uuid",
    }
client.GetV2GenAiAgentsUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsUUIDRequest{
        UUID: "uuid",
    }
client.PutV2GenAiAgentsUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAgentsUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAgentsUUIDRequest{
        UUID: "uuid",
    }
client.DeleteV2GenAiAgentsUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAgentsUUIDChildAgents(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAgentsUUIDChildAgentsRequest{
        UUID: "uuid",
    }
client.GetV2GenAiAgentsUUIDChildAgents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsUUIDDeploymentVisibility(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsUUIDDeploymentVisibilityRequest{
        UUID: "uuid",
    }
client.PutV2GenAiAgentsUUIDDeploymentVisibility(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAgentsUUIDUsage(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAgentsUUIDUsageRequest{
        UUID: "uuid",
    }
client.GetV2GenAiAgentsUUIDUsage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAgentsUUIDVersions(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAgentsUUIDVersionsRequest{
        UUID: "uuid",
    }
client.GetV2GenAiAgentsUUIDVersions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAgentsUUIDVersions(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAgentsUUIDVersionsRequest{
        UUID: "uuid",
    }
client.PutV2GenAiAgentsUUIDVersions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAnthropicKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiAnthropicKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiAnthropicKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiAnthropicKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAnthropicKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAnthropicKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.GetV2GenAiAnthropicKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiAnthropicKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiAnthropicKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.PutV2GenAiAnthropicKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiAnthropicKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiAnthropicKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.DeleteV2GenAiAnthropicKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiAnthropicKeysUUIDAgents(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiAnthropicKeysUUIDAgentsRequest{
        UUID: "uuid",
    }
client.GetV2GenAiAnthropicKeysUUIDAgents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiCustomModels() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiCustomModels(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiCustomModelsImport() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiCustomModelsImport(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiCustomModelsUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiCustomModelsUUIDRequest{
        UUID: "uuid",
    }
client.GetV2GenAiCustomModelsUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiCustomModelsUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiCustomModelsUUIDRequest{
        UUID: "uuid",
    }
client.DeleteV2GenAiCustomModelsUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PatchV2GenAiCustomModelsUUIDMetadata(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PatchV2GenAiCustomModelsUUIDMetadataRequest{
        UUID: "uuid",
    }
client.PatchV2GenAiCustomModelsUUIDMetadata(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationDatasets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiEvaluationDatasets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiEvaluationDatasets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiEvaluationDatasets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiEvaluationDatasetsFileUploadPresignedURLs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiEvaluationDatasetsFileUploadPresignedURLs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationDatasetsDatasetUUIDDownloadURL(DatasetUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiEvaluationDatasetsDatasetUUIDDownloadURLRequest{
        DatasetUUID: "dataset_uuid",
    }
client.GetV2GenAiEvaluationDatasetsDatasetUUIDDownloadURL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**datasetUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationMetrics() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiEvaluationMetrics(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiEvaluationRuns() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiEvaluationRuns(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationRunsEvaluationRunUUID(EvaluationRunUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiEvaluationRunsEvaluationRunUUIDRequest{
        EvaluationRunUUID: "evaluation_run_uuid",
    }
client.GetV2GenAiEvaluationRunsEvaluationRunUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationRunUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationRunsEvaluationRunUUIDResults(EvaluationRunUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiEvaluationRunsEvaluationRunUUIDResultsRequest{
        EvaluationRunUUID: "evaluation_run_uuid",
    }
client.GetV2GenAiEvaluationRunsEvaluationRunUUIDResults(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationRunUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationRunsEvaluationRunUUIDResultsPromptID(EvaluationRunUUID, PromptID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiEvaluationRunsEvaluationRunUUIDResultsPromptIDRequest{
        EvaluationRunUUID: "evaluation_run_uuid",
        PromptID: "prompt_id",
    }
client.GetV2GenAiEvaluationRunsEvaluationRunUUIDResultsPromptID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationRunUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationTestCases() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiEvaluationTestCases(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiEvaluationTestCases() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiEvaluationTestCases(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationTestCasesEvaluationTestCaseUUIDEvaluationRuns(EvaluationTestCaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiEvaluationTestCasesEvaluationTestCaseUUIDEvaluationRunsRequest{
        EvaluationTestCaseUUID: "evaluation_test_case_uuid",
    }
client.GetV2GenAiEvaluationTestCasesEvaluationTestCaseUUIDEvaluationRuns(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationTestCaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiEvaluationTestCasesTestCaseUUID(TestCaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiEvaluationTestCasesTestCaseUUIDRequest{
        TestCaseUUID: "test_case_uuid",
    }
client.GetV2GenAiEvaluationTestCasesTestCaseUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**testCaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiEvaluationTestCasesTestCaseUUID(TestCaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiEvaluationTestCasesTestCaseUUIDRequest{
        TestCaseUUID: "test_case_uuid",
    }
client.PutV2GenAiEvaluationTestCasesTestCaseUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**testCaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiIndexingJobs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiIndexingJobs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiIndexingJobs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiIndexingJobs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiIndexingJobsIndexingJobUUIDDataSources(IndexingJobUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiIndexingJobsIndexingJobUUIDDataSourcesRequest{
        IndexingJobUUID: "indexing_job_uuid",
    }
client.GetV2GenAiIndexingJobsIndexingJobUUIDDataSources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**indexingJobUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiIndexingJobsIndexingJobUUIDDetailsSignedURL(IndexingJobUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiIndexingJobsIndexingJobUUIDDetailsSignedURLRequest{
        IndexingJobUUID: "indexing_job_uuid",
    }
client.GetV2GenAiIndexingJobsIndexingJobUUIDDetailsSignedURL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**indexingJobUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiIndexingJobsUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiIndexingJobsUUIDRequest{
        UUID: "uuid",
    }
client.GetV2GenAiIndexingJobsUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiIndexingJobsUUIDCancel(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiIndexingJobsUUIDCancelRequest{
        UUID: "uuid",
    }
client.PutV2GenAiIndexingJobsUUIDCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiKnowledgeBases() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiKnowledgeBases(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiKnowledgeBases() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiKnowledgeBases(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiKnowledgeBasesDataSourcesFileUploadPresignedURLs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiKnowledgeBasesDataSourcesFileUploadPresignedURLs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSources(KnowledgeBaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesRequest{
        KnowledgeBaseUUID: "knowledge_base_uuid",
    }
client.GetV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSources(KnowledgeBaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesRequest{
        KnowledgeBaseUUID: "knowledge_base_uuid",
    }
client.PostV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesDataSourceUUID(KnowledgeBaseUUID, DataSourceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesDataSourceUUIDRequest{
        KnowledgeBaseUUID: "knowledge_base_uuid",
        DataSourceUUID: "data_source_uuid",
    }
client.PutV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesDataSourceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**dataSourceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesDataSourceUUID(KnowledgeBaseUUID, DataSourceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesDataSourceUUIDRequest{
        KnowledgeBaseUUID: "knowledge_base_uuid",
        DataSourceUUID: "data_source_uuid",
    }
client.DeleteV2GenAiKnowledgeBasesKnowledgeBaseUUIDDataSourcesDataSourceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**dataSourceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiKnowledgeBasesKnowledgeBaseUUIDIndexingJobs(KnowledgeBaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiKnowledgeBasesKnowledgeBaseUUIDIndexingJobsRequest{
        KnowledgeBaseUUID: "knowledge_base_uuid",
    }
client.GetV2GenAiKnowledgeBasesKnowledgeBaseUUIDIndexingJobs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiKnowledgeBasesUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiKnowledgeBasesUUIDRequest{
        UUID: "uuid",
    }
client.GetV2GenAiKnowledgeBasesUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiKnowledgeBasesUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiKnowledgeBasesUUIDRequest{
        UUID: "uuid",
    }
client.PutV2GenAiKnowledgeBasesUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiKnowledgeBasesUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiKnowledgeBasesUUIDRequest{
        UUID: "uuid",
    }
client.DeleteV2GenAiKnowledgeBasesUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiModelEvaluationDatasetsFileUploadPresignedURLs() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiModelEvaluationDatasetsFileUploadPresignedURLs(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelEvaluationMetrics() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelEvaluationMetrics(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelEvaluationPresets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelEvaluationPresets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelEvaluationPresetsEvalPresetUUID(EvalPresetUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiModelEvaluationPresetsEvalPresetUUIDRequest{
        EvalPresetUUID: "eval_preset_uuid",
    }
client.GetV2GenAiModelEvaluationPresetsEvalPresetUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalPresetUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiModelEvaluationPresetsEvalPresetUUID(EvalPresetUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiModelEvaluationPresetsEvalPresetUUIDRequest{
        EvalPresetUUID: "eval_preset_uuid",
    }
client.DeleteV2GenAiModelEvaluationPresetsEvalPresetUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalPresetUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelEvaluationRuns() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelEvaluationRuns(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiModelEvaluationRuns() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiModelEvaluationRuns(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelEvaluationRunsEvalRunUUID(EvalRunUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiModelEvaluationRunsEvalRunUUIDRequest{
        EvalRunUUID: "eval_run_uuid",
    }
client.GetV2GenAiModelEvaluationRunsEvalRunUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalRunUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiModelEvaluationRunsEvalRunUUID(EvalRunUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiModelEvaluationRunsEvalRunUUIDRequest{
        EvalRunUUID: "eval_run_uuid",
    }
client.DeleteV2GenAiModelEvaluationRunsEvalRunUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalRunUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiModelEvaluationRunsEvalRunUUIDCancel(EvalRunUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiModelEvaluationRunsEvalRunUUIDCancelRequest{
        EvalRunUUID: "eval_run_uuid",
    }
client.PutV2GenAiModelEvaluationRunsEvalRunUUIDCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalRunUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelEvaluationRunsEvalRunUUIDResultsDownloadURL(EvalRunUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiModelEvaluationRunsEvalRunUUIDResultsDownloadURLRequest{
        EvalRunUUID: "eval_run_uuid",
    }
client.GetV2GenAiModelEvaluationRunsEvalRunUUIDResultsDownloadURL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalRunUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModels() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModels(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsAPIKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelsAPIKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiModelsAPIKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiModelsAPIKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiModelsAPIKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiModelsAPIKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.PutV2GenAiModelsAPIKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiModelsAPIKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiModelsAPIKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.DeleteV2GenAiModelsAPIKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiModelsAPIKeysAPIKeyUUIDRegenerate(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiModelsAPIKeysAPIKeyUUIDRegenerateRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.PutV2GenAiModelsAPIKeysAPIKeyUUIDRegenerate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsCatalog() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelsCatalog(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsCatalogID(ID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiModelsCatalogIDRequest{
        ID: "id",
    }
client.GetV2GenAiModelsCatalogID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsRouters() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelsRouters(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiModelsRouters() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiModelsRouters(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsRoutersPresets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelsRoutersPresets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsRoutersTasksPresets() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiModelsRoutersTasksPresets(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiModelsRoutersUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiModelsRoutersUUIDRequest{
        UUID: "uuid",
    }
client.GetV2GenAiModelsRoutersUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiModelsRoutersUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiModelsRoutersUUIDRequest{
        UUID: "uuid",
    }
client.PutV2GenAiModelsRoutersUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiModelsRoutersUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiModelsRoutersUUIDRequest{
        UUID: "uuid",
    }
client.DeleteV2GenAiModelsRoutersUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiOauth2DropboxTokens() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiOauth2DropboxTokens(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiOauth2URL() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiOauth2URL(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiOpenaiKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiOpenaiKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiOpenaiKeys() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiOpenaiKeys(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiOpenaiKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiOpenaiKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.GetV2GenAiOpenaiKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiOpenaiKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiOpenaiKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.PutV2GenAiOpenaiKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiOpenaiKeysAPIKeyUUID(APIKeyUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiOpenaiKeysAPIKeyUUIDRequest{
        APIKeyUUID: "api_key_uuid",
    }
client.DeleteV2GenAiOpenaiKeysAPIKeyUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiOpenaiKeysUUIDAgents(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiOpenaiKeysUUIDAgentsRequest{
        UUID: "uuid",
    }
client.GetV2GenAiOpenaiKeysUUIDAgents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiRegions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiRegions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiScheduledIndexing() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiScheduledIndexing(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiScheduledIndexingKnowledgeBaseKnowledgeBaseUUID(KnowledgeBaseUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiScheduledIndexingKnowledgeBaseKnowledgeBaseUUIDRequest{
        KnowledgeBaseUUID: "knowledge_base_uuid",
    }
client.GetV2GenAiScheduledIndexingKnowledgeBaseKnowledgeBaseUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiScheduledIndexingUUID(UUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiScheduledIndexingUUIDRequest{
        UUID: "uuid",
    }
client.DeleteV2GenAiScheduledIndexingUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiWorkspaces() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV2GenAiWorkspaces(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV2GenAiWorkspaces() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV2GenAiWorkspaces(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiWorkspacesWorkspaceUUID(WorkspaceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiWorkspacesWorkspaceUUIDRequest{
        WorkspaceUUID: "workspace_uuid",
    }
client.GetV2GenAiWorkspacesWorkspaceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiWorkspacesWorkspaceUUID(WorkspaceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiWorkspacesWorkspaceUUIDRequest{
        WorkspaceUUID: "workspace_uuid",
    }
client.PutV2GenAiWorkspacesWorkspaceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DeleteV2GenAiWorkspacesWorkspaceUUID(WorkspaceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DeleteV2GenAiWorkspacesWorkspaceUUIDRequest{
        WorkspaceUUID: "workspace_uuid",
    }
client.DeleteV2GenAiWorkspacesWorkspaceUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiWorkspacesWorkspaceUUIDAgents(WorkspaceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiWorkspacesWorkspaceUUIDAgentsRequest{
        WorkspaceUUID: "workspace_uuid",
    }
client.GetV2GenAiWorkspacesWorkspaceUUIDAgents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutV2GenAiWorkspacesWorkspaceUUIDAgents(WorkspaceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PutV2GenAiWorkspacesWorkspaceUUIDAgentsRequest{
        WorkspaceUUID: "workspace_uuid",
    }
client.PutV2GenAiWorkspacesWorkspaceUUIDAgents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV2GenAiWorkspacesWorkspaceUUIDEvaluationTestCases(WorkspaceUUID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV2GenAiWorkspacesWorkspaceUUIDEvaluationTestCasesRequest{
        WorkspaceUUID: "workspace_uuid",
    }
client.GetV2GenAiWorkspacesWorkspaceUUIDEvaluationTestCases(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1ChatCompletions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1ChatCompletions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1Messages() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1Messages(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1Embeddings() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1Embeddings(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostAPIV1ChatCompletions() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostAPIV1ChatCompletions(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1ImagesGenerations() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1ImagesGenerations(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV1Models() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV1Models(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1Responses() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1Responses(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1AsyncInvoke() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1AsyncInvoke(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1BatchesFiles() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1BatchesFiles(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PutUploadURL() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PutUploadURL(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV1Batches() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GetV1Batches(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1Batches() -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.PostV1Batches(
        context.TODO(),
    )
}
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV1BatchesBatchID(BatchID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV1BatchesBatchIDRequest{
        BatchID: "batch_id",
    }
client.GetV1BatchesBatchID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GetV1BatchesBatchIDResults(BatchID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GetV1BatchesBatchIDResultsRequest{
        BatchID: "batch_id",
    }
client.GetV1BatchesBatchIDResults(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PostV1BatchesBatchIDCancel(BatchID) -> error</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PostV1BatchesBatchIDCancelRequest{
        BatchID: "batch_id",
    }
client.PostV1BatchesBatchIDCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchID:** `string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

