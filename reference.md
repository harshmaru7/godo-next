# Reference
## 1-Click Applications
<details><summary><code>client._1ClickApplications.OneClicksList() -> *godonext.OneClicksListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all available 1-Click applications, send a GET request to `/v2/1-clicks`. The `type` may
be provided as query paramater in order to restrict results to a certain type of 1-Click, for
example: `/v2/1-clicks?type=droplet`. Current supported types are `kubernetes` and `droplet`.

The response will be a JSON object with a key called `1_clicks`. This will be set to an array of
1-Click application data, each of which will contain the the slug and type for the 1-Click.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.OneClicksListRequest{}
client.1ClickApplications.OneClicksList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type_:** `*godonext.OneClicksListRequestType` — Restrict results to a certain type of 1-Click.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client._1ClickApplications.OneClicksInstallKubernetes(request) -> *godonext.OneClicksInstallKubernetesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To install a Kubernetes 1-Click application on a cluster, send a POST request to
`/v2/1-clicks/kubernetes`. The `addon_slugs` and `cluster_uuid` must be provided as body
parameter in order to specify which 1-Click application(s) to install. To list all available
1-Click Kubernetes applications, send a request to `/v2/1-clicks?type=kubernetes`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.OneClicksCreate{
        AddonSlugs: []string{
            "kube-state-metrics",
            "loki",
        },
        ClusterUUID: "50a994b6-c303-438f-9495-7e896cfe6b08",
    }
client.1ClickApplications.OneClicksInstallKubernetes(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**addonSlugs:** `[]string` — An array of 1-Click Application slugs to be installed to the Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**clusterUUID:** `string` — A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Account
<details><summary><code>client.Account.Get() -> *godonext.AccountGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about the current user account, send a GET request to `/v2/account`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Account.Get(
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

## SSH Keys
<details><summary><code>client.SSHKeys.SSHKeysList() -> *godonext.SSHKeysListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the keys in your account, send a GET request to `/v2/account/keys`. The response will be a JSON object with a key set to `ssh_keys`. The value of this will be an array of ssh_key objects, each of which contains the standard ssh_key attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SSHKeysListRequest{}
client.SSHKeys.SSHKeysList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SSHKeys.SSHKeysCreate(request) -> *godonext.SSHKeysCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add a new SSH public key to your DigitalOcean account, send a POST request to `/v2/account/keys`. Set the `name` attribute to the name you wish to use and the `public_key` attribute to the full public key you are adding.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SSHKeys{
        PublicKey: "ssh-rsa AEXAMPLEaC1yc2EAAAADAQABAAAAQQDDHr/jh2Jy4yALcK4JyWbVkPRaWmhck3IgCoeOO3z1e2dBowLh64QAM+Qb72pxekALga2oi4GvT+TlWNhzPH4V example",
        Name: "My SSH Public Key",
    }
client.SSHKeys.SSHKeysCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.SSHKeys` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SSHKeys.SSHKeysGet(SSHKeyIdentifier) -> *godonext.SSHKeysGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get information about a key, send a GET request to `/v2/account/keys/$KEY_ID` or `/v2/account/keys/$KEY_FINGERPRINT`.
The response will be a JSON object with the key `ssh_key` and value an ssh_key object which contains the standard ssh_key attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SSHKeysGetRequest{
        SSHKeyIdentifier: &godonext.SSHKeysGetRequestSSHKeyIdentifier{
            SSHKeyID: 512189,
        },
    }
client.SSHKeys.SSHKeysGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sshKeyIdentifier:** `*godonext.SSHKeysGetRequestSSHKeyIdentifier` — Either the ID or the fingerprint of an existing SSH key.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SSHKeys.SSHKeysUpdate(SSHKeyIdentifier, request) -> *godonext.SSHKeysUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the name of an SSH key, send a PUT request to either `/v2/account/keys/$SSH_KEY_ID` or `/v2/account/keys/$SSH_KEY_FINGERPRINT`. Set the `name` attribute to the new name you want to use.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SSHKeysUpdateRequest{
        SSHKeyIdentifier: &godonext.SSHKeysUpdateRequestSSHKeyIdentifier{
            SSHKeyID: 512189,
        },
    }
client.SSHKeys.SSHKeysUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sshKeyIdentifier:** `*godonext.SSHKeysUpdateRequestSSHKeyIdentifier` — Either the ID or the fingerprint of an existing SSH key.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*godonext.SSHKeyName` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SSHKeys.SSHKeysDelete(SSHKeyIdentifier) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy a public SSH key that you have in your account, send a DELETE request to `/v2/account/keys/$KEY_ID` or `/v2/account/keys/$KEY_FINGERPRINT`.
A 204 status will be returned, indicating that the action was successful and that the response body is empty.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SSHKeysDeleteRequest{
        SSHKeyIdentifier: &godonext.SSHKeysDeleteRequestSSHKeyIdentifier{
            SSHKeyID: 512189,
        },
    }
client.SSHKeys.SSHKeysDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sshKeyIdentifier:** `*godonext.SSHKeysDeleteRequestSSHKeyIdentifier` — Either the ID or the fingerprint of an existing SSH key.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Actions
<details><summary><code>client.Actions.List() -> *godonext.ActionsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This will be the entire list of actions taken on your account, so it will be quite large. As with any large collection returned by the API, the results will be paginated with only 20 on each page by default.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ActionsListRequest{}
client.Actions.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Actions.Get(ActionID) -> *godonext.ActionsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a specific action object, send a GET request to `/v2/actions/$ACTION_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ActionsGetRequest{
        ActionID: 1,
    }
client.Actions.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**actionID:** `int` — A unique numeric ID that can be used to identify and reference an action.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Add-Ons
<details><summary><code>client.AddOns.AddonsGetApp() -> *godonext.AddonsGetAppResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To fetch details of all available Add-On Applications, send a GET request to `/v2/add-ons/apps`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.AddOns.AddonsGetApp(
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

<details><summary><code>client.AddOns.AddonsGetAppMetadata(AppSlug) -> *godonext.AddonsGetAppMetadataResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To find out what metadata is required for a specific add-on, send a GET request to `/v2/add-ons/apps/{app_slug}/metadata`.
Metadata varies by application.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AddonsGetAppMetadataRequest{
        AppSlug: "example_app",
    }
client.AddOns.AddonsGetAppMetadata(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appSlug:** `string` — The slug identifier for the application whose metadata is being requested.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.AddOns.AddonsList() -> *godonext.AddonsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To fetch all Add-On Resources under your team, send a GET request to `/v2/add-ons/saas`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.AddOns.AddonsList(
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

<details><summary><code>client.AddOns.AddonsCreate(request) -> *godonext.AddonsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an add-on resource, send a POST request to `/v2/add-ons/saas` with required parameters.
Some add-ons require additional metadata to be provided in the request body. To find out
what metadata is required for a specific add-on, send a GET request to `/v2/add-ons/apps/{app_slug}/metadata`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AddonsResourceNew{
        AppSlug: "example-app",
        PlanSlug: "basic_plan",
        Name: "my-resource-01",
        Metadata: []*godonext.AddonsResourceMetadata{
            &godonext.AddonsResourceMetadata{
                Name: "property_name",
                Value: &godonext.AddonsResourceMetadataValue{
                    String: "example_value",
                },
            },
        },
    }
client.AddOns.AddonsCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appSlug:** `string` — The slug identifier for the application associated with the resource.
    
</dd>
</dl>

<dl>
<dd>

**planSlug:** `string` — The slug identifier for the plan associated with the resource.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The name of the addon resource.
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `[]*godonext.AddonsResourceMetadata` — Metadata associated with the resource, set by the user. Metadata expected varies per app, and can be verified with a GET request to "/v2/add-ons/apps/{app_slug}/metadata"
    
</dd>
</dl>

<dl>
<dd>

**linkedDropletID:** `*int` — ID of the droplet to be linked to this resource, if applicable.
    
</dd>
</dl>

<dl>
<dd>

**fleetUUID:** `*string` — UUID of the fleet/project to which this resource will belong.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.AddOns.AddonsGet(ResourceUUID) -> *godonext.AddonsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To fetch details of a specific Add-On Resource, send a GET request to `/v2/add-ons/saas/{resource_uuid}`.
Replace `{resource_uuid}` with the UUID of the resource you want to retrieve.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AddonsGetRequest{
        ResourceUUID: "123e4567-e89b-12d3-a456-426614174000",
    }
client.AddOns.AddonsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` — The UUID of the add-on resource to retrieve.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.AddOns.AddonsDelete(ResourceUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an add-on resource, send a DELETE request to `/v2/add-ons/saas/{resource_uuid}` with the UUID of the resource to delete. 
You cannot retrieve the resource after it has been deleted. The response indicates a request was sent to the 3rd party add-on provider to delete the resource.
You will no longer be billed for this resource.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AddonsDeleteRequest{
        ResourceUUID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.AddOns.AddonsDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` — A unique identifier for the add-on resource.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.AddOns.AddonsPatch(ResourceUUID, request) -> *godonext.AddonsPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To change the name of an Add-On Resource, send a PATCH request to `/v2/add-ons/saas/{resource_uuid}`.
Replace `{resource_uuid}` with the UUID of the resource for which you want to change the name.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AddonsPatchRequest{
        ResourceUUID: "123e4567-e89b-12d3-a456-426614174000",
        Name: "new-name",
    }
client.AddOns.AddonsPatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` — The UUID of the add-on resource to rename.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The new name for the add-on resource.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.AddOns.AddonsPatchPlan(ResourceUUID, request) -> *godonext.AddonsPatchPlanResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To change the plan associated with an Add-On Resource, send a PATCH request to `/v2/add-ons/saas/{resource_uuid}/plan`.
Replace `{resource_uuid}` with the UUID of the resource for which you want to change the plan.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AddonsPatchPlanRequest{
        ResourceUUID: "123e4567-e89b-12d3-a456-426614174000",
        PlanSlug: "basic_plan",
    }
client.AddOns.AddonsPatchPlan(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceUUID:** `string` — The UUID of the add-on resource to update.
    
</dd>
</dl>

<dl>
<dd>

**planSlug:** `string` — The slug identifier for the new plan to apply to the add-on resource.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Apps
<details><summary><code>client.Apps.List() -> *godonext.AppsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all apps on your account. Information about the current active deployment as well as any in progress ones will also be included for each app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsListRequest{}
client.Apps.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**withProjects:** `*bool` — Whether the project_id of listed apps should be fetched and included.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.Create(request) -> *godonext.AppResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new app by submitting an app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCreateAppRequest{
        Spec: &godonext.AppSpec{
            Name: "web-app",
            Region: godonext.AppSpecRegionNyc.Ptr(),
            DisableEdgeCache: godonext.Bool(
                true,
            ),
            DisableEmailObfuscation: godonext.Bool(
                false,
            ),
            EnhancedThreatControlEnabled: godonext.Bool(
                true,
            ),
            Services: []*godonext.AppServiceSpec{
                &godonext.AppServiceSpec{
                    Name: godonext.String(
                        "api",
                    ),
                    Github: &godonext.AppsGithubSourceSpec{
                        Branch: godonext.String(
                            "main",
                        ),
                        DeployOnPush: godonext.Bool(
                            true,
                        ),
                        Repo: godonext.String(
                            "digitalocean/sample-golang",
                        ),
                    },
                    RunCommand: godonext.String(
                        "bin/api",
                    ),
                    EnvironmentSlug: godonext.String(
                        "node-js",
                    ),
                    InstanceCount: godonext.Int64(
                        int64(2),
                    ),
                    InstanceSizeSlug: godonext.AppComponentInstanceBaseInstanceSizeSlugAppsS1Vcpu05Gb.Ptr(),
                },
            },
            Egress: &godonext.AppEgressSpec{
                Type: godonext.AppEgressTypeSpecDedicatedIP.Ptr(),
            },
            Vpc: &godonext.AppsVpc{
                ID: godonext.String(
                    "c22d8f48-4bc4-49f5-8ca0-58e7164427ac",
                ),
            },
        },
    }
client.Apps.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accept:** `*godonext.AppsCreateRequestAccept` — The content-type that should be used by the response. By default, the response will be `application/json`. `application/yaml` is also supported.
    
</dd>
</dl>

<dl>
<dd>

**spec:** `*godonext.AppSpec` 
    
</dd>
</dl>

<dl>
<dd>

**projectID:** `*string` 

The ID of the project the app should be assigned to. If omitted, it will be assigned to your default project.
<br><br>Requires `project:update` scope.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.Get(ID) -> *godonext.AppResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve details about an existing app by either its ID or name. To retrieve an app by its name, do not include an ID in the request path. Information about the current active deployment as well as any in progress ones will also be included in the response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetRequest{
        ID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Name: godonext.String(
            "myApp",
        ),
    }
client.Apps.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the app
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — The name of the app to retrieve.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.Update(ID, request) -> *godonext.AppResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing app by submitting a new app specification. For documentation on app specifications (`AppSpec` objects), please refer to [the product documentation](https://docs.digitalocean.com/products/app-platform/reference/app-spec/).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsUpdateAppRequest{
        ID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Spec: &godonext.AppSpec{
            Name: "web-app-01",
        },
    }
client.Apps.Update(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the app
    
</dd>
</dl>

<dl>
<dd>

**spec:** `*godonext.AppSpec` 
    
</dd>
</dl>

<dl>
<dd>

**updateAllSourceVersions:** `*bool` — Whether or not to update the source versions (for example fetching a new commit or image digest) of all components. By default (when this is false) only newly added sources will be updated to avoid changes like updating the scale of a component from also updating the respective code.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.Delete(ID) -> *godonext.AppsDeleteAppResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an existing app. Once deleted, all active deployments will be permanently shut down and the app deleted. If needed, be sure to back up your app specification so that you may re-create it at a later time.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsDeleteRequest{
        ID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The ID of the app
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.Restart(AppID, request) -> *godonext.AppsDeploymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Perform a rolling restart of all or specific components in an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsRestartRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.Restart(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**components:** `[]string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetLogsActiveDeployment(AppID, ComponentName) -> *godonext.AppsGetLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the logs of the active deployment if one exists. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment. Note log_type=BUILD logs will return logs associated with the current active deployment (being served). To view build logs associated with in-progress build, the query must explicitly reference the deployment id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetLogsActiveDeploymentRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        ComponentName: "component",
        Type: godonext.AppsGetLogsActiveDeploymentRequestTypeUnspecified,
        PodConnectionTimeout: godonext.String(
            "3m",
        ),
    }
client.Apps.GetLogsActiveDeployment(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` — An optional component name. If set, logs will be limited to this component only.
    
</dd>
</dl>

<dl>
<dd>

**follow:** `*bool` — Whether the logs should follow live updates.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.AppsGetLogsActiveDeploymentRequestType` 

The type of logs to retrieve
- BUILD: Build-time logs
- DEPLOY: Deploy-time logs
- RUN: Live run-time logs
- RUN_RESTARTED: Logs of crashed/restarted instances during runtime
- AUTOSCALE_EVENT: Logs of an autoscaling event (requires event_id)
    
</dd>
</dl>

<dl>
<dd>

**podConnectionTimeout:** `*string` — An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetExecActiveDeployment(AppID, ComponentName) -> *godonext.AppsGetExecResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a websocket URL that allows sending/receiving console input and output to a component of the active deployment if one exists.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetExecActiveDeploymentRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        ComponentName: "component",
        InstanceName: godonext.String(
            "go-app-d768568df-zz77d",
        ),
    }
client.Apps.GetExecActiveDeployment(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` — An optional component name. If set, logs will be limited to this component only.
    
</dd>
</dl>

<dl>
<dd>

**instanceName:** `*string` — The name of the actively running ephemeral compute instance
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetInstances(AppID) -> *godonext.AppInstances</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the list of running instances for a given application, including instance names and component types. Please note that these instances are ephemeral and may change over time. It is recommended not to make persistent changes or develop scripts that rely on their persistence.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetInstancesRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.GetInstances(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListDeployments(AppID) -> *godonext.AppsDeploymentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all deployments of an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsListDeploymentsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.ListDeployments(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**deploymentTypes:** `*godonext.AppsListDeploymentsRequestDeploymentTypesItem` 

Optional. Filter deployments by deployment_type
  - MANUAL: manual deployment
  - DEPLOY_ON_PUSH: deployment triggered by a push to the app's repository
  - MAINTENANCE: deployment for maintenance purposes
  - MANUAL_ROLLBACK: manual revert to a previous deployment
  - AUTO_ROLLBACK: automatic revert to a previous deployment
  - UPDATE_DATABASE_TRUSTED_SOURCES: update database trusted sources
  - AUTOSCALED: deployment that has been autoscaled
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.CreateDeployment(AppID, request) -> *godonext.AppsDeploymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creating an app deployment will pull the latest changes from your repository and schedule a new deployment for your app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCreateDeploymentRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.CreateDeployment(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**forceBuild:** `*bool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetDeployment(AppID, DeploymentID) -> *godonext.AppsDeploymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve information about an app deployment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetDeploymentRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        DeploymentID: "3aa4d20e-5527-4c00-b496-601fbd22520a",
    }
client.Apps.GetDeployment(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` — The deployment ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.CancelDeployment(AppID, DeploymentID) -> *godonext.AppsDeploymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Immediately cancel an in-progress deployment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCancelDeploymentRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        DeploymentID: "3aa4d20e-5527-4c00-b496-601fbd22520a",
    }
client.Apps.CancelDeployment(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` — The deployment ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetLogs(AppID, DeploymentID, ComponentName) -> *godonext.AppsGetLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the logs of a past, in-progress, or active deployment. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetLogsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        DeploymentID: "3aa4d20e-5527-4c00-b496-601fbd22520a",
        ComponentName: "component",
        Type: godonext.AppsGetLogsRequestTypeUnspecified,
        PodConnectionTimeout: godonext.String(
            "3m",
        ),
    }
client.Apps.GetLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` — The deployment ID
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` — An optional component name. If set, logs will be limited to this component only.
    
</dd>
</dl>

<dl>
<dd>

**follow:** `*bool` — Whether the logs should follow live updates.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.AppsGetLogsRequestType` 

The type of logs to retrieve
- BUILD: Build-time logs
- DEPLOY: Deploy-time logs
- RUN: Live run-time logs
- RUN_RESTARTED: Logs of crashed/restarted instances during runtime
- AUTOSCALE_EVENT: Logs of an autoscaling event (requires event_id)
    
</dd>
</dl>

<dl>
<dd>

**podConnectionTimeout:** `*string` — An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetLogsAggregate(AppID, DeploymentID) -> *godonext.AppsGetLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the logs of a past, in-progress, or active deployment. If a component name is specified, the logs will be limited to only that component. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetLogsAggregateRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        DeploymentID: "3aa4d20e-5527-4c00-b496-601fbd22520a",
        Type: godonext.AppsGetLogsAggregateRequestTypeUnspecified,
        PodConnectionTimeout: godonext.String(
            "3m",
        ),
    }
client.Apps.GetLogsAggregate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` — The deployment ID
    
</dd>
</dl>

<dl>
<dd>

**follow:** `*bool` — Whether the logs should follow live updates.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.AppsGetLogsAggregateRequestType` 

The type of logs to retrieve
- BUILD: Build-time logs
- DEPLOY: Deploy-time logs
- RUN: Live run-time logs
- RUN_RESTARTED: Logs of crashed/restarted instances during runtime
- AUTOSCALE_EVENT: Logs of an autoscaling event (requires event_id)
    
</dd>
</dl>

<dl>
<dd>

**podConnectionTimeout:** `*string` — An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetExec(AppID, DeploymentID, ComponentName) -> *godonext.AppsGetExecResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a websocket URL that allows sending/receiving console input and output to a component of the specified deployment if one exists. Optionally, the instance_name parameter can be provided to retrieve the exec URL for a specific instance. Note that instances are ephemeral; therefore, we recommended to avoid making persistent changes or such scripting around them.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetExecRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        DeploymentID: "3aa4d20e-5527-4c00-b496-601fbd22520a",
        ComponentName: "component",
        InstanceName: godonext.String(
            "go-app-d768568df-zz77d",
        ),
    }
client.Apps.GetExec(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `string` — The deployment ID
    
</dd>
</dl>

<dl>
<dd>

**componentName:** `string` — An optional component name. If set, logs will be limited to this component only.
    
</dd>
</dl>

<dl>
<dd>

**instanceName:** `*string` — The name of the actively running ephemeral compute instance
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetLogsActiveDeploymentAggregate(AppID) -> *godonext.AppsGetLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the logs of the active deployment if one exists. The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment. Note log_type=BUILD logs will return logs associated with the current active deployment (being served). To view build logs associated with in-progress build, the query must explicitly reference the deployment id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetLogsActiveDeploymentAggregateRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Type: godonext.AppsGetLogsActiveDeploymentAggregateRequestTypeUnspecified,
        PodConnectionTimeout: godonext.String(
            "3m",
        ),
    }
client.Apps.GetLogsActiveDeploymentAggregate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**follow:** `*bool` — Whether the logs should follow live updates.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.AppsGetLogsActiveDeploymentAggregateRequestType` 

The type of logs to retrieve
- BUILD: Build-time logs
- DEPLOY: Deploy-time logs
- RUN: Live run-time logs
- RUN_RESTARTED: Logs of crashed/restarted instances during runtime
- AUTOSCALE_EVENT: Logs of an autoscaling event (requires event_id)
    
</dd>
</dl>

<dl>
<dd>

**podConnectionTimeout:** `*string` — An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListJobInvocations(AppID) -> *godonext.AppJobInvocations</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all job invocations for an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsListJobInvocationsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        DeploymentID: godonext.String(
            "3aa4d20e-5527-4c00-b496-601fbd22520a",
        ),
    }
client.Apps.ListJobInvocations(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**jobNames:** `*godonext.Schema` — The job names to list job invocations for.
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `*string` — The deployment ID
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetJobInvocation(AppID, JobInvocationID) -> *godonext.AppJobInvocation</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a specific job invocation for an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetJobInvocationRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        JobInvocationID: "123e4567-e89b-12d3-a456-426",
        JobName: godonext.String(
            "component",
        ),
    }
client.Apps.GetJobInvocation(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**jobInvocationID:** `string` — The ID of the job invocation to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**jobName:** `*string` — The job name to list job invocations for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.CancelJobInvocation(AppID, JobInvocationID) -> *godonext.AppJobInvocation</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a specific job invocation for an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCancelJobInvocationRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        JobInvocationID: "123e4567-e89b-12d3-a456-426",
        JobName: godonext.String(
            "component",
        ),
    }
client.Apps.CancelJobInvocation(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**jobInvocationID:** `string` — The ID of the job invocation to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**jobName:** `*string` — The job name to list job invocations for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetJobInvocationLogs(AppID, JobName, JobInvocationID) -> *godonext.AppsGetLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the logs of a past, in-progress, or active deployment. If a component name is specified, the logs will be limited to only that component. If deployment is omitted the active deployment will be selected (if available). The response will include links to either real-time logs of an in-progress or active deployment or archived logs of a past deployment.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetJobInvocationLogsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        JobName: "component",
        JobInvocationID: "123e4567-e89b-12d3-a456-426",
        DeploymentID: godonext.String(
            "3aa4d20e-5527-4c00-b496-601fbd22520a",
        ),
        Type: godonext.AppsGetJobInvocationLogsRequestTypeJobInvocation,
        PodConnectionTimeout: godonext.String(
            "3m",
        ),
        TailLines: godonext.String(
            "100",
        ),
    }
client.Apps.GetJobInvocationLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**jobName:** `string` — The job name to list job invocations for.
    
</dd>
</dl>

<dl>
<dd>

**jobInvocationID:** `string` — The ID of the job invocation to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**deploymentID:** `*string` — The deployment ID
    
</dd>
</dl>

<dl>
<dd>

**follow:** `*bool` — Whether the logs should follow live updates.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.AppsGetJobInvocationLogsRequestType` — The type of logs to retrieve
    
</dd>
</dl>

<dl>
<dd>

**podConnectionTimeout:** `*string` — An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`.
    
</dd>
</dl>

<dl>
<dd>

**tailLines:** `*string` — The number of lines from the end of the logs to retrieve.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListEvents(AppID) -> *godonext.AppEvents</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all events for an app, including deployments and autoscaling events.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsListEventsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.ListEvents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**eventTypes:** `*godonext.AppsListEventsRequestEventTypesItem` — Filter events by event type.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetEvent(AppID, EventID) -> *godonext.AppsGetEventResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single event for an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetEventRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        EventID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.GetEvent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**eventID:** `string` — The event ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.CancelEvent(AppID, EventID) -> *godonext.AppsCancelEventResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel an in-progress autoscaling event.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCancelEventRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        EventID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.CancelEvent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**eventID:** `string` — The event ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetEventLogs(AppID, EventID) -> *godonext.AppsGetLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve the logs of an autoscaling event for an app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetEventLogsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        EventID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Type: godonext.AppsGetEventLogsRequestTypeUnspecified,
        PodConnectionTimeout: godonext.String(
            "3m",
        ),
    }
client.Apps.GetEventLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**eventID:** `string` — The event ID
    
</dd>
</dl>

<dl>
<dd>

**follow:** `*bool` — Whether the logs should follow live updates.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.AppsGetEventLogsRequestType` 

The type of logs to retrieve
- BUILD: Build-time logs
- DEPLOY: Deploy-time logs
- RUN: Live run-time logs
- RUN_RESTARTED: Logs of crashed/restarted instances during runtime
- AUTOSCALE_EVENT: Logs of an autoscaling event (requires event_id)
    
</dd>
</dl>

<dl>
<dd>

**podConnectionTimeout:** `*string` — An optional time duration to wait if the underlying component instance is not immediately available. Default: `3m`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListInstancesizes() -> *godonext.AppsListInstanceSizesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all instance sizes for `service`, `worker`, and `job` components.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Apps.ListInstancesizes(
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

<details><summary><code>client.Apps.GetInstancesize(Slug) -> *godonext.AppsGetInstanceSizeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve information about a specific instance size for `service`, `worker`, and `job` components.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetInstanceSizeRequest{
        Slug: "apps-s-1vcpu-0.5gb",
    }
client.Apps.GetInstancesize(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**slug:** `string` — The slug of the instance size
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListRegions() -> *godonext.AppsListRegionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all regions supported by App Platform.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Apps.ListRegions(
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

<details><summary><code>client.Apps.ValidateAppspec(request) -> *godonext.AppProposeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To propose and validate a spec for a new or existing app, send a POST request to the `/v2/apps/propose` endpoint. The request returns some information about the proposed app, including app cost and upgrade cost. If an existing app ID is specified, the app spec is treated as a proposed update to the existing app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppPropose{
        Spec: &godonext.AppSpec{
            Name: "web-app",
            Region: godonext.AppSpecRegionNyc.Ptr(),
            Services: []*godonext.AppServiceSpec{
                &godonext.AppServiceSpec{
                    Name: godonext.String(
                        "api",
                    ),
                    Github: &godonext.AppsGithubSourceSpec{
                        Branch: godonext.String(
                            "main",
                        ),
                        DeployOnPush: godonext.Bool(
                            true,
                        ),
                        Repo: godonext.String(
                            "digitalocean/sample-golang",
                        ),
                    },
                    RunCommand: godonext.String(
                        "bin/api",
                    ),
                    EnvironmentSlug: godonext.String(
                        "node-js",
                    ),
                    InstanceCount: godonext.Int64(
                        int64(2),
                    ),
                    InstanceSizeSlug: godonext.AppComponentInstanceBaseInstanceSizeSlugAppsS1Vcpu05Gb.Ptr(),
                },
            },
        },
        AppID: godonext.String(
            "b6bdf840-2854-4f87-a36c-5f231c617c84",
        ),
    }
client.Apps.ValidateAppspec(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**spec:** `*godonext.AppSpec` 
    
</dd>
</dl>

<dl>
<dd>

**appID:** `*string` — An optional ID of an existing app. If set, the spec will be treated as a proposed update to the specified app. The existing app is not modified using this method.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListAlerts(AppID) -> *godonext.AppsListAlertsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List alerts associated to the app and any components. This includes configuration information about the alerts including emails, slack webhooks, and triggering events or conditions.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsListAlertsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.ListAlerts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.AssignAlertdestinations(AppID, AlertID, request) -> *godonext.AppsAlertResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the emails and slack webhook destinations for app alerts. Emails must be associated to a user with access to the app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsAssignAppAlertDestinationsRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        AlertID: "5a624ab5-dd58-4b39-b7dd-8b7c36e8a91d",
    }
client.Apps.AssignAlertdestinations(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` — The alert ID
    
</dd>
</dl>

<dl>
<dd>

**emails:** `[]godonext.AppAlertEmail` 
    
</dd>
</dl>

<dl>
<dd>

**slackWebhooks:** `[]*godonext.AppAlertSlackWebhook` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.CreateRollback(AppID, request) -> *godonext.AppsDeploymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Rollback an app to a previous deployment. A new deployment will be created to perform the rollback.
The app will be pinned to the rollback deployment preventing any new deployments from being created,
either manually or through Auto Deploy on Push webhooks. To resume deployments, the rollback must be
either committed or reverted.

It is recommended to use the Validate App Rollback endpoint to double check if the rollback is
valid and if there are any warnings.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCreateRollbackRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Body: &godonext.AppsRollbackAppRequest{},
    }
client.Apps.CreateRollback(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.AppsRollbackAppRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ValidateRollback(AppID, request) -> *godonext.AppsValidateRollbackResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Check whether an app can be rolled back to a specific deployment. This endpoint can also be used
to check if there are any warnings or validation conditions that will cause the rollback to proceed
under unideal circumstances. For example, if a component must be rebuilt as part of the rollback
causing it to take longer than usual.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsValidateRollbackRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Body: &godonext.AppsRollbackAppRequest{},
    }
client.Apps.ValidateRollback(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.AppsRollbackAppRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.CommitRollback(AppID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Commit an app rollback. This action permanently applies the rollback and unpins the app to resume new deployments.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsCommitRollbackRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.CommitRollback(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.RevertRollback(AppID) -> *godonext.AppsDeploymentResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revert an app rollback. This action reverts the active rollback by creating a new deployment from the
latest app spec prior to the rollback and unpins the app to resume new deployments.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsRevertRollbackRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.RevertRollback(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetMetricsBandwidthDaily(AppID) -> *godonext.AppMetricsBandwidthUsage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve daily bandwidth usage metrics for a single app.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetMetricsBandwidthDailyRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        Date: godonext.Time(
            godonext.MustParseDateTime(
                "2023-01-17T00:00:00Z",
            ),
        ),
    }
client.Apps.GetMetricsBandwidthDaily(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>

<dl>
<dd>

**date:** `*time.Time` — Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.ListMetricsBandwidthDaily(request) -> *godonext.AppMetricsBandwidthUsage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve daily bandwidth usage metrics for multiple apps.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppMetricsBandwidthUsageRequest{
        AppIDs: []string{
            "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
            "c2a93513-8d9b-4223-9d61-5e7272c81cf5",
        },
        Date: godonext.Time(
            godonext.MustParseDateTime(
                "2023-01-17T00:00:00Z",
            ),
        ),
    }
client.Apps.ListMetricsBandwidthDaily(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appIDs:** `[]string` — A list of app IDs to query bandwidth metrics for.
    
</dd>
</dl>

<dl>
<dd>

**date:** `*time.Time` — Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Apps.GetHealth(AppID) -> *godonext.AppHealthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve information like health status, cpu and memory utilization of app components.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AppsGetHealthRequest{
        AppID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Apps.GetHealth(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## CDN Endpoints
<details><summary><code>client.CdnEndpoints.CdnListEndpoints() -> *godonext.CdnListEndpointsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the CDN endpoints available on your account, send a GET request to `/v2/cdn/endpoints`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CdnListEndpointsRequest{}
client.CdnEndpoints.CdnListEndpoints(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.CdnEndpoints.CdnCreateEndpoint(request) -> *godonext.CdnCreateEndpointResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new CDN endpoint, send a POST request to `/v2/cdn/endpoints`. The
origin attribute must be set to the fully qualified domain name (FQDN) of a
DigitalOcean Space. Optionally, the TTL may be configured by setting the `ttl`
attribute.

A custom subdomain may be configured by specifying the `custom_domain` and
`certificate_id` attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CdnEndpoint{
        Origin: "static-images.nyc3.digitaloceanspaces.com",
        TTL: godonext.Int(
            3600,
        ),
    }
client.CdnEndpoints.CdnCreateEndpoint(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.CdnEndpoint` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.CdnEndpoints.CdnGetEndpoint(CdnID) -> *godonext.CdnGetEndpointResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing CDN endpoint, send a GET request to `/v2/cdn/endpoints/$ENDPOINT_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CdnGetEndpointRequest{
        CdnID: "19f06b6a-3ace-4315-b086-499a0e521b76",
    }
client.CdnEndpoints.CdnGetEndpoint(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` — A unique identifier for a CDN endpoint.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.CdnEndpoints.CdnUpdateEndpoints(CdnID, request) -> *godonext.CdnUpdateEndpointsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the TTL, certificate ID, or the FQDN of the custom subdomain for
an existing CDN endpoint, send a PUT request to
`/v2/cdn/endpoints/$ENDPOINT_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UpdateEndpoint{
        CdnID: "19f06b6a-3ace-4315-b086-499a0e521b76",
    }
client.CdnEndpoints.CdnUpdateEndpoints(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` — A unique identifier for a CDN endpoint.
    
</dd>
</dl>

<dl>
<dd>

**ttl:** `*int` — The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.
    
</dd>
</dl>

<dl>
<dd>

**certificateID:** `*string` — The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided.
    
</dd>
</dl>

<dl>
<dd>

**customDomain:** `*string` — The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.CdnEndpoints.CdnDeleteEndpoint(CdnID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a specific CDN endpoint, send a DELETE request to
`/v2/cdn/endpoints/$ENDPOINT_ID`.

A status of 204 will be given. This indicates that the request was processed
successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CdnDeleteEndpointRequest{
        CdnID: "19f06b6a-3ace-4315-b086-499a0e521b76",
    }
client.CdnEndpoints.CdnDeleteEndpoint(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` — A unique identifier for a CDN endpoint.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.CdnEndpoints.CdnPurgeCache(CdnID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To purge cached content from a CDN endpoint, send a DELETE request to
`/v2/cdn/endpoints/$ENDPOINT_ID/cache`. The body of the request should include
a `files` attribute containing a list of cached file paths to be purged. A
path may be for a single file or may contain a wildcard (`*`) to recursively
purge all files under a directory. When only a wildcard is provided, all cached 
files will be purged. There is a rate limit of 50 files per 20 seconds that can 
be purged. CDN endpoints have a rate limit of 5 requests per 10 seconds. 
Purging files using a wildcard path counts as a single request against the API's 
rate limit. Two identical purge requests cannot be sent at the same time.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PurgeCache{
        CdnID: "19f06b6a-3ace-4315-b086-499a0e521b76",
        Files: []string{
            "path/to/image.png",
            "path/to/css/*",
        },
    }
client.CdnEndpoints.CdnPurgeCache(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**cdnID:** `string` — A unique identifier for a CDN endpoint.
    
</dd>
</dl>

<dl>
<dd>

**files:** `[]string` — An array of strings containing the path to the content to be purged from the CDN cache.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Certificates
<details><summary><code>client.Certificates.List() -> *godonext.CertificatesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the certificates available on your account, send a GET request to `/v2/certificates`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CertificatesListRequest{
        Name: godonext.String(
            "certificate-name",
        ),
    }
client.Certificates.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of expected certificate
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Certificates.Create(request) -> *godonext.CertificatesCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To upload new SSL certificate which you have previously generated, send a POST
request to `/v2/certificates`.

When uploading a user-generated certificate, the `private_key`,
`leaf_certificate`, and optionally the `certificate_chain` attributes should
be provided. The type must be set to `custom`.

When using Let's Encrypt to create a certificate, the `dns_names` attribute
must be provided, and the type must be set to `lets_encrypt`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CertificatesCreateRequest{
        CertificateRequestLetsEncrypt: &godonext.CertificateRequestLetsEncrypt{
            Name: "web-cert-01",
            DNSNames: []string{
                "www.example.com",
                "example.com",
            },
        },
    }
client.Certificates.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.CertificatesCreateRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Certificates.Get(CertificateID) -> *godonext.CertificatesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing certificate, send a GET request to `/v2/certificates/$CERTIFICATE_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CertificatesGetRequest{
        CertificateID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Certificates.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**certificateID:** `string` — A unique identifier for a certificate.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Certificates.Delete(CertificateID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a specific certificate, send a DELETE request to
`/v2/certificates/$CERTIFICATE_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CertificatesDeleteRequest{
        CertificateID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Certificates.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**certificateID:** `string` — A unique identifier for a certificate.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Billing
<details><summary><code>client.Billing.BalanceGet() -> *godonext.Balance</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the balances on a customer's account, send a GET request to `/v2/customers/my/balance`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Billing.BalanceGet(
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

<details><summary><code>client.Billing.BillingHistoryList() -> *godonext.BillingHistoryListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all billing history entries, send a GET request to `/v2/customers/my/billing_history`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Billing.BillingHistoryList(
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

<details><summary><code>client.Billing.InvoicesList() -> *godonext.InvoicesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all invoices, send a GET request to `/v2/customers/my/invoices`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InvoicesListRequest{}
client.Billing.InvoicesList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Billing.InvoicesGetByUUID(InvoiceUUID) -> *godonext.InvoicesGetByUUIDResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the invoice items for an invoice, send a GET request to `/v2/customers/my/invoices/$INVOICE_UUID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InvoicesGetByUUIDRequest{
        InvoiceUUID: "22737513-0ea7-4206-8ceb-98a575af7681",
    }
client.Billing.InvoicesGetByUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` — UUID of the invoice
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Billing.InvoicesGetCsvByUUID(InvoiceUUID) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a CSV for an invoice, send a GET request to `/v2/customers/my/invoices/$INVOICE_UUID/csv`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InvoicesGetCsvByUUIDRequest{
        InvoiceUUID: "<invoice_uuid>",
    }
client.Billing.InvoicesGetCsvByUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` — UUID of the invoice
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Billing.InvoicesGetPdfByUUID(InvoiceUUID) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a PDF for an invoice, send a GET request to `/v2/customers/my/invoices/$INVOICE_UUID/pdf`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InvoicesGetPdfByUUIDRequest{
        InvoiceUUID: "<invoice_uuid>",
    }
client.Billing.InvoicesGetPdfByUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` — UUID of the invoice
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Billing.InvoicesGetSummaryByUUID(InvoiceUUID) -> *godonext.InvoiceSummary</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a summary for an invoice, send a GET request to `/v2/customers/my/invoices/$INVOICE_UUID/summary`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InvoicesGetSummaryByUUIDRequest{
        InvoiceUUID: "22737513-0ea7-4206-8ceb-98a575af7681",
    }
client.Billing.InvoicesGetSummaryByUUID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**invoiceUUID:** `string` — UUID of the invoice
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Billing.BillingInsightsList(AccountUrn, StartDate, EndDate) -> *godonext.BillingInsightsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>


This endpoint returns day-over-day changes in billing resource usage based on nightly invoice items, including total amount, region, SKU, and description for a specified date range. It is important to note that the daily resource usage may not reflect month-end billing totals when totaled for a given month as nightly invoice item estimates do not necessarily encompass all invoicing factors for the entire month.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.BillingInsightsListRequest{
        AccountUrn: "do:team:12345678-1234-1234-1234-123456789012",
        StartDate: godonext.MustParseDate(
            "2025-01-01",
        ),
        EndDate: godonext.MustParseDate(
            "2025-01-31",
        ),
    }
client.Billing.BillingInsightsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accountUrn:** `string` — URN of the customer account, can be a team (do:team:uuid) or an organization (do:teamgroup:uuid)
    
</dd>
</dl>

<dl>
<dd>

**startDate:** `time.Time` — Start date for billing insights in YYYY-MM-DD format
    
</dd>
</dl>

<dl>
<dd>

**endDate:** `time.Time` — End date for billing insights in YYYY-MM-DD format. Must be within 31 days of start_date
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Databases
<details><summary><code>client.Databases.ListOptions() -> *godonext.Options</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the options available for the offered database engines, send a GET request to `/v2/databases/options`.
The result will be a JSON object with an `options` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Databases.ListOptions(
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

<details><summary><code>client.Databases.ListClusters() -> *godonext.DatabasesListClustersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the database clusters available on your account, send a GET request to `/v2/databases`. To limit the results to database clusters with a specific tag, include the `tag_name` query parameter set to the name of the tag. For example, `/v2/databases?tag_name=$TAG_NAME`.

The result will be a JSON object with a `databases` key. This will be set to an array of database objects, each of which will contain the standard database attributes.

The embedded `connection` and `private_connection` objects will contain the information needed to access the database cluster. For multi-node clusters, the `standby_connection` and `standby_private_connection` objects will contain the information needed to connect to the cluster's standby node(s).

The embedded `maintenance_window` object will contain information about any scheduled maintenance for the database cluster.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListClustersRequest{
        TagName: godonext.String(
            "production",
        ),
    }
client.Databases.ListClusters(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagName:** `*string` — Limits the results to database clusters with a specific tag.<br><br>Requires `tag:read` scope.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.CreateCluster(request) -> *godonext.DatabasesCreateClusterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a database cluster, send a POST request to `/v2/databases`. To see a list  of options for each engine, such as available regions, size slugs, and versions, send a GET request to the `/v2/databases/options` endpoint. The available sizes for  the `storage_size_mib` field depends on the cluster's size. To see a list of available sizes, see [Managed Database Pricing](https://www.digitalocean.com/pricing/managed-databases).

The create response returns a JSON object with a key called `database`. The value of this is an object that contains the standard attributes associated with a database cluster. The initial value of the database cluster's `status` attribute is `creating`. When the cluster is ready to receive traffic, this changes to `online`.

The embedded `connection` and `private_connection` objects contains the information needed to access the database cluster. For multi-node clusters, the `standby_connection` and `standby_private_connection` objects contain the information needed to connect to the cluster's standby node(s).

DigitalOcean managed PostgreSQL and MySQL database clusters take automated daily backups. To create a new database cluster based on a backup of an existing cluster, send a POST request to `/v2/databases`. In addition to the standard database cluster attributes, the JSON body must include a key named `backup_restore` with the name of the original database cluster and the timestamp of the backup to be restored. Creating a database from a backup is the same as forking a database in the control panel.

PostgreSQL and MySQL Advanced Edition clusters can be provisioned by setting `engine` to `advanced_pg` or `advanced_mysql`. Advanced Edition clusters are currently in public preview and target highly available workloads. `advanced_pg` supports 1-, 2-, and 3-node deployments; `advanced_mysql` only supports 1- and 3-node deployments. See the [PostgreSQL Advanced Edition](https://docs.digitalocean.com/products/databases/postgresql/how-to/use-advanced-edition-clusters/) and [MySQL Advanced Edition](https://docs.digitalocean.com/products/databases/mysql/how-to/use-advanced-edition-clusters/) documentation for the feature differences vs. Standard Edition and current preview limitations.

Note: Caching cluster creates are no longer supported as of 2025-04-30T00:00:00Z. Backups are also not supported for Caching or Valkey clusters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesCreateClusterRequest{
        Name: "backend",
        Engine: godonext.DatabaseClusterEnginePg,
        Version: godonext.String(
            "14",
        ),
        NumNodes: 2,
        Size: "db-s-2vcpu-4gb",
        Region: "nyc3",
        Tags: []string{
            "production",
        },
        StorageSizeMib: godonext.Int(
            61440,
        ),
    }
client.Databases.CreateCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**backupRestore:** `*godonext.DatabaseBackup` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetCluster(DatabaseClusterUUID) -> *godonext.DatabasesGetClusterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing database cluster, send a GET request to `/v2/databases/$DATABASE_ID`.

The response will be a JSON object with a database key. This will be set to an object containing the standard database cluster attributes.

The embedded `connection` and `private_connection` objects will contain the information needed to access the database cluster. For multi-node clusters, the `standby_connection` and `standby_private_connection` objects contain the information needed to connect to the cluster's standby node(s).

The embedded maintenance_window object will contain information about any scheduled maintenance for the database cluster.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetClusterRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DestroyCluster(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy a specific database, send a DELETE request to `/v2/databases/$DATABASE_ID`.
A status of 204 will be given. This indicates that the request was processed successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDestroyClusterRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.DestroyCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetConfig(DatabaseClusterUUID) -> *godonext.DatabasesGetConfigResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Shows configuration parameters for an existing database cluster by sending a GET request to
`/v2/databases/$DATABASE_ID/config`.
The response is a JSON object with a `config` key, which is set to an object
containing any database configuration parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetConfigRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.PatchConfig(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the configuration for an existing database cluster, send a PATCH request to
`/v2/databases/$DATABASE_ID/config`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabaseConfig{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.PatchConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**config:** `*godonext.DatabaseConfigConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetCa(DatabaseClusterUUID) -> *godonext.DatabasesGetCaResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the public certificate used to secure the connection to the database cluster send a GET request to
`/v2/databases/$DATABASE_ID/ca`.

The response will be a JSON object with a `ca` key. This will be set to an object
containing the base64 encoding of the public key certificate.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetCaRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetCa(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetMigrationstatus(DatabaseClusterUUID) -> *godonext.OnlineMigration</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the status of the most recent online migration, send a GET request to `/v2/databases/$DATABASE_ID/online-migration`. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetMigrationStatusRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetMigrationstatus(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateOnlinemigration(DatabaseClusterUUID, request) -> *godonext.OnlineMigration</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To start an online migration, send a PUT request to `/v2/databases/$DATABASE_ID/online-migration` endpoint. Migrating a cluster establishes a connection with an existing cluster and replicates its contents to the target cluster. Online migration is only available for MySQL, PostgreSQL, Caching, and Valkey clusters.
If the existing database is continuously being written to,  the migration process will continue for up to two weeks unless it is manually stopped. Online migration is only available for [MySQL](https://docs.digitalocean.com/products/databases/mysql/how-to/migrate/#:~:text=To%20migrate%20a%20MySQL%20database,then%20select%20Set%20Up%20Migration),  [PostgreSQL](https://docs.digitalocean.com/products/databases/postgresql/how-to/migrate/),  [Caching](https://docs.digitalocean.com/products/databases/redis/how-to/migrate/), and [Valkey](https://docs.digitalocean.com/products/databases/valkey/how-to/migrate/) clusters. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SourceDatabase{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Source: &godonext.SourceDatabaseSource{
            Host: godonext.String(
                "source-do-user-6607903-0.b.db.ondigitalocean.com",
            ),
            Port: godonext.Int(
                25060,
            ),
            Dbname: godonext.String(
                "defaultdb",
            ),
            Username: godonext.String(
                "doadmin",
            ),
            Password: godonext.String(
                "paakjnfe10rsrsmf",
            ),
        },
        DisableSsl: godonext.Bool(
            false,
        ),
        IgnoreDbs: []string{
            "db0",
            "db1",
        },
    }
client.Databases.UpdateOnlinemigration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**source:** `*godonext.SourceDatabaseSource` 
    
</dd>
</dl>

<dl>
<dd>

**disableSsl:** `*bool` — Enables SSL encryption when connecting to the source database.
    
</dd>
</dl>

<dl>
<dd>

**ignoreDbs:** `[]string` — List of databases that should be ignored during migration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteOnlinemigration(DatabaseClusterUUID, MigrationID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To stop an online migration, send a DELETE request to `/v2/databases/$DATABASE_ID/online-migration/$MIGRATION_ID`.

A status of 204 will be given. This indicates that the request was processed successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteOnlineMigrationRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        MigrationID: "77b28fc8-19ff-11eb-8c9c-c68e24557488",
    }
client.Databases.DeleteOnlinemigration(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**migrationID:** `string` — A unique identifier assigned to the online migration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateRegion(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To migrate a database cluster to a new region, send a `PUT` request to
`/v2/databases/$DATABASE_ID/migrate`. The body of the request must specify a
`region` attribute.

A successful request will receive a 202 Accepted status code with no body in
response. Querying the database cluster will show that its `status` attribute
will now be set to `migrating`. This will transition back to `online` when the
migration has completed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateRegionRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Region: "lon1",
    }
client.Databases.UpdateRegion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**region:** `string` — A slug identifier for the region to which the database cluster will be migrated.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateClustersize(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To resize a database cluster, send a PUT request to `/v2/databases/$DATABASE_ID/resize`. The body of the request must specify both the size and num_nodes attributes.
A successful request will receive a 202 Accepted status code with no body in response. Querying the database cluster will show that its status attribute will now be set to resizing. This will transition back to online when the resize operation has completed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabaseClusterResize{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Size: "db-s-4vcpu-8gb",
        NumNodes: 3,
        StorageSizeMib: godonext.Int(
            163840,
        ),
    }
client.Databases.UpdateClustersize(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**size:** `string` — A slug identifier representing desired the size of the nodes in the database cluster.
    
</dd>
</dl>

<dl>
<dd>

**numNodes:** `int` — The number of nodes in the database cluster. Valid values are are 1-3. In addition to the primary node, up to two standby nodes may be added for highly available configurations.
    
</dd>
</dl>

<dl>
<dd>

**storageSizeMib:** `*int` — Additional storage added to the cluster, in MiB. If null, no additional storage is added to the cluster, beyond what is provided as a base amount from the 'size' and any previously added additional storage.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListFirewallRules(DatabaseClusterUUID) -> *godonext.DatabasesListFirewallRulesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of a database cluster's firewall rules (known as "trusted sources" in the control panel), send a GET request to `/v2/databases/$DATABASE_ID/firewall`.
The result will be a JSON object with a `rules` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListFirewallRulesRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListFirewallRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateFirewallRules(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a database cluster's firewall rules (known as "trusted sources" in the control panel), send a PUT request to `/v2/databases/$DATABASE_ID/firewall` specifying which resources should be able to open connections to the database. You may limit connections to specific Droplets, Kubernetes clusters, or IP addresses. When a tag is provided, any Droplet or Kubernetes node with that tag applied to it will have access. The firewall is limited to 100 rules (or trusted sources). When possible, we recommend [placing your databases into a VPC network](https://docs.digitalocean.com/products/networking/vpc/) to limit access to them instead of using a firewall.
A successful
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateFirewallRulesRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Rules: []*godonext.FirewallRule{
            &godonext.FirewallRule{
                Type: godonext.FirewallRuleTypeIPAddr,
                Value: "192.168.1.1",
            },
            &godonext.FirewallRule{
                Type: godonext.FirewallRuleTypeK8S,
                Value: "ff2a6c52-5a44-4b63-b99c-0e98e7a63d61",
            },
            &godonext.FirewallRule{
                Type: godonext.FirewallRuleTypeDroplet,
                Value: "163973392",
            },
            &godonext.FirewallRule{
                Type: godonext.FirewallRuleTypeTag,
                Value: "backend",
                Description: godonext.String(
                    "a backend tag",
                ),
            },
        },
    }
client.Databases.UpdateFirewallRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**rules:** `[]*godonext.FirewallRule` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateMaintenancewindow(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To configure the window when automatic maintenance should be performed for a database cluster, send a PUT request to `/v2/databases/$DATABASE_ID/maintenance`.
A successful request will receive a 204 No Content status code with no body in response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateMaintenanceWindowRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Body: &godonext.DatabaseMaintenanceWindow{
            Day: "tuesday",
            Hour: "14:00",
        },
    }
client.Databases.UpdateMaintenancewindow(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DatabaseMaintenanceWindow` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.InstallUpdate(DatabaseClusterUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To start the installation of updates for a database cluster, send a PUT request to `/v2/databases/$DATABASE_ID/install_update`.
A successful request will receive a 204 No Content status code with no body in response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesInstallUpdateRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.InstallUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListBackups(DatabaseClusterUUID) -> *godonext.DatabasesListBackupsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the available backups of a PostgreSQL or MySQL database cluster, send a GET request to `/v2/databases/$DATABASE_ID/backups`.
**Note**: Backups are not supported for Caching or Valkey clusters.
The result will be a JSON object with a `backups key`. This will be set to an array of backup objects, each of which will contain the size of the backup and the timestamp at which it was created.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListBackupsRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListBackups(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListReplicas(DatabaseClusterUUID) -> *godonext.DatabasesListReplicasResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the read-only replicas associated with a database cluster, send a GET request to `/v2/databases/$DATABASE_ID/replicas`.

**Note**: Read-only replicas are not supported for Caching or Valkey clusters.

The result will be a JSON object with a `replicas` key. This will be set to an array of database replica objects, each of which will contain the standard database replica attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListReplicasRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListReplicas(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.CreateReplica(DatabaseClusterUUID, request) -> *godonext.DatabasesCreateReplicaResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a read-only replica for a PostgreSQL or MySQL database cluster, send a POST request to `/v2/databases/$DATABASE_ID/replicas` specifying the name it should be given, the size of the node to be used, and the region where it will be located.

**Note**: Read-only replicas are not supported for Caching or Valkey clusters.

The response will be a JSON object with a key called `replica`. The value of this will be an object that contains the standard attributes associated with a database replica. The initial value of the read-only replica's `status` attribute will be `forking`. When the replica is ready to receive traffic, this will transition to `active`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabaseReplica{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Name: "read-nyc3-01",
        Region: godonext.String(
            "nyc3",
        ),
        Size: godonext.String(
            "db-s-2vcpu-4gb",
        ),
        StorageSizeMib: godonext.Int(
            61440,
        ),
    }
client.Databases.CreateReplica(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The name to give the read-only replicating
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster.
    
</dd>
</dl>

<dl>
<dd>

**size:** `*string` — A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. <br><br>Requires `tag:create` scope.
    
</dd>
</dl>

<dl>
<dd>

**privateNetworkUUID:** `*string` — A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. <br><br>Requires `vpc:read` scope.
    
</dd>
</dl>

<dl>
<dd>

**connection:** `*godonext.DatabaseReplicaConnection` 
    
</dd>
</dl>

<dl>
<dd>

**privateConnection:** `*godonext.DatabaseReplicaPrivateConnection` 
    
</dd>
</dl>

<dl>
<dd>

**storageSizeMib:** `*int` — Additional storage added to the cluster, in MiB. If null, no additional storage is added to the cluster, beyond what is provided as a base amount from the 'size' and any previously added additional storage.
    
</dd>
</dl>

<dl>
<dd>

**doSettings:** `*godonext.DatabaseReplicaDoSettings` — DigitalOcean-specific settings for the read-only replica, including custom service CNAMEs.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListEventsLogs(DatabaseClusterUUID) -> *godonext.DatabasesListEventsLogsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the cluster events, send a GET request to
`/v2/databases/$DATABASE_ID/events`.

The result will be a JSON object with a `events` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListEventsLogsRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListEventsLogs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetReplica(DatabaseClusterUUID, ReplicaName) -> *godonext.DatabasesGetReplicaResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing database replica, send a GET request to `/v2/databases/$DATABASE_ID/replicas/$REPLICA_NAME`.

**Note**: Read-only replicas are not supported for Caching or Valkey clusters.

The response will be a JSON object with a `replica key`. This will be set to an object containing the standard database replica attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetReplicaRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        ReplicaName: "read-nyc3-01",
    }
client.Databases.GetReplica(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**replicaName:** `string` — The name of the database replica.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DestroyReplica(DatabaseClusterUUID, ReplicaName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy a specific read-only replica, send a DELETE request to `/v2/databases/$DATABASE_ID/replicas/$REPLICA_NAME`.

**Note**: Read-only replicas are not supported for Caching or Valkey clusters.

A status of 204 will be given. This indicates that the request was processed successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDestroyReplicaRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        ReplicaName: "read-nyc3-01",
    }
client.Databases.DestroyReplica(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**replicaName:** `string` — The name of the database replica.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.PromoteReplica(DatabaseClusterUUID, ReplicaName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To promote a specific read-only replica, send a PUT request to `/v2/databases/$DATABASE_ID/replicas/$REPLICA_NAME/promote`.

**Note**: Read-only replicas are not supported for Caching or Valkey clusters.

A status of 204 will be given. This indicates that the request was processed successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesPromoteReplicaRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        ReplicaName: "read-nyc3-01",
    }
client.Databases.PromoteReplica(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**replicaName:** `string` — The name of the database replica.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListUsers(DatabaseClusterUUID) -> *godonext.DatabasesListUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the users for your database cluster, send a GET request to
`/v2/databases/$DATABASE_ID/users`.

Note: User management is not supported for Caching or Valkey clusters.

The result will be a JSON object with a `users` key. This will be set to an array
of database user objects, each of which will contain the standard database user attributes.
User passwords will not show without the `database:view_credentials` scope.

For MySQL clusters, additional options will be contained in the mysql_settings object.

For MongoDB clusters, additional information will be contained in the mongo_user_settings object
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListUsersRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListUsers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.AddUser(DatabaseClusterUUID, request) -> *godonext.DatabasesAddUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add a new database user, send a POST request to `/v2/databases/$DATABASE_ID/users`
with the desired username.

Note: User management is not supported for Caching or Valkey clusters.

When adding a user to a MySQL cluster, additional options can be configured in the
`mysql_settings` object.

When adding a user to a Kafka cluster, additional options can be configured in
the `settings` object.

 When adding a user to a MongoDB cluster, additional options can be configured in
the `settings.mongo_user_settings` object.

The response will be a JSON object with a key called `user`. The value of this will be an
object that contains the standard attributes associated with a database user including
its randomly generated password.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesAddUserRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Name: "app-01",
    }
client.Databases.AddUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**readonly:** `*bool` 

(To be deprecated: use settings.mongo_user_settings.role instead for access controls to MongoDB databases). 
For MongoDB clusters, set to `true` to create a read-only user.
This option is not currently supported for other database engines.
           
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetUser(DatabaseClusterUUID, Username) -> *godonext.DatabasesGetUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing database user, send a GET request to
`/v2/databases/$DATABASE_ID/users/$USERNAME`.

Note: User management is not supported for Caching or Valkey clusters.

The response will be a JSON object with a `user` key. This will be set to an object
containing the standard database user attributes. The user's password will not show
up unless the `database:view_credentials` scope is present.

For MySQL clusters, additional options will be contained in the `mysql_settings`
object.

For Kafka clusters, additional options will be contained in the `settings` object.

For MongoDB clusters, additional information will be contained in the mongo_user_settings object
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetUserRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Username: "app-01",
    }
client.Databases.GetUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` — The name of the database user.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateUser(DatabaseClusterUUID, Username, request) -> *godonext.DatabasesUpdateUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an existing database user, send a PUT request to `/v2/databases/$DATABASE_ID/users/$USERNAME`
with the desired settings.

**Note**: only `settings` can be updated via this type of request. If you wish to change the name of a user,
you must recreate a new user.

The response will be a JSON object with a key called `user`. The value of this will be an
object that contains the name of the update database user, along with the `settings` object that
has been updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateUserRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Username: "app-01",
        Settings: &godonext.UserSettings{
            ACL: []*godonext.UserSettingsACLItem{
                &godonext.UserSettingsACLItem{
                    ID: godonext.String(
                        "acl128aaaa99239",
                    ),
                    Topic: "customer-events",
                    Permission: godonext.UserSettingsACLItemPermissionProduceconsume,
                },
                &godonext.UserSettingsACLItem{
                    ID: godonext.String(
                        "acl293098flskdf",
                    ),
                    Topic: "customer-events.*",
                    Permission: godonext.UserSettingsACLItemPermissionProduce,
                },
                &godonext.UserSettingsACLItem{
                    ID: godonext.String(
                        "acl128ajei20123",
                    ),
                    Topic: "customer-events",
                    Permission: godonext.UserSettingsACLItemPermissionConsume,
                },
            },
        },
    }
client.Databases.UpdateUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` — The name of the database user.
    
</dd>
</dl>

<dl>
<dd>

**settings:** `*godonext.UserSettings` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteUser(DatabaseClusterUUID, Username) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove a specific database user, send a DELETE request to
`/v2/databases/$DATABASE_ID/users/$USERNAME`.

A status of 204 will be given. This indicates that the request was processed
successfully, but that no response body is needed.

Note: User management is not supported for Caching or Valkey clusters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteUserRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Username: "app-01",
    }
client.Databases.DeleteUser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` — The name of the database user.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ResetAuth(DatabaseClusterUUID, Username, request) -> *godonext.DatabasesResetAuthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To reset the password for a database user, send a POST request to
`/v2/databases/$DATABASE_ID/users/$USERNAME/reset_auth`.

For `mysql` databases, the authentication method can be specifying by
including a key in the JSON body called `mysql_settings` with the `auth_plugin`
value specified.

The response will be a JSON object with a `user` key. This will be set to an
object containing the standard database user attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesResetAuthRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Username: "app-01",
        MysqlSettings: &godonext.MysqlSettings{
            AuthPlugin: godonext.MysqlSettingsAuthPluginCachingSha2Password,
        },
    }
client.Databases.ResetAuth(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**username:** `string` — The name of the database user.
    
</dd>
</dl>

<dl>
<dd>

**mysqlSettings:** `*godonext.MysqlSettings` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.List(DatabaseClusterUUID) -> *godonext.DatabasesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the databases in a clusters, send a GET request to
`/v2/databases/$DATABASE_ID/dbs`.

The result will be a JSON object with a `dbs` key. This will be set to an array
of database objects, each of which will contain the standard database attributes.

Note: Database management is not supported for Caching or Valkey clusters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.Add(DatabaseClusterUUID, request) -> *godonext.DatabasesAddResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add a new database to an existing cluster, send a POST request to
`/v2/databases/$DATABASE_ID/dbs`.

Note: Database management is not supported for Caching or Valkey clusters.

The response will be a JSON object with a key called `db`. The value of this will be
an object that contains the standard attributes associated with a database.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesAddRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Body: &godonext.Database{
            Name: "alpha",
        },
    }
client.Databases.Add(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.Database` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.Get(DatabaseClusterUUID, DatabaseName) -> *godonext.DatabasesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing database cluster, send a GET request to
`/v2/databases/$DATABASE_ID/dbs/$DB_NAME`.

Note: Database management is not supported for Caching or Valkey clusters.

The response will be a JSON object with a `db` key. This will be set to an object
containing the standard database attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        DatabaseName: "alpha",
    }
client.Databases.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**databaseName:** `string` — The name of the database.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.Delete(DatabaseClusterUUID, DatabaseName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a specific database, send a DELETE request to
`/v2/databases/$DATABASE_ID/dbs/$DB_NAME`.

A status of 204 will be given. This indicates that the request was processed
successfully, but that no response body is needed.

Note: Database management is not supported for Caching or Valkey clusters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        DatabaseName: "alpha",
    }
client.Databases.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**databaseName:** `string` — The name of the database.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListConnectionpools(DatabaseClusterUUID) -> *godonext.ConnectionPools</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the connection pools available to a PostgreSQL database cluster, send a GET request to `/v2/databases/$DATABASE_ID/pools`.
The result will be a JSON object with a `pools` key. This will be set to an array of connection pool objects.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListConnectionPoolsRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListConnectionpools(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.AddConnectionpool(DatabaseClusterUUID, request) -> *godonext.DatabasesAddConnectionPoolResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

For PostgreSQL database clusters, connection pools can be used to allow a
database to share its idle connections. The popular PostgreSQL connection
pooling utility PgBouncer is used to provide this service. [See here for more information](https://docs.digitalocean.com/products/databases/postgresql/how-to/manage-connection-pools/)
about how and why to use PgBouncer connection pooling including
details about the available transaction modes.

To add a new connection pool to a PostgreSQL database cluster, send a POST
request to `/v2/databases/$DATABASE_ID/pools` specifying a name for the pool,
the user to connect with, the database to connect to, as well as its desired
size and transaction mode.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesAddConnectionPoolRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Body: &godonext.ConnectionPool{
            Name: "backend-pool",
            Mode: "transaction",
            Size: 10,
            Db: "defaultdb",
            User: godonext.String(
                "doadmin",
            ),
        },
    }
client.Databases.AddConnectionpool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ConnectionPool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetConnectionpool(DatabaseClusterUUID, PoolName) -> *godonext.DatabasesGetConnectionPoolResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing connection pool for a PostgreSQL database cluster, send a GET request to `/v2/databases/$DATABASE_ID/pools/$POOL_NAME`.
The response will be a JSON object with a `pool` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetConnectionPoolRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        PoolName: "backend-pool",
    }
client.Databases.GetConnectionpool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**poolName:** `string` — The name used to identify the connection pool.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateConnectionpool(DatabaseClusterUUID, PoolName, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a connection pool for a PostgreSQL database cluster, send a PUT request to  `/v2/databases/$DATABASE_ID/pools/$POOL_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ConnectionPoolUpdate{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        PoolName: "backend-pool",
        Mode: "transaction",
        Size: 10,
        Db: "defaultdb",
        User: godonext.String(
            "doadmin",
        ),
    }
client.Databases.UpdateConnectionpool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**poolName:** `string` — The name used to identify the connection pool.
    
</dd>
</dl>

<dl>
<dd>

**mode:** `string` — The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement.
    
</dd>
</dl>

<dl>
<dd>

**size:** `int` — The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster.
    
</dd>
</dl>

<dl>
<dd>

**db:** `string` — The database for use with the connection pool.
    
</dd>
</dl>

<dl>
<dd>

**user:** `*string` — The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteConnectionpool(DatabaseClusterUUID, PoolName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a specific connection pool for a PostgreSQL database cluster, send
a DELETE request to `/v2/databases/$DATABASE_ID/pools/$POOL_NAME`.

A status of 204 will be given. This indicates that the request was processed
successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteConnectionPoolRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        PoolName: "backend-pool",
    }
client.Databases.DeleteConnectionpool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**poolName:** `string` — The name used to identify the connection pool.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetEvictionpolicy(DatabaseClusterUUID) -> *godonext.DatabasesGetEvictionPolicyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the configured eviction policy for an existing Caching or Valkey cluster, send a GET request to `/v2/databases/$DATABASE_ID/eviction_policy`.
The response will be a JSON object with an `eviction_policy` key. This will be set to a string representing the eviction policy.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetEvictionPolicyRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetEvictionpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateEvictionpolicy(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To configure an eviction policy for an existing Caching or Valkey cluster, send a PUT request to `/v2/databases/$DATABASE_ID/eviction_policy` specifying the desired policy.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateEvictionPolicyRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        EvictionPolicy: godonext.EvictionPolicyModelAllkeysLru,
    }
client.Databases.UpdateEvictionpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**evictionPolicy:** `*godonext.EvictionPolicyModel` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetSQLMode(DatabaseClusterUUID) -> *godonext.SQLMode</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the configured SQL modes for an existing MySQL cluster, send a GET request to `/v2/databases/$DATABASE_ID/sql_mode`.
The response will be a JSON object with a `sql_mode` key. This will be set to a string representing the configured SQL modes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetSQLModeRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetSQLMode(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateSQLMode(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To configure the SQL modes for an existing MySQL cluster, send a PUT request to `/v2/databases/$DATABASE_ID/sql_mode` specifying the desired modes. See the official MySQL 8 documentation for a [full list of supported SQL modes](https://dev.mysql.com/doc/refman/8.0/en/sql-mode.html#sql-mode-full).
A successful request will receive a 204 No Content status code with no body in response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateSQLModeRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Body: &godonext.SQLMode{
            SQLMode: "ANSI,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION,NO_ZERO_DATE,NO_ZERO_IN_DATE",
        },
    }
client.Databases.UpdateSQLMode(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.SQLMode` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateMajorVersion(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To upgrade the major version of a database, send a PUT request to `/v2/databases/$DATABASE_ID/upgrade`, specifying the target version.
A successful request will receive a 204 No Content status code with no body in response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Version2{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Version: godonext.String(
            "14",
        ),
    }
client.Databases.UpdateMajorVersion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**version:** `*godonext.Version` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetAutoscale(DatabaseClusterUUID) -> *godonext.DatabasesGetAutoscaleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the autoscale configuration for an existing database cluster, send a GET request to `/v2/databases/$DATABASE_ID/autoscale`.
The response will be a JSON object with autoscaling configuration details.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetAutoscaleRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetAutoscale(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateAutoscale(DatabaseClusterUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To configure autoscale settings for an existing database cluster, send a PUT request to `/v2/databases/$DATABASE_ID/autoscale`, specifying the autoscale configuration.
A successful request will receive a 204 No Content status code with no body in response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateAutoscaleRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Body: &godonext.DatabaseAutoscaleParams{
            Storage: &godonext.DatabaseAutoscaleParamsStorage{
                Enabled: true,
                ThresholdPercent: godonext.Int(
                    80,
                ),
                IncrementGib: godonext.Int(
                    10,
                ),
            },
        },
    }
client.Databases.UpdateAutoscale(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DatabaseAutoscaleParams` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListKafkaTopics(DatabaseClusterUUID) -> *godonext.DatabasesListKafkaTopicsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of a Kafka cluster's topics, send a GET request to
`/v2/databases/$DATABASE_ID/topics`.

The result will be a JSON object with a `topics` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListKafkaTopicsRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListKafkaTopics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.CreateKafkaTopic(DatabaseClusterUUID, request) -> *godonext.DatabasesCreateKafkaTopicResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a topic attached to a Kafka cluster, send a POST request to
`/v2/databases/$DATABASE_ID/topics`.

The result will be a JSON object with a `topic` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KafkaTopicCreate{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Name: godonext.String(
            "customer-events",
        ),
        Config: &godonext.KafkaTopicConfig{
            RetentionBytes: godonext.Int(
                -1,
            ),
            RetentionMs: godonext.Int(
                100000,
            ),
        },
    }
client.Databases.CreateKafkaTopic(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**config:** `*godonext.KafkaTopicConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetKafkaTopic(DatabaseClusterUUID, TopicName) -> *godonext.DatabasesGetKafkaTopicResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a given topic by name from the set of a Kafka cluster's topics,
send a GET request to `/v2/databases/$DATABASE_ID/topics/$TOPIC_NAME`.

The result will be a JSON object with a `topic` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetKafkaTopicRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        TopicName: "customer-events",
    }
client.Databases.GetKafkaTopic(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**topicName:** `string` — The name used to identify the Kafka topic.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateKafkaTopic(DatabaseClusterUUID, TopicName, request) -> *godonext.DatabasesUpdateKafkaTopicResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a topic attached to a Kafka cluster, send a PUT request to
`/v2/databases/$DATABASE_ID/topics/$TOPIC_NAME`.

The result will be a JSON object with a `topic` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KafkaTopicUpdate{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        TopicName: "customer-events",
        Config: &godonext.KafkaTopicConfig{
            RetentionBytes: godonext.Int(
                -1,
            ),
            RetentionMs: godonext.Int(
                100000,
            ),
        },
    }
client.Databases.UpdateKafkaTopic(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**topicName:** `string` — The name used to identify the Kafka topic.
    
</dd>
</dl>

<dl>
<dd>

**replicationFactor:** `*int` — The number of nodes to replicate data across the cluster.
    
</dd>
</dl>

<dl>
<dd>

**partitionCount:** `*int` — The number of partitions available for the topic. On update, this value can only be increased.
    
</dd>
</dl>

<dl>
<dd>

**config:** `*godonext.KafkaTopicConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteKafkaTopic(DatabaseClusterUUID, TopicName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a single topic within a Kafka cluster, send a DELETE request
to `/v2/databases/$DATABASE_ID/topics/$TOPIC_NAME`.

A status of 204 will be given. This indicates that the request was
processed successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteKafkaTopicRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        TopicName: "customer-events",
    }
client.Databases.DeleteKafkaTopic(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**topicName:** `string` — The name used to identify the Kafka topic.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListLogsink(DatabaseClusterUUID) -> *godonext.DatabasesListLogsinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list logsinks for a database cluster, send a GET request to
`/v2/databases/$DATABASE_ID/logsink`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListLogsinkRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.CreateLogsink(DatabaseClusterUUID, request) -> *godonext.DatabasesCreateLogsinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create logsink for a database cluster, send a POST request to
`/v2/databases/$DATABASE_ID/logsink`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LogsinkCreate{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SinkName: godonext.String(
            "logs-sink",
        ),
        SinkType: godonext.LogsinkBaseSinkTypeOpensearch.Ptr(),
        Config: &godonext.LogsinkCreateConfig{
            ElasticsearchLogsink: &godonext.ElasticsearchLogsink{
                URL: "https://user:passwd@192.168.0.1:25060",
                IndexPrefix: "opensearch-logs",
                IndexDaysMax: godonext.Int(
                    5,
                ),
            },
        },
    }
client.Databases.CreateLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**config:** `*godonext.LogsinkCreateConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetLogsink(DatabaseClusterUUID, LogsinkID) -> godonext.LogsinkSchema</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a logsink for a database cluster, send a GET request to
`/v2/databases/$DATABASE_ID/logsink/$LOGSINK_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetLogsinkRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        LogsinkID: "50484ec3-19d6-4cd3-b56f-3b0381c289a6",
    }
client.Databases.GetLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**logsinkID:** `string` — A unique identifier for a logsink of a database cluster
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateLogsink(DatabaseClusterUUID, LogsinkID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a logsink for a database cluster, send a PUT request to
`/v2/databases/$DATABASE_ID/logsink/$LOGSINK_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LogsinkUpdate{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        LogsinkID: "50484ec3-19d6-4cd3-b56f-3b0381c289a6",
        Config: &godonext.LogsinkUpdateConfig{
            RsyslogLogsink: &godonext.RsyslogLogsink{
                Server: "192.168.0.1",
                Port: 514,
                TLS: false,
                Format: godonext.RsyslogLogsinkFormatRfc3164,
            },
        },
    }
client.Databases.UpdateLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**logsinkID:** `string` — A unique identifier for a logsink of a database cluster
    
</dd>
</dl>

<dl>
<dd>

**config:** `*godonext.LogsinkUpdateConfig` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteLogsink(DatabaseClusterUUID, LogsinkID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a logsink for a database cluster, send a DELETE request to
`/v2/databases/$DATABASE_ID/logsink/$LOGSINK_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteLogsinkRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        LogsinkID: "50484ec3-19d6-4cd3-b56f-3b0381c289a6",
    }
client.Databases.DeleteLogsink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**logsinkID:** `string` — A unique identifier for a logsink of a database cluster
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListKafkaSchemas(DatabaseClusterUUID) -> *godonext.DatabasesListKafkaSchemasResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all schemas for a Kafka cluster, send a GET request to
`/v2/databases/$DATABASE_ID/schema-registry`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListKafkaSchemasRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListKafkaSchemas(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.CreateKafkaSchema(DatabaseClusterUUID, request) -> *godonext.KafkaSchemaVerbose</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a Kafka schema for a database cluster, send a POST request to
`/v2/databases/$DATABASE_ID/schema-registry`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabaseKafkaSchemaCreate{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SubjectName: godonext.String(
            "customer-schema",
        ),
        SchemaType: godonext.DatabaseKafkaSchemaCreateSchemaTypeAvro.Ptr(),
        Schema: godonext.String(
            `{
              "type": "record",
              "name": "Customer",
              "fields": [
                {"name": "id", "type": "string"},
                {"name": "name", "type": "string"},
                {"name": "email", "type": "string"},
                {"name": "created_at", "type": "long"}
              ]
            }
            `,
        ),
    }
client.Databases.CreateKafkaSchema(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `*string` — The name of the schema subject.
    
</dd>
</dl>

<dl>
<dd>

**schemaType:** `*godonext.DatabaseKafkaSchemaCreateSchemaType` — The type of the schema.
    
</dd>
</dl>

<dl>
<dd>

**schema:** `*string` — The schema definition in the specified format.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetKafkaSchema(DatabaseClusterUUID, SubjectName) -> *godonext.KafkaSchemaVersionVerbose</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a specific schema by subject name for a Kafka cluster, send a GET request to
`/v2/databases/$DATABASE_ID/schema-registry/$SUBJECT_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetKafkaSchemaRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SubjectName: "customer-schema",
    }
client.Databases.GetKafkaSchema(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` — The name of the Kafka schema subject.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteKafkaSchema(DatabaseClusterUUID, SubjectName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a specific schema by subject name for a Kafka cluster, send a DELETE request to
`/v2/databases/$DATABASE_ID/schema-registry/$SUBJECT_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteKafkaSchemaRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SubjectName: "customer-schema",
    }
client.Databases.DeleteKafkaSchema(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` — The name of the Kafka schema subject.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetKafkaSchemaVersion(DatabaseClusterUUID, SubjectName, Version) -> *godonext.KafkaSchemaVersionVerbose</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a specific schema by subject name for a Kafka cluster, send a GET request to
`/v2/databases/$DATABASE_ID/schema-registry/$SUBJECT_NAME/versions/$VERSION`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetKafkaSchemaVersionRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SubjectName: "customer-schema",
        Version: "1",
    }
client.Databases.GetKafkaSchemaVersion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` — The name of the Kafka schema subject.
    
</dd>
</dl>

<dl>
<dd>

**version:** `string` — The version of the Kafka schema subject.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetKafkaSchemaConfig(DatabaseClusterUUID) -> *godonext.DatabasesGetKafkaSchemaConfigResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the Schema Registry configuration for a Kafka cluster, send a GET request to
`/v2/databases/$DATABASE_ID/schema-registry/config`.
The response is a JSON object with a `compatibility_level` key, which is set to an object
containing any database configuration parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetKafkaSchemaConfigRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.GetKafkaSchemaConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateKafkaSchemaConfig(DatabaseClusterUUID, request) -> *godonext.DatabasesUpdateKafkaSchemaConfigResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the Schema Registry configuration for a Kafka cluster, send a PUT request to
`/v2/databases/$DATABASE_ID/schema-registry/config`.
The response is a JSON object with a `compatibility_level` key, which is set to an object
containing any database configuration parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateKafkaSchemaConfigRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        CompatibilityLevel: godonext.DatabasesUpdateKafkaSchemaConfigRequestCompatibilityLevelBackward,
    }
client.Databases.UpdateKafkaSchemaConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**compatibilityLevel:** `*godonext.DatabasesUpdateKafkaSchemaConfigRequestCompatibilityLevel` — The compatibility level of the schema registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetKafkaSchemaSubjectConfig(DatabaseClusterUUID, SubjectName) -> *godonext.DatabasesGetKafkaSchemaSubjectConfigResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the Schema Registry configuration for a Subject of a Kafka cluster, send a GET request to
`/v2/databases/$DATABASE_ID/schema-registry/config/$SUBJECT_NAME`.
The response is a JSON object with a `compatibility_level` key, which is set to an object
containing any database configuration parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesGetKafkaSchemaSubjectConfigRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SubjectName: "customer-schema",
    }
client.Databases.GetKafkaSchemaSubjectConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` — The name of the Kafka schema subject.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.UpdateKafkaSchemaSubjectConfig(DatabaseClusterUUID, SubjectName, request) -> *godonext.DatabasesUpdateKafkaSchemaSubjectConfigResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the Schema Registry configuration for a Subject of a Kafka cluster, send a PUT request to
`/v2/databases/$DATABASE_ID/schema-registry/config/$SUBJECT_NAME`.
The response is a JSON object with a `compatibility_level` key, which is set to an object
containing any database configuration parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesUpdateKafkaSchemaSubjectConfigRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        SubjectName: "customer-schema",
        CompatibilityLevel: godonext.DatabasesUpdateKafkaSchemaSubjectConfigRequestCompatibilityLevelBackward,
    }
client.Databases.UpdateKafkaSchemaSubjectConfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**subjectName:** `string` — The name of the Kafka schema subject.
    
</dd>
</dl>

<dl>
<dd>

**compatibilityLevel:** `*godonext.DatabasesUpdateKafkaSchemaSubjectConfigRequestCompatibilityLevel` — The compatibility level of the schema registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.GetClusterMetricsCredentials() -> *godonext.DatabasesGetClusterMetricsCredentialsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show the credentials for all database clusters' metrics endpoints, send a GET request to `/v2/databases/metrics/credentials`. The result will be a JSON object with a `credentials` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Databases.GetClusterMetricsCredentials(
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

<details><summary><code>client.Databases.UpdateClusterMetricsCredentials(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the credentials for all database clusters' metrics endpoints, send a PUT request to `/v2/databases/metrics/credentials`. A successful request will receive a 204 No Content status code  with no body in response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabaseMetricsCredentials{
        Credentials: &godonext.DatabasesBasicAuthCredentials{
            BasicAuthUsername: godonext.String(
                "new_username",
            ),
            BasicAuthPassword: godonext.String(
                "new_password",
            ),
        },
    }
client.Databases.UpdateClusterMetricsCredentials(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.DatabaseMetricsCredentials` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.ListOpeasearchIndexes(DatabaseClusterUUID) -> *godonext.DatabasesListOpeasearchIndexesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of a OpenSearch cluster's indexes, send a GET request to
`/v2/databases/$DATABASE_ID/indexes`.

The result will be a JSON object with a `indexes` key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesListOpeasearchIndexesRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
    }
client.Databases.ListOpeasearchIndexes(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Databases.DeleteOpensearchIndex(DatabaseClusterUUID, IndexName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a single index within OpenSearch cluster, send a DELETE request
to `/v2/databases/$DATABASE_ID/indexes/$INDEX_NAME`.

A status of 204 will be given. This indicates that the request was
processed successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DatabasesDeleteOpensearchIndexRequest{
        DatabaseClusterUUID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        IndexName: "logs-*",
    }
client.Databases.DeleteOpensearchIndex(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseClusterUUID:** `string` — A unique identifier for a database cluster.
    
</dd>
</dl>

<dl>
<dd>

**indexName:** `string` — The name of the OpenSearch index.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Dedicated Inference
<details><summary><code>client.DedicatedInference.DedicatedInferencesGet(DedicatedInferenceID) -> *godonext.DedicatedInferencesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve an existing Dedicated Inference by ID. Send a GET request to
`/v2/dedicated-inferences/{dedicated_inference_id}`. The status in the response
is one of active, new, provisioning, updating, deleting, or error.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesGetRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
    }
client.DedicatedInference.DedicatedInferencesGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesDelete(DedicatedInferenceID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an existing Dedicated Inference. Send a DELETE request to
`/v2/dedicated-inferences/{dedicated_inference_id}`. The response 202 Accepted
indicates the request was accepted for processing.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesDeleteRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
    }
client.DedicatedInference.DedicatedInferencesDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesPatch(DedicatedInferenceID, request) -> *godonext.DedicatedInferencesPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing Dedicated Inference. Send a PATCH request to
`/v2/dedicated-inferences/{dedicated_inference_id}` with updated `spec` and/or
`access_tokens`. Status will move to updating and return to active when done.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferenceUpdateRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
    }
client.DedicatedInference.DedicatedInferencesPatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>

<dl>
<dd>

**spec:** `*godonext.DedicatedInferenceSpec` 
    
</dd>
</dl>

<dl>
<dd>

**accessTokens:** `*godonext.DedicatedInferenceUpdateRequestAccessTokens` — Provider tokens for model access (e.g. gated Hugging Face models).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesList() -> *godonext.DedicatedInferencesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all Dedicated Inference instances for your team. Send a GET request to
`/v2/dedicated-inferences`. You may filter by region and use page and per_page
for pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesListRequest{}
client.DedicatedInference.DedicatedInferencesList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.DedicatedInferencesListRequestRegion` — Filter by region. Dedicated Inference is only available in nyc2, tor1, and atl1.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesCreate(request) -> *godonext.DedicatedInferencesCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new Dedicated Inference for your team. Send a POST request to
`/v2/dedicated-inferences` with a `spec` object (version, name, region, vpc,
enable_public_endpoint, model_deployments) and optional `access_tokens` (e.g.
hugging_face_token for gated models). The response code 202 Accepted indicates
the request was accepted for processing; it does not indicate success or failure.
The token value is returned only on create; store it securely.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferenceCreateRequest{
        Spec: &godonext.DedicatedInferenceSpec{
            Version: 1,
            Name: "new-dedicated-inference",
            Region: godonext.DedicatedInferenceSpecRegionAtl1,
            Vpc: &godonext.DedicatedInferenceSpecVpc{
                UUID: "997615ce-132d-4bae-9270-9ee21b395e5d",
            },
            EnablePublicEndpoint: true,
            ModelDeployments: []*godonext.ModelDeploymentSpec{
                &godonext.ModelDeploymentSpec{},
            },
        },
    }
client.DedicatedInference.DedicatedInferencesCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**spec:** `*godonext.DedicatedInferenceSpec` 
    
</dd>
</dl>

<dl>
<dd>

**accessTokens:** `map[string]string` — Key-value pairs for provider tokens (e.g. Hugging Face).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesListAccelerators(DedicatedInferenceID) -> *godonext.DedicatedInferencesListAcceleratorsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all accelerators (GPUs) in use by a Dedicated Inference instance. Send a
GET request to `/v2/dedicated-inferences/{dedicated_inference_id}/accelerators`.
Optionally filter by slug and use page/per_page for pagination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesListAcceleratorsRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
        Slug: godonext.String(
            "gpu-mi300x1-192gb",
        ),
    }
client.DedicatedInference.DedicatedInferencesListAccelerators(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**slug:** `*string` — Filter accelerators by GPU slug.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesGetAccelerator(DedicatedInferenceID, AcceleratorID) -> *godonext.DedicatedInferenceAccelerator</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a single accelerator by ID for a Dedicated Inference instance. Send a
GET request to `/v2/dedicated-inferences/{dedicated_inference_id}/accelerators/{accelerator_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesGetAcceleratorRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
        AcceleratorID: "5b5c619c-359c-44ca-87e2-47e98170c02f",
    }
client.DedicatedInference.DedicatedInferencesGetAccelerator(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>

<dl>
<dd>

**acceleratorID:** `string` — A unique identifier for a Dedicated Inference accelerator.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesGetCa(DedicatedInferenceID) -> *godonext.DedicatedInferencesGetCaResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get the CA certificate for a Dedicated Inference instance (base64-encoded).
Required for private endpoint connectivity. Send a GET request to
`/v2/dedicated-inferences/{dedicated_inference_id}/ca`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesGetCaRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
    }
client.DedicatedInference.DedicatedInferencesGetCa(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesListTokens(DedicatedInferenceID) -> *godonext.DedicatedInferencesListTokensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all access tokens for a Dedicated Inference instance. Token values are
not returned; only id, name, created_at, and is_managed. Send a GET request to
`/v2/dedicated-inferences/{dedicated_inference_id}/tokens`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesListTokensRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
    }
client.DedicatedInference.DedicatedInferencesListTokens(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesCreateTokens(DedicatedInferenceID, request) -> *godonext.DedicatedInferencesCreateTokensResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new access token for a Dedicated Inference instance. Send a POST
request to `/v2/dedicated-inferences/{dedicated_inference_id}/tokens` with a
`name`. The token value is returned only once in the response; store it securely.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferenceTokenCreateRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
        Name: "new-inference-token",
    }
client.DedicatedInference.DedicatedInferencesCreateTokens(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — Name for the new token.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesDeleteTokens(DedicatedInferenceID, TokenID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke (delete) an access token for a Dedicated Inference instance. Send a
DELETE request to `/v2/dedicated-inferences/{dedicated_inference_id}/tokens/{token_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DedicatedInferencesDeleteTokensRequest{
        DedicatedInferenceID: "6b5c619c-359c-44ca-87e2-47e98170c01d",
        TokenID: "f11d4795-c1db-4ac3-9aa6-a0ea3c58877e",
    }
client.DedicatedInference.DedicatedInferencesDeleteTokens(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dedicatedInferenceID:** `string` — A unique identifier for a Dedicated Inference instance.
    
</dd>
</dl>

<dl>
<dd>

**tokenID:** `string` — A unique identifier for a Dedicated Inference access token.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DedicatedInference.DedicatedInferencesListSizes() -> *godonext.DedicatedInferenceSizesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get available Dedicated Inference sizes and pricing for supported GPUs. Send a
GET request to `/v2/dedicated-inferences/sizes`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DedicatedInference.DedicatedInferencesListSizes(
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

<details><summary><code>client.DedicatedInference.DedicatedInferencesGetGpuModelConfig() -> *godonext.DedicatedInferenceGpuModelConfigsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get supported GPU and model configurations for Dedicated Inference. Use this to
discover supported GPU slugs and model slugs (e.g. Hugging Face). Send a GET
request to `/v2/dedicated-inferences/gpu-model-config`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.DedicatedInference.DedicatedInferencesGetGpuModelConfig(
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

## Domains
<details><summary><code>client.Domains.List() -> *godonext.DomainsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all of the domains in your account, send a GET request to `/v2/domains`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsListRequest{}
client.Domains.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Domains.Create(request) -> *godonext.DomainsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new domain, send a POST request to `/v2/domains`. Set the "name"
attribute to the domain name you are adding. Optionally, you may set the
"ip_address" attribute, and an A record will be automatically created pointing
to the apex domain.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Domain{
        Name: godonext.String(
            "example.com",
        ),
    }
client.Domains.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.Domain` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Domains.Get(DomainName) -> *godonext.DomainsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get details about a specific domain, send a GET request to `/v2/domains/$DOMAIN_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsGetRequest{
        DomainName: "example.com",
    }
client.Domains.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Domains.Delete(DomainName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a domain, send a DELETE request to `/v2/domains/$DOMAIN_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsDeleteRequest{
        DomainName: "example.com",
    }
client.Domains.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Domain Records
<details><summary><code>client.DomainRecords.DomainsListRecords(DomainName) -> *godonext.DomainsListRecordsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a listing of all records configured for a domain, send a GET request to `/v2/domains/$DOMAIN_NAME/records`.
The list of records returned can be filtered by using the `name` and `type` query parameters. For example, to only include A records for a domain, send a GET request to `/v2/domains/$DOMAIN_NAME/records?type=A`. `name` must be a fully qualified record name. For example, to only include records matching `sub.example.com`, send a GET request to `/v2/domains/$DOMAIN_NAME/records?name=sub.example.com`. Both name and type may be used together.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsListRecordsRequest{
        DomainName: "example.com",
        Name: godonext.String(
            "sub.example.com",
        ),
    }
client.DomainRecords.DomainsListRecords(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — A fully qualified record name. For example, to only include records matching sub.example.com, send a GET request to `/v2/domains/$DOMAIN_NAME/records?name=sub.example.com`.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.DomainsListRecordsRequestType` — The type of the DNS record. For example: A, CNAME, TXT, ...
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DomainRecords.DomainsCreateRecord(DomainName, request) -> *godonext.DomainsCreateRecordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new record to a domain, send a POST request to
`/v2/domains/$DOMAIN_NAME/records`.

The request must include all of the required fields for the domain record type
being added.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective required attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsCreateRecordRequest{
        DomainName: "example.com",
        Body: &godonext.DomainsCreateRecordRequestBody{
            DomainRecordA: &godonext.DomainRecordA{
                Type: "A",
                Name: "www",
                Data: "162.10.66.0",
                TTL: godonext.Int(
                    1800,
                ),
            },
        },
    }
client.DomainRecords.DomainsCreateRecord(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DomainsCreateRecordRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DomainRecords.DomainsGetRecord(DomainName, DomainRecordID) -> *godonext.DomainsGetRecordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a specific domain record, send a GET request to `/v2/domains/$DOMAIN_NAME/records/$RECORD_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsGetRecordRequest{
        DomainName: "example.com",
        DomainRecordID: 1,
    }
client.DomainRecords.DomainsGetRecord(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `int` — The unique identifier of the domain record.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DomainRecords.DomainsUpdateRecord(DomainName, DomainRecordID, request) -> *godonext.DomainsUpdateRecordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an existing record, send a PUT request to
`/v2/domains/$DOMAIN_NAME/records/$DOMAIN_RECORD_ID`. Any attribute valid for
the record type can be set to a new value for the record.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsUpdateRecordRequest{
        DomainName: "example.com",
        DomainRecordID: 1,
        Body: &godonext.DomainRecord{
            Type: "CNAME",
            Name: godonext.String(
                "blog",
            ),
        },
    }
client.DomainRecords.DomainsUpdateRecord(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `int` — The unique identifier of the domain record.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DomainRecord` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DomainRecords.DomainsDeleteRecord(DomainName, DomainRecordID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a record for a domain, send a DELETE request to
`/v2/domains/$DOMAIN_NAME/records/$DOMAIN_RECORD_ID`.

The record will be deleted and the response status will be a 204. This
indicates a successful request with no body returned.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsDeleteRecordRequest{
        DomainName: "example.com",
        DomainRecordID: 1,
    }
client.DomainRecords.DomainsDeleteRecord(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `int` — The unique identifier of the domain record.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DomainRecords.DomainsPatchRecord(DomainName, DomainRecordID, request) -> *godonext.DomainsPatchRecordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an existing record, send a PATCH request to
`/v2/domains/$DOMAIN_NAME/records/$DOMAIN_RECORD_ID`. Any attribute valid for
the record type can be set to a new value for the record.

See the [attribute table](#tag/Domain-Records) for details regarding record
types and their respective attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DomainsPatchRecordRequest{
        DomainName: "example.com",
        DomainRecordID: 1,
        Body: &godonext.DomainRecord{
            Type: "A",
            Name: godonext.String(
                "blog",
            ),
        },
    }
client.DomainRecords.DomainsPatchRecord(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**domainName:** `string` — The name of the domain itself.
    
</dd>
</dl>

<dl>
<dd>

**domainRecordID:** `int` — The unique identifier of the domain record.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DomainRecord` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Droplets
<details><summary><code>client.Droplets.List() -> *godonext.DropletsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all Droplets in your account, send a GET request to `/v2/droplets`.

The response body will be a JSON object with a key of `droplets`. This will be
set to an array containing objects each representing a Droplet. These will
contain the standard Droplet attributes.

### Filtering Results by Tag

It's possible to request filtered results by including certain query parameters.
To only list Droplets assigned to a specific tag, include the `tag_name` query
parameter set to the name of the tag in your GET request. For example,
`/v2/droplets?tag_name=$TAG_NAME`.

### GPU Droplets

By default, only non-GPU Droplets are returned. To list only GPU Droplets, set
the `type` query parameter to `gpus`. For example, `/v2/droplets?type=gpus`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListRequest{
        TagName: godonext.String(
            "env:prod",
        ),
        Name: godonext.String(
            "web-01",
        ),
    }
client.Droplets.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**tagName:** `*string` — Used to filter Droplets by a specific tag. Can not be combined with `name` or `type`.<br>Requires `tag:read` scope.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Used to filter list response by Droplet name returning only exact matches. It is case-insensitive and can not be combined with `tag_name`.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.DropletsListRequestType` — When `type` is set to `gpus`, only GPU Droplets will be returned. By default, only non-GPU Droplets are returned. Can not be combined with `tag_name`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.Create(request) -> *godonext.DropletsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new Droplet, send a POST request to `/v2/droplets` setting the
required attributes.

A Droplet will be created using the provided information. The response body
will contain a JSON object with a key called `droplet`. The value will be an
object containing the standard attributes for your new Droplet. The response
code, 202 Accepted, does not indicate the success or failure of the operation,
just that the request has been accepted for processing. The `actions` returned
as part of the response's `links` object can be used to check the status
of the Droplet create event.

### Create Multiple Droplets

Creating multiple Droplets is very similar to creating a single Droplet.
Instead of sending `name` as a string, send `names` as an array of strings. A
Droplet will be created for each name you send using the associated
information. Up to ten Droplets may be created this way at a time.

Rather than returning a single Droplet, the response body will contain a JSON
array with a key called `droplets`. This will be set to an array of JSON
objects, each of which will contain the standard Droplet attributes. The
response code, 202 Accepted, does not indicate the success or failure of any
operation, just that the request has been accepted for processing. The array
of `actions` returned as part of the response's `links` object can be used to
check the status of each individual Droplet create event.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsCreateRequest{
        DropletSingleCreate: &godonext.DropletSingleCreate{
            Region: godonext.String(
                "nyc3",
            ),
            Size: "s-1vcpu-1gb",
            Image: &godonext.DropletCreateImage{
                String: "ubuntu-20-04-x64",
            },
            SSHKeys: []*godonext.DropletCreateSSHKeysItem{
                &godonext.DropletCreateSSHKeysItem{
                    Integer: 289794,
                },
                &godonext.DropletCreateSSHKeysItem{
                    String: "3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45",
                },
            },
            Backups: godonext.Bool(
                true,
            ),
            Ipv6: godonext.Bool(
                true,
            ),
            Monitoring: godonext.Bool(
                true,
            ),
            Tags: []string{
                "env:prod",
                "web",
            },
            UserData: godonext.String(
                `#cloud-config
                runcmd:
                  - touch /test.txt
                `,
            ),
            VpcUUID: godonext.String(
                "760e09ef-dc84-11e8-981e-3cfdfeaae000",
            ),
            Name: "example.com",
        },
    }
client.Droplets.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.DropletsCreateRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.DestroyBytag() -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete **all** Droplets assigned to a specific tag, include the `tag_name`
query parameter set to the name of the tag in your DELETE request. For
example, `/v2/droplets?tag_name=$TAG_NAME`.

This endpoint requires `tag:read` scope.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsDestroyByTagRequest{
        TagName: "env:test",
    }
client.Droplets.DestroyBytag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagName:** `string` — Specifies Droplets to be deleted by tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.Get(DropletID) -> *godonext.DropletsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an individual Droplet, send a GET request to
`/v2/droplets/$DROPLET_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsGetRequest{
        DropletID: 1,
    }
client.Droplets.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.Destroy(DropletID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a Droplet, send a DELETE request to `/v2/droplets/$DROPLET_ID`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsDestroyRequest{
        DropletID: 1,
    }
client.Droplets.Destroy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListBackups(DropletID) -> *godonext.DropletsListBackupsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve any backups associated with a Droplet, send a GET request to
`/v2/droplets/$DROPLET_ID/backups`.

You will get back a JSON object that has a `backups` key. This will be set to
an array of backup objects, each of which contain the standard
Droplet backup attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListBackupsRequest{
        DropletID: 1,
    }
client.Droplets.ListBackups(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.GetBackupPolicy(DropletID) -> *godonext.DropletsGetBackupPolicyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an individual Droplet's backup policy, send a GET
request to `/v2/droplets/$DROPLET_ID/backups/policy`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsGetBackupPolicyRequest{
        DropletID: 1,
    }
client.Droplets.GetBackupPolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListBackupPolicies() -> *godonext.DropletsListBackupPoliciesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list information about the backup policies for all Droplets in the account,
send a GET request to `/v2/droplets/backups/policies`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListBackupPoliciesRequest{}
client.Droplets.ListBackupPolicies(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListSupportedBackupPolicies() -> *godonext.DropletsListSupportedBackupPoliciesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all supported Droplet backup policies, send a GET
request to `/v2/droplets/backups/supported_policies`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Droplets.ListSupportedBackupPolicies(
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

<details><summary><code>client.Droplets.ListSnapshots(DropletID) -> *godonext.DropletsListSnapshotsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the snapshots that have been created from a Droplet, send a GET
request to `/v2/droplets/$DROPLET_ID/snapshots`.

You will get back a JSON object that has a `snapshots` key. This will be set
to an array of snapshot objects, each of which contain the standard Droplet
snapshot attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListSnapshotsRequest{
        DropletID: 1,
    }
client.Droplets.ListSnapshots(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListKernels(DropletID) -> *godonext.DropletsListKernelsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all kernels available to a Droplet, send a GET request
to `/v2/droplets/$DROPLET_ID/kernels`

The response will be a JSON object that has a key called `kernels`. This will
be set to an array of `kernel` objects, each of which contain the standard
`kernel` attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListKernelsRequest{
        DropletID: 1,
    }
client.Droplets.ListKernels(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListFirewalls(DropletID) -> *godonext.DropletsListFirewallsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all firewalls available to a Droplet, send a GET request
to `/v2/droplets/$DROPLET_ID/firewalls`

The response will be a JSON object that has a key called `firewalls`. This will
be set to an array of `firewall` objects, each of which contain the standard
`firewall` attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListFirewallsRequest{
        DropletID: 1,
    }
client.Droplets.ListFirewalls(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListNeighbors(DropletID) -> *godonext.DropletsListNeighborsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of any "neighbors" (i.e. Droplets that are co-located on
the same physical hardware) for a specific Droplet, send a GET request to
`/v2/droplets/$DROPLET_ID/neighbors`.

The results will be returned as a JSON object with a key of `droplets`. This
will be set to an array containing objects representing any other Droplets
that share the same physical hardware. An empty array indicates that the
Droplet is not co-located any other Droplets associated with your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListNeighborsRequest{
        DropletID: 1,
    }
client.Droplets.ListNeighbors(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListAssociatedresources(DropletID) -> *godonext.DropletsListAssociatedResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list the associated billable resources that can be destroyed along with a
Droplet, send a GET request to the
`/v2/droplets/$DROPLET_ID/destroy_with_associated_resources` endpoint.

This endpoint will only return resources that you are authorized to see. For
example, to see associated Reserved IPs, include the `reserved_ip:read` scope.

The response will be a JSON object containing `snapshots`, `volumes`, and
`volume_snapshots` keys. Each will be set to an array of objects containing
information about the associated resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsListAssociatedResourcesRequest{
        DropletID: 1,
    }
client.Droplets.ListAssociatedresources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.DestroyWithassociatedresourcesselective(DropletID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy a Droplet along with a sub-set of its associated resources, send a
DELETE request to the `/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/selective`
endpoint. The JSON body of the request should include `reserved_ips`, `snapshots`, `volumes`,
or `volume_snapshots` keys each set to an array of IDs for the associated
resources to be destroyed. The IDs can be found by querying the Droplet's
associated resources. Any associated resource not included in the request
will remain and continue to accrue changes on your account.

A successful response will include a 202 response code and no content. Use
the status endpoint to check on the success or failure of the destruction of
the individual resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SelectiveDestroyAssociatedResource{
        DropletID: 1,
    }
client.Droplets.DestroyWithassociatedresourcesselective(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**floatingIps:** `[]string` — An array of unique identifiers for the floating IPs to be scheduled for deletion.
    
</dd>
</dl>

<dl>
<dd>

**reservedIps:** `[]string` — An array of unique identifiers for the reserved IPs to be scheduled for deletion.
    
</dd>
</dl>

<dl>
<dd>

**snapshots:** `[]string` — An array of unique identifiers for the snapshots to be scheduled for deletion.
    
</dd>
</dl>

<dl>
<dd>

**volumes:** `[]string` — An array of unique identifiers for the volumes to be scheduled for deletion.
    
</dd>
</dl>

<dl>
<dd>

**volumeSnapshots:** `[]string` — An array of unique identifiers for the volume snapshots to be scheduled for deletion.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.DestroyWithassociatedresourcesdangerous(DropletID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy a Droplet along with all of its associated resources, send a DELETE
request to the `/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/dangerous`
endpoint. The headers of this request must include an `X-Dangerous` key set to
`true`. To preview which resources will be destroyed, first query the
Droplet's associated resources. This operation _can not_ be reverse and should
be used with caution.

A successful response will include a 202 response code and no content. Use the
status endpoint to check on the success or failure of the destruction of the
individual resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsDestroyWithAssociatedResourcesDangerousRequest{
        DropletID: 1,
        Dangerous: true,
    }
client.Droplets.DestroyWithassociatedresourcesdangerous(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**dangerous:** `bool` — Acknowledge this action will destroy the Droplet and all associated resources and _can not_ be reversed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.GetDestroyassociatedresourcesstatus(DropletID) -> *godonext.AssociatedResourceStatus</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To check on the status of a request to destroy a Droplet with its associated
resources, send a GET request to the
`/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/status` endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsGetDestroyAssociatedResourcesStatusRequest{
        DropletID: 1,
    }
client.Droplets.GetDestroyassociatedresourcesstatus(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.DestroyRetrywithassociatedresources(DropletID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

If the status of a request to destroy a Droplet with its associated resources
reported any errors, it can be retried by sending a POST request to the
`/v2/droplets/$DROPLET_ID/destroy_with_associated_resources/retry` endpoint.

Only one destroy can be active at a time per Droplet. If a retry is issued
while another destroy is in progress for the Droplet a 409 status code will
be returned. A successful response will include a 202 response code and no
content.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletsDestroyRetryWithAssociatedResourcesRequest{
        DropletID: 1,
    }
client.Droplets.DestroyRetrywithassociatedresources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Droplets.ListNeighborsids() -> *godonext.NeighborIDs</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all Droplets that are co-located on the same physical
hardware, send a GET request to `/v2/reports/droplet_neighbors_ids`.

The results will be returned as a JSON object with a key of `neighbor_ids`.
This will be set to an array of arrays. Each array will contain a set of
Droplet IDs for Droplets that share a physical server. An empty array
indicates that all Droplets associated with your account are located on
separate physical hardware.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Droplets.ListNeighborsids(
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

## Droplet Actions
<details><summary><code>client.DropletActions.DropletActionsList(DropletID) -> *godonext.DropletActionsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a list of all actions that have been executed for a Droplet, send
a GET request to `/v2/droplets/$DROPLET_ID/actions`.

The results will be returned as a JSON object with an `actions` key. This will
be set to an array filled with `action` objects containing the standard
`action` attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletActionsListRequest{
        DropletID: 1,
    }
client.DropletActions.DropletActionsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletActions.DropletActionsPost(DropletID, request) -> *godonext.DropletActionsPostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To initiate an action on a Droplet send a POST request to
`/v2/droplets/$DROPLET_ID/actions`. In the JSON body to the request,
set the `type` attribute to one of the supported action types:

| Action                                   | Details | Required Permissions |
| ---------------------------------------- | ----------- | ----------- |
| <nobr>`enable_backups`</nobr>            | Enables backups for a Droplet | <nobr>`droplet:update`</nobr> |
| <nobr>`disable_backups`</nobr>           | Disables backups for a Droplet | <nobr>`droplet:update`</nobr> |
| <nobr>`change_backup_policy`</nobr>      | Update the backup policy for a Droplet | <nobr>`droplet:update`</nobr> |
| <nobr>`reboot`</nobr>                    | Reboots a Droplet. A `reboot` action is an attempt to reboot the Droplet in a graceful way, similar to using the `reboot` command from the console. | <nobr>`droplet:update`</nobr> |
| <nobr>`power_cycle`</nobr>               | Power cycles a Droplet. A `powercycle` action is similar to pushing the reset button on a physical machine, it's similar to booting from scratch. | <nobr>`droplet:update`</nobr> |
| <nobr>`shutdown`</nobr>                  | Shuts down a Droplet. A shutdown action is an attempt to shutdown the Droplet in a graceful way, similar to using the `shutdown` command from the console. Since a `shutdown` command can fail, this action guarantees that the command is issued, not that it succeeds. The preferred way to turn off a Droplet is to attempt a shutdown, with a reasonable timeout, followed by a `power_off` action to ensure the Droplet is off. | <nobr>`droplet:update`</nobr> |
| <nobr>`power_off`</nobr>                 | Powers off a Droplet. A `power_off` event is a hard shutdown and should only be used if the `shutdown` action is not successful. It is similar to cutting the power on a server and could lead to complications. | <nobr>`droplet:update`</nobr> |
| <nobr>`power_on`</nobr>                  | Powers on a Droplet. | <nobr>`droplet:update`</nobr> |
| <nobr>`restore`</nobr>                   | Restore a Droplet using a backup image. The image ID that is passed in must be a backup of the current Droplet instance. The operation will leave any embedded SSH keys intact. | <nobr>`droplet:update`</nobr><br><nobr>`droplet:admin`</nobr> |
| <nobr>`password_reset`</nobr>            | Resets the root password for a Droplet. A new password will be provided via email. It must be changed after first use. | <nobr>`droplet:update`</nobr><br><nobr>`droplet:admin`</nobr> |
| <nobr>`resize`</nobr>                    | Resizes a Droplet. Set the `size` attribute to a size slug. If a permanent resize with disk changes included is desired, set the `disk` attribute to `true`. | <nobr>`droplet:update`</nobr><br><nobr>`droplet:create`</nobr> |
| <nobr>`rebuild`</nobr>                   | Rebuilds a Droplet from a new base image. Set the `image` attribute to an image ID or slug. | <nobr>`droplet:update`</nobr><br><nobr>`droplet:admin`</nobr> |
| <nobr>`rename`</nobr>                    | Renames a Droplet. | <nobr>`droplet:update`</nobr> |
| <nobr>`change_kernel`</nobr>             | Changes a Droplet's kernel. Only applies to Droplets with externally managed kernels. All Droplets created after March 2017 use internal kernels by default. | <nobr>`droplet:update`</nobr> |
| <nobr>`enable_ipv6`</nobr>               | Enables IPv6 for a Droplet. Once enabled for a Droplet, IPv6 can not be disabled. When enabling IPv6 on an existing Droplet, [additional OS-level configuration](https://docs.digitalocean.com/products/networking/ipv6/how-to/enable/#on-existing-droplets) is required. | <nobr>`droplet:update`</nobr> |
| <nobr>`snapshot`</nobr>                  | Takes a snapshot of a Droplet. | <nobr>`droplet:update`</nobr><br><nobr>`image:create`</nobr> |
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletActionsPostRequest{
        DropletID: 1,
        Body: &godonext.DropletActionsPostRequestBody{
            DropletActionEnableBackups: &godonext.DropletActionEnableBackups{
                Type: godonext.DropletActionTypeEnableBackups,
                BackupPolicy: &godonext.DropletActionEnableBackupsBackupPolicy{
                    Plan: godonext.DropletActionEnableBackupsBackupPolicyPlanDaily.Ptr(),
                    Hour: godonext.Int(
                        20,
                    ),
                },
            },
        },
    }
client.DropletActions.DropletActionsPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DropletActionsPostRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletActions.DropletActionsPostByTag(request) -> *godonext.DropletActionsPostByTagResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Some actions can be performed in bulk on tagged Droplets. The actions can be
initiated by sending a POST to `/v2/droplets/actions?tag_name=$TAG_NAME` with
the action arguments.

Only a sub-set of action types are supported:

- `power_cycle`
- `power_on`
- `power_off`
- `shutdown`
- `enable_ipv6`
- `enable_backups`
- `disable_backups`
- `snapshot` (also requires `image:create` permission)
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletActionsPostByTagRequest{
        TagName: godonext.String(
            "env:prod",
        ),
        Body: &godonext.DropletActionsPostByTagRequestBody{
            EnableBackups: &godonext.DropletAction{},
        },
    }
client.DropletActions.DropletActionsPostByTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagName:** `*string` — Used to filter Droplets by a specific tag. Can not be combined with `name` or `type`.<br>Requires `tag:read` scope.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DropletActionsPostByTagRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletActions.DropletActionsGet(DropletID, ActionID) -> *godonext.DropletActionsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a Droplet action, send a GET request to
`/v2/droplets/$DROPLET_ID/actions/$ACTION_ID`.

The response will be a JSON object with a key called `action`. The value will
be a Droplet action object.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DropletActionsGetRequest{
        DropletID: 1,
        ActionID: 1,
    }
client.DropletActions.DropletActionsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dropletID:** `int` — A unique identifier for a Droplet instance.
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `int` — A unique numeric ID that can be used to identify and reference an action.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Droplet Autoscale Pools
<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsList() -> *godonext.AutoscalepoolsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all autoscale pools in your team, send a GET request to `/v2/droplets/autoscale`.
The response body will be a JSON object with a key of `autoscale_pools` containing an array of autoscale pool objects.
These each contain the standard autoscale pool attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsListRequest{
        Name: godonext.String(
            "my-autoscale-pool",
        ),
    }
client.DropletAutoscalePools.AutoscalepoolsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — The name of the autoscale pool
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsCreate(request) -> *godonext.AutoscalepoolsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new autoscale pool, send a POST request to `/v2/droplets/autoscale` setting the required attributes.

The response body will contain a JSON object with a key called `autoscale_pool` containing the standard attributes for the new autoscale pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalePoolCreate{
        Name: "my-autoscale-pool",
        Config: &godonext.AutoscalePoolCreateConfig{
            AutoscalePoolDynamicConfig: &godonext.AutoscalePoolDynamicConfig{
                MinInstances: 1,
                MaxInstances: 5,
                TargetCPUUtilization: godonext.Float64(
                    0.5,
                ),
                CooldownMinutes: godonext.Int(
                    10,
                ),
            },
        },
        DropletTemplate: &godonext.AutoscalePoolDropletTemplate{
            Name: godonext.String(
                "example.com",
            ),
            Region: godonext.AutoscalePoolDropletTemplateRegionNyc3,
            Size: "c-2",
            Image: "ubuntu-20-04-x64",
            SSHKeys: []string{
                "3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45",
            },
            Tags: []string{
                "env:prod",
                "web",
            },
            VpcUUID: godonext.String(
                "760e09ef-dc84-11e8-981e-3cfdfeaae000",
            ),
            Ipv6: godonext.Bool(
                true,
            ),
            UserData: godonext.String(
                `#cloud-config
                runcmd:
                  - touch /test.txt
                `,
            ),
        },
    }
client.DropletAutoscalePools.AutoscalepoolsCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.AutoscalePoolCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsGet(AutoscalePoolID) -> *godonext.AutoscalepoolsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an individual autoscale pool, send a GET request to
`/v2/droplets/autoscale/$AUTOSCALE_POOL_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsGetRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
    }
client.DropletAutoscalePools.AutoscalepoolsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsUpdate(AutoscalePoolID, request) -> *godonext.AutoscalepoolsUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the configuration of an existing autoscale pool, send a PUT request to
`/v2/droplets/autoscale/$AUTOSCALE_POOL_ID`. The request must contain a full representation
of the autoscale pool including existing attributes. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsUpdateRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Body: &godonext.AutoscalePoolCreate{
            Name: "my-autoscale-pool",
            Config: &godonext.AutoscalePoolCreateConfig{
                AutoscalePoolStaticConfig: &godonext.AutoscalePoolStaticConfig{
                    TargetNumberInstances: 2,
                },
            },
            DropletTemplate: &godonext.AutoscalePoolDropletTemplate{
                Name: godonext.String(
                    "example.com",
                ),
                Region: godonext.AutoscalePoolDropletTemplateRegionNyc3,
                Size: "c-2",
                Image: "ubuntu-20-04-x64",
                SSHKeys: []string{
                    "3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45",
                },
                Tags: []string{
                    "env:prod",
                    "web",
                },
                VpcUUID: godonext.String(
                    "760e09ef-dc84-11e8-981e-3cfdfeaae000",
                ),
                Ipv6: godonext.Bool(
                    true,
                ),
                UserData: godonext.String(
                    `#cloud-config
                    runcmd:
                      - touch /test.txt
                    `,
                ),
            },
        },
    }
client.DropletAutoscalePools.AutoscalepoolsUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.AutoscalePoolCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsDelete(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy an autoscale pool, send a DELETE request to the `/v2/droplets/autoscale/$AUTOSCALE_POOL_ID` endpoint.

A successful response will include a 202 response code and no content. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsDeleteRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
    }
client.DropletAutoscalePools.AutoscalepoolsDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsDeleteDangerous(AutoscalePoolID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy an autoscale pool and its associated resources (Droplets),
send a DELETE request to the `/v2/droplets/autoscale/$AUTOSCALE_POOL_ID/dangerous` endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsDeleteDangerousRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Dangerous: true,
    }
client.DropletAutoscalePools.AutoscalepoolsDeleteDangerous(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**dangerous:** `bool` — Acknowledge this action will destroy the autoscale pool and its associated resources and _can not_ be reversed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsListMembers(AutoscalePoolID) -> *godonext.AutoscalepoolsListMembersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list the Droplets in an autoscale pool, send a GET request to `/v2/droplets/autoscale/$AUTOSCALE_POOL_ID/members`.

The response body will be a JSON object with a key of `droplets`. This will be
set to an array containing information about each of the Droplets in the autoscale pool.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsListMembersRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
    }
client.DropletAutoscalePools.AutoscalepoolsListMembers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.DropletAutoscalePools.AutoscalepoolsListHistory(AutoscalePoolID) -> *godonext.AutoscalepoolsListHistoryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the scaling history events of an autoscale pool, send a GET request to `/v2/droplets/autoscale/$AUTOSCALE_POOL_ID/history`.

The response body will be a JSON object with a key of `history`. This will be
set to an array containing objects each representing a history event. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AutoscalepoolsListHistoryRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
    }
client.DropletAutoscalePools.AutoscalepoolsListHistory(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Firewalls
<details><summary><code>client.Firewalls.List() -> *godonext.FirewallsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the firewalls available on your account, send a GET request to `/v2/firewalls`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsListRequest{}
client.Firewalls.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.Create(request) -> *godonext.FirewallsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new firewall, send a POST request to `/v2/firewalls`. The request
must contain at least one inbound or outbound access rule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := map[string]any{
        "droplet_ids": []any{
            8043964,
        },
        "inbound_rules": []any{
            map[string]any{
                "ports": "80",
                "protocol": "tcp",
                "sources": map[string]any{
                    "load_balancer_uids": []any{
                        "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                    },
                },
            },
            map[string]any{
                "ports": "22",
                "protocol": "tcp",
                "sources": map[string]any{
                    "addresses": []any{
                        "18.0.0.0/8",
                    },
                    "tags": []any{
                        "gateway",
                    },
                },
            },
        },
        "name": "firewall",
        "outbound_rules": []any{
            map[string]any{
                "destinations": map[string]any{
                    "addresses": []any{
                        "0.0.0.0/0",
                        "::/0",
                    },
                },
                "ports": "80",
                "protocol": "tcp",
            },
        },
    }
client.Firewalls.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `any` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.Get(FirewallID) -> *godonext.FirewallsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing firewall, send a GET request to `/v2/firewalls/$FIREWALL_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsGetRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
    }
client.Firewalls.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.Update(FirewallID, request) -> *godonext.FirewallsUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the configuration of an existing firewall, send a PUT request to
`/v2/firewalls/$FIREWALL_ID`. The request should contain a full representation
of the firewall including existing attributes. **Note that any attributes that
are not provided will be reset to their default values.**
<br><br>You must have read access (e.g. `droplet:read`) to all resources attached
to the firewall to successfully update the firewall.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsUpdateRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        Body: map[string]any{
            "droplet_ids": []any{
                8043964,
            },
            "inbound_rules": []any{
                map[string]any{
                    "ports": "8080",
                    "protocol": "tcp",
                    "sources": map[string]any{
                        "load_balancer_uids": []any{
                            "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                        },
                    },
                },
                map[string]any{
                    "ports": "22",
                    "protocol": "tcp",
                    "sources": map[string]any{
                        "addresses": []any{
                            "18.0.0.0/8",
                        },
                        "tags": []any{
                            "gateway",
                        },
                    },
                },
            },
            "name": "frontend-firewall",
            "outbound_rules": []any{
                map[string]any{
                    "destinations": map[string]any{
                        "addresses": []any{
                            "0.0.0.0/0",
                            "::/0",
                        },
                    },
                    "ports": "8080",
                    "protocol": "tcp",
                },
            },
            "tags": []any{
                "frontend",
            },
        },
    }
client.Firewalls.Update(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**request:** `any` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.Delete(FirewallID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a firewall send a DELETE request to `/v2/firewalls/$FIREWALL_ID`.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsDeleteRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
    }
client.Firewalls.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.AssignDroplets(FirewallID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To assign a Droplet to a firewall, send a POST request to
`/v2/firewalls/$FIREWALL_ID/droplets`. In the body of the request, there
should be a `droplet_ids` attribute containing a list of Droplet IDs.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsAssignDropletsRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        DropletIDs: []int{
            49696269,
        },
    }
client.Firewalls.AssignDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**dropletIDs:** `[]int` — An array containing the IDs of the Droplets to be assigned to the firewall.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.DeleteDroplets(FirewallID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove a Droplet from a firewall, send a DELETE request to
`/v2/firewalls/$FIREWALL_ID/droplets`. In the body of the request, there should
be a `droplet_ids` attribute containing a list of Droplet IDs.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsDeleteDropletsRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        DropletIDs: []int{
            49696269,
        },
    }
client.Firewalls.DeleteDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**dropletIDs:** `[]int` — An array containing the IDs of the Droplets to be removed from the firewall.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.AddTags(FirewallID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To assign a tag representing a group of Droplets to a firewall, send a POST
request to `/v2/firewalls/$FIREWALL_ID/tags`. In the body of the request,
there should be a `tags` attribute containing a list of tag names.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsAddTagsRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        Tags: []string{
            "frontend",
        },
    }
client.Firewalls.AddTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — An array containing the names of the Tags to be assigned to the firewall.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.DeleteTags(FirewallID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove a tag representing a group of Droplets from a firewall, send a
DELETE request to `/v2/firewalls/$FIREWALL_ID/tags`. In the body of the
request, there should be a `tags` attribute containing a list of tag names.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsDeleteTagsRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        Tags: []string{
            "frontend",
        },
    }
client.Firewalls.DeleteTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — An array containing the names of the Tags to be removed from the firewall.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.AddRules(FirewallID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add additional access rules to a firewall, send a POST request to
`/v2/firewalls/$FIREWALL_ID/rules`. The body of the request may include an
inbound_rules and/or outbound_rules attribute containing an array of rules to
be added.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsAddRulesRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        Body: &godonext.FirewallsAddRulesRequestBody{
            Unknown: map[string]any{
                "inbound_rules": []any{
                    map[string]any{
                        "ports": "3306",
                        "protocol": "tcp",
                        "sources": map[string]any{
                            "droplet_ids": []any{
                                49696269,
                            },
                        },
                    },
                },
                "outbound_rules": []any{
                    map[string]any{
                        "destinations": map[string]any{
                            "droplet_ids": []any{
                                49696269,
                            },
                        },
                        "ports": "3306",
                        "protocol": "tcp",
                    },
                },
            },
        },
    }
client.Firewalls.AddRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.FirewallsAddRulesRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Firewalls.DeleteRules(FirewallID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove access rules from a firewall, send a DELETE request to
`/v2/firewalls/$FIREWALL_ID/rules`. The body of the request may include an
`inbound_rules` and/or `outbound_rules` attribute containing an array of rules
to be removed.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FirewallsDeleteRulesRequest{
        FirewallID: "bb4b2611-3d72-467b-8602-280330ecd65c",
        Body: &godonext.FirewallsDeleteRulesRequestBody{
            Unknown: map[string]any{
                "inbound_rules": []any{
                    map[string]any{
                        "ports": "3306",
                        "protocol": "tcp",
                        "sources": map[string]any{
                            "droplet_ids": []any{
                                49696269,
                            },
                        },
                    },
                },
                "outbound_rules": []any{
                    map[string]any{
                        "destinations": map[string]any{
                            "droplet_ids": []any{
                                49696269,
                            },
                        },
                        "ports": "3306",
                        "protocol": "tcp",
                    },
                },
            },
        },
    }
client.Firewalls.DeleteRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**firewallID:** `string` — A unique ID that can be used to identify and reference a firewall.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.FirewallsDeleteRulesRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Floating IPs
<details><summary><code>client.FloatingIPs.FloatingIPsList() -> *godonext.FloatingIPsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the floating IPs available on your account, send a GET request to `/v2/floating_ips`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPsListRequest{}
client.FloatingIPs.FloatingIPsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.FloatingIPs.FloatingIPsCreate(request) -> *godonext.FloatingIPsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

On creation, a floating IP must be either assigned to a Droplet or reserved to a region.
* To create a new floating IP assigned to a Droplet, send a POST
  request to `/v2/floating_ips` with the `droplet_id` attribute.

* To create a new floating IP reserved to a region, send a POST request to
  `/v2/floating_ips` with the `region` attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPCreate{
        FloatingIPCreateDropletID: &godonext.FloatingIPCreateDropletID{
            DropletID: 2457247,
        },
    }
client.FloatingIPs.FloatingIPsCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.FloatingIPCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.FloatingIPs.FloatingIPsGet(FloatingIP) -> *godonext.FloatingIPsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about a floating IP, send a GET request to `/v2/floating_ips/$FLOATING_IP_ADDR`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPsGetRequest{
        FloatingIP: "45.55.96.47",
    }
client.FloatingIPs.FloatingIPsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` — A floating IP address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.FloatingIPs.FloatingIPsDelete(FloatingIP) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a floating IP and remove it from your account, send a DELETE request
to `/v2/floating_ips/$FLOATING_IP_ADDR`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPsDeleteRequest{
        FloatingIP: "45.55.96.47",
    }
client.FloatingIPs.FloatingIPsDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` — A floating IP address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Floating IP Actions
<details><summary><code>client.FloatingIPActions.FloatingIPsActionList(FloatingIP) -> *godonext.FloatingIPsActionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve all actions that have been executed on a floating IP, send a GET request to `/v2/floating_ips/$FLOATING_IP/actions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPsActionListRequest{
        FloatingIP: "45.55.96.47",
    }
client.FloatingIPActions.FloatingIPsActionList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` — A floating IP address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.FloatingIPActions.FloatingIPsActionPost(FloatingIP, request) -> *godonext.FloatingIPsActionPostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To initiate an action on a floating IP send a POST request to
`/v2/floating_ips/$FLOATING_IP/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action     | Details
|------------|--------
| `assign`   | Assigns a floating IP to a Droplet
| `unassign` | Unassign a floating IP from a Droplet
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPsActionPostRequest{
        FloatingIP: "45.55.96.47",
        Body: &godonext.FloatingIPsActionPostRequestBody{
            FloatingIPActionUnassign: &godonext.FloatingIPActionUnassign{},
        },
    }
client.FloatingIPActions.FloatingIPsActionPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` — A floating IP address.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.FloatingIPsActionPostRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.FloatingIPActions.FloatingIPsActionGet(FloatingIP, ActionID) -> *godonext.FloatingIPsActionGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the status of a floating IP action, send a GET request to `/v2/floating_ips/$FLOATING_IP/actions/$ACTION_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FloatingIPsActionGetRequest{
        FloatingIP: "45.55.96.47",
        ActionID: 1,
    }
client.FloatingIPActions.FloatingIPsActionGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**floatingIP:** `string` — A floating IP address.
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `int` — A unique numeric ID that can be used to identify and reference an action.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Functions
<details><summary><code>client.Functions.ListNamespaces() -> *godonext.FunctionsListNamespacesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a list of namespaces associated with the current user. To get all namespaces, send a GET request to `/v2/functions/namespaces`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Functions.ListNamespaces(
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

<details><summary><code>client.Functions.CreateNamespace(request) -> *godonext.FunctionsCreateNamespaceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new serverless functions namespace in the desired region and associates it with the provided label. A namespace is a collection of functions and their associated packages, triggers, and project specifications. To create a namespace, send a POST request to `/v2/functions/namespaces` with the `region` and `label` properties.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CreateNamespace{
        Region: "nyc1",
        Label: "my namespace",
    }
client.Functions.CreateNamespace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**region:** `string` — The [datacenter region](https://docs.digitalocean.com/products/platform/availability-matrix/#available-datacenters) in which to create the namespace.
    
</dd>
</dl>

<dl>
<dd>

**label:** `string` — The namespace's unique name.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.GetNamespace(NamespaceID) -> *godonext.FunctionsGetNamespaceResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Gets the namespace details for the given namespace UUID. To get namespace details, send a GET request to `/v2/functions/namespaces/$NAMESPACE_ID` with no parameters.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsGetNamespaceRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    }
client.Functions.GetNamespace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.DeleteNamespace(NamespaceID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes the given namespace.  When a namespace is deleted all assets, in the namespace are deleted, this includes packages, functions and triggers. Deleting a namespace is a destructive operation and assets in the namespace are not recoverable after deletion. Some metadata is retained, such as activations, or soft deleted for reporting purposes.
To delete namespace, send a DELETE request to `/v2/functions/namespaces/$NAMESPACE_ID`.
A successful deletion returns a 204 response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsDeleteNamespaceRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    }
client.Functions.DeleteNamespace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.ListTriggers(NamespaceID) -> *godonext.FunctionsListTriggersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a list of triggers associated with the current user and namespace. To get all triggers, send a GET request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsListTriggersRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    }
client.Functions.ListTriggers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.CreateTrigger(NamespaceID, request) -> *godonext.FunctionsCreateTriggerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new trigger for a given function in a namespace. To create a trigger, send a POST request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers` with the `name`, `function`, `type`, `is_enabled` and `scheduled_details` properties.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CreateTrigger{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        Name: "my trigger",
        Function: "hello",
        Type: "SCHEDULED",
        IsEnabled: true,
        ScheduledDetails: &godonext.ScheduledDetails{
            Cron: "* * * * *",
        },
    }
client.Functions.CreateTrigger(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The trigger's unique name within the namespace.
    
</dd>
</dl>

<dl>
<dd>

**function:** `string` — Name of function(action) that exists in the given namespace.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `string` — One of different type of triggers. Currently only SCHEDULED is supported.
    
</dd>
</dl>

<dl>
<dd>

**isEnabled:** `bool` — Indicates weather the trigger is paused or unpaused.
    
</dd>
</dl>

<dl>
<dd>

**scheduledDetails:** `*godonext.ScheduledDetails` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.GetTrigger(NamespaceID, TriggerName) -> *godonext.FunctionsGetTriggerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Gets the trigger details. To get the trigger details, send a GET request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers/$TRIGGER_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsGetTriggerRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        TriggerName: "my trigger",
    }
client.Functions.GetTrigger(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**triggerName:** `string` — The name of the trigger to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.UpdateTrigger(NamespaceID, TriggerName, request) -> *godonext.FunctionsUpdateTriggerResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the details of the given trigger. To update a trigger, send a PUT request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers/$TRIGGER_NAME` with new values for the `is_enabled ` or `scheduled_details` properties.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UpdateTrigger{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        TriggerName: "my trigger",
    }
client.Functions.UpdateTrigger(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**triggerName:** `string` — The name of the trigger to be managed.
    
</dd>
</dl>

<dl>
<dd>

**isEnabled:** `*bool` — Indicates weather the trigger is paused or unpaused.
    
</dd>
</dl>

<dl>
<dd>

**scheduledDetails:** `*godonext.ScheduledDetails` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.DeleteTrigger(NamespaceID, TriggerName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes the given trigger.
To delete trigger, send a DELETE request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers/$TRIGGER_NAME`.
A successful deletion returns a 204 response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsDeleteTriggerRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        TriggerName: "my trigger",
    }
client.Functions.DeleteTrigger(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**triggerName:** `string` — The name of the trigger to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.FunctionsAccessKeyList(NamespaceID) -> *godonext.FunctionsAccessKeyListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists all access keys for a serverless functions namespace.

To list access keys, send a GET request to `/v2/functions/namespaces/{namespace_id}/keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsAccessKeyListRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    }
client.Functions.FunctionsAccessKeyList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.FunctionsAccessKeyCreate(NamespaceID, request) -> *godonext.FunctionsAccessKeyCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new access key for a serverless functions namespace. 
The access key can be used to authenticate requests to the namespace's functions.
The secret key is only returned once upon creation.

To create an access key, send a POST request to `/v2/functions/namespaces/{namespace_id}/keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AccessKeyCreateRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        Name: "my-function-access-key",
    }
client.Functions.FunctionsAccessKeyCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The access key's name.
    
</dd>
</dl>

<dl>
<dd>

**expiresIn:** `*string` — The duration after which the access key expires, specified as a human-readable duration string in the format `<int>h` (hours) or `<int>d` (days). Minimum value is `1h`. If omitted, the key will never expire.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.FunctionsAccessKeyUpdate(NamespaceID, KeyID, request) -> *godonext.FunctionsAccessKeyUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the name of an access key for a serverless functions namespace.

To update an access key, send a PUT request to `/v2/functions/namespaces/{namespace_id}/keys/{key_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsAccessKeyUpdateRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        KeyID: "dof-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        Name: "updated-key-name",
    }
client.Functions.FunctionsAccessKeyUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**keyID:** `string` — The ID of the access key to be managed.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The new name for the access key.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Functions.FunctionsAccessKeyDelete(NamespaceID, KeyID) -> map[string]any</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an access key for a serverless functions namespace.

To delete an access key, send a DELETE request to `/v2/functions/namespaces/{namespace_id}/keys/{key_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.FunctionsAccessKeyDeleteRequest{
        NamespaceID: "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
        KeyID: "dof-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    }
client.Functions.FunctionsAccessKeyDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**namespaceID:** `string` — The ID of the namespace to be managed.
    
</dd>
</dl>

<dl>
<dd>

**keyID:** `string` — The ID of the access key to be managed.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Images
<details><summary><code>client.Images.List() -> *godonext.ImagesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the images available on your account, send a GET request to /v2/images.

## Filtering Results
-----

It's possible to request filtered results by including certain query parameters.

**Image Type**

Either 1-Click Application or OS Distribution images can be filtered by using the `type` query parameter.

> Important: The `type` query parameter does not directly relate to the `type` attribute.

To retrieve only ***distribution*** images, include the `type` query parameter set to distribution, `/v2/images?type=distribution`.

To retrieve only ***application*** images, include the `type` query parameter set to application, `/v2/images?type=application`.

**User Images**

To retrieve only the private images of a user, include the `private` query parameter set to true, `/v2/images?private=true`.

**Tags**

To list all images assigned to a specific tag, include the `tag_name` query parameter set to the name of the tag in your GET request. For example, `/v2/images?tag_name=$TAG_NAME`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesListRequest{
        TagName: godonext.String(
            "base-image",
        ),
    }
client.Images.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type_:** `*godonext.ImagesListRequestType` — Filters results based on image type which can be either `application` or `distribution`.
    
</dd>
</dl>

<dl>
<dd>

**private:** `*bool` — Used to filter only user images.
    
</dd>
</dl>

<dl>
<dd>

**tagName:** `*string` — Used to filter images by a specific tag.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.CreateCustom(request) -> *godonext.ImagesCreateCustomResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new custom image, send a POST request to /v2/images.
The body must contain a url attribute pointing to a Linux virtual machine
image to be imported into DigitalOcean.
The image must be in the raw, qcow2, vhdx, vdi, or vmdk format.
It may be compressed using gzip or bzip2 and must be smaller than 100 GB after
 being decompressed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImageNewCustom{
        Name: godonext.String(
            "ubuntu-18.04-minimal",
        ),
        Distribution: godonext.DistributionUbuntu.Ptr(),
        Description: godonext.String(
            "Cloud-optimized image w/ small footprint",
        ),
        URL: "http://cloud-images.ubuntu.com/minimal/releases/bionic/release/ubuntu-18.04-minimal-cloudimg-amd64.img",
        Region: godonext.RegionSlugNyc3,
        Tags: []string{
            "base-image",
            "prod",
        },
    }
client.Images.CreateCustom(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**url:** `string` — A URL from which the custom Linux virtual machine image may be retrieved.  The image it points to must be in the raw, qcow2, vhdx, vdi, or vmdk format.  It may be compressed using gzip or bzip2 and must be smaller than 100 GB after being decompressed.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.RegionSlug` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `*godonext.TagsArray` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.Get(ImageID) -> *godonext.ImagesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve information about an image, send a `GET` request to
`/v2/images/$IDENTIFIER`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesGetRequest{
        ImageID: &godonext.ImagesGetRequestImageID{
            Integer: 1,
        },
    }
client.Images.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `*godonext.ImagesGetRequestImageID` 

A unique number (id) or string (slug) used to identify and reference a
specific image.

**Public** images can be identified by image `id` or `slug`.

**Private** images *must* be identified by image `id`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.Update(ImageID, request) -> *godonext.ImagesUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an image, send a `PUT` request to `/v2/images/$IMAGE_ID`.
Set the `name` attribute to the new value you would like to use.
For custom images, the `description` and `distribution` attributes may also be updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesUpdateRequest{
        ImageID: 1,
        Body: &godonext.ImageUpdate{},
    }
client.Images.Update(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ImageUpdate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.Delete(ImageID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a snapshot or custom image, send a `DELETE` request to `/v2/images/$IMAGE_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesDeleteRequest{
        ImageID: 1,
    }
client.Images.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.PostAccountTransferCreate(ImageID, request) -> *godonext.ImagesPostAccountTransferCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To initiate an account transfer for an image, send a POST request to
`/v2/images/$IMAGE_ID/account_transfer`.

Only snapshot images may be transferred by this endpoint to another account.

An image account transfer always has exactly one recipient, specified in the request body.
The recipient can be one of the following:

* A DigitalOcean account, denoted by `recipient_email` in the request body.
The recipient will receive an email with instructions to accept the transfer.
Once the recipient accepts the transfer, the image will be moved to their
account.

* A DigitalOcean team, denoted by `recipient_uuid` in the request body. If the
user has sufficient permissions in the recipient team, the transfer will be
automatically accepted and the image will be moved to the recipient team's
account. Otherwise, the transfer will be pending until a user with sufficient
permissions in the recipient team accepts the transfer.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesPostAccountTransferCreateRequest{
        ImageID: 1,
        Body: &godonext.ImagesPostAccountTransferCreate{
            ImagesPostAccountTransferCreateRecipientEmail: &godonext.ImagesPostAccountTransferCreateRecipientEmail{
                RecipientEmail: "alice@example.com",
            },
        },
    }
client.Images.PostAccountTransferCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ImagesPostAccountTransferCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.PostAccountTransferAccept(ImageID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To accept an account transfer for an image, send a POST request to
`/v2/images/$IMAGE_ID/account_transfer/accept`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesPostAccountTransferAccept{
        ImageID: 1,
        TransferID: 3164444,
        RecipientUUID: "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    }
client.Images.PostAccountTransferAccept(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**transferID:** `int` — A unique number that used to identify and reference an image account transfer.
    
</dd>
</dl>

<dl>
<dd>

**recipientUUID:** `string` — The UUID of the team that the image will be transferred to.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.PostAccountTransferCancel(ImageID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To cancel an account transfer for an image, send a POST request to
`/v2/images/$IMAGE_ID/account_transfer/cancel`.

Only the sender of an image account transfer can cancel the transfer.
If the transfer is canceled, the image will remain in the sender's account
and will not be transferred to the recipient.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesPostAccountTransferCancel{
        ImageID: 1,
        TransferID: 3164444,
    }
client.Images.PostAccountTransferCancel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**transferID:** `int` — A unique number that used to identify and reference an image account transfer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Images.PostAccountTransferDecline(ImageID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To decline an account transfer for an image, send a POST request to
`/v2/images/$IMAGE_ID/account_transfer/decline`.

Only the recipient of an image account transfer can decline the transfer.
If the transfer is declined, the image will remain in the sender's account
and will not be transferred to the recipient.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImagesPostAccountTransferDecline{
        ImageID: 1,
        TransferID: 3164444,
    }
client.Images.PostAccountTransferDecline(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**transferID:** `int` — A unique number that used to identify and reference an image account transfer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Image Actions
<details><summary><code>client.ImageActions.ImageActionsList(ImageID) -> *godonext.ImageActionsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve all actions that have been executed on an image, send a GET request to `/v2/images/$IMAGE_ID/actions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImageActionsListRequest{
        ImageID: 1,
    }
client.ImageActions.ImageActionsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ImageActions.ImageActionsPost(ImageID, request) -> *godonext.Action</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The following actions are available on an Image.

## Convert an Image to a Snapshot

To convert an image, for example, a backup to a snapshot, send a POST request
to `/v2/images/$IMAGE_ID/actions`. Set the `type` attribute to `convert`.

## Transfer an Image

To transfer an image to another region, send a POST request to
`/v2/images/$IMAGE_ID/actions`. Set the `type` attribute to `transfer` and set
`region` attribute to the slug identifier of the region you wish to transfer
to.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImageActionsPostRequest{
        ImageID: 1,
        Body: &godonext.ImageActionsPostRequestBody{
            ImageActionBase: &godonext.ImageActionBase{
                Type: godonext.ImageActionBaseTypeConvert,
            },
        },
    }
client.ImageActions.ImageActionsPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ImageActionsPostRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ImageActions.ImageActionsGet(ImageID, ActionID) -> *godonext.Action</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the status of an image action, send a GET request to `/v2/images/$IMAGE_ID/actions/$IMAGE_ACTION_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ImageActionsGetRequest{
        ImageID: 1,
        ActionID: 1,
    }
client.ImageActions.ImageActionsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**imageID:** `int` — A unique number that can be used to identify and reference a specific image.
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `int` — A unique numeric ID that can be used to identify and reference an action.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Kubernetes
<details><summary><code>client.Kubernetes.ListClusters() -> *godonext.KubernetesListClustersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the Kubernetes clusters on your account, send a GET request
to `/v2/kubernetes/clusters`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesListClustersRequest{}
client.Kubernetes.ListClusters(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.CreateCluster(request) -> *godonext.KubernetesCreateClusterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new Kubernetes cluster, send a POST request to
`/v2/kubernetes/clusters`. The request must contain at least one node pool
with at least one worker.

The request may contain a maintenance window policy describing a time period
when disruptive maintenance tasks may be carried out. Omitting the policy
implies that a window will be chosen automatically. See
[here](https://docs.digitalocean.com/products/kubernetes/how-to/upgrade-cluster/)
for details.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Cluster{
        Name: "prod-cluster-01",
        Region: "nyc1",
        Version: "1.18.6-do.0",
        NodePools: []*godonext.KubernetesNodePool{
            &godonext.KubernetesNodePool{
                Size: godonext.String(
                    "s-1vcpu-2gb",
                ),
                Name: godonext.String(
                    "worker-pool",
                ),
                Count: godonext.Int(
                    3,
                ),
            },
        },
    }
client.Kubernetes.CreateCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.Cluster` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetCluster(ClusterID) -> *godonext.KubernetesGetClusterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing Kubernetes cluster, send a GET request
to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetClusterRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.GetCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.UpdateCluster(ClusterID, request) -> *godonext.KubernetesUpdateClusterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a Kubernetes cluster, send a PUT request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID` and specify one or more of the
attributes below.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ClusterUpdate{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        Name: "prod-cluster-01",
    }
client.Kubernetes.UpdateCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — A human-readable name for a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`.
    
</dd>
</dl>

<dl>
<dd>

**maintenancePolicy:** `*godonext.MaintenancePolicy` 
    
</dd>
</dl>

<dl>
<dd>

**autoUpgrade:** `*bool` — A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.
    
</dd>
</dl>

<dl>
<dd>

**surgeUpgrade:** `*bool` — A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.
    
</dd>
</dl>

<dl>
<dd>

**ha:** `*bool` — A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled. When omitted on create, the default is version-dependent; for DOKS 1.36.0 and later, the default is true; for earlier versions, the default is false.
    
</dd>
</dl>

<dl>
<dd>

**controlPlaneFirewall:** `*godonext.ControlPlaneFirewall` 
    
</dd>
</dl>

<dl>
<dd>

**clusterAutoscalerConfiguration:** `*godonext.ClusterAutoscalerConfiguration` 
    
</dd>
</dl>

<dl>
<dd>

**sso:** `*godonext.SSO` 
    
</dd>
</dl>

<dl>
<dd>

**routingAgent:** `*godonext.RoutingAgent` 
    
</dd>
</dl>

<dl>
<dd>

**amdGpuDevicePlugin:** `*godonext.AmdGpuDevicePlugin` 
    
</dd>
</dl>

<dl>
<dd>

**amdGpuDeviceMetricsExporterPlugin:** `*godonext.AmdGpuDeviceMetricsExporterPlugin` 
    
</dd>
</dl>

<dl>
<dd>

**nvidiaGpuDevicePlugin:** `*godonext.NvidiaGpuDevicePlugin` 
    
</dd>
</dl>

<dl>
<dd>

**rdmaSharedDevPlugin:** `*godonext.RdmaSharedDevPlugin` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.DeleteCluster(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a Kubernetes cluster and all services deployed to it, send a DELETE
request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID`.

A 204 status code with no body will be returned in response to a successful
request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesDeleteClusterRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.DeleteCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.ListAssociatedresources(ClusterID) -> *godonext.AssociatedKubernetesResources</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list the associated billable resources that can be destroyed along with a cluster, send a GET request to the `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/destroy_with_associated_resources` endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesListAssociatedResourcesRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.ListAssociatedresources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.DestroyAssociatedresourcesselective(ClusterID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a Kubernetes cluster along with a subset of its associated resources,
send a DELETE request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/destroy_with_associated_resources/selective`.

The JSON body of the request should include `load_balancers`, `volumes`, or
`volume_snapshots` keys each set to an array of IDs for the associated
resources to be destroyed.

The IDs can be found by querying the cluster's associated resources endpoint.
Any associated resource not included in the request will remain and continue
to accrue changes on your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DestroyAssociatedKubernetesResources{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.DestroyAssociatedresourcesselective(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**loadBalancers:** `[]string` — A list of IDs for associated load balancers to destroy along with the cluster.
    
</dd>
</dl>

<dl>
<dd>

**volumes:** `[]string` — A list of IDs for associated volumes to destroy along with the cluster.
    
</dd>
</dl>

<dl>
<dd>

**volumeSnapshots:** `[]string` — A list of IDs for associated volume snapshots to destroy along with the cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.DestroyAssociatedresourcesdangerous(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a Kubernetes cluster with all of its associated resources, send a
DELETE request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/destroy_with_associated_resources/dangerous`.
A 204 status code with no body will be returned in response to a successful request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesDestroyAssociatedResourcesDangerousRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.DestroyAssociatedresourcesdangerous(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetKubeconfig(ClusterID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint returns a kubeconfig file in YAML format. It can be used to
connect to and administer the cluster using the Kubernetes command line tool,
`kubectl`, or other programs supporting kubeconfig files (e.g., client libraries).

The resulting kubeconfig file uses token-based authentication for clusters
supporting it, and certificate-based authentication otherwise. For a list of
supported versions and more information, see "[How to Connect to a DigitalOcean
Kubernetes Cluster](https://docs.digitalocean.com/products/kubernetes/how-to/connect-to-cluster/)".

To retrieve a kubeconfig file for use with a Kubernetes cluster, send a GET
request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/kubeconfig`.

Clusters supporting token-based authentication may define an expiration by
passing a duration in seconds as a query parameter to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/kubeconfig?expiry_seconds=$DURATION_IN_SECONDS`.
If not set or 0, then the token will have a 7 day expiry. The query parameter
has no impact for other kubeconfig types.

Using an `sso` kubeconfig type requires `doctl` to be installed to handle the client side
of the OAuth2 flow.

Kubernetes Roles granted to a user are derived from that user's
DigitalOcean role. Predefined roles (Owner, Member, Modifier etc.) have an automatic mapping
to Kubernetes roles. Custom roles are not automatically mapped to any Kubernetes roles,
and require [additional configuration](https://docs.digitalocean.com/products/kubernetes/how-to/set-up-custom-rolebindings/)
by a cluster administrator.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetKubeconfigRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.GetKubeconfig(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**expirySeconds:** `*int` — The duration in seconds that the returned Kubernetes credentials will be valid. If not set or 0, the credentials will have a 7 day expiry.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.KubernetesGetKubeconfigRequestType` 

The type of credentials to return in the kubeconfig. When omitted, the
default credential type for the cluster is used: `sso` for clusters with SSO enabled, `token` for clusters without SSO enabled.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetCredentials(ClusterID) -> *godonext.Credentials</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint returns a JSON object . It can be used to programmatically
construct Kubernetes clients which cannot parse kubeconfig files.

The resulting JSON object contains token-based authentication for clusters
supporting it, and certificate-based authentication otherwise. For a list of
supported versions and more information, see "[How to Connect to a DigitalOcean
Kubernetes Cluster](https://docs.digitalocean.com/products/kubernetes/how-to/connect-to-cluster/)".

To retrieve credentials for accessing a Kubernetes cluster, send a GET
request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/credentials`.

Clusters supporting token-based authentication may define an expiration by
passing a duration in seconds as a query parameter to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/credentials?expiry_seconds=$DURATION_IN_SECONDS`.
If not set or 0, then the token will have a 7 day expiry. The query parameter
has no impact in certificate-based authentication.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetCredentialsRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.GetCredentials(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**expirySeconds:** `*int` — The duration in seconds that the returned Kubernetes credentials will be valid. If not set or 0, the credentials will have a 7 day expiry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetAvailableupgrades(ClusterID) -> *godonext.KubernetesGetAvailableUpgradesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To determine whether a cluster can be upgraded, and the versions to which it
can be upgraded, send a GET request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/upgrades`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetAvailableUpgradesRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.GetAvailableupgrades(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.UpgradeCluster(ClusterID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To immediately upgrade a Kubernetes cluster to a newer patch release of
Kubernetes, send a POST request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/upgrade`.
The body of the request must specify a version attribute.

Available upgrade versions for a cluster can be fetched from
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/upgrades`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesUpgradeClusterRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.UpgradeCluster(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**version:** `*string` — The slug identifier for the version of Kubernetes that the cluster will be upgraded to.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.ListNodepools(ClusterID) -> *godonext.KubernetesListNodePoolsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the node pools in a Kubernetes clusters, send a GET request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesListNodePoolsRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.ListNodepools(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.AddNodepool(ClusterID, request) -> *godonext.KubernetesAddNodePoolResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add an additional node pool to a Kubernetes clusters, send a POST request
to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools` with the following
attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesAddNodePoolRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        Body: &godonext.KubernetesNodePool{
            Size: godonext.String(
                "s-1vcpu-2gb",
            ),
            Name: godonext.String(
                "new-pool",
            ),
            Count: godonext.Int(
                3,
            ),
            Tags: []string{
                "frontend",
            },
            AutoScale: godonext.Bool(
                true,
            ),
            MinNodes: godonext.Int(
                3,
            ),
            MaxNodes: godonext.Int(
                6,
            ),
        },
    }
client.Kubernetes.AddNodepool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.KubernetesNodePool` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetNodepool(ClusterID, NodePoolID) -> *godonext.KubernetesGetNodePoolResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about a specific node pool in a Kubernetes cluster, send
a GET request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetNodePoolRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        NodePoolID: "cdda885e-7663-40c8-bc74-3a036c66545d",
    }
client.Kubernetes.GetNodepool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` — A unique ID that can be used to reference a Kubernetes node pool.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.UpdateNodepool(ClusterID, NodePoolID, request) -> *godonext.KubernetesUpdateNodePoolResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the name of a node pool, edit the tags applied to it, or adjust its
number of nodes, send a PUT request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID` with the
following attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesUpdateNodePoolRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        NodePoolID: "cdda885e-7663-40c8-bc74-3a036c66545d",
        Body: &godonext.KubernetesNodePoolBase{},
    }
client.Kubernetes.UpdateNodepool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` — A unique ID that can be used to reference a Kubernetes node pool.
    
</dd>
</dl>

<dl>
<dd>

**request:** `godonext.KubernetesNodePoolUpdate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.DeleteNodepool(ClusterID, NodePoolID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a node pool, send a DELETE request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID`.

A 204 status code with no body will be returned in response to a successful
request. Nodes in the pool will subsequently be drained and deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesDeleteNodePoolRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        NodePoolID: "cdda885e-7663-40c8-bc74-3a036c66545d",
    }
client.Kubernetes.DeleteNodepool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` — A unique ID that can be used to reference a Kubernetes node pool.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.DeleteNode(ClusterID, NodePoolID, NodeID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a single node in a pool, send a DELETE request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID/nodes/$NODE_ID`.

Appending the `skip_drain=1` query parameter to the request causes node
draining to be skipped. Omitting the query parameter or setting its value to
`0` carries out draining prior to deletion.

Appending the `replace=1` query parameter to the request causes the node to
be replaced by a new one after deletion. Omitting the query parameter or
setting its value to `0` deletes without replacement.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesDeleteNodeRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        NodePoolID: "cdda885e-7663-40c8-bc74-3a036c66545d",
        NodeID: "478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f",
    }
client.Kubernetes.DeleteNode(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` — A unique ID that can be used to reference a Kubernetes node pool.
    
</dd>
</dl>

<dl>
<dd>

**nodeID:** `string` — A unique ID that can be used to reference a node in a Kubernetes node pool.
    
</dd>
</dl>

<dl>
<dd>

**skipDrain:** `*int` — Specifies whether or not to drain workloads from a node before it is deleted. Setting it to `1` causes node draining to be skipped. Omitting the query parameter or setting its value to `0` carries out draining prior to deletion.
    
</dd>
</dl>

<dl>
<dd>

**replace:** `*int` — Specifies whether or not to replace a node after it has been deleted. Setting it to `1` causes the node to be replaced by a new one after deletion. Omitting the query parameter or setting its value to `0` deletes without replacement.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.RecycleNodePool(ClusterID, NodePoolID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The endpoint has been deprecated. Please use the DELETE
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/node_pools/$NODE_POOL_ID/nodes/$NODE_ID`
method instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesRecycleNodePoolRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        NodePoolID: "cdda885e-7663-40c8-bc74-3a036c66545d",
    }
client.Kubernetes.RecycleNodePool(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**nodePoolID:** `string` — A unique ID that can be used to reference a Kubernetes node pool.
    
</dd>
</dl>

<dl>
<dd>

**nodes:** `[]string` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetClusteruser(ClusterID) -> *godonext.User</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information the user associated with a Kubernetes cluster, send a GET
request to `/v2/kubernetes/clusters/$K8S_CLUSTER_ID/user`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetClusterUserRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.GetClusteruser(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.ListOptions() -> *godonext.KubernetesOptions</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list the versions of Kubernetes available for use, the regions that support Kubernetes, and the available node sizes, send a GET request to `/v2/kubernetes/options`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Kubernetes.ListOptions(
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

<details><summary><code>client.Kubernetes.GetClusterlintresults(ClusterID) -> *godonext.ClusterlintResults</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To request clusterlint diagnostics for your cluster, send a GET request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/clusterlint`. If the `run_id` query
parameter is provided, then the diagnostics for the specific run is fetched.
By default, the latest results are shown.

To find out how to address clusterlint feedback, please refer to
[the clusterlint check documentation](https://github.com/digitalocean/clusterlint/blob/master/checks.md).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetClusterLintResultsRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        RunID: godonext.String(
            "50c2f44c-011d-493e-aee5-361a4a0d1844",
        ),
    }
client.Kubernetes.GetClusterlintresults(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**runID:** `*string` — Specifies the clusterlint run whose results will be retrieved.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.RunClusterlint(ClusterID, request) -> *godonext.KubernetesRunClusterLintResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Clusterlint helps operators conform to Kubernetes best practices around
resources, security and reliability to avoid common problems while operating
or upgrading the clusters.

To request a clusterlint run on your cluster, send a POST request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/clusterlint`. This will run all
checks present in the `doks` group by default, if a request body is not
specified. Optionally specify the below attributes.

For information about the available checks, please refer to
[the clusterlint check documentation](https://github.com/digitalocean/clusterlint/blob/master/checks.md).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ClusterlintRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
    }
client.Kubernetes.RunClusterlint(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**includeGroups:** `[]string` — An array of check groups that will be run when clusterlint executes checks.
    
</dd>
</dl>

<dl>
<dd>

**includeChecks:** `[]string` — An array of checks that will be run when clusterlint executes checks.
    
</dd>
</dl>

<dl>
<dd>

**excludeGroups:** `[]string` — An array of check groups that will be omitted when clusterlint executes checks.
    
</dd>
</dl>

<dl>
<dd>

**excludeChecks:** `[]string` — An array of checks that will be run when clusterlint executes checks.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.AddRegistry(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To integrate the container registry with Kubernetes clusters, send a POST request to `/v2/kubernetes/registry`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ClusterRegistry{}
client.Kubernetes.AddRegistry(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ClusterRegistry` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.RemoveRegistry(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove the container registry from Kubernetes clusters, send a DELETE request to `/v2/kubernetes/registry`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ClusterRegistry{}
client.Kubernetes.RemoveRegistry(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ClusterRegistry` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.AddRegistries(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To integrate the container registries with Kubernetes clusters, send a POST request to `/v2/kubernetes/registries`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ClusterRegistries{}
client.Kubernetes.AddRegistries(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ClusterRegistries` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.RemoveRegistries(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove the container registries from Kubernetes clusters, send a DELETE request to `/v2/kubernetes/registries`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ClusterRegistries{}
client.Kubernetes.RemoveRegistries(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ClusterRegistries` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Kubernetes.GetStatusMessages(ClusterID) -> *godonext.KubernetesGetStatusMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve status messages for a Kubernetes cluster, send a GET request to
`/v2/kubernetes/clusters/$K8S_CLUSTER_ID/status_messages`. Status messages inform users of any issues that come up during the cluster lifecycle.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.KubernetesGetStatusMessagesRequest{
        ClusterID: "bd5f5959-5e1e-4205-a714-a914373942af",
        Since: godonext.Time(
            godonext.MustParseDateTime(
                "2018-11-15T16:00:11Z",
            ),
        ),
    }
client.Kubernetes.GetStatusMessages(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**clusterID:** `string` — A unique ID that can be used to reference a Kubernetes cluster.
    
</dd>
</dl>

<dl>
<dd>

**since:** `*time.Time` — A timestamp used to return status messages emitted since the specified time. The timestamp should be in ISO8601 format.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Load Balancers
<details><summary><code>client.LoadBalancers.LoadBalancersList() -> *godonext.LoadBalancersListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the load balancer instances on your account, send a GET request
to `/v2/load_balancers`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersListRequest{}
client.LoadBalancers.LoadBalancersList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersCreate(request) -> *godonext.LoadBalancersCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new load balancer instance, send a POST request to
`/v2/load_balancers`.

You can specify the Droplets that will sit behind the load balancer using one
of two methods:

* Set `droplet_ids` to a list of specific Droplet IDs.
* Set `tag` to the name of a tag. All Droplets with this tag applied will be
  assigned to the load balancer. Additional Droplets will be automatically
  assigned as they are tagged.

These methods are mutually exclusive.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancerCreate{
        LoadBalancerCreateZero: &godonext.LoadBalancerCreateZero{
            Name: godonext.String(
                "example-lb-01",
            ),
            ProjectID: godonext.String(
                "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
            ),
            ForwardingRules: []*godonext.ForwardingRule{
                &godonext.ForwardingRule{
                    EntryProtocol: godonext.ForwardingRuleEntryProtocolHTTP,
                    EntryPort: 80,
                    TargetProtocol: godonext.ForwardingRuleTargetProtocolHTTP,
                    TargetPort: 80,
                },
                &godonext.ForwardingRule{
                    EntryProtocol: godonext.ForwardingRuleEntryProtocolHTTPS,
                    EntryPort: 443,
                    TargetProtocol: godonext.ForwardingRuleTargetProtocolHTTPS,
                    TargetPort: 443,
                    TLSPassthrough: godonext.Bool(
                        true,
                    ),
                },
            },
            HTTPIdleTimeoutSeconds: godonext.Int(
                60,
            ),
            Firewall: &godonext.LbFirewall{
                Deny: []string{
                    "cidr:1.2.0.0/16",
                    "ip:2.3.4.5",
                },
                Allow: []string{
                    "ip:1.2.3.4",
                    "cidr:2.3.4.0/24",
                },
            },
            DropletIDs: []int{
                3164444,
                3164445,
            },
            Region: godonext.RegionSlugNyc3,
        },
    }
client.LoadBalancers.LoadBalancersCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.LoadBalancerCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersGet(LbID) -> *godonext.LoadBalancersGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about a load balancer instance, send a GET request to
`/v2/load_balancers/$LOAD_BALANCER_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersGetRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.LoadBalancers.LoadBalancersGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersUpdate(LbID, request) -> *godonext.LoadBalancersUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a load balancer's settings, send a PUT request to
`/v2/load_balancers/$LOAD_BALANCER_ID`. The request should contain a full
representation of the load balancer including existing attributes. It may
contain _one of_ the `droplets_ids` or `tag` attributes as they are mutually
exclusive. **Note that any attribute that is not provided will be reset to its
default value.**
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersUpdateRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.LoadBalancerCreate{
            LoadBalancerCreateZero: &godonext.LoadBalancerCreateZero{
                Name: godonext.String(
                    "updated-example-lb-01",
                ),
                ProjectID: godonext.String(
                    "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
                ),
                ForwardingRules: []*godonext.ForwardingRule{
                    &godonext.ForwardingRule{
                        EntryProtocol: godonext.ForwardingRuleEntryProtocolHTTP,
                        EntryPort: 80,
                        TargetProtocol: godonext.ForwardingRuleTargetProtocolHTTP,
                        TargetPort: 80,
                        CertificateID: godonext.String(
                            "",
                        ),
                        TLSPassthrough: godonext.Bool(
                            false,
                        ),
                    },
                    &godonext.ForwardingRule{
                        EntryProtocol: godonext.ForwardingRuleEntryProtocolHTTPS,
                        EntryPort: 443,
                        TargetProtocol: godonext.ForwardingRuleTargetProtocolHTTPS,
                        TargetPort: 443,
                        CertificateID: godonext.String(
                            "",
                        ),
                        TLSPassthrough: godonext.Bool(
                            true,
                        ),
                    },
                },
                HealthCheck: &godonext.HealthCheck{
                    Protocol: godonext.HealthCheckProtocolHTTP.Ptr(),
                    Port: godonext.Int(
                        80,
                    ),
                    Path: godonext.String(
                        "/",
                    ),
                    CheckIntervalSeconds: godonext.Int(
                        10,
                    ),
                    ResponseTimeoutSeconds: godonext.Int(
                        5,
                    ),
                    UnhealthyThreshold: godonext.Int(
                        3,
                    ),
                    HealthyThreshold: godonext.Int(
                        5,
                    ),
                },
                StickySessions: &godonext.StickySessions{
                    Type: godonext.StickySessionsTypeNone.Ptr(),
                },
                RedirectHTTPToHTTPS: godonext.Bool(
                    false,
                ),
                EnableProxyProtocol: godonext.Bool(
                    true,
                ),
                EnableBackendKeepalive: godonext.Bool(
                    true,
                ),
                HTTPIdleTimeoutSeconds: godonext.Int(
                    60,
                ),
                VpcUUID: godonext.String(
                    "c33931f2-a26a-4e61-b85c-4e95a2ec431b",
                ),
                Firewall: &godonext.LbFirewall{
                    Deny: []string{
                        "cidr:1.2.0.0/16",
                        "ip:2.3.4.5",
                    },
                    Allow: []string{
                        "ip:1.2.3.4",
                        "cidr:2.3.4.0/24",
                    },
                },
                DropletIDs: []int{
                    3164444,
                    3164445,
                },
                Region: godonext.RegionSlugNyc3,
            },
        },
    }
client.LoadBalancers.LoadBalancersUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.LoadBalancerCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersDelete(LbID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a load balancer instance, disassociating any Droplets assigned to it
and removing it from your account, send a DELETE request to
`/v2/load_balancers/$LOAD_BALANCER_ID`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersDeleteRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.LoadBalancers.LoadBalancersDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersDeleteCache(LbID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a Global load balancer CDN cache, send a DELETE request to
`/v2/load_balancers/$LOAD_BALANCER_ID/cache`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersDeleteCacheRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.LoadBalancers.LoadBalancersDeleteCache(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersAddDroplets(LbID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To assign a Droplet to a load balancer instance, send a POST request to
`/v2/load_balancers/$LOAD_BALANCER_ID/droplets`. In the body of the request,
there should be a `droplet_ids` attribute containing a list of Droplet IDs.
Individual Droplets can not be added to a load balancer configured with a
Droplet tag. Attempting to do so will result in a "422 Unprocessable Entity"
response from the API.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersAddDropletsRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        DropletIDs: []int{
            3164444,
            3164445,
        },
    }
client.LoadBalancers.LoadBalancersAddDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**dropletIDs:** `[]int` — An array containing the IDs of the Droplets assigned to the load balancer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersRemoveDroplets(LbID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove a Droplet from a load balancer instance, send a DELETE request to
`/v2/load_balancers/$LOAD_BALANCER_ID/droplets`. In the body of the request,
there should be a `droplet_ids` attribute containing a list of Droplet IDs.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersRemoveDropletsRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        DropletIDs: []int{
            3164444,
            3164445,
        },
    }
client.LoadBalancers.LoadBalancersRemoveDroplets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**dropletIDs:** `[]int` — An array containing the IDs of the Droplets assigned to the load balancer.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersAddForwardingRules(LbID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add an additional forwarding rule to a load balancer instance, send a POST
request to `/v2/load_balancers/$LOAD_BALANCER_ID/forwarding_rules`. In the body
of the request, there should be a `forwarding_rules` attribute containing an
array of rules to be added.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersAddForwardingRulesRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        ForwardingRules: []*godonext.ForwardingRule{
            &godonext.ForwardingRule{
                EntryProtocol: godonext.ForwardingRuleEntryProtocolHTTP,
                EntryPort: 443,
                TargetProtocol: godonext.ForwardingRuleTargetProtocolHTTP,
                TargetPort: 80,
            },
        },
    }
client.LoadBalancers.LoadBalancersAddForwardingRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**forwardingRules:** `[]*godonext.ForwardingRule` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.LoadBalancers.LoadBalancersRemoveForwardingRules(LbID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove forwarding rules from a load balancer instance, send a DELETE
request to `/v2/load_balancers/$LOAD_BALANCER_ID/forwarding_rules`. In the
body of the request, there should be a `forwarding_rules` attribute containing
an array of rules to be removed.

No response body will be sent back, but the response code will indicate
success. Specifically, the response code will be a 204, which means that the
action was successful with no returned body data.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.LoadBalancersRemoveForwardingRulesRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        ForwardingRules: []*godonext.ForwardingRule{
            &godonext.ForwardingRule{
                EntryProtocol: godonext.ForwardingRuleEntryProtocolHTTP,
                EntryPort: 443,
                TargetProtocol: godonext.ForwardingRuleTargetProtocolHTTP,
                TargetPort: 80,
            },
        },
    }
client.LoadBalancers.LoadBalancersRemoveForwardingRules(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**forwardingRules:** `[]*godonext.ForwardingRule` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Monitoring
<details><summary><code>client.Monitoring.ListAlertpolicy() -> *godonext.MonitoringListAlertPolicyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all alert policies that are configured for the given account. To List all alert policies, send a GET request to `/v2/monitoring/alerts`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringListAlertPolicyRequest{}
client.Monitoring.ListAlertpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.CreateAlertpolicy(request) -> *godonext.MonitoringCreateAlertPolicyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new alert, send a POST request to `/v2/monitoring/alerts`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AlertPolicyRequest{
        Alerts: &godonext.Alerts{
            Email: []string{
                "bob@exmaple.com",
            },
            Slack: []*godonext.SlackDetails{
                &godonext.SlackDetails{
                    Channel: "Production Alerts",
                    URL: "https://hooks.slack.example/services/T1234567/AAAAAAAA/ZZZZZZ",
                },
            },
        },
        Compare: godonext.AlertPolicyRequestCompareGreaterThan,
        Description: "CPU Alert",
        Enabled: true,
        Entities: []string{
            "192018292",
        },
        Tags: []string{
            "droplet_tag",
        },
        Type: godonext.AlertPolicyRequestTypeV1InsightsDropletLoad1,
        Value: 80,
        Window: godonext.AlertPolicyRequestWindowFiveM,
    }
client.Monitoring.CreateAlertpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.AlertPolicyRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetAlertpolicy(AlertUUID) -> *godonext.MonitoringGetAlertPolicyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a given alert policy, send a GET request to `/v2/monitoring/alerts/{alert_uuid}`
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetAlertPolicyRequest{
        AlertUUID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Monitoring.GetAlertpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alertUUID:** `string` — A unique identifier for an alert policy.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.UpdateAlertpolicy(AlertUUID, request) -> *godonext.MonitoringUpdateAlertPolicyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update en existing policy, send a PUT request to `v2/monitoring/alerts/{alert_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringUpdateAlertPolicyRequest{
        AlertUUID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.AlertPolicyRequest{
            Alerts: &godonext.Alerts{
                Email: []string{
                    "bob@exmaple.com",
                },
                Slack: []*godonext.SlackDetails{
                    &godonext.SlackDetails{
                        Channel: "Production Alerts",
                        URL: "https://hooks.slack.example/services/T1234567/AAAAAAAA/ZZZZZZ",
                    },
                },
            },
            Compare: godonext.AlertPolicyRequestCompareGreaterThan,
            Description: "CPU Alert",
            Enabled: true,
            Entities: []string{
                "192018292",
            },
            Tags: []string{
                "droplet_tag",
            },
            Type: godonext.AlertPolicyRequestTypeV1InsightsDropletLoad1,
            Value: 80,
            Window: godonext.AlertPolicyRequestWindowFiveM,
        },
    }
client.Monitoring.UpdateAlertpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alertUUID:** `string` — A unique identifier for an alert policy.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.AlertPolicyRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.DeleteAlertpolicy(AlertUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an alert policy, send a DELETE request to `/v2/monitoring/alerts/{alert_uuid}`
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringDeleteAlertPolicyRequest{
        AlertUUID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Monitoring.DeleteAlertpolicy(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alertUUID:** `string` — A unique identifier for an alert policy.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletbandwidthmetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve bandwidth metrics for a given Droplet, send a GET request to `/v2/monitoring/metrics/droplet/bandwidth`. Use the `interface` query parameter to specify if the results should be for the `private` or `public` interface. Use the `direction` query parameter to specify if the results should be for `inbound` or `outbound` traffic.
The metrics in the response body are in megabits per second (Mbps).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletBandwidthMetricsRequest{
        HostID: "17209102",
        Interface: godonext.MonitoringGetDropletBandwidthMetricsRequestInterfacePrivate,
        Direction: godonext.MonitoringGetDropletBandwidthMetricsRequestDirectionInbound,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletbandwidthmetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**interface_:** `*godonext.MonitoringGetDropletBandwidthMetricsRequestInterface` — The network interface.
    
</dd>
</dl>

<dl>
<dd>

**direction:** `*godonext.MonitoringGetDropletBandwidthMetricsRequestDirection` — The traffic direction.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletcpumetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve CPU metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/cpu`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletCPUMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletcpumetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletfilesystemfreemetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve filesystem free metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/filesystem_free`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletFilesystemFreeMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletfilesystemfreemetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletfilesystemsizemetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve filesystem size metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/filesystem_size`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletFilesystemSizeMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletfilesystemsizemetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletload1Metrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve 1 minute load average metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/load_1`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletLoad1MetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletload1Metrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletload5Metrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve 5 minute load average metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/load_5`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletLoad5MetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletload5Metrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletload15Metrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve 15 minute load average metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/load_15`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletLoad15MetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletload15Metrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletmemorycachedmetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve cached memory metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/memory_cached`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletMemoryCachedMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletmemorycachedmetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletmemoryfreemetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve free memory metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/memory_free`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletMemoryFreeMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletmemoryfreemetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletmemorytotalmetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve total memory metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/memory_total`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletMemoryTotalMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletmemorytotalmetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletmemoryavailablemetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve available memory metrics for a given droplet, send a GET request to `/v2/monitoring/metrics/droplet/memory_available`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletMemoryAvailableMetricsRequest{
        HostID: "17209102",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletmemoryavailablemetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**hostID:** `string` — The droplet ID.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetAppmemorypercentagemetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve memory percentage metrics for a given app, send a GET request to `/v2/monitoring/metrics/apps/memory_percentage`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetAppMemoryPercentageMetricsRequest{
        AppID: "2db3c021-15ad-4088-bfe8-99dc972b9cf6",
        AppComponent: godonext.String(
            "sample-application",
        ),
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetAppmemorypercentagemetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app UUID.
    
</dd>
</dl>

<dl>
<dd>

**appComponent:** `*string` — The app component name.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetAppcpupercentagemetrics() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve cpu percentage metrics for a given app, send a GET request to `/v2/monitoring/metrics/apps/cpu_percentage`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetAppCPUPercentageMetricsRequest{
        AppID: "2db3c021-15ad-4088-bfe8-99dc972b9cf6",
        AppComponent: godonext.String(
            "sample-application",
        ),
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetAppcpupercentagemetrics(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app UUID.
    
</dd>
</dl>

<dl>
<dd>

**appComponent:** `*string` — The app component name.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetApprestartcountmetricsYml() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve restart count metrics for a given app, send a GET request to `/v2/monitoring/metrics/apps/restart_count`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetAppRestartCountMetricsYmlRequest{
        AppID: "2db3c021-15ad-4088-bfe8-99dc972b9cf6",
        AppComponent: godonext.String(
            "sample-application",
        ),
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetApprestartcountmetricsYml(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**appID:** `string` — The app UUID.
    
</dd>
</dl>

<dl>
<dd>

**appComponent:** `*string` — The app component name.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendConnectionsCurrent() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend total current active connections for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_connections_current`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendConnectionsCurrentRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendConnectionsCurrent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendConnectionsLimit() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend max connections limit for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_connections_limit`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendConnectionsLimitRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendConnectionsLimit(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendCPUUtilization() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend average percentage CPU utilization for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_cpu_utilization`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendCPUUtilizationRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendCPUUtilization(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendFirewallDroppedBytes() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve firewall dropped bytes for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_firewall_dropped_bytes`. This is currently only supported for network load balancers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendFirewallDroppedBytesRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendFirewallDroppedBytes(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendFirewallDroppedPackets() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve firewall dropped packets per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_firewall_dropped_packets`. This is currently only supported for network load balancers.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendFirewallDroppedPacketsRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendFirewallDroppedPackets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendHTTPResponses() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend HTTP rate of response code for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_http_responses`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendHTTPResponsesRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendHTTPResponses(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendHTTPRequestsPerSecond() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend HTTP requests per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_http_requests_per_second`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendHTTPRequestsPerSecondRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendHTTPRequestsPerSecond(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendNetworkThroughputHTTP() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend HTTP throughput in bytes per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_network_throughput_http`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendNetworkThroughputHTTPRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendNetworkThroughputHTTP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendNetworkThroughputUDP() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend UDP throughput in bytes per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_network_throughput_udp`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendNetworkThroughputUDPRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendNetworkThroughputUDP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendNetworkThroughputTCP() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend TCP throughput in bytes per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_network_throughput_tcp`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendNetworkThroughputTCPRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendNetworkThroughputTCP(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendNlbTCPNetworkThroughput() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend TCP throughput in bytes per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_nlb_tcp_network_throughput`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendNlbTCPNetworkThroughputRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendNlbTCPNetworkThroughput(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendNlbUDPNetworkThroughput() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend UDP throughput in bytes per second for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_nlb_udp_network_throughput`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendNlbUDPNetworkThroughputRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendNlbUDPNetworkThroughput(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendTLSConnectionsCurrent() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend current TLS connections rate for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_tls_connections_current`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendTLSConnectionsCurrentRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendTLSConnectionsCurrent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendTLSConnectionsLimit() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend max TLS connections limit for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_tls_connections_limit`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendTLSConnectionsLimitRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendTLSConnectionsLimit(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbFrontendTLSConnectionsExceedingRateLimit() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve frontend closed TLS connections for exceeded rate limit for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/frontend_tls_connections_exceeding_rate_limit`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbFrontendTLSConnectionsExceedingRateLimitRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbFrontendTLSConnectionsExceedingRateLimit(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPSessionDurationAvg() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets average HTTP session duration in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_session_duration_avg`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPSessionDurationAvgRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPSessionDurationAvg(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPSessionDuration50P() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets 50th percentile HTTP session duration in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_session_duration_50p`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPSessionDuration50PRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPSessionDuration50P(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPSessionDuration95P() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets 95th percentile HTTP session duration in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_session_duration_95p`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPSessionDuration95PRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPSessionDuration95P(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPResponseTimeAvg() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets average HTTP response time in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_response_time_avg`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPResponseTimeAvgRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPResponseTimeAvg(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPResponseTime50P() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets 50th percentile HTTP response time in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_response_time_50p`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPResponseTime50PRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPResponseTime50P(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPResponseTime95P() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets 95th percentile HTTP response time in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_response_time_95p`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPResponseTime95PRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPResponseTime95P(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPResponseTime99P() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets 99th percentile HTTP response time in seconds for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_response_time_99p`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPResponseTime99PRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPResponseTime99P(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsQueueSize() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets queue size for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_queue_size`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsQueueSizeRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsQueueSize(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHTTPResponses() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets HTTP rate of response code for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_http_responses`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHTTPResponsesRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHTTPResponses(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsConnections() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets active connections for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_connections`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsConnectionsRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsConnections(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsHealthChecks() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets health check status for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_health_checks`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsHealthChecksRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsHealthChecks(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetLbDropletsDowntime() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve Droplets downtime status for a given load balancer, send a GET request to `/v2/monitoring/metrics/load_balancer/droplets_downtime`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetLbDropletsDowntimeRequest{
        LbID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetLbDropletsDowntime(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**lbID:** `string` — A unique identifier for a load balancer.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletAutoscaleCurrentInstances() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the current size for a given Droplet Autoscale Pool, send a GET request to `/v2/monitoring/metrics/droplet_autoscale/current_instances`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletAutoscaleCurrentInstancesRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletAutoscaleCurrentInstances(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletAutoscaleTargetInstances() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the target size for a given Droplet Autoscale Pool, send a GET request to `/v2/monitoring/metrics/droplet_autoscale/target_instances`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletAutoscaleTargetInstancesRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletAutoscaleTargetInstances(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletAutoscaleCurrentCPUUtilizationYml() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the current average CPU utilization for a given Droplet Autoscale Pool, send a GET request to `/v2/monitoring/metrics/droplet_autoscale/current_cpu_utilization`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletAutoscaleCurrentCPUUtilizationYmlRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletAutoscaleCurrentCPUUtilizationYml(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletAutoscaleTargetCPUUtilization() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the target average CPU utilization for a given Droplet Autoscale Pool, send a GET request to `/v2/monitoring/metrics/droplet_autoscale/target_cpu_utilization`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletAutoscaleTargetCPUUtilizationRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletAutoscaleTargetCPUUtilization(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletAutoscaleCurrentMemoryUtilization() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the current average memory utilization for a given Droplet Autoscale Pool, send a GET request to `/v2/monitoring/metrics/droplet_autoscale/current_memory_utilization`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletAutoscaleCurrentMemoryUtilizationRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletAutoscaleCurrentMemoryUtilization(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDropletAutoscaleTargetMemoryUtilization() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the target average memory utilization for a given Droplet Autoscale Pool, send a GET request to `/v2/monitoring/metrics/droplet_autoscale/target_memory_utilization`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDropletAutoscaleTargetMemoryUtilizationRequest{
        AutoscalePoolID: "0d3db13e-a604-4944-9827-7ec2642d32ac",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDropletAutoscaleTargetMemoryUtilization(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**autoscalePoolID:** `string` — A unique identifier for an autoscale pool.
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlCPUUsage() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve CPU usage (percent) for a MySQL cluster. Response is a time series of cluster-level CPU usage. Use **aggregate** to get avg, max, or min over the range.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlCPUUsageRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Aggregate: godonext.MonitoringGetDatabaseMysqlCPUUsageRequestAggregateAvg,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlCPUUsage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**aggregate:** `*godonext.MonitoringGetDatabaseMysqlCPUUsageRequestAggregate` — Aggregation over the time range (avg, max, or min).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlLoad() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve load metrics for a MySQL cluster. Use **metric** for the window: **load1** (1-minute), **load5** (5-minute), or **load15** (15-minute). Use **aggregate** to get either the average (avg) or maximum (max) over that window over the time range.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlLoadRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Metric: godonext.MonitoringGetDatabaseMysqlLoadRequestMetricLoad1,
        Aggregate: godonext.MonitoringGetDatabaseMysqlLoadRequestAggregateAvg,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlLoad(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**metric:** `*godonext.MonitoringGetDatabaseMysqlLoadRequestMetric` — Load window: **load1** (1-minute), **load5** (5-minute), **load15** (15-minute). The value is either average or max over that window, depending on the **aggregate** parameter (avg or max).
    
</dd>
</dl>

<dl>
<dd>

**aggregate:** `*godonext.MonitoringGetDatabaseMysqlLoadRequestAggregate` — Aggregation over the time range (avg or max).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlMemoryUsage() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve memory usage (percent) for a MySQL cluster. Use **aggregate** (avg, max, or min) over the time range.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlMemoryUsageRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Aggregate: godonext.MonitoringGetDatabaseMysqlMemoryUsageRequestAggregateAvg,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlMemoryUsage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**aggregate:** `*godonext.MonitoringGetDatabaseMysqlMemoryUsageRequestAggregate` — Aggregation over the time range (avg, max, or min).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlDiskUsage() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve disk usage (percent) for a MySQL cluster. Use **aggregate** (avg, max, or min) over the time range.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlDiskUsageRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Aggregate: godonext.MonitoringGetDatabaseMysqlDiskUsageRequestAggregateAvg,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlDiskUsage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**aggregate:** `*godonext.MonitoringGetDatabaseMysqlDiskUsageRequestAggregate` — Aggregation over the time range (avg, max, or min).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlThreadsConnected() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve current threads connected for a MySQL service (gauge).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlThreadsConnectedRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlThreadsConnected(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlThreadsCreatedRate() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve threads created rate for a MySQL service (per second).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlThreadsCreatedRateRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlThreadsCreatedRate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlThreadsActive() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve active (running) threads for a MySQL service.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlThreadsActiveRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlThreadsActive(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlIndexVsSequentialReads() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve index vs sequential reads ratio (percent) for a MySQL service — i.e. percentage of reads using an index.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlIndexVsSequentialReadsRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlIndexVsSequentialReads(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlOpRates() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve operations rate (per second) for a MySQL service. Use **metric** to choose select, insert, update, or delete.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlOpRatesRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Metric: godonext.MonitoringGetDatabaseMysqlOpRatesRequestMetricSelect,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlOpRates(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**metric:** `*godonext.MonitoringGetDatabaseMysqlOpRatesRequestMetric` — Operation type (select, insert, update, or delete).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlSchemaThroughput() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve table I/O throughput (rows per second) for a schema. Requires **schema** and **metric** (insert, fetch, update, delete).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlSchemaThroughputRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Schema: "defaultdb",
        Metric: godonext.MonitoringGetDatabaseMysqlSchemaThroughputRequestMetricInsert,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlSchemaThroughput(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**schema:** `string` — The schema (database) name.
    
</dd>
</dl>

<dl>
<dd>

**metric:** `*godonext.MonitoringGetDatabaseMysqlSchemaThroughputRequestMetric` — Table I/O operation (insert, fetch, update, or delete).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDatabaseMysqlSchemaLatency() -> *godonext.Metrics</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve table I/O latency (seconds) for a schema. Requires **schema** and **metric** (insert, fetch, update, delete).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDatabaseMysqlSchemaLatencyRequest{
        DbID: "9cc10173-e9ea-4176-9dbc-a4cee4c4ff30",
        Schema: "defaultdb",
        Metric: godonext.MonitoringGetDatabaseMysqlSchemaLatencyRequestMetricInsert,
        Start: "1620683817",
        End: "1620705417",
    }
client.Monitoring.GetDatabaseMysqlSchemaLatency(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dbID:** `string` — The DBaaS cluster UUID (database ID).
    
</dd>
</dl>

<dl>
<dd>

**schema:** `string` — The schema (database) name.
    
</dd>
</dl>

<dl>
<dd>

**metric:** `*godonext.MonitoringGetDatabaseMysqlSchemaLatencyRequestMetric` — Table I/O operation (insert, fetch, update, or delete).
    
</dd>
</dl>

<dl>
<dd>

**start:** `string` — UNIX timestamp to start metric window.
    
</dd>
</dl>

<dl>
<dd>

**end:** `string` — UNIX timestamp to end metric window.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.ListDestinations() -> *godonext.MonitoringListDestinationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all logging destinations, send a GET request to `/v2/monitoring/sinks/destinations`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Monitoring.ListDestinations(
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

<details><summary><code>client.Monitoring.CreateDestination(request) -> *godonext.MonitoringCreateDestinationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new destination, send a POST request to `/v2/monitoring/sinks/destinations`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.DestinationRequest{
        Name: godonext.String(
            "managed_opensearch_cluster",
        ),
        Type: godonext.DestinationRequestTypeOpensearchDbaas,
        Config: &godonext.OpensearchConfigRequest{
            Endpoint: "db-opensearch-nyc3-123456-do-user-123456-0.g.db.ondigitalocean.com",
            ClusterUUID: godonext.String(
                "85148069-7e35-4999-80bd-6fa1637ca385",
            ),
            ClusterName: godonext.String(
                "managed_dbaas_cluster",
            ),
            IndexName: godonext.String(
                "logs",
            ),
            RetentionDays: godonext.Int(
                14,
            ),
        },
    }
client.Monitoring.CreateDestination(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.DestinationRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetDestination(DestinationUUID) -> *godonext.MonitoringGetDestinationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get the details of a destination, send a GET request to `/v2/monitoring/sinks/destinations/${destination_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetDestinationRequest{
        DestinationUUID: "1a64809f-1708-48ee-a742-dec8d481b8d1",
    }
client.Monitoring.GetDestination(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `string` — A unique identifier for a destination.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.UpdateDestination(DestinationUUID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the details of a destination, send a PATCH request to `/v2/monitoring/sinks/destinations/${destination_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringUpdateDestinationRequest{
        DestinationUUID: "1a64809f-1708-48ee-a742-dec8d481b8d1",
        Body: &godonext.DestinationRequest{
            Type: godonext.DestinationRequestTypeOpensearchDbaas,
            Config: &godonext.OpensearchConfigRequest{
                Endpoint: "example.com",
            },
        },
    }
client.Monitoring.UpdateDestination(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `string` — A unique identifier for a destination.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.DestinationRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.DeleteDestination(DestinationUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a destination and all associated sinks, send a DELETE request to `/v2/monitoring/sinks/destinations/${destination_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringDeleteDestinationRequest{
        DestinationUUID: "1a64809f-1708-48ee-a742-dec8d481b8d1",
    }
client.Monitoring.DeleteDestination(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `string` — A unique identifier for a destination.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.ListSinks() -> *godonext.MonitoringListSinksResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all sinks, send a GET request to `/v2/monitoring/sinks`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringListSinksRequest{
        ResourceID: godonext.String(
            "do:droplet:13457723",
        ),
    }
client.Monitoring.ListSinks(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resourceID:** `*godonext.Urn` — A unique URN for a resource.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.CreateSink(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new sink, send a POST request to `/v2/monitoring/sinks`. Forwards logs from the 
resources identified in `resources` to the specified pre-existing destination.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringCreateSinkRequest{}
client.Monitoring.CreateSink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**destinationUUID:** `*string` — A unique identifier for an already-existing destination.
    
</dd>
</dl>

<dl>
<dd>

**resources:** `[]*godonext.SinkResource` — List of resources identified by their URNs.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.GetSink(SinkUUID) -> *godonext.MonitoringGetSinkResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get the details of a sink (resources and destination), send a GET request to `/v2/monitoring/sinks/${sink_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringGetSinkRequest{
        SinkUUID: "78b172b6-52c3-4a4b-96d5-78d3f1a0b18c",
    }
client.Monitoring.GetSink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sinkUUID:** `string` — A unique identifier for a sink.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Monitoring.DeleteSink(SinkUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a sink, send a DELETE request to `/v2/monitoring/sinks/${sink_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MonitoringDeleteSinkRequest{
        SinkUUID: "78b172b6-52c3-4a4b-96d5-78d3f1a0b18c",
    }
client.Monitoring.DeleteSink(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sinkUUID:** `string` — A unique identifier for a sink.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## NFS
<details><summary><code>client.Nfs.List() -> *godonext.NfsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list NFS shares, send a GET request to `/v2/nfs?region=${region}`.

A successful request will return all NFS shares belonging to the authenticated user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsListRequest{
        Region: godonext.String(
            "atl1",
        ),
    }
client.Nfs.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Nfs.Create(request) -> *godonext.NfsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new NFS share, send a POST request to `/v2/nfs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsRequest{
        Name: "sammy-share-drive",
        SizeGib: 1024,
        Region: "atl1",
        VpcIDs: []string{
            "796c6fe3-2a1d-4da2-9f3e-38239827dc91",
        },
        PerformanceTier: godonext.String(
            "standard",
        ),
    }
client.Nfs.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — The human-readable name of the share.
    
</dd>
</dl>

<dl>
<dd>

**sizeGib:** `int` — The desired/provisioned size of the share in GiB (Gibibytes). Must be >= 50.
    
</dd>
</dl>

<dl>
<dd>

**region:** `string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>

<dl>
<dd>

**vpcIDs:** `[]string` — List of VPC IDs that should be able to access the share.
    
</dd>
</dl>

<dl>
<dd>

**performanceTier:** `*string` — The performance tier of the share.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Nfs.Get(NfsID) -> *godonext.NfsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get an NFS share, send a GET request to `/v2/nfs/{nfs_id}?region=${region}`.

A successful request will return the NFS share.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsGetRequest{
        NfsID: "0a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
        Region: godonext.String(
            "atl1",
        ),
    }
client.Nfs.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsID:** `string` — The unique ID of the NFS share
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Nfs.Delete(NfsID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an NFS share, send a DELETE request to `/v2/nfs/{nfs_id}?region=${region}`.

A successful request will return a `204 No Content` status code.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsDeleteRequest{
        NfsID: "0a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
        Region: godonext.String(
            "atl1",
        ),
    }
client.Nfs.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsID:** `string` — The unique ID of the NFS share
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Nfs.ListSnapshot() -> *godonext.NfsSnapshotListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all NFS snapshots, send a GET request to `/v2/nfs/snapshots?region=${region}&share_id={share_id}`.

A successful request will return all NFS snapshots belonging to the authenticated user in the specified region.

Optionally, you can filter snapshots by a specific NFS share by including the `share_id` query parameter.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsListSnapshotRequest{
        Region: godonext.String(
            "atl1",
        ),
        ShareID: godonext.String(
            "0a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
        ),
    }
client.Nfs.ListSnapshot(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>

<dl>
<dd>

**shareID:** `*string` — The unique ID of an NFS share. If provided, only snapshots of this specific share will be returned.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Nfs.GetSnapshot(NfsSnapshotID) -> *godonext.NfsSnapshotGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get an NFS snapshot, send a GET request to `/v2/nfs/snapshots/{nfs_snapshot_id}?region=${region}`.

A successful request will return the NFS snapshot.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsGetSnapshotRequest{
        NfsSnapshotID: "0a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
        Region: godonext.String(
            "atl1",
        ),
    }
client.Nfs.GetSnapshot(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsSnapshotID:** `string` — The unique ID of the NFS snapshot
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Nfs.DeleteSnapshot(NfsSnapshotID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an NFS snapshot, send a DELETE request to `/v2/nfs/snapshots/{nfs_snapshot_id}?region=${region}`.

A successful request will return a `204 No Content` status code.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsDeleteSnapshotRequest{
        NfsSnapshotID: "0a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
        Region: godonext.String(
            "atl1",
        ),
    }
client.Nfs.DeleteSnapshot(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsSnapshotID:** `string` — The unique ID of the NFS snapshot
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region slug (e.g., nyc2, atl1) where the NFS share resides.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## NFS Actions
<details><summary><code>client.NfsActions.NfsCreateAction(NfsID, request) -> *godonext.NfsActionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To execute an action (such as resize) on a specified NFS share, 
send a POST request to `/v2/nfs/{nfs_id}/actions`. In the JSON body 
to the request, set the `type` attribute to on of the supported action types:

| Action                           | Details |
| -------------------------------- | ----------- |
| <nobr>`resize`</nobr>            | Resizes an NFS share. Set the size_gib attribute to a desired value in GiB |
| <nobr>`snapshot`</nobr>          | Takes a snapshot of an NFS share |
| <nobr>`attach`</nobr>            | Attaches an NFS share to a VPC. Set the vpc_id attribute to the desired VPC ID |
| <nobr>`detach`</nobr>            | Detaches an NFS share from a VPC. Set the vpc_id attribute to the desired VPC ID |
| <nobr>`reassign`</nobr>          | Reassigns an NFS share from one VPC to another. Set the old_vpc_id and new_vpc_id attributes to the desired VPC IDs |
| <nobr>`switch_performance_tier`</nobr> | Switches the performance tier of an NFS share. Set the performance_tier attribute to the desired tier (e.g., standard, high) |
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.NfsCreateActionRequest{
        NfsID: "0a1b2c3d-4e5f-6a7b-8c9d-0e1f2a3b4c5d",
        Body: &godonext.NfsCreateActionRequestBody{
            NfsActionResize: &godonext.NfsActionResize{
                Type: godonext.NfsActionTypeResize,
            },
        },
    }
client.NfsActions.NfsCreateAction(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**nfsID:** `string` — The unique ID of the NFS share
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.NfsCreateActionRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Partner Network Connect
<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsList() -> *godonext.PartnerAttachmentsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the Partner Attachments on your account, send a `GET` request to `/v2/partner_network_connect/attachments`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsListRequest{}
client.PartnerNetworkConnect.PartnerAttachmentsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsCreate(request) -> *godonext.PartnerAttachmentsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new partner attachment, send a `POST` request to
`/v2/partner_network_connect/attachments` with a JSON object containing the
required configuration details.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentWritable{
        Name: "env.prod-partner-network-connect",
        ConnectionBandwidthInMbps: 1000,
        Region: godonext.PartnerAttachmentWritableRegionNyc,
        NaasProvider: "megaport",
        VpcIDs: []string{
            "c140286f-e6ce-4131-8b7b-df4590ce8d6a",
            "994a2735-dc84-11e8-80bc-3cfdfea9fba1",
        },
    }
client.PartnerNetworkConnect.PartnerAttachmentsCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — The name of the partner attachment. Must be unique and may only contain alphanumeric characters, dashes, and periods.
    
</dd>
</dl>

<dl>
<dd>

**connectionBandwidthInMbps:** `int` — Bandwidth (in Mbps) of the connection.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.PartnerAttachmentWritableRegion` — The region to create the partner attachment.
    
</dd>
</dl>

<dl>
<dd>

**naasProvider:** `string` 
    
</dd>
</dl>

<dl>
<dd>

**vpcIDs:** `[]string` — An array of VPCs IDs.
    
</dd>
</dl>

<dl>
<dd>

**parentUUID:** `*string` — Optional associated partner attachment UUID
    
</dd>
</dl>

<dl>
<dd>

**bgp:** `*godonext.PartnerAttachmentWritableBgp` — Optional BGP configurations
    
</dd>
</dl>

<dl>
<dd>

**redundancyZone:** `*godonext.PartnerAttachmentWritableRedundancyZone` — Optional redundancy zone for the partner attachment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsGet(PaID) -> *godonext.PartnerAttachmentsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get the details of a partner attachment, send a `GET` request to
`/v2/partner_network_connect/attachments/{pa_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsGetRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.PartnerNetworkConnect.PartnerAttachmentsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsDelete(PaID) -> *godonext.PartnerAttachmentsDeleteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an existing partner attachment, send a `DELETE` request to
`/v2/partner_network_connect/attachments/{pa_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsDeleteRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.PartnerNetworkConnect.PartnerAttachmentsDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsPatch(PaID, request) -> *godonext.PartnerAttachmentsPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an existing partner attachment, send a `PATCH` request to
`/v2/partner_network_connect/attachments/{pa_id}` with a JSON object containing the
fields to be updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsPatchRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.PartnerAttachmentUpdatable{
            PartnerAttachmentUpdatableName: &godonext.PartnerAttachmentUpdatableName{
                Name: "env.prod-partner-network-connect",
            },
        },
    }
client.PartnerNetworkConnect.PartnerAttachmentsPatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.PartnerAttachmentUpdatable` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsGetBgpAuthKey(PaID) -> *godonext.PartnerAttachmentsGetBgpAuthKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get the current BGP auth key for a partner attachment, send a `GET` request to
`/v2/partner_network_connect/attachments/{pa_id}/bgp_auth_key`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsGetBgpAuthKeyRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.PartnerNetworkConnect.PartnerAttachmentsGetBgpAuthKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsListRemoteRoutes(PaID) -> *godonext.PartnerAttachmentsListRemoteRoutesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all remote routes associated with a partner attachment, send a `GET` request to
`/v2/partner_network_connect/attachments/{pa_id}/remote_routes`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsListRemoteRoutesRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.PartnerNetworkConnect.PartnerAttachmentsListRemoteRoutes(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsGetServiceKey(PaID) -> *godonext.PartnerAttachmentsGetServiceKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get the current service key for a partner attachment, send a `GET` request to
`/v2/partner_network_connect/attachments/{pa_id}/service_key`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsGetServiceKeyRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.PartnerNetworkConnect.PartnerAttachmentsGetServiceKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.PartnerNetworkConnect.PartnerAttachmentsCreateServiceKey(PaID) -> *godonext.PartnerAttachmentsCreateServiceKeyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This operation generates a new service key for the specified partner attachment. The operation is asynchronous, and the response is an empty JSON object returned with a 202 status code. To poll for the new service key, send a `GET` request to `/v2/partner_network_connect/attachments/{pa_id}/service_key`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.PartnerAttachmentsCreateServiceKeyRequest{
        PaID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.PartnerNetworkConnect.PartnerAttachmentsCreateServiceKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**paID:** `string` — A unique identifier for a partner attachment.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Projects
<details><summary><code>client.Projects.List() -> *godonext.ProjectsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all your projects, send a GET request to `/v2/projects`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsListRequest{}
client.Projects.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.Create(request) -> *godonext.ProjectsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a project, send a POST request to `/v2/projects`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectBase{}
client.Projects.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ProjectBase` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.GetDefault() -> *godonext.ProjectsGetDefaultResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get your default project, send a GET request to `/v2/projects/default`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Projects.GetDefault(
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

<details><summary><code>client.Projects.UpdateDefault(request) -> *godonext.ProjectsUpdateDefaultResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update you default project, send a PUT request to `/v2/projects/default`. All of the following attributes must be sent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Project{}
client.Projects.UpdateDefault(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.Project` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.PatchDefault(request) -> *godonext.ProjectsPatchDefaultResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update only specific attributes of your default project, send a PATCH request to `/v2/projects/default`. At least one of the following attributes needs to be sent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Project{
        Name: godonext.String(
            "my-web-api",
        ),
    }
client.Projects.PatchDefault(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.Project` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.Get(ProjectID) -> *godonext.ProjectsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a project, send a GET request to `/v2/projects/$PROJECT_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsGetRequest{
        ProjectID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Projects.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` — A unique identifier for a project.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.Update(ProjectID, request) -> *godonext.ProjectsUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a project, send a PUT request to `/v2/projects/$PROJECT_ID`. All of the following attributes must be sent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsUpdateRequest{
        ProjectID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.Project{},
    }
client.Projects.Update(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` — A unique identifier for a project.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.Project` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.Delete(ProjectID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a project, send a DELETE request to `/v2/projects/$PROJECT_ID`. To
be deleted, a project must not have any resources assigned to it. Any existing
resources must first be reassigned or destroyed, or you will receive a 412 error.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsDeleteRequest{
        ProjectID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Projects.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` — A unique identifier for a project.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Projects.Patch(ProjectID, request) -> *godonext.ProjectsPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update only specific attributes of a project, send a PATCH request to `/v2/projects/$PROJECT_ID`. At least one of the following attributes needs to be sent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsPatchRequest{
        ProjectID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.Project{
            Name: godonext.String(
                "my-web-api",
            ),
        },
    }
client.Projects.Patch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` — A unique identifier for a project.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.Project` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Project Resources
<details><summary><code>client.ProjectResources.ProjectsListResources(ProjectID) -> *godonext.ProjectsListResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all your resources in a project, send a GET request to `/v2/projects/$PROJECT_ID/resources`.

This endpoint will only return resources that you are authorized to see. For example, to see Droplets in a project, include the `droplet:read` scope.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsListResourcesRequest{
        ProjectID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.ProjectResources.ProjectsListResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` — A unique identifier for a project.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ProjectResources.ProjectsAssignResources(ProjectID, request) -> *godonext.ProjectsAssignResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To assign resources to a project, send a POST request to `/v2/projects/$PROJECT_ID/resources`.

You must have both `project:update` and `<resource>:read` scopes to assign new resources. For example, to assign a Droplet to a project, include both the `project:update` and `droplet:read` scopes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectsAssignResourcesRequest{
        ProjectID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.ProjectAssignment{
            Resources: []godonext.Urn{
                "do:droplet:13457723",
                "do:domain:example.com",
            },
        },
    }
client.ProjectResources.ProjectsAssignResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**projectID:** `string` — A unique identifier for a project.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ProjectAssignment` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ProjectResources.ProjectsListResourcesDefault() -> *godonext.ProjectsListResourcesDefaultResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all your resources in your default project, send a GET request to `/v2/projects/default/resources`.

Only resources that you are authorized to see will be returned. For example, to see Droplets in a project, include the `droplet:read` scope.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ProjectResources.ProjectsListResourcesDefault(
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

<details><summary><code>client.ProjectResources.ProjectsAssignResourcesDefault(request) -> *godonext.ProjectsAssignResourcesDefaultResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To assign resources to your default project, send a POST request to `/v2/projects/default/resources`.

You must have both project:update and <resource>:read scopes to assign new resources. For example, to assign a Droplet to the default project, include both the `project:update` and `droplet:read` scopes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ProjectAssignment{
        Resources: []godonext.Urn{
            "do:droplet:13457723",
            "do:domain:example.com",
        },
    }
client.ProjectResources.ProjectsAssignResourcesDefault(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ProjectAssignment` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Regions
<details><summary><code>client.Regions.List() -> *godonext.RegionsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the regions that are available, send a GET request to `/v2/regions`.
The response will be a JSON object with a key called `regions`. The value of this will be an array of `region` objects, each of which will contain the standard region attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegionsListRequest{}
client.Regions.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Container Registries
<details><summary><code>client.ContainerRegistries.RegistriesList() -> *godonext.RegistriesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get information about any container registry in your account, send a GET request to `/v2/registries/`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistries.RegistriesList(
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

<details><summary><code>client.ContainerRegistries.RegistriesCreate(request) -> *godonext.RegistriesCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create your container registry, send a POST request to `/v2/registries`.

The `name` becomes part of the URL for images stored in the registry. For
example, if your registry is called `example`, an image in it will have the
URL `registry.digitalocean.com/example/image:tag`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MultiregistryCreate{
        Name: "example",
    }
client.ContainerRegistries.RegistriesCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.
    
</dd>
</dl>

<dl>
<dd>

**subscriptionTierSlug:** `*godonext.MultiregistryCreateSubscriptionTierSlug` — The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.MultiregistryCreateRegion` — Slug of the region where registry data is stored. When not provided, a region will be selected.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesGet(RegistryName) -> *godonext.RegistriesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get information about any container registry in your account, send a GET request to `/v2/registries/{registry_name}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesGetRequest{
        RegistryName: "example",
    }
client.ContainerRegistries.RegistriesGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesDelete(RegistryName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete your container registry, destroying all container image data stored in it, send a DELETE request to `/v2/registries/{registry_name}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesDeleteRequest{
        RegistryName: "example",
    }
client.ContainerRegistries.RegistriesDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesGetDockerCredentials(RegistryName) -> *godonext.DockerCredentials</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

In order to access your container registry with the Docker client or from a
Kubernetes cluster, you will need to configure authentication. The necessary
JSON configuration can be retrieved by sending a GET request to
`/v2/registries/{registry_name}/docker-credentials`.

The response will be in the format of a Docker `config.json` file. To use the
config in your Kubernetes cluster, create a Secret with:

    kubectl create secret generic docr \
      --from-file=.dockerconfigjson=config.json \
      --type=kubernetes.io/dockerconfigjson

By default, the returned credentials have read-only access to your registry
and cannot be used to push images. This is appropriate for most Kubernetes
clusters. To retrieve read/write credentials, suitable for use with the Docker
client or in a CI system, read_write may be provided as query parameter. For
example: `/v2/registries/{registry_name}/docker-credentials?read_write=true`

By default, the returned credentials will not expire. To retrieve credentials
with an expiry set, expiry_seconds may be provided as a query parameter. For
example: `/v2/registries/{registry_name}/docker-credentials?expiry_seconds=3600` will return
credentials that expire after one hour.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesGetDockerCredentialsRequest{
        RegistryName: "example",
    }
client.ContainerRegistries.RegistriesGetDockerCredentials(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesGetSubscription() -> *godonext.RegistriesGetSubscriptionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A subscription is automatically created when you configure your container registry. To get information about your subscription, send a GET request to `/v2/registries/subscription`. It is similar to GET `/v2/registry/subscription`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistries.RegistriesGetSubscription(
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

<details><summary><code>client.ContainerRegistries.RegistriesUpdateSubscription(request) -> *godonext.RegistriesUpdateSubscriptionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

After creating your registry, you can switch to a different subscription tier to better suit your needs. To do this, send a POST request to `/v2/registries/subscription`. It is similar to POST `/v2/registry/subscription`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesUpdateSubscriptionRequest{}
client.ContainerRegistries.RegistriesUpdateSubscription(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tierSlug:** `*godonext.RegistriesUpdateSubscriptionRequestTierSlug` — The slug of the subscription tier to sign up for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesGetOptions() -> *godonext.RegistriesGetOptionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint serves to provide additional information as to which option values are available when creating a container registry.
There are multiple subscription tiers available for container registry. Each tier allows a different number of image repositories to be created in your registry, and has a different amount of storage and transfer included.
There are multiple regions available for container registry and controls where your data is stored.
To list the available options, send a GET request to `/v2/registries/options`. This is similar to GET `/v2/registry/options`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistries.RegistriesGetOptions(
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

<details><summary><code>client.ContainerRegistries.RegistriesGetGarbageCollection(RegistryName) -> *godonext.RegistriesGetGarbageCollectionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get information about the currently-active garbage collection for a registry, send a GET request to `/v2/registry/$REGISTRY_NAME/garbage-collection`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesGetGarbageCollectionRequest{
        RegistryName: "example",
    }
client.ContainerRegistries.RegistriesGetGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesRunGarbageCollection(RegistryName) -> *godonext.RegistriesRunGarbageCollectionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Garbage collection enables users to clear out unreferenced blobs (layer &
manifest data) after deleting one or more manifests from a repository. If
there are no unreferenced blobs resulting from the deletion of one or more
manifests, garbage collection is effectively a noop.
[See here for more information](https://docs.digitalocean.com/products/container-registry/how-to/clean-up-container-registry/)
about how and why you should clean up your container registry periodically.

To request a garbage collection run on your registry, send a POST request to
`/v2/registries/$REGISTRY_NAME/garbage-collection`. This will initiate the
following sequence of events on your registry.

* Set the registry to read-only mode, meaning no further write-scoped
  JWTs will be issued to registry clients. Existing write-scoped JWTs will
  continue to work until they expire which can take up to 15 minutes.
* Wait until all existing write-scoped JWTs have expired.
* Scan all registry manifests to determine which blobs are unreferenced.
* Delete all unreferenced blobs from the registry.
* Record the number of blobs deleted and bytes freed, mark the garbage
  collection status as `success`.
* Remove the read-only mode restriction from the registry, meaning write-scoped
  JWTs will once again be issued to registry clients.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesRunGarbageCollectionRequest{
        RegistryName: "example",
    }
client.ContainerRegistries.RegistriesRunGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesListGarbageCollections(RegistryName) -> *godonext.RegistriesListGarbageCollectionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get information about past garbage collections for a registry, send a GET request to `/v2/registry/$REGISTRY_NAME/garbage-collections`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesListGarbageCollectionsRequest{
        RegistryName: "example",
    }
client.ContainerRegistries.RegistriesListGarbageCollections(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesUpdateGarbageCollection(RegistryName, GarbageCollectionUUID, request) -> *godonext.RegistriesUpdateGarbageCollectionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To cancel the currently-active garbage collection for a registry, send a PUT request to `/v2/registries/$REGISTRY_NAME/garbage-collection/$GC_UUID` and specify one or more of the attributes below. It is similar to PUT `/v2/registries/$REGISTRY_NAME/garbage-collection/$GC_UUID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesUpdateGarbageCollectionRequest{
        RegistryName: "example",
        GarbageCollectionUUID: "eff0feee-49c7-4e8f-ba5c-a320c109c8a8",
        Body: &godonext.UpdateRegistry{},
    }
client.ContainerRegistries.RegistriesUpdateGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**garbageCollectionUUID:** `string` — The UUID of a garbage collection run.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.UpdateRegistry` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesListRepositoriesV2(RegistryName) -> *godonext.RegistriesListRepositoriesV2Response</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all repositories in your container registry, send a GET request to `/v2/registries/$REGISTRY_NAME/repositoriesV2`. It is similar to GET `/v2/registry/$REGISTRY_NAME/repositoriesV2`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesListRepositoriesV2Request{
        RegistryName: "example",
        PageToken: godonext.String(
            "eyJUb2tlbiI6IkNnZGpiMjlz",
        ),
    }
client.ContainerRegistries.RegistriesListRepositoriesV2(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return. Ignored when 'page_token' is provided.
    
</dd>
</dl>

<dl>
<dd>

**pageToken:** `*string` — Token to retrieve of the next or previous set of results more quickly than using 'page'.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesDeleteRepository(RegistryName, RepositoryName) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a container repository including all of its tags, send a DELETE request to
`/v2/registries/$REGISTRY_NAME/repositories/$REPOSITORY_NAME`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesDeleteRepositoryRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
    }
client.ContainerRegistries.RegistriesDeleteRepository(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesListRepositoryTags(RegistryName, RepositoryName) -> *godonext.RegistriesListRepositoryTagsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all tags in one of your container registry's repository, send a GET
request to `/v2/registries/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to list tags for
`registry.digitalocean.com/example/my/repo`, the path would be
`/v2/registry/example/repositories/my%2Frepo/tags`. 

It is similar to GET `/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesListRepositoryTagsRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
    }
client.ContainerRegistries.RegistriesListRepositoryTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesDeleteRepositoryTag(RegistryName, RepositoryName, RepositoryTag) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a container repository tag in on of our container registries, send a DELETE request to
`/v2/registries/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags/$TAG`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to delete
`registry.digitalocean.com/example/my/repo:mytag`, the path would be
`/v2/registry/example/repositories/my%2Frepo/tags/mytag`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully. It is similar to DELETE `/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags/$TAG`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesDeleteRepositoryTagRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
        RepositoryTag: "06a447a",
    }
client.ContainerRegistries.RegistriesDeleteRepositoryTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**repositoryTag:** `string` — The name of a container registry repository tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesListRepositoryManifests(RegistryName, RepositoryName) -> *godonext.RegistriesListRepositoryManifestsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all manifests in your container registry repository, send a GET
request to `/v2/registries/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/digests`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to list manifests for
`registry.digitalocean.com/example/my/repo`, the path would be
`/v2/registry/example/repositories/my%2Frepo/digests`.

It is similar to `/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/digests`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesListRepositoryManifestsRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
    }
client.ContainerRegistries.RegistriesListRepositoryManifests(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesDeleteRepositoryManifest(RegistryName, RepositoryName, ManifestDigest) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a container repository manifest by digest in one of your registries, send a DELETE request to
`/v2/registries/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/digests/$MANIFEST_DIGEST`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to delete
`registry.digitalocean.com/example/my/repo@sha256:abcd`, the path would be
`/v2/registry/example/repositories/my%2Frepo/digests/sha256:abcd`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.

It is similar to DELETE `/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/digests/$MANIFEST_DIGEST`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistriesDeleteRepositoryManifestRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
        ManifestDigest: "sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221",
    }
client.ContainerRegistries.RegistriesDeleteRepositoryManifest(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**manifestDigest:** `string` — The manifest digest of a container registry repository tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistries.RegistriesValidateName(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To validate that a container registry name is available for use, send a POST
request to `/v2/registries/validate-name`.

If the name is both formatted correctly and available, the response code will
be 204 and contain no body. If the name is already in use, the response will
be a 409 Conflict. 

It is similar to `/v2/registry/validate-name`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ValidateRegistry{
        Name: "example",
    }
client.ContainerRegistries.RegistriesValidateName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ValidateRegistry` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Container Registry
<details><summary><code>client.ContainerRegistry.RegistryGet() -> *godonext.RegistryGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To get information about your container registry, send a GET
request to `/v2/registry`.

This operation is not compatible with multiple registries in a DO account. You should use `/v2/registries/{registry_name}` instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistry.RegistryGet(
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

<details><summary><code>client.ContainerRegistry.RegistryCreate(request) -> *godonext.RegistryCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To create your container registry, send a POST request to `/v2/registry`.

The `name` becomes part of the URL for images stored in the registry. For
example, if your registry is called `example`, an image in it will have the
URL `registry.digitalocean.com/example/image:tag`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryCreate{
        Name: "example",
        SubscriptionTierSlug: godonext.RegistryCreateSubscriptionTierSlugStarter,
    }
client.ContainerRegistry.RegistryCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `string` — A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.
    
</dd>
</dl>

<dl>
<dd>

**subscriptionTierSlug:** `*godonext.RegistryCreateSubscriptionTierSlug` — The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.RegistryCreateRegion` — Slug of the region where registry data is stored. When not provided, a region will be selected.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryDelete() -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To delete your container registry, destroying all container image
data stored in it, send a DELETE request to `/v2/registry`.

This operation is not compatible with multiple registries in a DO account. You should use `/v2/registries/{registry_name}` instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistry.RegistryDelete(
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

<details><summary><code>client.ContainerRegistry.RegistryGetSubscription() -> *godonext.RegistryGetSubscriptionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

A subscription is automatically created when you configure your
container registry. To get information about your subscription, send a GET
request to `/v2/registry/subscription`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistry.RegistryGetSubscription(
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

<details><summary><code>client.ContainerRegistry.RegistryUpdateSubscription(request) -> *godonext.RegistryUpdateSubscriptionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

After creating your registry, you can switch to a different
subscription tier to better suit your needs. To do this, send a POST request
to `/v2/registry/subscription`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryUpdateSubscriptionRequest{}
client.ContainerRegistry.RegistryUpdateSubscription(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tierSlug:** `*godonext.RegistryUpdateSubscriptionRequestTierSlug` — The slug of the subscription tier to sign up for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryGetDockerCredentials() -> *godonext.DockerCredentials</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

In order to access your container registry with the Docker client or from a
Kubernetes cluster, you will need to configure authentication. The necessary
JSON configuration can be retrieved by sending a GET request to
`/v2/registry/docker-credentials`.

The response will be in the format of a Docker `config.json` file. To use the
config in your Kubernetes cluster, create a Secret with:

    kubectl create secret generic docr \
      --from-file=.dockerconfigjson=config.json \
      --type=kubernetes.io/dockerconfigjson

By default, the returned credentials have read-only access to your registry
and cannot be used to push images. This is appropriate for most Kubernetes
clusters. To retrieve read/write credentials, suitable for use with the Docker
client or in a CI system, read_write may be provided as query parameter. For
example: `/v2/registry/docker-credentials?read_write=true`

By default, the returned credentials will not expire. To retrieve credentials
with an expiry set, expiry_seconds may be provided as a query parameter. For
example: `/v2/registry/docker-credentials?expiry_seconds=3600` will return
credentials that expire after one hour.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryGetDockerCredentialsRequest{}
client.ContainerRegistry.RegistryGetDockerCredentials(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**expirySeconds:** `*int` — The duration in seconds that the returned registry credentials will be valid. If not set or 0, the credentials will not expire.
    
</dd>
</dl>

<dl>
<dd>

**readWrite:** `*bool` — By default, the registry credentials allow for read-only access. Set this query parameter to `true` to obtain read-write credentials.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryValidateName(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

 To validate that a container registry name is available for use, send a POST
 request to `/v2/registry/validate-name`.

 If the name is both formatted correctly and available, the response code will
 be 204 and contain no body. If the name is already in use, the response will
 be a 409 Conflict.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ValidateRegistry{
        Name: "example",
    }
client.ContainerRegistry.RegistryValidateName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ValidateRegistry` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryListRepositories(RegistryName) -> *godonext.RegistryListRepositoriesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

This endpoint has been deprecated in favor of the _List All Container Registry Repositories [V2]_ endpoint.

To list all repositories in your container registry, send a GET
request to `/v2/registry/$REGISTRY_NAME/repositories`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryListRepositoriesRequest{
        RegistryName: "example",
    }
client.ContainerRegistry.RegistryListRepositories(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryListRepositoriesV2(RegistryName) -> *godonext.RegistryListRepositoriesV2Response</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To list all repositories in your container registry, send a GET
request to `/v2/registry/$REGISTRY_NAME/repositoriesV2`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryListRepositoriesV2Request{
        RegistryName: "example",
        PageToken: godonext.String(
            "eyJUb2tlbiI6IkNnZGpiMjlz",
        ),
    }
client.ContainerRegistry.RegistryListRepositoriesV2(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return. Ignored when 'page_token' is provided.
    
</dd>
</dl>

<dl>
<dd>

**pageToken:** `*string` — Token to retrieve of the next or previous set of results more quickly than using 'page'.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryListRepositoryTags(RegistryName, RepositoryName) -> *godonext.RegistryListRepositoryTagsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To list all tags in your container registry repository, send a GET
request to `/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to list tags for
`registry.digitalocean.com/example/my/repo`, the path would be
`/v2/registry/example/repositories/my%2Frepo/tags`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryListRepositoryTagsRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
    }
client.ContainerRegistry.RegistryListRepositoryTags(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryDeleteRepositoryTag(RegistryName, RepositoryName, RepositoryTag) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To delete a container repository tag, send a DELETE request to
`/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/tags/$TAG`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to delete
`registry.digitalocean.com/example/my/repo:mytag`, the path would be
`/v2/registry/example/repositories/my%2Frepo/tags/mytag`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryDeleteRepositoryTagRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
        RepositoryTag: "06a447a",
    }
client.ContainerRegistry.RegistryDeleteRepositoryTag(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**repositoryTag:** `string` — The name of a container registry repository tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryListRepositoryManifests(RegistryName, RepositoryName) -> *godonext.RegistryListRepositoryManifestsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To list all manifests in your container registry repository, send a GET
request to `/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/digests`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to list manifests for
`registry.digitalocean.com/example/my/repo`, the path would be
`/v2/registry/example/repositories/my%2Frepo/digests`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryListRepositoryManifestsRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
    }
client.ContainerRegistry.RegistryListRepositoryManifests(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryDeleteRepositoryManifest(RegistryName, RepositoryName, ManifestDigest) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To delete a container repository manifest by digest, send a DELETE request to
`/v2/registry/$REGISTRY_NAME/repositories/$REPOSITORY_NAME/digests/$MANIFEST_DIGEST`.

Note that if your repository name contains `/` characters, it must be
URL-encoded in the request URL. For example, to delete
`registry.digitalocean.com/example/my/repo@sha256:abcd`, the path would be
`/v2/registry/example/repositories/my%2Frepo/digests/sha256:abcd`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryDeleteRepositoryManifestRequest{
        RegistryName: "example",
        RepositoryName: "repo-1",
        ManifestDigest: "sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221",
    }
client.ContainerRegistry.RegistryDeleteRepositoryManifest(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**repositoryName:** `string` — The name of a container registry repository. If the name contains `/` characters, they must be URL-encoded, e.g. `%2F`.
    
</dd>
</dl>

<dl>
<dd>

**manifestDigest:** `string` — The manifest digest of a container registry repository tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryGetGarbageCollection(RegistryName) -> *godonext.RegistryGetGarbageCollectionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To get information about the currently-active garbage collection
for a registry, send a GET request to `/v2/registry/$REGISTRY_NAME/garbage-collection`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryGetGarbageCollectionRequest{
        RegistryName: "example",
    }
client.ContainerRegistry.RegistryGetGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryRunGarbageCollection(RegistryName, request) -> *godonext.RegistryRunGarbageCollectionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

Garbage collection enables users to clear out unreferenced blobs (layer &
manifest data) after deleting one or more manifests from a repository. If
there are no unreferenced blobs resulting from the deletion of one or more
manifests, garbage collection is effectively a noop.
[See here for more information](https://docs.digitalocean.com/products/container-registry/how-to/clean-up-container-registry/)
about how and why you should clean up your container registry periodically.

To request a garbage collection run on your registry, send a POST request to
`/v2/registry/$REGISTRY_NAME/garbage-collection`. This will initiate the
following sequence of events on your registry.

* Set the registry to read-only mode, meaning no further write-scoped
  JWTs will be issued to registry clients. Existing write-scoped JWTs will
  continue to work until they expire which can take up to 15 minutes.
* Wait until all existing write-scoped JWTs have expired.
* Scan all registry manifests to determine which blobs are unreferenced.
* Delete all unreferenced blobs from the registry.
* Record the number of blobs deleted and bytes freed, mark the garbage
  collection status as `success`.
* Remove the read-only mode restriction from the registry, meaning write-scoped
  JWTs will once again be issued to registry clients.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryRunGc{
        RegistryName: "example",
    }
client.ContainerRegistry.RegistryRunGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.RegistryRunGcType` — Type of the garbage collection to run against this registry
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryListGarbageCollections(RegistryName) -> *godonext.RegistryListGarbageCollectionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To get information about past garbage collections for a registry,
send a GET request to `/v2/registry/$REGISTRY_NAME/garbage-collections`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryListGarbageCollectionsRequest{
        RegistryName: "example",
    }
client.ContainerRegistry.RegistryListGarbageCollections(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryUpdateGarbageCollection(RegistryName, GarbageCollectionUUID, request) -> *godonext.RegistryUpdateGarbageCollectionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

To cancel the currently-active garbage collection for a registry,
send a PUT request to `/v2/registry/$REGISTRY_NAME/garbage-collection/$GC_UUID`
and specify one or more of the attributes below.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.RegistryUpdateGarbageCollectionRequest{
        RegistryName: "example",
        GarbageCollectionUUID: "eff0feee-49c7-4e8f-ba5c-a320c109c8a8",
        Body: &godonext.UpdateRegistry{},
    }
client.ContainerRegistry.RegistryUpdateGarbageCollection(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**registryName:** `string` — The name of a container registry.
    
</dd>
</dl>

<dl>
<dd>

**garbageCollectionUUID:** `string` — The UUID of a garbage collection run.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.UpdateRegistry` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ContainerRegistry.RegistryGetOptions() -> *godonext.RegistryGetOptionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

**Note: This endpoint is deprecated and may be removed in a future version. There is no alternative.****Note: This endpoint is deprecated. Please use the `/v2/registries` endpoint instead.**

This endpoint serves to provide additional information as to which option values
are available when creating a container registry.

There are multiple subscription tiers available for container registry. Each
tier allows a different number of image repositories to be created in your
registry, and has a different amount of storage and transfer included.

There are multiple regions available for container registry and controls
where your data is stored.

To list the available options, send a GET request to
`/v2/registry/options`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ContainerRegistry.RegistryGetOptions(
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

## Reserved IPs
<details><summary><code>client.ReservedIPs.ReservedIPsList() -> *godonext.ReservedIPsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the reserved IPs available on your account, send a GET request to `/v2/reserved_ips`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPsListRequest{}
client.ReservedIPs.ReservedIPsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPs.ReservedIPsCreate(request) -> *godonext.ReservedIPsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

On creation, a reserved IP must be either assigned to a Droplet or reserved to a region.
* To create a new reserved IP assigned to a Droplet, send a POST
  request to `/v2/reserved_ips` with the `droplet_id` attribute.

* To create a new reserved IP reserved to a region, send a POST request to
  `/v2/reserved_ips` with the `region` attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPCreate{
        ReservedIPCreateDropletID: &godonext.ReservedIPCreateDropletID{
            DropletID: 2457247,
        },
    }
client.ReservedIPs.ReservedIPsCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ReservedIPCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPs.ReservedIPsGet(ReservedIP) -> *godonext.ReservedIPsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about a reserved IP, send a GET request to `/v2/reserved_ips/$RESERVED_IP_ADDR`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPsGetRequest{
        ReservedIP: "45.55.96.47",
    }
client.ReservedIPs.ReservedIPsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` — A reserved IP address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPs.ReservedIPsDelete(ReservedIP) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a reserved IP and remove it from your account, send a DELETE request
to `/v2/reserved_ips/$RESERVED_IP_ADDR`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPsDeleteRequest{
        ReservedIP: "45.55.96.47",
    }
client.ReservedIPs.ReservedIPsDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` — A reserved IP address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Reserved IP Actions
<details><summary><code>client.ReservedIPActions.ReservedIPsActionsList(ReservedIP) -> *godonext.ReservedIPsActionsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve all actions that have been executed on a reserved IP, send a GET request to `/v2/reserved_ips/$RESERVED_IP/actions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPsActionsListRequest{
        ReservedIP: "45.55.96.47",
    }
client.ReservedIPActions.ReservedIPsActionsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` — A reserved IP address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPActions.ReservedIPsActionsPost(ReservedIP, request) -> *godonext.ReservedIPsActionsPostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To initiate an action on a reserved IP send a POST request to
`/v2/reserved_ips/$RESERVED_IP/actions`. In the JSON body to the request,
set the `type` attribute to on of the supported action types:

| Action     | Details
|------------|--------
| `assign`   | Assigns a reserved IP to a Droplet
| `unassign` | Unassign a reserved IP from a Droplet
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPsActionsPostRequest{
        ReservedIP: "45.55.96.47",
        Body: &godonext.ReservedIPsActionsPostRequestBody{
            ReservedIPActionUnassign: &godonext.ReservedIPActionUnassign{},
        },
    }
client.ReservedIPActions.ReservedIPsActionsPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` — A reserved IP address.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ReservedIPsActionsPostRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPActions.ReservedIPsActionsGet(ReservedIP, ActionID) -> *godonext.ReservedIPsActionsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the status of a reserved IP action, send a GET request to `/v2/reserved_ips/$RESERVED_IP/actions/$ACTION_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPsActionsGetRequest{
        ReservedIP: "45.55.96.47",
        ActionID: 1,
    }
client.ReservedIPActions.ReservedIPsActionsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIP:** `string` — A reserved IP address.
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `int` — A unique numeric ID that can be used to identify and reference an action.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Reserved IPv6
<details><summary><code>client.ReservedIPv6.ReservedIPv6List() -> *godonext.ReservedIPv6ListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the reserved IPv6s available on your account, send a GET request to `/v2/reserved_ipv6`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPv6ListRequest{}
client.ReservedIPv6.ReservedIPv6List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPv6.ReservedIPv6Create(request) -> *godonext.ReservedIPv6CreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

On creation, a reserved IPv6 must be reserved to a region.
* To create a new reserved IPv6 reserved to a region, send a POST request to
  `/v2/reserved_ipv6` with the `region_slug` attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIpv6Create{
        RegionSlug: "nyc3",
    }
client.ReservedIPv6.ReservedIPv6Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**regionSlug:** `string` — The slug identifier for the region the reserved IPv6 will be reserved to.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPv6.ReservedIPv6Get(ReservedIpv6) -> *godonext.ReservedIPv6GetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about a reserved IPv6, send a GET request to `/v2/reserved_ipv6/$RESERVED_IPV6`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPv6GetRequest{
        ReservedIpv6: "2409:40d0:f7:1017:74b4:3a96:105e:4c6e",
    }
client.ReservedIPv6.ReservedIPv6Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIpv6:** `string` — A reserved IPv6 address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ReservedIPv6.ReservedIPv6Delete(ReservedIpv6) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a reserved IP and remove it from your account, send a DELETE request
to `/v2/reserved_ipv6/$RESERVED_IPV6`.

A successful request will receive a 204 status code with no body in response.
This indicates that the request was processed successfully.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ReservedIPv6DeleteRequest{
        ReservedIpv6: "2409:40d0:f7:1017:74b4:3a96:105e:4c6e",
    }
client.ReservedIPv6.ReservedIPv6Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**reservedIpv6:** `string` — A reserved IPv6 address.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## BYOIP Prefixes
<details><summary><code>client.ByoipPrefixes.ByoipPrefixesList() -> *godonext.ByoipPrefixesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all BYOIP prefixes, send a GET request to `/v2/byoip_prefixes`.
A successful response will return a list of all BYOIP prefixes associated with the account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ByoipPrefixesListRequest{}
client.ByoipPrefixes.ByoipPrefixesList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ByoipPrefixes.ByoipPrefixesCreate(request) -> *godonext.ByoipPrefixesCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a BYOIP prefix, send a POST request to `/v2/byoip_prefixes`.

A successful request will initiate the process of bringing your BYOIP Prefix into your account.
The response will include the details of the created prefix, including its UUID and status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ByoipPrefixCreate{
        Prefix: "203.11.13.0/24",
        Region: "nyc3",
        Signature: "<sample-signature>",
    }
client.ByoipPrefixes.ByoipPrefixesCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**prefix:** `string` — The IP prefix in CIDR notation to bring
    
</dd>
</dl>

<dl>
<dd>

**region:** `string` — The region where the prefix will be created
    
</dd>
</dl>

<dl>
<dd>

**signature:** `string` — The signature hash for the prefix creation request
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ByoipPrefixes.ByoipPrefixesGet(ByoipPrefixUUID) -> *godonext.ByoipPrefixesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a BYOIP prefix, send a GET request to `/v2/byoip_prefixes/$byoip_prefix_uuid`. 

A successful response will return the details of the specified BYOIP prefix.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ByoipPrefixesGetRequest{
        ByoipPrefixUUID: "f47ac10b-58cc-4372-a567-0e02b2c3d479",
    }
client.ByoipPrefixes.ByoipPrefixesGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` — The unique identifier for the BYOIP Prefix.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ByoipPrefixes.ByoipPrefixesDelete(ByoipPrefixUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a BYOIP prefix and remove it from your account, send a DELETE request
to `/v2/byoip_prefixes/$byoip_prefix_uuid`.

A successful request will receive a 202 status code with no body in response.
This indicates that the request was accepted and the prefix is being deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ByoipPrefixesDeleteRequest{
        ByoipPrefixUUID: "f47ac10b-58cc-4372-a567-0e02b2c3d479",
    }
client.ByoipPrefixes.ByoipPrefixesDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` — The unique identifier for the BYOIP Prefix.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ByoipPrefixes.ByoipPrefixesPatch(ByoipPrefixUUID, request) -> *godonext.ByoipPrefixesPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a BYOIP prefix, send a PATCH request to `/v2/byoip_prefixes/$byoip_prefix_uuid`.

Currently, you can update the advertisement status of the prefix.
The response will include the updated details of the prefix.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ByoipPrefixUpdate{
        ByoipPrefixUUID: "f47ac10b-58cc-4372-a567-0e02b2c3d479",
    }
client.ByoipPrefixes.ByoipPrefixesPatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` — A unique identifier for a BYOIP prefix.
    
</dd>
</dl>

<dl>
<dd>

**advertise:** `*bool` — Whether the BYOIP prefix should be advertised
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ByoipPrefixes.ByoipPrefixesListResources(ByoipPrefixUUID) -> *godonext.ByoipPrefixesListResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list resources associated with BYOIP prefixes, send a GET request to `/v2/byoip_prefixes/{byoip_prefix_uuid}/ips`.

A successful response will return a list of resources associated with the specified BYOIP prefix.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ByoipPrefixesListResourcesRequest{
        ByoipPrefixUUID: "f47ac10b-58cc-4372-a567-0e02b2c3d479",
    }
client.ByoipPrefixes.ByoipPrefixesListResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**byoipPrefixUUID:** `string` — The unique identifier for the BYOIP Prefix.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Security
<details><summary><code>client.Security.ListScans() -> *godonext.SecurityListScansResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all CSPM scans, send a GET request to `/v2/security/scans`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityListScansRequest{}
client.Security.ListScans(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.CreateScan() -> *godonext.SecurityCreateScanResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a CSPM scan, send a POST request to `/v2/security/scans`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.Security.CreateScan(
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

<details><summary><code>client.Security.GetScan(ScanID) -> *godonext.SecurityGetScanResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a CSPM scan by ID, send a GET request to `/v2/security/scans/{scan_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityGetScanRequest{
        ScanID: "497dcba3-ecbf-4587-a2dd-5eb0665e6880",
        Type: godonext.String(
            "CSPM",
        ),
    }
client.Security.GetScan(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**scanID:** `string` — The scan UUID.
    
</dd>
</dl>

<dl>
<dd>

**severity:** `*godonext.SecurityGetScanRequestSeverity` — The finding severity level to include.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*string` — The finding type to include.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.GetLatestScan() -> *godonext.SecurityGetLatestScanResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get the latest CSPM scan, send a GET request to `/v2/security/scans/latest`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityGetLatestScanRequest{
        Type: godonext.String(
            "CSPM",
        ),
    }
client.Security.GetLatestScan(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**severity:** `*godonext.SecurityGetLatestScanRequestSeverity` — The finding severity level to include.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*string` — The finding type to include.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.CreateScanRule(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To mark a scan finding as a false positive, send a POST request to
`/v2/security/scans/rules` to create a new scan rule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityCreateScanRuleRequest{}
client.Security.CreateScanRule(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**resource:** `*string` — The URN of a resource to exclude from future scans.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.ListScanFindingAffectedResources(ScanID, FindingUUID) -> *godonext.SecurityListScanFindingAffectedResourcesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get affected resources for a scan finding, send a GET request to `/v2/security/scans/{scan_id}/findings/{finding_uuid}/affected_resources`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityListScanFindingAffectedResourcesRequest{
        ScanID: "497dcba3-ecbf-4587-a2dd-5eb0665e6880",
        FindingUUID: "50e14f43-dd4e-412f-864d-78943ea28d91",
    }
client.Security.ListScanFindingAffectedResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**scanID:** `string` — The scan UUID.
    
</dd>
</dl>

<dl>
<dd>

**findingUUID:** `string` — The finding UUID.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.ListSettings() -> *godonext.Settings</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list CSPM scan settings, send a GET request to `/v2/security/settings`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityListSettingsRequest{}
client.Security.ListSettings(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.UpdateSettingsPlan(request) -> *godonext.SecurityUpdateSettingsPlanResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update CSPM plan coverage, send a PUT request to `/v2/security/settings/plan`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityUpdateSettingsPlanRequest{}
client.Security.UpdateSettingsPlan(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tierCoverage:** `map[string]*godonext.SecurityUpdateSettingsPlanRequestTierCoverageValue` — Scan coverage for each available plan tier.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.CreateSuppression(request) -> *godonext.SuppressedResourceRoot</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To suppress scan findings, send a POST request to `/v2/security/settings/suppressions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityCreateSuppressionRequest{}
client.Security.CreateSuppression(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**ruleUUID:** `*string` — The rule UUID to suppress for the listed resources.
    
</dd>
</dl>

<dl>
<dd>

**resources:** `[]string` — The URNs of resources to suppress for the rule.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Security.DeleteSuppression(SuppressionUUID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To remove a suppression, send a DELETE request to `/v2/security/settings/suppressions/{suppression_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SecurityDeleteSuppressionRequest{
        SuppressionUUID: "5b3b2b2d-5c9c-4a61-9e2f-4d8f80f30a12",
    }
client.Security.DeleteSuppression(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**suppressionUUID:** `string` — The suppression UUID to remove.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Sizes
<details><summary><code>client.Sizes.List() -> *godonext.SizesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of available Droplet sizes, send a GET request to `/v2/sizes`.
The response will be a JSON object with a key called `sizes`. The value of this will be an array of `size` objects each of which contain the standard size attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SizesListRequest{}
client.Sizes.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Snapshots
<details><summary><code>client.Snapshots.List() -> *godonext.SnapshotsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the snapshots available on your account, send a GET request to
`/v2/snapshots`.

The response will be a JSON object with a key called `snapshots`. This will be
set to an array of `snapshot` objects, each of which will contain the standard
snapshot attributes.

### Filtering Results by Resource Type

It's possible to request filtered results by including certain query parameters.

#### List Droplet Snapshots

To retrieve only snapshots based on Droplets, include the `resource_type`
query parameter set to `droplet`. For example, `/v2/snapshots?resource_type=droplet`.

#### List Volume Snapshots

To retrieve only snapshots based on volumes, include the `resource_type`
query parameter set to `volume`. For example, `/v2/snapshots?resource_type=volume`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SnapshotsListRequest{}
client.Snapshots.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**resourceType:** `*godonext.SnapshotsListRequestResourceType` — Used to filter snapshots by a resource type.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Snapshots.Get(SnapshotID) -> *godonext.SnapshotsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve information about a snapshot, send a GET request to
`/v2/snapshots/$SNAPSHOT_ID`.

The response will be a JSON object with a key called `snapshot`. The value of
this will be an snapshot object containing the standard snapshot attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SnapshotsGetRequest{
        SnapshotID: &godonext.SnapshotsGetRequestSnapshotID{
            Integer: 6372321,
        },
    }
client.Snapshots.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `*godonext.SnapshotsGetRequestSnapshotID` — Either the ID of an existing snapshot. This will be an integer for a Droplet snapshot or a string for a volume snapshot.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Snapshots.Delete(SnapshotID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Both Droplet and volume snapshots are managed through the `/v2/snapshots/`
endpoint. To delete a snapshot, send a DELETE request to
`/v2/snapshots/$SNAPSHOT_ID`.

A status of 204 will be given. This indicates that the request was processed
successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SnapshotsDeleteRequest{
        SnapshotID: &godonext.SnapshotsDeleteRequestSnapshotID{
            Integer: 6372321,
        },
    }
client.Snapshots.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `*godonext.SnapshotsDeleteRequestSnapshotID` — Either the ID of an existing snapshot. This will be an integer for a Droplet snapshot or a string for a volume snapshot.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Spaces Keys
<details><summary><code>client.SpacesKeys.SpacesKeyList() -> *godonext.SpacesKeyListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list Spaces Access Key, send a GET request to `/v2/spaces/keys`. Sort parameter must be used with Sort Direction.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SpacesKeyListRequest{
        Sort: godonext.String(
            "created_at",
        ),
        SortDirection: godonext.String(
            "desc",
        ),
        Name: godonext.String(
            "my-access-key",
        ),
        Bucket: godonext.String(
            "my-bucket",
        ),
        Permission: godonext.String(
            "read",
        ),
    }
client.SpacesKeys.SpacesKeyList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**sort:** `*string` — The field to sort by.
    
</dd>
</dl>

<dl>
<dd>

**sortDirection:** `*string` — The direction to sort by. Possible values are `asc` or `desc`.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — The access key's name.
    
</dd>
</dl>

<dl>
<dd>

**bucket:** `*string` — The bucket's name.
    
</dd>
</dl>

<dl>
<dd>

**permission:** `*string` — The permission of the access key. Possible values are `read`, `readwrite`, `fullaccess`, or an empty string.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SpacesKeys.SpacesKeyCreate(request) -> *godonext.SpacesKeyCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new Spaces Access Key, send a POST request to `/v2/spaces/keys`.
At the moment, you cannot mix a fullaccess permission with scoped permissions.
A fullaccess permission will be prioritized if fullaccess and scoped permissions are both added.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Key{
        Name: godonext.String(
            "read-only-key",
        ),
        Grants: []*godonext.Grant{
            &godonext.Grant{
                Bucket: "my-bucket",
                Permission: "read",
            },
        },
    }
client.SpacesKeys.SpacesKeyCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.Key` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SpacesKeys.SpacesKeyGet(AccessKey) -> *godonext.SpacesKeyGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a Spaces Access Key, send a GET request to `/v2/spaces/keys/$ACCESS_KEY`.

A successful request will return the Access Key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SpacesKeyGetRequest{
        AccessKey: "DOACCESSKEYEXAMPLE",
    }
client.SpacesKeys.SpacesKeyGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` — The access key's ID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SpacesKeys.SpacesKeyUpdate(AccessKey, request) -> *godonext.SpacesKeyUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update Spaces Access Key, send a PUT or PATCH request to `/v2/spaces/keys/$ACCESS_KEY`. At the moment, you cannot convert a
fullaccess key to a scoped key or vice versa. You can only update the name of the key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SpacesKeyUpdateRequest{
        AccessKey: "DOACCESSKEYEXAMPLE",
        Body: &godonext.Key{
            Name: godonext.String(
                "new-key-name",
            ),
        },
    }
client.SpacesKeys.SpacesKeyUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` — The access key's ID.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.Key` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SpacesKeys.SpacesKeyDelete(AccessKey) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a Spaces Access Key, send a DELETE request to `/v2/spaces/keys/$ACCESS_KEY`.

A successful request will return a `204 No Content` status code.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SpacesKeyDeleteRequest{
        AccessKey: "DOACCESSKEYEXAMPLE",
    }
client.SpacesKeys.SpacesKeyDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` — The access key's ID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.SpacesKeys.SpacesKeyPatch(AccessKey, request) -> *godonext.SpacesKeyPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update Spaces Access Key, send a PUT or PATCH request to `/v2/spaces/keys/$ACCESS_KEY`. At the moment, you cannot convert a
fullaccess key to a scoped key or vice versa. You can only update the name of the key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.SpacesKeyPatchRequest{
        AccessKey: "DOACCESSKEYEXAMPLE",
        Body: &godonext.Key{
            Name: godonext.String(
                "new-key-name",
            ),
        },
    }
client.SpacesKeys.SpacesKeyPatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**accessKey:** `string` — The access key's ID.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.Key` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tags
<details><summary><code>client.Tags.List() -> *godonext.TagsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of your tags, you can send a GET request to `/v2/tags`.

This endpoint will only return tagged resources that you are authorized to see
(e.g. Droplets will only be returned if you have `droplet:read`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.TagsListRequest{}
client.Tags.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.Create(request) -> *godonext.TagsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a tag you can send a POST request to `/v2/tags` with a `name` attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.Tags{}
client.Tags.Create(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.Tags` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.Get(TagID) -> *godonext.TagsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve an individual tag, you can send a `GET` request to
`/v2/tags/$TAG_NAME`.

This endpoint will only return tagged resources that you are authorized to see.
For example, to see tagged Droplets, include the `droplet:read` scope.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.TagsGetRequest{
        TagID: "awesome",
    }
client.Tags.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` — The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores. There is a limit of 255 characters per tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.Delete(TagID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

A tag can be deleted by sending a `DELETE` request to `/v2/tags/$TAG_NAME`. Deleting a tag also untags all the resources that have previously been tagged by the Tag
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.TagsDeleteRequest{
        TagID: "awesome",
    }
client.Tags.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` — The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores. There is a limit of 255 characters per tag.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.AssignResources(TagID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Resources can be tagged by sending a POST request to
`/v2/tags/$TAG_NAME/resources` with an array of json objects containing
`resource_id` and `resource_type` attributes.

Currently only tagging of Droplets, Databases, Images, Volumes, and Volume
Snapshots is supported. `resource_type` is expected to be the string `droplet`,
`database`, `image`, `volume` or `volume_snapshot`. `resource_id` is expected
to be the ID of the resource as a string.

In order to tag a resource, you must have both `tag:create` and `<resource type>:update` scopes. For example, 
to tag a Droplet, you must have `tag:create` and `droplet:update`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.TagsAssignResourcesRequest{
        TagID: "awesome",
        Body: &godonext.TagsResource{
            Resources: []*godonext.TagsResourceResourcesItem{
                &godonext.TagsResourceResourcesItem{
                    ResourceID: godonext.String(
                        "9569411",
                    ),
                    ResourceType: godonext.TagsResourceResourcesItemResourceTypeDroplet.Ptr(),
                },
                &godonext.TagsResourceResourcesItem{
                    ResourceID: godonext.String(
                        "7555620",
                    ),
                    ResourceType: godonext.TagsResourceResourcesItemResourceTypeImage.Ptr(),
                },
                &godonext.TagsResourceResourcesItem{
                    ResourceID: godonext.String(
                        "3d80cb72-342b-4aaa-b92e-4e4abb24a933",
                    ),
                    ResourceType: godonext.TagsResourceResourcesItemResourceTypeVolume.Ptr(),
                },
            },
        },
    }
client.Tags.AssignResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` — The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores. There is a limit of 255 characters per tag.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.TagsResource` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Tags.UnassignResources(TagID, request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Resources can be untagged by sending a DELETE request to
`/v2/tags/$TAG_NAME/resources` with an array of json objects containing
`resource_id` and `resource_type` attributes.

Currently only untagging of Droplets, Databases, Images, Volumes, and Volume
Snapshots is supported. `resource_type` is expected to be the string `droplet`,
`database`, `image`, `volume` or `volume_snapshot`. `resource_id` is expected
to be the ID of the resource as a string.

In order to untag a resource, you must have both `tag:delete` and `<resource type>:update` scopes. For example, 
to untag a Droplet, you must have `tag:delete` and `droplet:update`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.TagsUnassignResourcesRequest{
        TagID: "awesome",
        Body: &godonext.TagsResource{
            Resources: []*godonext.TagsResourceResourcesItem{
                &godonext.TagsResourceResourcesItem{
                    ResourceID: godonext.String(
                        "9569411",
                    ),
                    ResourceType: godonext.TagsResourceResourcesItemResourceTypeDroplet.Ptr(),
                },
                &godonext.TagsResourceResourcesItem{
                    ResourceID: godonext.String(
                        "7555620",
                    ),
                    ResourceType: godonext.TagsResourceResourcesItemResourceTypeImage.Ptr(),
                },
                &godonext.TagsResourceResourcesItem{
                    ResourceID: godonext.String(
                        "3d80cb72-342b-4aaa-b92e-4e4abb24a933",
                    ),
                    ResourceType: godonext.TagsResourceResourcesItemResourceTypeVolume.Ptr(),
                },
            },
        },
    }
client.Tags.UnassignResources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**tagID:** `string` — The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores. There is a limit of 255 characters per tag.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.TagsResource` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Block Storage
<details><summary><code>client.BlockStorage.VolumesList() -> *godonext.VolumesListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the block storage volumes available on your account, send a GET request to `/v2/volumes`.
## Filtering Results
### By Region
The `region` may be provided as query parameter in order to restrict results to volumes available in a specific region. For example: `/v2/volumes?region=nyc1`
### By Name
It is also possible to list volumes on your account that match a specified name. To do so, send a GET request with the volume's name as a query parameter to `/v2/volumes?name=$VOLUME_NAME`.
**Note:** You can only create one volume per region with the same name.
### By Name and Region
It is also possible to retrieve information about a block storage volume by name. To do so, send a GET request with the volume's name and the region slug for the region it is located in as query parameters to `/v2/volumes?name=$VOLUME_NAME&region=nyc1`.


</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumesListRequest{
        Name: godonext.String(
            "example",
        ),
    }
client.BlockStorage.VolumesList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `*string` — The block storage volume's name.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.RegionSlug` — The slug identifier for the region where the resource is available.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumesCreate(request) -> *godonext.VolumesCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new volume, send a POST request to `/v2/volumes`. Optionally, a `filesystem_type` attribute may be provided in order to automatically format the volume's filesystem. Pre-formatted volumes are automatically mounted when attached to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS Droplets created on or after April 26, 2018. Attaching pre-formatted volumes to Droplets without support for auto-mounting is not recommended.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumesCreateRequest{
        VolumesExt4: &godonext.VolumesExt4{
            Name: godonext.String(
                "ext4-example",
            ),
            Description: godonext.String(
                "Block store for examples",
            ),
            SizeGigabytes: godonext.Int(
                10,
            ),
            FilesystemType: godonext.String(
                "ext4",
            ),
            Region: godonext.RegionSlugNyc1,
            FilesystemLabel: godonext.String(
                "ext4_volume_01",
            ),
        },
    }
client.BlockStorage.VolumesCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.VolumesCreateRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumesDeleteByName() -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Block storage volumes may also be deleted by name by sending a DELETE request with the volume's **name** and the **region slug** for the region it is located in as query parameters to `/v2/volumes?name=$VOLUME_NAME&region=nyc1`.
No response body will be sent back, but the response code will indicate success. Specifically, the response code will be a 204, which means that the action was successful with no returned body data.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumesDeleteByNameRequest{
        Name: godonext.String(
            "example",
        ),
    }
client.BlockStorage.VolumesDeleteByName(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `*string` — The block storage volume's name.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.RegionSlug` — The slug identifier for the region where the resource is available.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumeSnapshotsGetByID(SnapshotID) -> *godonext.VolumeSnapshotsGetByIDResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the details of a snapshot that has been created from a volume, send a GET request to `/v2/volumes/snapshots/$VOLUME_SNAPSHOT_ID`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeSnapshotsGetByIDRequest{
        SnapshotID: "fbe805e8-866b-11e6-96bf-000f53315a41",
    }
client.BlockStorage.VolumeSnapshotsGetByID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `string` — The unique identifier for the snapshot.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumeSnapshotsDeleteByID(SnapshotID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a volume snapshot, send a DELETE request to
`/v2/volumes/snapshots/$VOLUME_SNAPSHOT_ID`.

A status of 204 will be given. This indicates that the request was processed
successfully, but that no response body is needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeSnapshotsDeleteByIDRequest{
        SnapshotID: "fbe805e8-866b-11e6-96bf-000f53315a41",
    }
client.BlockStorage.VolumeSnapshotsDeleteByID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**snapshotID:** `string` — The unique identifier for the snapshot.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumesGet(VolumeID) -> *godonext.VolumesGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about a block storage volume, send a GET request to `/v2/volumes/$VOLUME_ID`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumesGetRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
    }
client.BlockStorage.VolumesGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumesDelete(VolumeID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a block storage volume, destroying all data and removing it from your account, send a DELETE request to `/v2/volumes/$VOLUME_ID`.
No response body will be sent back, but the response code will indicate success. Specifically, the response code will be a 204, which means that the action was successful with no returned body data.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumesDeleteRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
    }
client.BlockStorage.VolumesDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumeSnapshotsList(VolumeID) -> *godonext.VolumeSnapshotsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the snapshots that have been created from a volume, send a GET request to `/v2/volumes/$VOLUME_ID/snapshots`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeSnapshotsListRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
    }
client.BlockStorage.VolumeSnapshotsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorage.VolumeSnapshotsCreate(VolumeID, request) -> *godonext.VolumeSnapshotsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a snapshot from a volume, sent a POST request to `/v2/volumes/$VOLUME_ID/snapshots`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeSnapshotsCreateRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
        Name: "big-data-snapshot1475261774",
    }
client.BlockStorage.VolumeSnapshotsCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — A human-readable name for the volume snapshot.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `*godonext.TagsArray` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Block Storage Actions
<details><summary><code>client.BlockStorageActions.VolumeActionsPost(request) -> *godonext.VolumeActionsPostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To initiate an action on a block storage volume by Name, send a POST request to
`~/v2/volumes/actions`. The body should contain the appropriate
attributes for the respective action.

## Attach a Block Storage Volume to a Droplet

| Attribute   | Details                                                             |
| ----------- | ------------------------------------------------------------------- |
| type        | This must be `attach`                                               |
| volume_name | The name of the block storage volume                                |
| droplet_id  | Set to the Droplet's ID                                             |
| region      | Set to the slug representing the region where the volume is located |

Each volume may only be attached to a single Droplet. However, up to fifteen
volumes may be attached to a Droplet at a time. Pre-formatted volumes will be
automatically mounted to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS
Droplets created on or after April 26, 2018 when attached. On older Droplets,
[additional configuration](https://docs.digitalocean.com/products/volumes/how-to/mount/)
is required.

## Remove a Block Storage Volume from a Droplet

| Attribute   | Details                                                             |
| ----------- | ------------------------------------------------------------------- |
| type        | This must be `detach`                                               |
| volume_name | The name of the block storage volume                                |
| droplet_id  | Set to the Droplet's ID                                             |
| region      | Set to the slug representing the region where the volume is located |
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeActionsPostRequest{
        Body: &godonext.VolumeActionsPostRequestBody{
            VolumeActionPostAttach: &godonext.VolumeActionPostAttach{
                Type: godonext.VolumeActionPostBaseTypeAttach,
                Region: godonext.RegionSlugNyc1.Ptr(),
                DropletID: 11612190,
                Tags: []string{
                    "aninterestingtag",
                },
            },
        },
    }
client.BlockStorageActions.VolumeActionsPost(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.VolumeActionsPostRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorageActions.VolumeActionsList(VolumeID) -> *godonext.VolumeActionsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve all actions that have been executed on a volume, send a GET request to `/v2/volumes/$VOLUME_ID/actions`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeActionsListRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
    }
client.BlockStorageActions.VolumeActionsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorageActions.VolumeActionsPostByID(VolumeID, request) -> *godonext.VolumeActionsPostByIDResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To initiate an action on a block storage volume by Id, send a POST request to
`~/v2/volumes/$VOLUME_ID/actions`. The body should contain the appropriate
attributes for the respective action.

## Attach a Block Storage Volume to a Droplet

| Attribute  | Details                                                             |
| ---------- | ------------------------------------------------------------------- |
| type       | This must be `attach`                                               |
| droplet_id | Set to the Droplet's ID                                             |
| region     | Set to the slug representing the region where the volume is located |

Each volume may only be attached to a single Droplet. However, up to fifteen
volumes may be attached to a Droplet at a time. Pre-formatted volumes will be
automatically mounted to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS
Droplets created on or after April 26, 2018 when attached. On older Droplets,
[additional configuration](https://docs.digitalocean.com/products/volumes/how-to/mount/)
is required.

## Remove a Block Storage Volume from a Droplet

| Attribute  | Details                                                             |
| ---------- | ------------------------------------------------------------------- |
| type       | This must be `detach`                                               |
| droplet_id | Set to the Droplet's ID                                             |
| region     | Set to the slug representing the region where the volume is located |

## Resize a Volume

| Attribute      | Details                                                             |
| -------------- | ------------------------------------------------------------------- |
| type           | This must be `resize`                                               |
| size_gigabytes | The new size of the block storage volume in GiB (1024^3)            |
| region         | Set to the slug representing the region where the volume is located |

Volumes may only be resized upwards. The maximum size for a volume is 16TiB.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeActionsPostByIDRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
        Body: &godonext.VolumeActionsPostByIDRequestBody{
            VolumeActionPostAttach: &godonext.VolumeActionPostAttach{
                Type: godonext.VolumeActionPostBaseTypeAttach,
                Region: godonext.RegionSlugNyc1.Ptr(),
                DropletID: 11612190,
                Tags: []string{
                    "aninterestingtag",
                },
            },
        },
    }
client.BlockStorageActions.VolumeActionsPostByID(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.VolumeActionsPostByIDRequestBody` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BlockStorageActions.VolumeActionsGet(VolumeID, ActionID) -> *godonext.VolumeActionsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve the status of a volume action, send a GET request to `/v2/volumes/$VOLUME_ID/actions/$ACTION_ID`.

</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VolumeActionsGetRequest{
        VolumeID: "7724db7c-e098-11e5-b522-000f53304e51",
        ActionID: 1,
    }
client.BlockStorageActions.VolumeActionsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**volumeID:** `string` — The ID of the block storage volume.
    
</dd>
</dl>

<dl>
<dd>

**actionID:** `int` — A unique numeric ID that can be used to identify and reference an action.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## VPCs
<details><summary><code>client.Vpcs.List() -> *godonext.VpcsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the VPCs on your account, send a GET request to `/v2/vpcs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsListRequest{}
client.Vpcs.List(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.Create(request) -> *godonext.VpcsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a VPC, send a POST request to `/v2/vpcs` specifying the attributes
in the table below in the JSON body.

**Note:** If you do not currently have a VPC network in a specific datacenter
region, the first one that you create will be set as the default for that
region. The default VPC for a region cannot be changed or deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsCreateRequest{}
client.Vpcs.Create(
        context.TODO(),
        request,
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

<details><summary><code>client.Vpcs.Get(VpcID) -> *godonext.VpcsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing VPC, send a GET request to `/v2/vpcs/$VPC_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsGetRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Vpcs.Get(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.Update(VpcID, request) -> *godonext.VpcsUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update information about a VPC, send a PUT request to `/v2/vpcs/$VPC_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsUpdateRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Vpcs.Update(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.Delete(VpcID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a VPC, send a DELETE request to `/v2/vpcs/$VPC_ID`. A 204 status
code with no body will be returned in response to a successful request.

The default VPC for a region can not be deleted. Additionally, a VPC can only
be deleted if it does not contain any member resources. Attempting to delete
a region's default VPC or a VPC that still has members will result in a
403 Forbidden error response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsDeleteRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Vpcs.Delete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.Patch(VpcID, request) -> *godonext.VpcsPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a subset of information about a VPC, send a PATCH request to
`/v2/vpcs/$VPC_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsPatchRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Vpcs.Patch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.ListMembers(VpcID) -> *godonext.VpcsListMembersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the resources that are members of a VPC, send a GET request to
`/v2/vpcs/$VPC_ID/members`.

To only list resources of a specific type that are members of the VPC,
included a `resource_type` query parameter. For example, to only list Droplets
in the VPC, send a GET request to `/v2/vpcs/$VPC_ID/members?resource_type=droplet`.

Only resources that you are authorized to see will be returned (e.g. to see Droplets,
you must have `droplet:read`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsListMembersRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        ResourceType: godonext.String(
            "droplet",
        ),
    }
client.Vpcs.ListMembers(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>

<dl>
<dd>

**resourceType:** `*string` — Used to filter VPC members by a resource type.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.ListPeerings(VpcID) -> *godonext.VpcsListPeeringsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of a VPC's peerings, send a GET request to
`/v2/vpcs/$VPC_ID/peerings`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsListPeeringsRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Vpcs.ListPeerings(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.CreatePeerings(VpcID, request) -> *godonext.VpcsCreatePeeringsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new VPC peering for a given VPC, send a POST request to
`/v2/vpcs/$VPC_ID/peerings`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsCreatePeeringsRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Name: "nyc1-blr1-peering",
        VpcsCreatePeeringsRequestVpcID: "c140286f-e6ce-4131-8b7b-df4590ce8d6a",
    }
client.Vpcs.CreatePeerings(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>

<dl>
<dd>

**name:** `string` — The name of the VPC peering. Must be unique and may only contain alphanumeric characters, dashes, and periods.
    
</dd>
</dl>

<dl>
<dd>

**vpcsCreatePeeringsRequestVpcID:** `string` — The ID of the VPC to peer with.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Vpcs.PatchPeerings(VpcID, VpcPeeringID, request) -> *godonext.VpcsPatchPeeringsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the name of a VPC peering in a particular VPC, send a PATCH request 
to `/v2/vpcs/$VPC_ID/peerings/$VPC_PEERING_ID` with the new `name` in the 
request body.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcsPatchPeeringsRequest{
        VpcID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        VpcPeeringID: "5a4981aa-9653-4bd1-bef5-d6bff52042e4",
        Body: &godonext.VpcPeeringUpdatable{},
    }
client.Vpcs.PatchPeerings(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcID:** `string` — A unique identifier for a VPC.
    
</dd>
</dl>

<dl>
<dd>

**vpcPeeringID:** `string` — A unique identifier for a VPC peering.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.VpcPeeringUpdatable` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## VPC Peerings
<details><summary><code>client.VpcPeerings.VpcPeeringsList() -> *godonext.VpcPeeringsListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the VPC peerings on your account, send a GET request to `/v2/vpc_peerings`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcPeeringsListRequest{}
client.VpcPeerings.VpcPeeringsList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.RegionSlug` — The slug identifier for the region where the resource is available.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcPeerings.VpcPeeringsCreate(request) -> *godonext.VpcPeeringsCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new VPC Peering, send a POST request to `/v2/vpc_peerings` 
specifying a name and a list of two VPC IDs to peer. The response code, 202 
Accepted, does not indicate the success or failure of the operation, just 
that the request has been accepted for processing.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcPeeringsCreateRequest{}
client.VpcPeerings.VpcPeeringsCreate(
        context.TODO(),
        request,
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

<details><summary><code>client.VpcPeerings.VpcPeeringsGet(VpcPeeringID) -> *godonext.VpcPeeringsGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing VPC Peering, send a GET request to `/v2/vpc_peerings/$VPC_PEERING_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcPeeringsGetRequest{
        VpcPeeringID: "5a4981aa-9653-4bd1-bef5-d6bff52042e4",
    }
client.VpcPeerings.VpcPeeringsGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcPeeringID:** `string` — A unique identifier for a VPC peering.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcPeerings.VpcPeeringsDelete(VpcPeeringID) -> *godonext.VpcPeeringsDeleteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a VPC peering, send a DELETE request to `/v2/vpc_peerings/$VPC_PEERING_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcPeeringsDeleteRequest{
        VpcPeeringID: "5a4981aa-9653-4bd1-bef5-d6bff52042e4",
    }
client.VpcPeerings.VpcPeeringsDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcPeeringID:** `string` — A unique identifier for a VPC peering.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcPeerings.VpcPeeringsPatch(VpcPeeringID, request) -> *godonext.VpcPeeringsPatchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the name of a VPC peering, send a PATCH request to `/v2/vpc_peerings/$VPC_PEERING_ID` with the new `name` in the request body.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcPeeringsPatchRequest{
        VpcPeeringID: "5a4981aa-9653-4bd1-bef5-d6bff52042e4",
        Body: &godonext.VpcPeeringUpdatable{},
    }
client.VpcPeerings.VpcPeeringsPatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**vpcPeeringID:** `string` — A unique identifier for a VPC peering.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.VpcPeeringUpdatable` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## VPC NAT Gateways
<details><summary><code>client.VpcNatGateways.VpcnatgatewaysList() -> *godonext.VpcnatgatewaysListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all VPC NAT gateways in your team, send a GET request to `/v2/vpc_nat_gateways`.
The response body will be a JSON object with a key of `vpc_nat_gateways` containing an array of VPC NAT gateway objects.
These each contain the standard VPC NAT gateway attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcnatgatewaysListRequest{
        Name: godonext.String(
            "my-vpc-nat-gateway",
        ),
    }
client.VpcNatGateways.VpcnatgatewaysList(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>

<dl>
<dd>

**state:** `*godonext.VpcnatgatewaysListRequestState` — The current state of the VPC NAT gateway.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*godonext.VpcnatgatewaysListRequestRegion` — The region where the VPC NAT gateway is located.
    
</dd>
</dl>

<dl>
<dd>

**type_:** `*godonext.VpcnatgatewaysListRequestType` — The type of the VPC NAT gateway.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — The name of the VPC NAT gateway.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcNatGateways.VpcnatgatewaysCreate(request) -> *godonext.VpcnatgatewaysCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new VPC NAT gateway, send a POST request to `/v2/vpc_nat_gateways` setting the required attributes.

The response body will contain a JSON object with a key called `vpc_nat_gateway` containing the standard attributes for the new VPC NAT gateway.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcNatGatewayCreate{
        Name: "test-vpc-nat-gateways",
        Type: godonext.VpcNatGatewayCreateTypePublic,
        Region: godonext.VpcNatGatewayCreateRegionTor1,
        Size: 1,
        Vpcs: []*godonext.VpcNatGatewayCreateVpcsItem{
            &godonext.VpcNatGatewayCreateVpcsItem{
                VpcUUID: "0eb1752f-807b-4562-a077-8018e13ab1fb",
                DefaultGateway: godonext.Bool(
                    true,
                ),
            },
        },
        UDPTimeoutSeconds: godonext.Int(
            30,
        ),
        IcmpTimeoutSeconds: godonext.Int(
            30,
        ),
        TCPTimeoutSeconds: godonext.Int(
            30,
        ),
    }
client.VpcNatGateways.VpcnatgatewaysCreate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.VpcNatGatewayCreate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcNatGateways.VpcnatgatewaysGet(ID) -> *godonext.VpcnatgatewaysGetResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an individual VPC NAT gateway, send a GET request to
`/v2/vpc_nat_gateways/$VPC_NAT_GATEWAY_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcnatgatewaysGetRequest{
        ID: "70e1b58d-cdec-4e95-b3ee-2d4d95feff51",
    }
client.VpcNatGateways.VpcnatgatewaysGet(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The unique identifier of the VPC NAT gateway.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcNatGateways.VpcnatgatewaysUpdate(ID, request) -> *godonext.VpcnatgatewaysUpdateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the configuration of an existing VPC NAT Gateway, send a PUT request to
`/v2/vpc_nat_gateways/$VPC_NAT_GATEWAY_ID`. The request must contain a full representation
of the VPC NAT Gateway including existing attributes. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcnatgatewaysUpdateRequest{
        ID: "70e1b58d-cdec-4e95-b3ee-2d4d95feff51",
        Body: &godonext.VpcNatGatewayUpdate{
            Name: "test-vpc-nat-gateways-updated",
            Size: 2,
            Vpcs: []*godonext.VpcNatGatewayUpdateVpcsItem{
                &godonext.VpcNatGatewayUpdateVpcsItem{
                    VpcUUID: godonext.String(
                        "0eb1752f-807b-4562-a077-8018e13ab1fb",
                    ),
                    DefaultGateway: godonext.Bool(
                        false,
                    ),
                },
            },
            UDPTimeoutSeconds: godonext.Int(
                60,
            ),
            IcmpTimeoutSeconds: godonext.Int(
                60,
            ),
            TCPTimeoutSeconds: godonext.Int(
                60,
            ),
        },
    }
client.VpcNatGateways.VpcnatgatewaysUpdate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The unique identifier of the VPC NAT gateway.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.VpcNatGatewayUpdate` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.VpcNatGateways.VpcnatgatewaysDelete(ID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To destroy a VPC NAT Gateway, send a DELETE request to the `/v2/vpc_nat_gateways/$VPC_NAT_GATEWAY_ID` endpoint.

A successful response will include a 202 response code and no content. 
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.VpcnatgatewaysDeleteRequest{
        ID: "70e1b58d-cdec-4e95-b3ee-2d4d95feff51",
    }
client.VpcNatGateways.VpcnatgatewaysDelete(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `string` — The unique identifier of the VPC NAT gateway.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Uptime
<details><summary><code>client.Uptime.ListChecks() -> *godonext.UptimeListChecksResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the Uptime checks on your account, send a GET request to `/v2/uptime/checks`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeListChecksRequest{}
client.Uptime.ListChecks(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.CreateCheck(request) -> *godonext.UptimeCreateCheckResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an Uptime check, send a POST request to `/v2/uptime/checks` specifying the attributes
in the table below in the JSON body.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CheckUpdatable{}
client.Uptime.CreateCheck(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.CheckUpdatable` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.GetCheck(CheckID) -> *godonext.UptimeGetCheckResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing check, send a GET request to `/v2/uptime/checks/$CHECK_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeGetCheckRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Uptime.GetCheck(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.UpdateCheck(CheckID, request) -> *godonext.UptimeUpdateCheckResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the settings of an Uptime check, send a PUT request to `/v2/uptime/checks/$CHECK_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeUpdateCheckRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.CheckUpdatable{},
    }
client.Uptime.UpdateCheck(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.CheckUpdatable` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.DeleteCheck(CheckID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an Uptime check, send a DELETE request to `/v2/uptime/checks/$CHECK_ID`. A 204 status
code with no body will be returned in response to a successful request.


Deleting a check will also delete alerts associated with the check.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeDeleteCheckRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Uptime.DeleteCheck(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.GetCheckstate(CheckID) -> *godonext.UptimeGetCheckStateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing check's state, send a GET request to `/v2/uptime/checks/$CHECK_ID/state`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeGetCheckStateRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Uptime.GetCheckstate(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.ListAlerts(CheckID) -> *godonext.UptimeListAlertsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all of the alerts for an Uptime check, send a GET request to `/v2/uptime/checks/$CHECK_ID/alerts`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeListAlertsRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
    }
client.Uptime.ListAlerts(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items returned per page
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Which 'page' of paginated results to return.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.CreateAlert(CheckID, request) -> *godonext.UptimeCreateAlertResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an Uptime alert, send a POST request to `/v2/uptime/checks/$CHECK_ID/alerts` specifying the attributes
in the table below in the JSON body.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeCreateAlertRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        Body: &godonext.Alert{},
    }
client.Uptime.CreateAlert(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.Alert` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.GetAlert(CheckID, AlertID) -> *godonext.UptimeGetAlertResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To show information about an existing alert, send a GET request to `/v2/uptime/checks/$CHECK_ID/alerts/$ALERT_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeGetAlertRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        AlertID: "17f0f0ae-b7e5-4ef6-86e3-aa569db58284",
    }
client.Uptime.GetAlert(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` — A unique identifier for an alert.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.UpdateAlert(CheckID, AlertID, request) -> *godonext.UptimeUpdateAlertResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the settings of an Uptime alert, send a PUT request to `/v2/uptime/checks/$CHECK_ID/alerts/$ALERT_ID`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeUpdateAlertRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        AlertID: "17f0f0ae-b7e5-4ef6-86e3-aa569db58284",
        Body: &godonext.AlertUpdatable{},
    }
client.Uptime.UpdateAlert(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` — A unique identifier for an alert.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.AlertUpdatable` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.Uptime.DeleteAlert(CheckID, AlertID) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an Uptime alert, send a DELETE request to `/v2/uptime/checks/$CHECK_ID/alerts/$ALERT_ID`. A 204 status
code with no body will be returned in response to a successful request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.UptimeDeleteAlertRequest{
        CheckID: "4de7ac8b-495b-4884-9a69-1050c6793cd6",
        AlertID: "17f0f0ae-b7e5-4ef6-86e3-aa569db58284",
    }
client.Uptime.DeleteAlert(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**checkID:** `string` — A unique identifier for a check.
    
</dd>
</dl>

<dl>
<dd>

**alertID:** `string` — A unique identifier for an alert.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## GradientAI Platform
<details><summary><code>client.GradientAiPlatform.GenaiListAgents() -> *godonext.APIListAgentsOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all agents, send a GET request to `/v2/gen-ai/agents`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAgentsRequest{}
client.GradientAiPlatform.GenaiListAgents(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**onlyDeployed:** `*bool` — Only list agents that are deployed.
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateAgent(request) -> *godonext.APICreateAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new agent, send a POST request to `/v2/gen-ai/agents`. The response body contains a JSON object with the newly created agent object.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateAgentInputPublic{}
client.GradientAiPlatform.GenaiCreateAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**anthropicKeyUUID:** `*string` — Optional Anthropic API key ID to use with Anthropic models
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — A text description of the agent, not used in inference
    
</dd>
</dl>

<dl>
<dd>

**instruction:** `*string` — Agent instruction. Instructions help your agent to perform its job effectively. See [Write Effective Agent Instructions](https://docs.digitalocean.com/products/genai-platform/concepts/best-practices/#agent-instructions) for best practices.
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `[]string` — Ids of the knowledge base(s) to attach to the agent
    
</dd>
</dl>

<dl>
<dd>

**mcpServers:** `[]*godonext.APIMcpServer` — MCP (Model Context Protocol) servers to attach to the agent
    
</dd>
</dl>

<dl>
<dd>

**modelProviderKeyUUID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**modelRouterUUID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**modelUUID:** `*string` — Identifier for the foundation model.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Agent name
    
</dd>
</dl>

<dl>
<dd>

**openAiKeyUUID:** `*string` — Optional OpenAI API key ID to use with OpenAI models
    
</dd>
</dl>

<dl>
<dd>

**projectID:** `*string` — The id of the DigitalOcean project this agent will belong to
    
</dd>
</dl>

<dl>
<dd>

**reasoningEffort:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — The DigitalOcean region to deploy your agent in
    
</dd>
</dl>

<dl>
<dd>

**routerPresetSlug:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — Agent tag to organize related resources
    
</dd>
</dl>

<dl>
<dd>

**thinkingTokenBudget:** `*int64` 
    
</dd>
</dl>

<dl>
<dd>

**workspaceUUID:** `*string` — Identifier for the workspace
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListAgentAPIKeys(AgentUUID) -> *godonext.APIListAgentAPIKeysOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all agent API keys, send a GET request to `/v2/gen-ai/agents/{agent_uuid}/api_keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAgentAPIKeysRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListAgentAPIKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateAgentAPIKey(AgentUUID, request) -> *godonext.APICreateAgentAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an agent API key, send a POST request to `/v2/gen-ai/agents/{agent_uuid}/api_keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateAgentAPIKeyInputPublic{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiCreateAgentAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**apiCreateAgentAPIKeyInputPublicAgentUUID:** `*string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — A human friendly name to identify the key
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAgentAPIKey(AgentUUID, APIKeyUUID, request) -> *godonext.APIUpdateAgentAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an agent API key, send a PUT request to `/v2/gen-ai/agents/{agent_uuid}/api_keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateAgentAPIKeyInputPublic{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAgentAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAgentAPIKeyInputPublicAgentUUID:** `*string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAgentAPIKeyInputPublicAPIKeyUUID:** `*string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteAgentAPIKey(AgentUUID, APIKeyUUID) -> *godonext.APIDeleteAgentAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an API key for an agent, send a DELETE request to `/v2/gen-ai/agents/{agent_uuid}/api_keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteAgentAPIKeyRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteAgentAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — A unique identifier for your agent.
    
</dd>
</dl>

<dl>
<dd>

**apiKeyUUID:** `string` — API key for an agent.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiRegenerateAgentAPIKey(AgentUUID, APIKeyUUID) -> *godonext.APIRegenerateAgentAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To regenerate an agent API key, send a PUT request to `/v2/gen-ai/agents/{agent_uuid}/api_keys/{api_key_uuid}/regenerate`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiRegenerateAgentAPIKeyRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiRegenerateAgentAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiAttachAgentFunction(AgentUUID, request) -> *godonext.APILinkAgentFunctionOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a function route for an agent, send a POST request to `/v2/gen-ai/agents/{agent_uuid}/functions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APILinkAgentFunctionInputPublic{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiAttachAgentFunction(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**apiLinkAgentFunctionInputPublicAgentUUID:** `*string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Function description
    
</dd>
</dl>

<dl>
<dd>

**faasName:** `*string` — The name of the function in the DigitalOcean functions platform
    
</dd>
</dl>

<dl>
<dd>

**faasNamespace:** `*string` — The namespace of the function in the DigitalOcean functions platform
    
</dd>
</dl>

<dl>
<dd>

**functionName:** `*string` — Function name
    
</dd>
</dl>

<dl>
<dd>

**inputSchema:** `map[string]any` — Describe the input schema for the function so the agent may call it
    
</dd>
</dl>

<dl>
<dd>

**outputSchema:** `map[string]any` — Describe the output schema for the function so the agent handle its response
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAgentFunction(AgentUUID, FunctionUUID, request) -> *godonext.APIUpdateAgentFunctionOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update the function route, send a PUT request to `/v2/gen-ai/agents/{agent_uuid}/functions/{function_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateAgentFunctionInputPublic{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        FunctionUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAgentFunction(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**functionUUID:** `string` — Function id
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAgentFunctionInputPublicAgentUUID:** `*string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Funciton description
    
</dd>
</dl>

<dl>
<dd>

**faasName:** `*string` — The name of the function in the DigitalOcean functions platform
    
</dd>
</dl>

<dl>
<dd>

**faasNamespace:** `*string` — The namespace of the function in the DigitalOcean functions platform
    
</dd>
</dl>

<dl>
<dd>

**functionName:** `*string` — Function name
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAgentFunctionInputPublicFunctionUUID:** `*string` — Function id
    
</dd>
</dl>

<dl>
<dd>

**inputSchema:** `map[string]any` — Describe the input schema for the function so the agent may call it
    
</dd>
</dl>

<dl>
<dd>

**outputSchema:** `map[string]any` — Describe the output schema for the function so the agent handle its response
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDetachAgentFunction(AgentUUID, FunctionUUID) -> *godonext.APIUnlinkAgentFunctionOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a function route from an agent, send a DELETE request to `/v2/gen-ai/agents/{agent_uuid}/functions/{function_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDetachAgentFunctionRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        FunctionUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDetachAgentFunction(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — The id of the agent the function route belongs to.
    
</dd>
</dl>

<dl>
<dd>

**functionUUID:** `string` — The function route to be destroyed. This does not destroy the function itself.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiAttachAgentGuardrails(AgentUUID, request) -> *godonext.APILinkAgentGuardrailOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To attach guardrails to an agent, send a POST request to `/v2/gen-ai/agents/{agent_uuid}/guardrails`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APILinkAgentGuardrailsInputPublic{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiAttachAgentGuardrails(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — The UUID of the agent.
    
</dd>
</dl>

<dl>
<dd>

**apiLinkAgentGuardrailsInputPublicAgentUUID:** `*string` — The UUID of the agent.
    
</dd>
</dl>

<dl>
<dd>

**guardrails:** `[]*godonext.APIAgentGuardrailInput` — The list of guardrails to attach.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDetachAgentGuardrail(AgentUUID, GuardrailUUID) -> *godonext.APIUnlinkAgentGuardrailOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To detach a guardrail from an agent, send a DELETE request to `/v2/gen-ai/agents/{agent_uuid}/guardrails/{guardrail_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDetachAgentGuardrailRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        GuardrailUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDetachAgentGuardrail(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — The UUID of the agent.
    
</dd>
</dl>

<dl>
<dd>

**guardrailUUID:** `string` — The UUID of the guardrail to detach.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiAttachKnowledgeBases(AgentUUID) -> *godonext.APILinkKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To attach knowledge bases to an agent, send a POST request to `/v2/gen-ai/agents/{agent_uuid}/knowledge_bases`
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiAttachKnowledgeBasesRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiAttachKnowledgeBases(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — A unique identifier for an agent.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiAttachKnowledgeBase(AgentUUID, KnowledgeBaseUUID) -> *godonext.APILinkKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To attach a knowledge base to an agent, send a POST request to `/v2/gen-ai/agents/{agent_uuid}/knowledge_bases/{knowledge_base_uuid}`
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiAttachKnowledgeBaseRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiAttachKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — A unique identifier for an agent.
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — A unique identifier for a knowledge base.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDetachKnowledgeBase(AgentUUID, KnowledgeBaseUUID) -> *godonext.APIUnlinkKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To detach a knowledge base from an agent, send a DELETE request to `/v2/gen-ai/agents/{agent_uuid}/knowledge_bases/{knowledge_base_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDetachKnowledgeBaseRequest{
        AgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDetachKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUID:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — Knowledge base id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiAttachAgent(ParentAgentUUID, ChildAgentUUID, request) -> *godonext.APILinkAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add an agent route to an agent, send a POST request to `/v2/gen-ai/agents/{parent_agent_uuid}/child_agents/{child_agent_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APILinkAgentInputPublic{
        ParentAgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        ChildAgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiAttachAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**parentAgentUUID:** `string` — A unique identifier for the parent agent.
    
</dd>
</dl>

<dl>
<dd>

**childAgentUUID:** `string` — Routed agent id
    
</dd>
</dl>

<dl>
<dd>

**apiLinkAgentInputPublicChildAgentUUID:** `*string` — Routed agent id
    
</dd>
</dl>

<dl>
<dd>

**ifCase:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**apiLinkAgentInputPublicParentAgentUUID:** `*string` — A unique identifier for the parent agent.
    
</dd>
</dl>

<dl>
<dd>

**routeName:** `*string` — Name of route
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAttachedAgent(ParentAgentUUID, ChildAgentUUID, request) -> *godonext.APIUpdateLinkedAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an agent route for an agent, send a PUT request to `/v2/gen-ai/agents/{parent_agent_uuid}/child_agents/{child_agent_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateLinkedAgentInputPublic{
        ParentAgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        ChildAgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAttachedAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**parentAgentUUID:** `string` — A unique identifier for the parent agent.
    
</dd>
</dl>

<dl>
<dd>

**childAgentUUID:** `string` — Routed agent id
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateLinkedAgentInputPublicChildAgentUUID:** `*string` — Routed agent id
    
</dd>
</dl>

<dl>
<dd>

**ifCase:** `*string` — Describes the case in which the child agent should be used
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateLinkedAgentInputPublicParentAgentUUID:** `*string` — A unique identifier for the parent agent.
    
</dd>
</dl>

<dl>
<dd>

**routeName:** `*string` — Route name
    
</dd>
</dl>

<dl>
<dd>

**uuid:** `*string` — Unique id of linkage
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDetachAgent(ParentAgentUUID, ChildAgentUUID) -> *godonext.APIUnlinkAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an agent route from a parent agent, send a DELETE request to `/v2/gen-ai/agents/{parent_agent_uuid}/child_agents/{child_agent_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDetachAgentRequest{
        ParentAgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        ChildAgentUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDetachAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**parentAgentUUID:** `string` — Pagent agent id
    
</dd>
</dl>

<dl>
<dd>

**childAgentUUID:** `string` — Routed agent id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetAgent(UUID) -> *godonext.APIGetAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve details of an agent, GET request to `/v2/gen-ai/agents/{uuid}`. The response body is a JSON object containing the agent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetAgentRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Unique agent id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAgent(UUID, request) -> *godonext.APIUpdateAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an agent, send a PUT request to `/v2/gen-ai/agents/{uuid}`. The response body is a JSON object containing the agent.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateAgentInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Unique agent id
    
</dd>
</dl>

<dl>
<dd>

**agentLogInsightsEnabled:** `*bool` 
    
</dd>
</dl>

<dl>
<dd>

**allowedDomains:** `[]string` — Optional list of allowed domains for the chatbot - Must use fully qualified domain name (FQDN) such as https://example.com
    
</dd>
</dl>

<dl>
<dd>

**anthropicKeyUUID:** `*string` — Optional anthropic key uuid for use with anthropic models
    
</dd>
</dl>

<dl>
<dd>

**clearMcpServers:** `*bool` — When true, removes all MCP servers from the agent. Use this instead of sending an empty mcp_servers array.
    
</dd>
</dl>

<dl>
<dd>

**conversationLogsEnabled:** `*bool` — Optional update of conversation logs enabled
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Agent description
    
</dd>
</dl>

<dl>
<dd>

**instruction:** `*string` — Agent instruction. Instructions help your agent to perform its job effectively. See [Write Effective Agent Instructions](https://docs.digitalocean.com/products/genai-platform/concepts/best-practices/#agent-instructions) for best practices.
    
</dd>
</dl>

<dl>
<dd>

**k:** `*int64` — How many results should be considered from an attached knowledge base
    
</dd>
</dl>

<dl>
<dd>

**maxTokens:** `*int64` — Specifies the maximum number of tokens the model can process in a single input or output, set as a number between 1 and 512. This determines the length of each response.
    
</dd>
</dl>

<dl>
<dd>

**mcpServers:** `[]*godonext.APIMcpServer` — MCP (Model Context Protocol) servers to attach to the agent
    
</dd>
</dl>

<dl>
<dd>

**modelProviderKeyUUID:** `*string` — Optional Model Provider uuid for use with provider models
    
</dd>
</dl>

<dl>
<dd>

**modelRouterUUID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**modelUUID:** `*string` — Identifier for the foundation model.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Agent name
    
</dd>
</dl>

<dl>
<dd>

**openAiKeyUUID:** `*string` — Optional OpenAI key uuid for use with OpenAI models
    
</dd>
</dl>

<dl>
<dd>

**projectID:** `*string` — The id of the DigitalOcean project this agent will belong to
    
</dd>
</dl>

<dl>
<dd>

**provideCitations:** `*bool` 
    
</dd>
</dl>

<dl>
<dd>

**reasoningEffort:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**retrievalMethod:** `*godonext.APIRetrievalMethod` 
    
</dd>
</dl>

<dl>
<dd>

**routerPresetSlug:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — A set of abitrary tags to organize your agent
    
</dd>
</dl>

<dl>
<dd>

**temperature:** `*float64` — Controls the model’s creativity, specified as a number between 0 and 1. Lower values produce more predictable and conservative responses, while higher values encourage creativity and variation.
    
</dd>
</dl>

<dl>
<dd>

**thinkingTokenBudget:** `*int64` 
    
</dd>
</dl>

<dl>
<dd>

**topP:** `*float64` — Defines the cumulative probability threshold for word selection, specified as a number between 0 and 1. Higher values allow for more diverse outputs, while lower values ensure focused and coherent responses.
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAgentInputPublicUUID:** `*string` — Unique agent id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteAgent(UUID) -> *godonext.APIDeleteAgentOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an agent, send a DELETE request to `/v2/gen-ai/agents/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteAgentRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteAgent(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Unique agent id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetAgentChildren(UUID) -> *godonext.APIGetChildrenOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To view agent routes for an agent, send a GET requtest to `/v2/gen-ai/agents/{uuid}/child_agents`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetAgentChildrenRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetAgentChildren(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Agent id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAgentDeploymentVisibility(UUID, request) -> *godonext.APIUpdateAgentDeploymentVisbilityOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Check whether an agent is public or private. To update the agent status, send a PUT request to `/v2/gen-ai/agents/{uuid}/deployment_visibility`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateAgentDeploymentVisibilityInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAgentDeploymentVisibility(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Unique id
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAgentDeploymentVisibilityInputPublicUUID:** `*string` — Unique id
    
</dd>
</dl>

<dl>
<dd>

**visibility:** `*godonext.APIDeploymentVisibility` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetAgentUsage(UUID) -> *godonext.APIGetAgentUsageOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get agent usage, send a GET request to `/v2/gen-ai/agents/{uuid}/usage`. Returns usage metrics for the specified agent within the provided time range.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetAgentUsageRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        Start: godonext.String(
            `"example string"`,
        ),
        Stop: godonext.String(
            `"example string"`,
        ),
    }
client.GradientAiPlatform.GenaiGetAgentUsage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Agent id
    
</dd>
</dl>

<dl>
<dd>

**start:** `*string` — Return all usage data from this date.
    
</dd>
</dl>

<dl>
<dd>

**stop:** `*string` — Return all usage data up to this date, if omitted, will return up to the current date.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListAgentVersions(UUID) -> *godonext.APIListAgentVersionsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all agent versions, send a GET request to `/v2/gen-ai/agents/{uuid}/versions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAgentVersionsRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListAgentVersions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Agent uuid
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiRollbackToAgentVersion(UUID, request) -> *godonext.APIRollbackToAgentVersionOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update to a specific agent version, send a PUT request to `/v2/gen-ai/agents/{uuid}/versions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIRollbackToAgentVersionInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiRollbackToAgentVersion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Agent unique identifier
    
</dd>
</dl>

<dl>
<dd>

**apiRollbackToAgentVersionInputPublicUUID:** `*string` — Agent unique identifier
    
</dd>
</dl>

<dl>
<dd>

**versionHash:** `*string` — Unique identifier
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListAnthropicAPIKeys() -> *godonext.APIListAnthropicAPIKeysOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all Anthropic API keys, send a GET request to `/v2/gen-ai/anthropic/keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAnthropicAPIKeysRequest{}
client.GradientAiPlatform.GenaiListAnthropicAPIKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateAnthropicAPIKey(request) -> *godonext.APICreateAnthropicAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an Anthropic API key, send a POST request to `/v2/gen-ai/anthropic/keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateAnthropicAPIKeyInputPublic{}
client.GradientAiPlatform.GenaiCreateAnthropicAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKey:** `*string` — Anthropic API key
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the key
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetAnthropicAPIKey(APIKeyUUID) -> *godonext.APIGetAnthropicAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve details of an Anthropic API key, send a GET request to `/v2/gen-ai/anthropic/keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetAnthropicAPIKeyRequest{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetAnthropicAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAnthropicAPIKey(APIKeyUUID, request) -> *godonext.APIUpdateAnthropicAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an Anthropic API key, send a PUT request to `/v2/gen-ai/anthropic/keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateAnthropicAPIKeyInputPublic{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAnthropicAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**apiKey:** `*string` — Anthropic API key
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateAnthropicAPIKeyInputPublicAPIKeyUUID:** `*string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the key
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteAnthropicAPIKey(APIKeyUUID) -> *godonext.APIDeleteAnthropicAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an Anthropic API key, send a DELETE request to `/v2/gen-ai/anthropic/keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteAnthropicAPIKeyRequest{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteAnthropicAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListAgentsByAnthropicKey(UUID) -> *godonext.APIListAgentsByAnthropicKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List Agents by Anthropic Key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAgentsByAnthropicKeyRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListAgentsByAnthropicKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Unique ID of Anthropic key
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListCustomModels() -> *godonext.APIListCustomModelsOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list custom models, send a GET request to `/v2/gen-ai/custom_models`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListCustomModelsRequest{}
client.GradientAiPlatform.GenaiListCustomModels(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number for pagination.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of items per page.
    
</dd>
</dl>

<dl>
<dd>

**status:** `*godonext.GenaiListCustomModelsRequestStatus` — Filter by model status.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiImportCustomModel(request) -> *godonext.APIImportCustomModelOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To import a custom model, send a POST request to `/v2/gen-ai/custom_models/import`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIImportCustomModelInputPublic{}
client.GradientAiPlatform.GenaiImportCustomModel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**acceptTermsAndConditions:** `*bool` — Whether the caller accepts the terms and conditions for importing this model
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Description of the model
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name for the imported model
    
</dd>
</dl>

<dl>
<dd>

**preferredGpuRegion:** `*string` — Preferred GPU region for deployment
    
</dd>
</dl>

<dl>
<dd>

**sourceRef:** `*godonext.CustomModelSourceRef` 
    
</dd>
</dl>

<dl>
<dd>

**sourceType:** `*godonext.CustomModelSourceType` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `*godonext.CustomModelTags` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetCustomModel(UUID) -> *godonext.APIGetCustomModelOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve details of a custom model, send a GET request to `/v2/gen-ai/custom_models/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetCustomModelRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetCustomModel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — UUID of the custom model to retrieve
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteCustomModel(UUID) -> *godonext.APIDeleteCustomModelOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a custom model, send a DELETE request to `/v2/genai/custom_models/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteCustomModelRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteCustomModel(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — UUID of the custom model to delete
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateCustomModelMetadata(UUID, request) -> *godonext.APIUpdateCustomModelMetadataOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update custom model metadata, send a PATCH request to `/v2/gen-ai/custom_models/{uuid}/metadata`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateCustomModelMetadataInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateCustomModelMetadata(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — UUID of the custom model to update
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `*godonext.CustomModelTags` 
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateCustomModelMetadataInputPublicUUID:** `*string` — UUID of the custom model to update
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListEvaluationDatasets() -> *godonext.APIListEvaluationDatasetsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list evaluation datasets, send a GET request to `/v2/gen-ai/evaluation_datasets`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListEvaluationDatasetsRequest{}
client.GradientAiPlatform.GenaiListEvaluationDatasets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**datasetType:** `*godonext.GenaiListEvaluationDatasetsRequestDatasetType` — Filter by evaluation dataset type.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateEvaluationDataset(request) -> *godonext.APICreateEvaluationDatasetOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an evaluation dataset, send a POST request to `/v2/gen-ai/evaluation_datasets`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateEvaluationDatasetInputPublic{}
client.GradientAiPlatform.GenaiCreateEvaluationDataset(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**datasetType:** `*godonext.APIEvaluationDatasetType` 
    
</dd>
</dl>

<dl>
<dd>

**fileUploadDataset:** `*godonext.APIFileUploadDataSource` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — The name of the agent evaluation dataset.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateEvaluationDatasetFileUploadPresignedURLs(request) -> *godonext.APICreateDataSourceFileUploadPresignedURLsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create presigned URLs for evaluation dataset file upload, send a POST request to `/v2/gen-ai/evaluation_datasets/file_upload_presigned_urls`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateDataSourceFileUploadPresignedURLsInputPublic{}
client.GradientAiPlatform.GenaiCreateEvaluationDatasetFileUploadPresignedURLs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.APICreateDataSourceFileUploadPresignedURLsInputPublic` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetEvaluationDatasetDownloadURL(DatasetUUID) -> *godonext.APIGetEvaluationDatasetDownloadURLOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a presigned download URL for an evaluation dataset, send a GET request to `/v2/genai/evaluation_datasets/{dataset_uuid}/download_url`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetEvaluationDatasetDownloadURLRequest{
        DatasetUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetEvaluationDatasetDownloadURL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**datasetUUID:** `string` — UUID of the evaluation dataset.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListEvaluationMetrics() -> *godonext.APIListEvaluationMetricsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all evaluation metrics, send a GET request to `/v2/gen-ai/evaluation_metrics`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GradientAiPlatform.GenaiListEvaluationMetrics(
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

<details><summary><code>client.GradientAiPlatform.GenaiRunEvaluationTestCase(request) -> *godonext.APIRunEvaluationTestCaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To run an evaluation test case, send a POST request to `/v2/gen-ai/evaluation_runs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIRunEvaluationTestCaseInputPublic{}
client.GradientAiPlatform.GenaiRunEvaluationTestCase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentDeploymentNames:** `[]string` — Agent deployment names to run the test case against (ADK agent workspaces).
    
</dd>
</dl>

<dl>
<dd>

**agentUUIDs:** `[]string` — Agent UUIDs to run the test case against (legacy agents).
    
</dd>
</dl>

<dl>
<dd>

**runName:** `*string` — The name of the run.
    
</dd>
</dl>

<dl>
<dd>

**testCaseUUID:** `*string` — Test-case UUID to run
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetEvaluationRun(EvaluationRunUUID) -> *godonext.APIGetEvaluationRunOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrive information about an existing evaluation run, send a GET request to `/v2/gen-ai/evaluation_runs/{evaluation_run_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetEvaluationRunRequest{
        EvaluationRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetEvaluationRun(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationRunUUID:** `string` — Evaluation run UUID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetEvaluationRunResults(EvaluationRunUUID) -> *godonext.APIGetEvaluationRunResultsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve results of an evaluation run, send a GET request to `/v2/gen-ai/evaluation_runs/{evaluation_run_uuid}/results`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetEvaluationRunResultsRequest{
        EvaluationRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetEvaluationRunResults(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationRunUUID:** `string` — Evaluation run UUID.
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetEvaluationRunPromptResults(EvaluationRunUUID, PromptID) -> *godonext.APIGetEvaluationRunPromptResultsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve results of an evaluation run, send a GET request to `/v2/gen-ai/evaluation_runs/{evaluation_run_uuid}/results/{prompt_id}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetEvaluationRunPromptResultsRequest{
        EvaluationRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        PromptID: 1,
    }
client.GradientAiPlatform.GenaiGetEvaluationRunPromptResults(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationRunUUID:** `string` — Evaluation run UUID.
    
</dd>
</dl>

<dl>
<dd>

**promptID:** `int` — Prompt ID to get results for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListEvaluationTestCases() -> *godonext.APIListEvaluationTestCasesOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all evaluation test cases, send a GET request to `/v2/gen-ai/evaluation_test_cases`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GradientAiPlatform.GenaiListEvaluationTestCases(
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

<details><summary><code>client.GradientAiPlatform.GenaiCreateEvaluationTestCase(request) -> *godonext.APICreateEvaluationTestCaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an evaluation test-case send a POST request to `/v2/gen-ai/evaluation_test_cases`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateEvaluationTestCaseInputPublic{}
client.GradientAiPlatform.GenaiCreateEvaluationTestCase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentWorkspaceName:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**datasetUUID:** `*string` — Dataset against which the test‑case is executed.
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Description of the test case.
    
</dd>
</dl>

<dl>
<dd>

**metrics:** `[]string` — Full metric list to use for evaluation test case.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the test case.
    
</dd>
</dl>

<dl>
<dd>

**starMetric:** `*godonext.APIStarMetric` 
    
</dd>
</dl>

<dl>
<dd>

**workspaceUUID:** `*string` — The workspace uuid.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListEvaluationRunsByTestCase(EvaluationTestCaseUUID) -> *godonext.APIListEvaluationRunsByTestCaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all evaluation runs by test case, send a GET request to `/v2/gen-ai/evaluation_test_cases/{evaluation_test_case_uuid}/evaluation_runs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListEvaluationRunsByTestCaseRequest{
        EvaluationTestCaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListEvaluationRunsByTestCase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evaluationTestCaseUUID:** `string` — Evaluation run UUID.
    
</dd>
</dl>

<dl>
<dd>

**evaluationTestCaseVersion:** `*int` — Version of the test case.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetEvaluationTestCase(TestCaseUUID) -> *godonext.APIGetEvaluationTestCaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrive information about an existing evaluation test case, send a GET request to `/v2/gen-ai/evaluation_test_case/{test_case_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetEvaluationTestCaseRequest{
        TestCaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetEvaluationTestCase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**testCaseUUID:** `string` — The test case uuid to retrieve.
    
</dd>
</dl>

<dl>
<dd>

**evaluationTestCaseVersion:** `*int` — Version of the test case.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateEvaluationTestCase(TestCaseUUID, request) -> *godonext.APIUpdateEvaluationTestCaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an evaluation test-case send a PUT request to `/v2/gen-ai/evaluation_test_cases/{test_case_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateEvaluationTestCaseInputPublic{
        TestCaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateEvaluationTestCase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**testCaseUUID:** `string` — Test-case UUID to update
    
</dd>
</dl>

<dl>
<dd>

**datasetUUID:** `*string` — Dataset against which the test‑case is executed.
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Description of the test case.
    
</dd>
</dl>

<dl>
<dd>

**metrics:** `*godonext.APIEvaluationTestCaseMetricList` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the test case.
    
</dd>
</dl>

<dl>
<dd>

**starMetric:** `*godonext.APIStarMetric` 
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateEvaluationTestCaseInputPublicTestCaseUUID:** `*string` — Test-case UUID to update
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListIndexingJobs() -> *godonext.APIListKnowledgeBaseIndexingJobsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all indexing jobs for a knowledge base, send a GET request to `/v2/gen-ai/indexing_jobs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListIndexingJobsRequest{}
client.GradientAiPlatform.GenaiListIndexingJobs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateIndexingJob(request) -> *godonext.APIStartKnowledgeBaseIndexingJobOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To start an indexing job for a knowledge base, send a POST request to `/v2/gen-ai/indexing_jobs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIStartKnowledgeBaseIndexingJobInputPublic{}
client.GradientAiPlatform.GenaiCreateIndexingJob(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**dataSourceUUIDs:** `[]string` — List of data source ids to index, if none are provided, all data sources will be indexed
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `*string` — Knowledge base id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListIndexingJobDataSources(IndexingJobUUID) -> *godonext.APIListIndexingJobDataSourcesOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all datasources for an indexing job, send a GET request to `/v2/gen-ai/indexing_jobs/{indexing_job_uuid}/data_sources`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListIndexingJobDataSourcesRequest{
        IndexingJobUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListIndexingJobDataSources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**indexingJobUUID:** `string` — Uuid of the indexing job
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetIndexingJobDetailsSignedURL(IndexingJobUUID) -> *godonext.APIGetIndexingJobDetailsSignedURLOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a signed URL for indexing job details, send a GET request to `/v2/gen-ai/indexing_jobs/{uuid}/details_signed_url`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetIndexingJobDetailsSignedURLRequest{
        IndexingJobUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetIndexingJobDetailsSignedURL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**indexingJobUUID:** `string` — The uuid of the indexing job
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetIndexingJob(UUID) -> *godonext.APIGetKnowledgeBaseIndexingJobOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get status of an indexing Job for a knowledge base, send a GET request to `/v2/gen-ai/indexing_jobs/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetIndexingJobRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetIndexingJob(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Indexing job id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCancelIndexingJob(UUID, request) -> *godonext.APICancelKnowledgeBaseIndexingJobOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To cancel an indexing job for a knowledge base, send a PUT request to `/v2/gen-ai/indexing_jobs/{uuid}/cancel`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICancelKnowledgeBaseIndexingJobInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiCancelIndexingJob(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — A unique identifier for an indexing job.
    
</dd>
</dl>

<dl>
<dd>

**apiCancelKnowledgeBaseIndexingJobInputPublicUUID:** `*string` — A unique identifier for an indexing job.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListKnowledgeBases() -> *godonext.APIListKnowledgeBasesOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all knowledge bases, send a GET request to `/v2/gen-ai/knowledge_bases`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListKnowledgeBasesRequest{}
client.GradientAiPlatform.GenaiListKnowledgeBases(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateKnowledgeBase(request) -> *godonext.APICreateKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a knowledge base, send a POST request to `/v2/gen-ai/knowledge_bases`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateKnowledgeBaseInputPublic{}
client.GradientAiPlatform.GenaiCreateKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**databaseID:** `*string` 

Identifier of the DigitalOcean OpenSearch database this knowledge base will use, optional.
If not provided, we create a new database for the knowledge base in
the same region as the knowledge base.
    
</dd>
</dl>

<dl>
<dd>

**datasources:** `[]*godonext.APIKbDataSource` — Optional data sources to attach at creation. Omit or use an empty list to create the knowledge base without sources, then add sources (with chunking strategy and sizes) using [Add a Data Source to a Knowledge Base](#operation/create_knowledge_base_data_source). When provided, see [Organize Data Sources](https://docs.digitalocean.com/products/gradient-ai-platform/how-to/create-manage-agent-knowledge-bases/#add-data-sources) for best practices.
    
</dd>
</dl>

<dl>
<dd>

**embeddingModelUUID:** `*string` — Identifier for the [embedding model](https://docs.digitalocean.com/products/genai-platform/details/models/#embedding-models).
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the knowledge base.
    
</dd>
</dl>

<dl>
<dd>

**projectID:** `*string` — Identifier of the DigitalOcean project this knowledge base will belong to.
    
</dd>
</dl>

<dl>
<dd>

**region:** `*string` — The datacenter region to deploy the knowledge base in.
    
</dd>
</dl>

<dl>
<dd>

**rerankingConfig:** `*godonext.APIRerankingConfiguration` 
    
</dd>
</dl>

<dl>
<dd>

**size:** `*godonext.APIOpenSearchPlanSize` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — Tags to organize your knowledge base.
    
</dd>
</dl>

<dl>
<dd>

**vpcUUID:** `*string` — The VPC to deploy the knowledge base database in
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateDataSourceFileUploadPresignedURLs(request) -> *godonext.APICreateDataSourceFileUploadPresignedURLsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create presigned URLs for knowledge base data source file upload, send a POST request to `/v2/gen-ai/knowledge_bases/data_sources/file_upload_presigned_urls`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateDataSourceFileUploadPresignedURLsInputPublic{}
client.GradientAiPlatform.GenaiCreateDataSourceFileUploadPresignedURLs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.APICreateDataSourceFileUploadPresignedURLsInputPublic` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListKnowledgeBaseDataSources(KnowledgeBaseUUID) -> *godonext.APIListKnowledgeBaseDataSourcesOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all data sources for a knowledge base, send a GET request to `/v2/gen-ai/knowledge_bases/{knowledge_base_uuid}/data_sources`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListKnowledgeBaseDataSourcesRequest{
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListKnowledgeBaseDataSources(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — Knowledge base id
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateKnowledgeBaseDataSource(KnowledgeBaseUUID, request) -> *godonext.APICreateKnowledgeBaseDataSourceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To add a data source to a knowledge base, send a POST request to `/v2/gen-ai/knowledge_bases/{knowledge_base_uuid}/data_sources`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateKnowledgeBaseDataSourceInputPublic{
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiCreateKnowledgeBaseDataSource(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — Knowledge base id
    
</dd>
</dl>

<dl>
<dd>

**awsDataSource:** `*godonext.APIAwsDataSource` 
    
</dd>
</dl>

<dl>
<dd>

**chunkingAlgorithm:** `*godonext.APIChunkingAlgorithm` 
    
</dd>
</dl>

<dl>
<dd>

**chunkingOptions:** `*godonext.APIChunkingOptions` 
    
</dd>
</dl>

<dl>
<dd>

**apiCreateKnowledgeBaseDataSourceInputPublicKnowledgeBaseUUID:** `*string` — Knowledge base id
    
</dd>
</dl>

<dl>
<dd>

**spacesDataSource:** `*godonext.APISpacesDataSource` 
    
</dd>
</dl>

<dl>
<dd>

**webCrawlerDataSource:** `*godonext.APIWebCrawlerDataSource` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateKnowledgeBaseDataSource(KnowledgeBaseUUID, DataSourceUUID, request) -> *godonext.APIUpdateKnowledgeBaseDataSourceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a data source (e.g. chunking options), send a PUT request to `/v2/gen-ai/knowledge_bases/{knowledge_base_uuid}/data_sources/{data_source_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateKnowledgeBaseDataSourceInputPublic{
        KnowledgeBaseUUID: "123e4567-e89b-12d3-a456-426614174000",
        DataSourceUUID: "123e4567-e89b-12d3-a456-426614174000",
    }
client.GradientAiPlatform.GenaiUpdateKnowledgeBaseDataSource(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — Knowledge Base ID (Path Parameter)
    
</dd>
</dl>

<dl>
<dd>

**dataSourceUUID:** `string` — Data Source ID (Path Parameter)
    
</dd>
</dl>

<dl>
<dd>

**chunkingAlgorithm:** `*godonext.APIChunkingAlgorithm` 
    
</dd>
</dl>

<dl>
<dd>

**chunkingOptions:** `*godonext.APIChunkingOptions` 
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateKnowledgeBaseDataSourceInputPublicDataSourceUUID:** `*string` — Data Source ID (Path Parameter)
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateKnowledgeBaseDataSourceInputPublicKnowledgeBaseUUID:** `*string` — Knowledge Base ID (Path Parameter)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteKnowledgeBaseDataSource(KnowledgeBaseUUID, DataSourceUUID) -> *godonext.APIDeleteKnowledgeBaseDataSourceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a data source from a knowledge base, send a DELETE request to `/v2/gen-ai/knowledge_bases/{knowledge_base_uuid}/data_sources/{data_source_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteKnowledgeBaseDataSourceRequest{
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
        DataSourceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteKnowledgeBaseDataSource(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — Knowledge base id
    
</dd>
</dl>

<dl>
<dd>

**dataSourceUUID:** `string` — Data source id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListIndexingJobsByKnowledgeBase(KnowledgeBaseUUID) -> *godonext.APIListKnowledgeBaseIndexingJobsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list latest 15 indexing jobs for a knowledge base, send a GET request to `/v2/gen-ai/knowledge_bases/{knowledge_base_uuid}/indexing_jobs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListIndexingJobsByKnowledgeBaseRequest{
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListIndexingJobsByKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — Knowledge base uuid in string
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetKnowledgeBase(UUID) -> *godonext.APIGetKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrive information about an existing knowledge base, send a GET request to `/v2/gen-ai/knowledge_bases/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetKnowledgeBaseRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Knowledge base id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateKnowledgeBase(UUID, request) -> *godonext.APIUpdateKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a knowledge base, send a PUT request to `/v2/gen-ai/knowledge_bases/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateKnowledgeBaseInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Knowledge base id
    
</dd>
</dl>

<dl>
<dd>

**databaseID:** `*string` — The id of the DigitalOcean database this knowledge base will use, optional.
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Knowledge base name
    
</dd>
</dl>

<dl>
<dd>

**projectID:** `*string` — The id of the DigitalOcean project this knowledge base will belong to
    
</dd>
</dl>

<dl>
<dd>

**rerankingConfig:** `*godonext.APIRerankingConfiguration` 
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]string` — Tags to organize your knowledge base.
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateKnowledgeBaseInputPublicUUID:** `*string` — Knowledge base id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteKnowledgeBase(UUID) -> *godonext.APIDeleteKnowledgeBaseOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a knowledge base, send a DELETE request to `/v2/gen-ai/knowledge_bases/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteKnowledgeBaseRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteKnowledgeBase(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Knowledge base id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateModelEvalDatasetUploadPresignedURLs(request) -> *godonext.APICreateDataSourceFileUploadPresignedURLsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create presigned URLs for model evaluation dataset file upload, send a POST request to `/v2/genai/model_evaluation/datasets/file_upload_presigned_urls`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateModelEvalDatasetUploadPresignedURLsInputPublic{}
client.GradientAiPlatform.GenaiCreateModelEvalDatasetUploadPresignedURLs(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**files:** `[]*godonext.APIPresignedURLFile` — A list of files to generate presigned URLs for.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelEvaluationMetrics() -> *godonext.APIListModelEvaluationMetricsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all available metrics for model evaluation, send a GET request to `/v2/genai/model_evaluation_metrics`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GradientAiPlatform.GenaiListModelEvaluationMetrics(
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

<details><summary><code>client.GradientAiPlatform.GenaiListModelEvaluationPresets() -> *godonext.APIListModelEvaluationPresetsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all saved model evaluation presets, send a GET request to `/v2/genai/model_evaluation_presets`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GradientAiPlatform.GenaiListModelEvaluationPresets(
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

<details><summary><code>client.GradientAiPlatform.GenaiGetModelEvaluationPreset(EvalPresetUUID) -> *godonext.APIGetModelEvaluationPresetOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a saved model evaluation preset, send a GET request to `/v2/genai/model_evaluation_presets/{eval_preset_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetModelEvaluationPresetRequest{
        EvalPresetUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetModelEvaluationPreset(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalPresetUUID:** `string` — UUID of the evaluation preset.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteModelEvaluationPreset(EvalPresetUUID) -> godonext.APIDeleteModelEvaluationPresetOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a saved model evaluation preset, send a DELETE request to `/v2/gen-ai/model_evaluation_presets/{eval_preset_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteModelEvaluationPresetRequest{
        EvalPresetUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteModelEvaluationPreset(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalPresetUUID:** `string` — UUID of the evaluation preset to delete.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelEvaluationRuns() -> *godonext.APIListModelEvaluationRunsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list model evaluation runs, send a GET request to `/v2/genai/model_evaluation_runs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelEvaluationRunsRequest{
        EvalPresetUUID: godonext.String(
            "123e4567-e89b-12d3-a456-426614174000",
        ),
        Search: godonext.String(
            "example string",
        ),
    }
client.GradientAiPlatform.GenaiListModelEvaluationRuns(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalPresetUUID:** `*string` — UUID of the evaluation preset to filter by.
    
</dd>
</dl>

<dl>
<dd>

**status:** `*godonext.GenaiListModelEvaluationRunsRequestStatus` — Filter by evaluation run status.
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>

<dl>
<dd>

**statuses:** `*godonext.GenaiListModelEvaluationRunsRequestStatusesItem` — Filter by one or more statuses. Empty means no status filter.
    
</dd>
</dl>

<dl>
<dd>

**candidateTypes:** `*godonext.GenaiListModelEvaluationRunsRequestCandidateTypesItem` 

Filter by one or more candidate model source types
(serverless, dedicated, router). Empty means no candidate-type filter.
    
</dd>
</dl>

<dl>
<dd>

**search:** `*string` 

Free-text search across the eval run name, candidate model name and
dataset name (case-insensitive substring match). Empty means no search.
    
</dd>
</dl>

<dl>
<dd>

**sortBy:** `*godonext.GenaiListModelEvaluationRunsRequestSortBy` — Field to sort by. Defaults to creation date when unspecified.
    
</dd>
</dl>

<dl>
<dd>

**sortDirection:** `*godonext.GenaiListModelEvaluationRunsRequestSortDirection` — Sort direction. Defaults to descending when unspecified.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateModelEvaluationRun(request) -> *godonext.APICreateModelEvaluationRunOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a model evaluation run, send a POST request to `/v2/genai/model_evaluation_runs`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateModelEvaluationRunInputPublic{}
client.GradientAiPlatform.GenaiCreateModelEvaluationRun(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**candidateInferenceConfig:** `*godonext.APICandidateInferenceConfig` 
    
</dd>
</dl>

<dl>
<dd>

**candidateModelName:** `*string` 

Model slug used to call the candidate model API.
For dedicated inference, this is the model slug from the deployment.
For serverless, this should match the model's internal name.
    
</dd>
</dl>

<dl>
<dd>

**candidateModelSource:** `*godonext.APICandidateModelSource` 
    
</dd>
</dl>

<dl>
<dd>

**candidateModelUUID:** `*string` — UUID of the candidate model to evaluate.
    
</dd>
</dl>

<dl>
<dd>

**datasetUUID:** `*string` — UUID of the dataset to use for evaluation.
    
</dd>
</dl>

<dl>
<dd>

**evalPresetUUID:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**judgeModelUUID:** `*string` — UUID of the judge model used to score responses.
    
</dd>
</dl>

<dl>
<dd>

**metricUUIDs:** `[]string` — UUIDs of metrics to evaluate (selected from ListModelEvaluationMetrics).
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**presetName:** `*string` 
    
</dd>
</dl>

<dl>
<dd>

**saveAsPreset:** `*bool` 

If true, saves the inline config as a reusable preset  
Ignored when eval_preset_uuid is provided.
    
</dd>
</dl>

<dl>
<dd>

**source:** `*string` — Source of the run creation (api, sdk, cli).
    
</dd>
</dl>

<dl>
<dd>

**starMetric:** `*godonext.APIStarMetric` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetModelEvaluationRun(EvalRunUUID) -> *godonext.APIGetModelEvaluationRunOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve a model evaluation run, send a GET request to `/v2/genai/model_evaluation_runs/{eval_run_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetModelEvaluationRunRequest{
        EvalRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetModelEvaluationRun(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalRunUUID:** `string` — UUID of the evaluation run.
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number for per-prompt results (defaults to 1).
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Number of per-prompt results per page (defaults to 50).
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteModelEvaluationRun(EvalRunUUID) -> *godonext.APIDeleteModelEvaluationRunOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a model evaluation run, send a DELETE request to `/v2/gen-ai/model_evaluation_runs/{eval_run_uuid}`. The run must be in a terminal status (`successful`, `partially_successful`, `failed`, or `cancelled`). For runs still in progress, either wait for the run to finish or cancel it, then retry the delete once the run reaches a terminal status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteModelEvaluationRunRequest{
        EvalRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteModelEvaluationRun(
        context.TODO(),
        request,
    )
}
```
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

UUID of the model evaluation run to delete. The run must be in a terminal
status (`successful`, `partially_successful`, `failed`, or `cancelled`).
For runs still in progress, either wait for the run to finish or cancel
it, then retry the delete.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCancelModelEvaluationRun(EvalRunUUID, request) -> *godonext.APICancelModelEvaluationRunOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To cancel an in-progress model evaluation run, send a PUT request to `/v2/gen-ai/model_evaluation_runs/{eval_run_uuid}/cancel`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICancelModelEvaluationRunInputPublic{
        EvalRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiCancelModelEvaluationRun(
        context.TODO(),
        request,
    )
}
```
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

UUID of the model evaluation run to cancel. Returned by `CreateModelEvaluationRun`
and listed via `ListModelEvaluationRuns`. The run must be in a non-terminal status
(queued, running_dataset, or evaluating_results); already-terminal runs return an
error.
    
</dd>
</dl>

<dl>
<dd>

**apiCancelModelEvaluationRunInputPublicEvalRunUUID:** `*string` 

UUID of the model evaluation run to cancel. Returned by `CreateModelEvaluationRun`
and listed via `ListModelEvaluationRuns`. The run must be in a non-terminal status
(queued, running_dataset, or evaluating_results); already-terminal runs return an
error.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetModelEvaluationRunResultsDownloadURL(EvalRunUUID) -> *godonext.APIGetModelEvaluationRunResultsDownloadURLOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To get a presigned download URL for model evaluation run results (gzip-compressed JSON), send a GET request to `/v2/genai/model_evaluation_runs/{eval_run_uuid}/results/download_url`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetModelEvaluationRunResultsDownloadURLRequest{
        EvalRunUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetModelEvaluationRunResultsDownloadURL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**evalRunUUID:** `string` — UUID of the evaluation run.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModels() -> *godonext.APIListModelsOutputPublic</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all models, send a GET request to `/v2/gen-ai/models`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelsRequest{}
client.GradientAiPlatform.GenaiListModels(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**usecases:** `*godonext.GenaiListModelsRequestUsecasesItem` 

Include only models defined for the listed usecases.

 - MODEL_USECASE_UNKNOWN: The use case of the model is unknown
 - MODEL_USECASE_AGENT: The model maybe used in an agent
 - MODEL_USECASE_FINETUNED: The model maybe used for fine tuning
 - MODEL_USECASE_KNOWLEDGEBASE: The model maybe used for knowledge bases (embedding models)
 - MODEL_USECASE_GUARDRAIL: The model maybe used for guardrails
 - MODEL_USECASE_REASONING: The model usecase for reasoning
 - MODEL_USECASE_SERVERLESS: The model usecase for serverless inference
    
</dd>
</dl>

<dl>
<dd>

**publicOnly:** `*bool` — Only include models that are publicly available.
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelAPIKeys() -> *godonext.APIListModelAPIKeysOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all model API keys, send a GET request to `/v2/gen-ai/models/api_keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelAPIKeysRequest{}
client.GradientAiPlatform.GenaiListModelAPIKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateModelAPIKey(request) -> *godonext.APICreateModelAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a model API key, send a POST request to `/v2/gen-ai/models/api_keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateModelAPIKeyInputPublic{}
client.GradientAiPlatform.GenaiCreateModelAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `*string` — A human friendly name to identify the key
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateModelAPIKey(APIKeyUUID, request) -> *godonext.APIUpdateModelAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a model API key, send a PUT request to `/v2/gen-ai/models/api_keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateModelAPIKeyInputPublic{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateModelAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateModelAPIKeyInputPublicAPIKeyUUID:** `*string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteModelAPIKey(APIKeyUUID) -> *godonext.APIDeleteModelAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an API key for a model, send a DELETE request to `/v2/gen-ai/models/api_keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteModelAPIKeyRequest{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteModelAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key for an agent.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiRegenerateModelAPIKey(APIKeyUUID) -> *godonext.APIRegenerateModelAPIKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To regenerate a model API key, send a PUT request to `/v2/gen-ai/models/api_keys/{api_key_uuid}/regenerate`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiRegenerateModelAPIKeyRequest{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiRegenerateModelAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelCatalog() -> *godonext.APIListModelCatalogOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all available models.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelCatalogRequest{}
client.GradientAiPlatform.GenaiListModelCatalog(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetModelCatalogCard(ID) -> *godonext.APIGetModelCatalogCardOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns detailed information for a specific model in the catalog including capabilities, pricing, and code examples.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetModelCatalogCardRequest{
        ID: `"example string"`,
        ModelID: godonext.String(
            `"example string"`,
        ),
    }
client.GradientAiPlatform.GenaiGetModelCatalogCard(
        context.TODO(),
        request,
    )
}
```
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

<dl>
<dd>

**modelID:** `*string` — Model identifier used for API calls (e.g., "llama3.1-70b-instruct"). Alternative to UUID lookup.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelRouters() -> *godonext.APIListModelRoutersOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list model routers, send a GET request to `/v2/gen-ai/models/routers`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelRoutersRequest{}
client.GradientAiPlatform.GenaiListModelRouters(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateModelRouter(request) -> *godonext.APICreateModelRouterOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a model router, send a POST request to `/v2/gen-ai/models/routers`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateModelRouterInputPublic{}
client.GradientAiPlatform.GenaiCreateModelRouter(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `*string` — Model router description
    
</dd>
</dl>

<dl>
<dd>

**fallbackModels:** `[]string` — Fallback models
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Model router name
    
</dd>
</dl>

<dl>
<dd>

**policies:** `[]*godonext.APIModelRouterTaskPolicy` — Router policies
    
</dd>
</dl>

<dl>
<dd>

**regions:** `[]string` — Target regions for the router
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelRouterPresets() -> *godonext.APIListModelRouterPresetsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list model router presets, send a GET request to `/v2/gen-ai/models/routers/presets`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelRouterPresetsRequest{}
client.GradientAiPlatform.GenaiListModelRouterPresets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListModelRouterTaskPresets() -> *godonext.APIListModelRouterTaskPresetsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list model router task presets, send a GET request to `/v2/gen-ai/models/routers/tasks/presets`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListModelRouterTaskPresetsRequest{}
client.GradientAiPlatform.GenaiListModelRouterTaskPresets(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetModelRouter(UUID) -> *godonext.APIGetModelRouterOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve details of a model router, send a GET request to `/v2/gen-ai/models/routers/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetModelRouterRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetModelRouter(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Model router id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateModelRouter(UUID, request) -> *godonext.APIUpdateModelRouterOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a model router, send a PUT request to `/v2/gen-ai/models/routers/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateModelRouterInputPublic{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateModelRouter(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Model router id
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Model router description
    
</dd>
</dl>

<dl>
<dd>

**fallbackModels:** `[]map[string]any` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Model router name
    
</dd>
</dl>

<dl>
<dd>

**policies:** `[]*godonext.APIModelRouterTaskPolicy` — Router policies
    
</dd>
</dl>

<dl>
<dd>

**regions:** `[]string` — Target regions for the router
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateModelRouterInputPublicUUID:** `*string` — Model router id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteModelRouter(UUID) -> *godonext.APIDeleteModelRouterOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a model router, send a DELETE request to `/v2/gen-ai/models/routers/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteModelRouterRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteModelRouter(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Model router id
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateOauth2DropboxTokens(request) -> *godonext.APIDropboxOauth2GetTokensOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To obtain the refresh token, needed for creation of data sources, send a GET request to `/v2/gen-ai/oauth2/dropbox/tokens`. Pass the code you obtrained from the oauth flow in the field 'code'
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIDropboxOauth2GetTokensInput{}
client.GradientAiPlatform.GenaiCreateOauth2DropboxTokens(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**code:** `*string` — The oauth2 code from google
    
</dd>
</dl>

<dl>
<dd>

**redirectURL:** `*string` — Redirect url
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetOauth2URL() -> *godonext.APIGenerateOauth2URLOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To generate an Oauth2-URL for use with your localhost, send a GET request to `/v2/gen-ai/oauth2/url`. Pass 'http://localhost:3000 as redirect_url
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetOauth2URLRequest{
        Type: godonext.String(
            `"example string"`,
        ),
        RedirectURL: godonext.String(
            `"example string"`,
        ),
    }
client.GradientAiPlatform.GenaiGetOauth2URL(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type_:** `*string` — Type "google" / "dropbox".
    
</dd>
</dl>

<dl>
<dd>

**redirectURL:** `*string` — The redirect url.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListOpenaiAPIKeys() -> *godonext.APIListOpenAiapiKeysOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all OpenAI API keys, send a GET request to `/v2/gen-ai/openai/keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListOpenaiAPIKeysRequest{}
client.GradientAiPlatform.GenaiListOpenaiAPIKeys(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateOpenaiAPIKey(request) -> *godonext.APICreateOpenAiapiKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create an OpenAI API key, send a POST request to `/v2/gen-ai/openai/keys`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateOpenAiapiKeyInputPublic{}
client.GradientAiPlatform.GenaiCreateOpenaiAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKey:** `*string` — OpenAI API key
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the key
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetOpenaiAPIKey(APIKeyUUID) -> *godonext.APIGetOpenAiapiKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve details of an OpenAI API key, send a GET request to `/v2/gen-ai/openai/keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetOpenaiAPIKeyRequest{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetOpenaiAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateOpenaiAPIKey(APIKeyUUID, request) -> *godonext.APIUpdateOpenAiapiKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update an OpenAI API key, send a PUT request to `/v2/gen-ai/openai/keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateOpenAiapiKeyInputPublic{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateOpenaiAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**apiKey:** `*string` — OpenAI API key
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateOpenAiapiKeyInputPublicAPIKeyUUID:** `*string` — API key ID
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the key
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteOpenaiAPIKey(APIKeyUUID) -> *godonext.APIDeleteOpenAiapiKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete an OpenAI API key, send a DELETE request to `/v2/gen-ai/openai/keys/{api_key_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteOpenaiAPIKeyRequest{
        APIKeyUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteOpenaiAPIKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**apiKeyUUID:** `string` — API key ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListAgentsByOpenaiKey(UUID) -> *godonext.APIListAgentsByOpenAiKeyOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List Agents by OpenAI Key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAgentsByOpenaiKeyRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListAgentsByOpenaiKey(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — Unique ID of OpenAI key
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListDatacenterRegions() -> *godonext.APIListRegionsOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all datacenter regions, send a GET request to `/v2/gen-ai/regions`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListDatacenterRegionsRequest{}
client.GradientAiPlatform.GenaiListDatacenterRegions(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**servesInference:** `*bool` — Include datacenters that serve inference.
    
</dd>
</dl>

<dl>
<dd>

**servesBatch:** `*bool` — Include datacenters that are capable of running batch jobs.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiCreateScheduledIndexing(request) -> *godonext.APICreateScheduledIndexingOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create scheduled indexing for a knowledge base, send a POST request to `/v2/gen-ai/scheduled-indexing`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateScheduledIndexingInputPublic{}
client.GradientAiPlatform.GenaiCreateScheduledIndexing(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**days:** `[]int` — Days for execution (day is represented same as in a cron expression, e.g. Monday begins with 1 )
    
</dd>
</dl>

<dl>
<dd>

**knowledgeBaseUUID:** `*string` — Knowledge base uuid for which the schedule is created
    
</dd>
</dl>

<dl>
<dd>

**time:** `*string` — Time of execution (HH:MM) UTC
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetScheduledIndexing(KnowledgeBaseUUID) -> *godonext.APIGetScheduledIndexingOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get Scheduled Indexing for knowledge base using knoweldge base uuid, send a GET request to `/v2/gen-ai/scheduled-indexing/knowledge-base/{knowledge_base_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetScheduledIndexingRequest{
        KnowledgeBaseUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetScheduledIndexing(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**knowledgeBaseUUID:** `string` — UUID of the scheduled indexing entry
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteScheduledIndexing(UUID) -> *godonext.APIDeleteScheduledIndexingOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete Scheduled Indexing for knowledge base, send a DELETE request to `/v2/gen-ai/scheduled-indexing/{uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteScheduledIndexingRequest{
        UUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteScheduledIndexing(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**uuid:** `string` — UUID of the scheduled indexing
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListWorkspaces() -> *godonext.APIListWorkspacesOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all workspaces, send a GET request to `/v2/gen-ai/workspaces`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.GradientAiPlatform.GenaiListWorkspaces(
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

<details><summary><code>client.GradientAiPlatform.GenaiCreateWorkspace(request) -> *godonext.APICreateWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To create a new workspace, send a POST request to `/v2/gen-ai/workspaces`. The response body contains a JSON object with the newly created workspace object.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APICreateWorkspaceInputPublic{}
client.GradientAiPlatform.GenaiCreateWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agentUUIDs:** `[]string` — Ids of the agents(s) to attach to the workspace
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — Description of the workspace
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — Name of the workspace
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiGetWorkspace(WorkspaceUUID) -> *godonext.APIGetWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To retrieve details of a workspace, GET request to `/v2/gen-ai/workspaces/{workspace_uuid}`. The response body is a JSON object containing the workspace.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiGetWorkspaceRequest{
        WorkspaceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiGetWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` — Workspace UUID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateWorkspace(WorkspaceUUID, request) -> *godonext.APIUpdateWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To update a workspace, send a PUT request to `/v2/gen-ai/workspaces/{workspace_uuid}`. The response body is a JSON object containing the workspace.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIUpdateWorkspaceInputPublic{
        WorkspaceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` — Workspace UUID.
    
</dd>
</dl>

<dl>
<dd>

**description:** `*string` — The new description of the workspace
    
</dd>
</dl>

<dl>
<dd>

**name:** `*string` — The new name of the workspace
    
</dd>
</dl>

<dl>
<dd>

**apiUpdateWorkspaceInputPublicWorkspaceUUID:** `*string` — Workspace UUID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiDeleteWorkspace(WorkspaceUUID) -> *godonext.APIDeleteWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To delete a workspace, send a DELETE request to `/v2/gen-ai/workspace/{workspace_uuid}`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiDeleteWorkspaceRequest{
        WorkspaceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiDeleteWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` — Workspace UUID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListAgentsByWorkspace(WorkspaceUUID) -> *godonext.APIListAgentsByWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all agents by a Workspace, send a GET request to `/v2/gen-ai/workspaces/{workspace_uuid}/agents`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListAgentsByWorkspaceRequest{
        WorkspaceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListAgentsByWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` — Workspace UUID.
    
</dd>
</dl>

<dl>
<dd>

**onlyDeployed:** `*bool` — Only list agents that are deployed.
    
</dd>
</dl>

<dl>
<dd>

**page:** `*int` — Page number.
    
</dd>
</dl>

<dl>
<dd>

**perPage:** `*int` — Items per page.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiUpdateAgentsWorkspace(WorkspaceUUID, request) -> *godonext.APIMoveAgentsToWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To move all listed agents a given workspace, send a PUT request to `/v2/gen-ai/workspaces/{workspace_uuid}/agents`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.APIMoveAgentsToWorkspaceInputPublic{
        WorkspaceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiUpdateAgentsWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` — Workspace uuid to move agents to
    
</dd>
</dl>

<dl>
<dd>

**agentUUIDs:** `[]string` — Agent uuids
    
</dd>
</dl>

<dl>
<dd>

**apiMoveAgentsToWorkspaceInputPublicWorkspaceUUID:** `*string` — Workspace uuid to move agents to
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.GradientAiPlatform.GenaiListEvaluationTestCasesByWorkspace(WorkspaceUUID) -> *godonext.APIListEvaluationTestCasesByWorkspaceOutput</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

To list all evaluation test cases by a workspace, send a GET request to `/v2/gen-ai/workspaces/{workspace_uuid}/evaluation_test_cases`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.GenaiListEvaluationTestCasesByWorkspaceRequest{
        WorkspaceUUID: `"123e4567-e89b-12d3-a456-426614174000"`,
    }
client.GradientAiPlatform.GenaiListEvaluationTestCasesByWorkspace(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**workspaceUUID:** `string` — Workspace UUID.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Serverless Inference
<details><summary><code>client.ServerlessInference.InferenceCreateChatCompletion(request) -> *godonext.ChatCompletionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a model response for the given chat conversation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.ChatCompletionRequest{
        Messages: []*godonext.ChatMessage{
            &godonext.ChatMessage{
                Role: godonext.ChatMessageRoleSystem,
            },
        },
        Model: "llama3-8b-instruct",
    }
client.ServerlessInference.InferenceCreateChatCompletion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `*godonext.ChatCompletionRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ServerlessInference.InferenceCreateMessages(request) -> *godonext.MessagesCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Send a structured list of input messages with text and/or image content, and the model will generate the next message in the conversation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.MessagesCreateRequest{
        Model: "claude-opus-4-6",
        MaxTokens: 1,
        Messages: []*godonext.MessagesAPIMessageParam{
            &godonext.MessagesAPIMessageParam{
                Role: godonext.MessagesAPIMessageParamRoleUser,
                Content: &godonext.MessagesAPIMessageParamContent{
                    String: "content",
                },
            },
        },
    }
client.ServerlessInference.InferenceCreateMessages(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — Model ID (for example `claude-opus-4-6` or a serverless model id).
    
</dd>
</dl>

<dl>
<dd>

**maxTokens:** `int` — Maximum tokens to generate before stopping.
    
</dd>
</dl>

<dl>
<dd>

**messages:** `[]*godonext.MessagesAPIMessageParam` — Conversation turns. Each item has `role` `user` or `assistant` and `content` as a string or an array of content blocks.
    
</dd>
</dl>

<dl>
<dd>

**system:** `*godonext.MessagesCreateRequestSystem` — System prompt as plain text or as an array of text blocks.
    
</dd>
</dl>

<dl>
<dd>

**stopSequences:** `[]string` — Custom strings that stop generation when produced.
    
</dd>
</dl>

<dl>
<dd>

**stream:** `*bool` — When true, the response is streamed using server-sent events (SSE).
    
</dd>
</dl>

<dl>
<dd>

**temperature:** `*float64` — Sampling temperature between 0.0 and 1.0.
    
</dd>
</dl>

<dl>
<dd>

**topP:** `*float64` — Nucleus sampling; use either `temperature` or `top_p`, not both.
    
</dd>
</dl>

<dl>
<dd>

**topK:** `*int` — Top-K sampling cutoff.
    
</dd>
</dl>

<dl>
<dd>

**tools:** `[]*godonext.MessagesToolDefinitionParam` — Tool definitions the model may invoke.
    
</dd>
</dl>

<dl>
<dd>

**toolChoice:** `*godonext.MessagesToolChoiceParam` 
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `*godonext.MessagesCreateRequestMetadata` — Optional request metadata.
    
</dd>
</dl>

<dl>
<dd>

**reasoningEffort:** `*godonext.MessagesCreateRequestReasoningEffort` — DigitalOcean extension for reasoning-capable models. Ignored by executors that do not support it.
    
</dd>
</dl>

<dl>
<dd>

**speed:** `*godonext.MessagesCreateRequestSpeed` — DigitalOcean extension for preferred inference speed. Ignored when not supported.
    
</dd>
</dl>

<dl>
<dd>

**thinking:** `*godonext.MessagesThinkingConfigParam` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ServerlessInference.InferenceCreateEmbedding(request) -> *godonext.EmbeddingsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create vector embeddings for one or more text inputs. OpenAI-compatible request and response. Unknown fields in the request body are rejected. There is no streaming response for this endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.EmbeddingsRequest{
        Model: "qwen3-embedding-0.6b",
        Input: &godonext.EmbeddingsRequestInput{
            String: "hello world",
        },
    }
client.ServerlessInference.InferenceCreateEmbedding(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — Model id to use for embeddings. Must match a model your account can access.
    
</dd>
</dl>

<dl>
<dd>

**input:** `*godonext.EmbeddingsRequestInput` — A single string or 1–2048 strings; each string produces one row in `data`, in order.
    
</dd>
</dl>

<dl>
<dd>

**user:** `*string` — Optional end-user identifier to help with abuse monitoring.
    
</dd>
</dl>

<dl>
<dd>

**encodingFormat:** `*godonext.EmbeddingsRequestEncodingFormat` — How embedding values are returned in each `data[].embedding` field.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ServerlessInference.InferenceCreateImage(request) -> *godonext.ImagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a high-quality image from a text prompt using GPT-IMAGE-1, the latest image generation model with automatic prompt optimization and enhanced visual capabilities.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CreateImageRequest{
        Prompt: "A cute baby sea otter floating on its back in calm blue water",
        Model: "openai-gpt-image-1",
        N: 1,
    }
client.ServerlessInference.InferenceCreateImage(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**prompt:** `string` — A text description of the desired image(s). Supports up to 32,000 characters and provides automatic prompt optimization for best results.
    
</dd>
</dl>

<dl>
<dd>

**model:** `string` — The model to use for image generation.
    
</dd>
</dl>

<dl>
<dd>

**moderation:** `*string` — The moderation setting for the image generation. Supported values: low, auto.
    
</dd>
</dl>

<dl>
<dd>

**background:** `*string` — The background setting for the image generation. Supported values: transparent, opaque, auto.
    
</dd>
</dl>

<dl>
<dd>

**outputFormat:** `*string` — The output format for the image generation. Supported values: png, webp, jpeg.
    
</dd>
</dl>

<dl>
<dd>

**outputCompression:** `*int` — The output compression level for the image generation (0-100).
    
</dd>
</dl>

<dl>
<dd>

**n:** `int` — The number of images to generate. Must be between 1 and 10.
    
</dd>
</dl>

<dl>
<dd>

**quality:** `*string` — The quality of the image that will be generated. Supported values: auto, high, medium, low.
    
</dd>
</dl>

<dl>
<dd>

**size:** `*godonext.CreateImageRequestSize` — The size of the generated images. GPT-IMAGE-1 supports: auto (automatically select best size), 1536x1024 (landscape), 1024x1536 (portrait).
    
</dd>
</dl>

<dl>
<dd>

**stream:** `*bool` — If set to true, partial image data will be streamed as the image is being generated. The response will be sent as server-sent events with partial image chunks. When stream is true, partial_images must be greater than 0.
    
</dd>
</dl>

<dl>
<dd>

**partialImages:** `*int` — The number of partial image chunks to return during streaming generation. Defaults to 0. When stream=true, this must be greater than 0 to receive progressive updates of the image as it is being generated.
    
</dd>
</dl>

<dl>
<dd>

**user:** `*string` — A unique identifier representing your end-user, which can help DigitalOcean to monitor and detect abuse.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ServerlessInference.InferenceListModels() -> *godonext.ListModelsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists the currently available models, and provides basic information about each one such as the owner and availability.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.ServerlessInference.InferenceListModels(
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

<details><summary><code>client.ServerlessInference.InferenceCreateResponse(request) -> *godonext.CreateResponseResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate text responses from text prompts. This endpoint supports both streaming and non-streaming responses for supported text models.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.CreateResponseRequest{
        Model: "openai-gpt-oss-20b",
        Input: &godonext.CreateResponseRequestInput{
            String: "What is the capital of France?",
        },
    }
client.ServerlessInference.InferenceCreateResponse(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**model:** `string` — The model ID of the model you want to use. Get the model ID using `/v1/models` or on the available models page.
    
</dd>
</dl>

<dl>
<dd>

**input:** `*godonext.CreateResponseRequestInput` — The prompt or input content you want the model to respond to. Can be a simple text string or an array of message objects for conversation context.
    
</dd>
</dl>

<dl>
<dd>

**maxOutputTokens:** `*int` — The maximum number of tokens to generate in the response.
    
</dd>
</dl>

<dl>
<dd>

**temperature:** `*float64` — A value between 0.0 and 2.0 to control randomness and creativity. Lower values like 0.2 make the output more focused and deterministic, while higher values like 0.8 make it more random.
    
</dd>
</dl>

<dl>
<dd>

**stream:** `*bool` — Set to true to stream partial responses as Server-Sent Events.
    
</dd>
</dl>

<dl>
<dd>

**instructions:** `*string` — System-level instructions for the model. This sets the behavior and context for the response generation.
    
</dd>
</dl>

<dl>
<dd>

**topP:** `*float64` — An alternative to sampling with temperature, called nucleus sampling, where the model considers the results of the tokens with top_p probability mass.
    
</dd>
</dl>

<dl>
<dd>

**streamOptions:** `*godonext.CreateResponseRequestStreamOptions` — Options for streaming response. Only set this when you set stream to true.
    
</dd>
</dl>

<dl>
<dd>

**tools:** `[]*godonext.CreateResponseRequestToolsItem` — A list of tools the model may call.
    
</dd>
</dl>

<dl>
<dd>

**toolChoice:** `*godonext.CreateResponseRequestToolChoice` — Controls which (if any) tool is called by the model.
    
</dd>
</dl>

<dl>
<dd>

**stop:** `*godonext.CreateResponseRequestStop` — Up to 4 sequences where the API will stop generating further tokens.
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `map[string]*string` — Set of key-value pairs that can be attached to the request.
    
</dd>
</dl>

<dl>
<dd>

**user:** `*string` — A unique identifier representing your end-user.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ServerlessInference.InferenceCreateAsyncInvoke(request) -> *godonext.AsyncInvokeResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate Image, Audio, or Text-to-Speech Using fal Models. This endpoint starts an asynchronous job and returns a request_id. The job status is QUEUED initially. Use the request_id to poll for the result.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AsyncInvokeRequest{
        ModelID: "fal-ai/flux/schnell",
        Input: &godonext.AsyncInvokeRequestInput{
            Prompt: godonext.String(
                "A futuristic city at sunset",
            ),
        },
    }
client.ServerlessInference.InferenceCreateAsyncInvoke(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**modelID:** `string` — The ID of the model to invoke asynchronously.
    
</dd>
</dl>

<dl>
<dd>

**input:** `*godonext.AsyncInvokeRequestInput` 

The input parameters for the model invocation. Fields vary by model type.

For **image generation** models (e.g., `fal-ai/flux/schnell`, `fal-ai/fast-sdxl`), use `prompt` along with optional image parameters like `output_format`, `num_inference_steps`, `guidance_scale`, `num_images`, and `enable_safety_checker`.

For **audio generation** models (e.g., `fal-ai/stable-audio-25/text-to-audio`), use `prompt` along with `seconds_total` to control the duration.

For **text-to-speech** models (e.g., `fal-ai/elevenlabs/tts/multilingual-v2`), use `text` with the content you want converted to speech.
    
</dd>
</dl>

<dl>
<dd>

**tags:** `[]*godonext.AsyncInvokeRequestTagsItem` — An optional list of key-value tags to attach to the invocation request for tracking or categorization.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Agent Inference
<details><summary><code>client.AgentInference.AgentInferenceCreateChatCompletion(request) -> *godonext.ChatCompletionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a model response for the given chat conversation via a customer-provisioned
agent endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.AgentInferenceCreateChatCompletionRequest{
        Agent: true,
        Body: &godonext.ChatCompletionRequest{
            Messages: []*godonext.ChatMessage{
                &godonext.ChatMessage{
                    Role: godonext.ChatMessageRoleSystem,
                },
            },
            Model: "llama3-8b-instruct",
        },
    }
client.AgentInference.AgentInferenceCreateChatCompletion(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**agent:** `bool` — Must be set to true for agent-based completion behavior.
    
</dd>
</dl>

<dl>
<dd>

**request:** `*godonext.ChatCompletionRequest` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Batch Inference
<details><summary><code>client.BatchInference.InferenceCreateBatchFile(request) -> *godonext.BatchFileCreateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a file record and returns a `file_id` plus a short-lived presigned `PUT` URL (typically valid for ~15 minutes). Upload the raw JSONL bytes to `upload_url` (see `PUT /{upload_path}`) before calling `POST /v1/batches`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.BatchFileCreateRequest{
        FileName: "batch_requests.jsonl",
    }
client.BatchInference.InferenceCreateBatchFile(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fileName:** `string` — The file you plan to upload. Must end with `.jsonl` (case-insensitive) and contain one request per line in the schema expected by the target `provider`.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BatchInference.InferenceUploadBatchFile(request) -> error</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Uploads the raw JSONL bytes to the presigned `upload_url` returned by `POST /v1/batches/files`.

**The URL is dynamic — do not construct it.** Use the `upload_url` value from the previous step verbatim. Its host, path, and query parameters are part of the short-lived (~15 minute) signature and change per request; the server and path shown here are illustrative. If the URL expires before the upload completes, create a new file intent and retry.

`POST /v1/batches` performs a `HEAD` check on the uploaded object and will reject the batch if this upload has not completed.

Send the raw JSONL bytes verbatim. Presigned PUT URLs are signature-sensitive to request headers — prefer `application/octet-stream` or omit `Content-Type` entirely. A custom value (for example `application/jsonl`) can cause signature mismatches unless the URL was signed for that exact header.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
client.BatchInference.InferenceUploadBatchFile(
        context.TODO(),
        request,
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

<details><summary><code>client.BatchInference.InferenceListBatches() -> *godonext.BatchListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a cursor-paginated list of batch jobs, ordered newest first. Use `limit` to control page size and `after` to page forward using the `last_id` from the previous response.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InferenceListBatchesRequest{
        After: godonext.String(
            "7b2e9c1a-6f4d-4d9b-a0f1-5c4b7e2f8a12",
        ),
    }
client.BatchInference.InferenceListBatches(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**after:** `*string` — Cursor for pagination. Pass the `last_id` value from the previous response to fetch the next page. Omit for the first page.
    
</dd>
</dl>

<dl>
<dd>

**limit:** `*int` — Maximum number of batches to return per page.
    
</dd>
</dl>

<dl>
<dd>

**status:** `*godonext.InferenceListBatchesRequestStatus` — Optional filter restricting results to batches in the given lifecycle state.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BatchInference.InferenceCreateBatch(request) -> *godonext.Batch</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Submits a batch job against a previously uploaded JSONL input file. The upload must have completed before this call; otherwise the request is rejected.

Supply a unique `request_id` to make the submission idempotent — retries with the same value return the existing job. When `provider` is `openai`, the `url` on each JSONL line must match `endpoint`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.BatchCreateRequest{
        FileID: "a1b2c3d4-e5f6-4789-90ab-cdef12345678",
        Provider: godonext.BatchCreateRequestProviderOpenai,
        Endpoint: godonext.BatchCreateRequestEndpointV1ChatCompletions.Ptr(),
        CompletionWindow: godonext.BatchCreateRequestCompletionWindowTwentyFourH,
        RequestID: "c7e3ad1e-20c3-4e47-9bf2-6f2a4d6a2f11",
    }
client.BatchInference.InferenceCreateBatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**fileID:** `string` — The `file_id` returned by `POST /v1/batches/files`.
    
</dd>
</dl>

<dl>
<dd>

**provider:** `*godonext.BatchCreateRequestProvider` — The inference provider whose JSONL schema the input file conforms to. `openai` follows the OpenAI Batch API input schema (`custom_id`, `method`, `url`, `body`); `anthropic` follows the Anthropic Message Batches JSONL conventions.
    
</dd>
</dl>

<dl>
<dd>

**endpoint:** `*godonext.BatchCreateRequestEndpoint` — Inference endpoint each request is dispatched to. **Required when `provider` is `openai` and must match the `url` on every JSONL line. Must be omitted when `provider` is `anthropic`.**
    
</dd>
</dl>

<dl>
<dd>

**completionWindow:** `*godonext.BatchCreateRequestCompletionWindow` — Time window in which the job must complete. Jobs that do not finish in time transition to `expired`.
    
</dd>
</dl>

<dl>
<dd>

**requestID:** `string` — Client-supplied idempotency key. Retries with the same value return the existing job instead of creating a duplicate.
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `map[string]*string` — Optional string-valued metadata to attach to the job.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BatchInference.InferenceGetBatch(BatchID) -> *godonext.Batch</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the current state of a batch job. Poll until `status` reaches a terminal value (`completed`, `failed`, `expired`, or `cancelled`).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InferenceGetBatchRequest{
        BatchID: "0e9d1d35-3d1e-4d66-9a2f-8c7e0f6b3e21",
    }
client.BatchInference.InferenceGetBatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchID:** `string` — The batch job identifier.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BatchInference.InferenceGetBatchResults(BatchID) -> *godonext.BatchResultsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns short-lived presigned download URLs for the output (and optional error sidecar) of a completed batch job. If results are not yet ready, the response sets `result_available: false` or returns `412 Precondition Failed`; in both cases, keep polling batch status and retry.

Download the artifacts soon after fetching — the URLs are short-lived. Result files themselves are retained for up to 30 days after the job completes, after which they are deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InferenceGetBatchResultsRequest{
        BatchID: "0e9d1d35-3d1e-4d66-9a2f-8c7e0f6b3e21",
    }
client.BatchInference.InferenceGetBatchResults(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchID:** `string` — The batch job identifier.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.BatchInference.InferenceCancelBatch(BatchID) -> *godonext.Batch</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Requests cancellation of a batch job. The job transitions to `cancelling` and, once in-flight requests drain, to `cancelled`. Jobs already in a terminal state (`completed`, `failed`, `expired`, `cancelled`) cannot be cancelled and return `409 Conflict`. Cancellation is also rejected with `409 Conflict` while the job has not yet been submitted to the upstream provider — there is nothing to cancel until the provider batch id is assigned.

Partial results produced before cancellation remain available via `GET /v1/batches/{batch_id}/results`.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```go
request := &godonext.InferenceCancelBatchRequest{
        BatchID: "0e9d1d35-3d1e-4d66-9a2f-8c7e0f6b3e21",
    }
client.BatchInference.InferenceCancelBatch(
        context.TODO(),
        request,
    )
}
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**batchID:** `string` — The batch job identifier.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

