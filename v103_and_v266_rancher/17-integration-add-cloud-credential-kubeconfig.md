## Test Case: Create Cloud Credential With External Harvester's Kubeconfig
## Test Date: 07/28/22
### Result: FAIL

## Notes:
- failure to fetch resource id when trying to create a cluster using the external harvester kubeconfig 
```
GET /v3/cloudcredentials/[object%20Object] HTTP/2
Host: k3scluster.localdomain
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:101.0) Gecko/20100101 Firefox/101.0
Accept: application/json
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
x-api-csrf: af309f726d
Connection: keep-alive
Referer: https://k3scluster.localdomain/dashboard/c/c-m-n59bx9p6/manager/provisioning.cattle.io.cluster/create?type=harvester
Cookie: R_PCS=light; R_LOCALE=en-us; R_REDIRECTED=true; CSRF=af309f726d; R_SESS=token-kvnvh:kbnzh75bkld2b6xrlpg2m6ztv6thldw2966zknt72prtrn64cdl2r4
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
TE: trailers

### RESPONSE ####
{"baseType":"error","code":"NotFound","message":"failed to find resource by id","status":404,"type":"error"}
```

Questions:
- should it be able to auto-complete images?

Cycle:
-  Creating server [fleet-default/test-rke2-pool1-799222e1-2fgsl] of kind (HarvesterMachine) for machine test-rke2-pool1-76d4c44598-4pf4g in infrastructure provider 
-  Deleting server [fleet-default/test-rke2-pool1-799222e1-2fgsl] of kind (HarvesterMachine) for machine test-rke2-pool1-76d4c44598-4pf4g in infrastructure provider 
-  Creating server [fleet-default/test-rke2-pool1-799222e1-5nwzr] of kind (HarvesterMachine) for machine test-rke2-pool1-76d4c44598-48njq in infrastructure provider 
-  Deleting server [fleet-default/test-rke2-pool1-799222e1-5nwzr] of kind (HarvesterMachine) for machine test-rke2-pool1-76d4c44598-48njq in infrastructure provider 
-  Creating server [fleet-default/test-rke2-pool1-799222e1-64hhh] of kind (HarvesterMachine) for machine test-rke2-pool1-76d4c44598-gg67w in infrastructure provider 


```
┌─────────────────────────────────────────────────────────────────────────────────────────── Logs(fleet-default/test-rke2-pool1-799222e1-z98cb-machine-provision)[1m] ───────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                                Autoscroll:On     FullScreen:Off     Timestamps:Off     Wrap:Off                                                                                                │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg Downloading driver from https://k3scluster.localdomain/assets/docker-machine-driver-harvester                                                                                                           │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg Doing /etc/rancher/ssl                                                                                                                                                                                  │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg docker-machine-driver-harvester                                                                                                                                                                         │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg docker-machine-driver-harvester: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), statically linked, stripped                                                                                       │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg Trying to access option  which does not exist                                                                                                                                                           │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg THIS ***WILL*** CAUSE UNEXPECTED BEHAVIOR                                                                                                                                                               │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg Type assertion did not go smoothly to string for key                                                                                                                                                    │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg Running pre-create checks...                                                                                                                                                                            │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg Error with pre-create check: "invalid configuration: no configuration has been provided, try setting KUBERNETES_MASTER environment variable"                                                            │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg The default lines below are for a sh/bash shell, you can specify the shell you're using, with the --shell flag.                                                                                         │
│ test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg                                                                                                                                                                                                         │
│ Stream closed EOF for fleet-default/test-rke2-pool1-799222e1-z98cb-machine-provision-72lqg (machine)                                                                                                                                                           │
│                                                                                                             
```

```
 Failed creating server [fleet-default/test-rke2-pool1-799222e1-4vtnz] of kind (HarvesterMachine) for machine test-rke2-pool1-76d4c44598-btzfj in infrastructure provider: CreateError: Downloading driver from https://k3scluster.localdomain/assets/docker-machine-driver-harvester Doing /etc/rancher/ssl docker-machine-driver-harvester docker-machine-driver-harvester: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), statically linked, stripped Trying to access option which does not exist THIS ***WILL*** CAUSE UNEXPECTED BEHAVIOR Type assertion did not go smoothly to string for key Running pre-create checks... Error with pre-create check: "invalid configuration: no configuration has been provided, try setting KUBERNETES_MASTER environment variable" The default lines below are for a sh/bash shell, you can specify the shell you're using, with the --shell flag. 
 ```