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
