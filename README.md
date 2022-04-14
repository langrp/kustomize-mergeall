# kustomize-mergeall
Example for Kustomize feature mergeall.

Apply using
```shell
kubectl apply -k overlay/dev
```

Deploys example application roles with different configMap on each level:
1. Environment overlay level - example uses dev environment, that configures environment name
2. Cluster level - configures common cluster connections. This level should override properties
   from environment level
3. Role level - defines common properties for given role. Any property defined here should override
   properties from above levels
4. Base level - defines base role properties