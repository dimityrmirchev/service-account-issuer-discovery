# Service Account Issuer Discovery

[![reuse compliant](https://reuse.software/badge/reuse-compliant.svg)](https://reuse.software/)

A simple server that allows exposing the OpenID discovery documents of a Kubernetes cluster.

Work in progress... Partial documentation ahead.

### Quick start

To run the server with minimal configuration export the `KUBECONFIG` environment variable and run:
``` 
go run main.go --hostname=<issuer-of-cluster>
```
Or pass the `kubeconfig` as a flag:
``` 
go run main.go --kubeconfig=<path-to-my-kubeconfig> --hostname=<issuer-of-cluster>
```

Retrieve the `well-known` document by querying `/.well-known/openid-configuration`.
