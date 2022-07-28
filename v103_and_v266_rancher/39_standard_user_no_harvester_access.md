# Test Run: 07/26/22
# Test Result: PASS
# Test-Case: https://harvester.github.io/tests/manual/harvester-rancher/39-rbac-standard-user-no-access/

# Notes:
- verified User1/user1 based Standard User is unable to see virtualization, cloud credentials, etc.
- verified User1/user1 is able to see the cluster they are a cluster member of

![ex](./imgs/39-admin-sees-but-user1-doesnt.png)
![ex-2](./imgs/39-admin-sees-virtualization-but-user1-doesnt.png)
![ex-3](./imgs/39-standard-user-creation.png)
![ex-4](./imgs/39-can-interact-with-cluster-if-given-permission.png)