## learn-volume-operators

Opearor using Kubebuilder: volume
### Steps
- Init folder 
```
kubebuilder init --domain volumes.nj.io --repo k9s-operator-demo-volume
```
- Create new api DemoVolume
```
kubebuilder create api  --group demo --version v1 --kind DemoVolume
```

- Update `api/v1/<operator-name>_types.go` file and generate manifests
```
make generate
make manifests
```

- install crd in cluster
> Note: Make sure the cluster is connected
```
make install
make run
# Try to apply the manifest
kubectl apply -f config/samples/demo_v1_demovolume.yaml
```
- update the reconciler logic and run
```
make run
```
### References: 
- [Dinesh Majrekar Session on Kubernetes Operator](https://www.youtube.com/watch?v=LLVoyXjYlYM)