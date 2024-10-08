# provider-litellm

`provider-litellm` is a Crossplane Provider designed to facilitate sending HTTP requests as resources.

## Installation

To install `provider-litellm`, you have two options:

1. Using the Crossplane CLI in a Kubernetes cluster where Crossplane is installed:

   ```console
   crossplane xpkg install provider xpkg.upbound.io/crossplane-contrib/provider-litellm:v1.0.4
   ```

2. Manually creating a Provider by applying the following YAML:

   ```yaml
   apiVersion: pkg.crossplane.io/v1
   kind: Provider
   metadata:
     name: provider-litellm
   spec:
     package: "xpkg.upbound.io/crossplane-contrib/provider-litellm:v1.0.4"
   ```

## Supported Resources

`provider-litellm` supports the following resources:

- **Request:** Manages a resource through HTTP requests. See [Request CRD documentation](resources-docs/request_docs.md).

## Usage

### Request

Manage a resource through HTTP requests with a `Request` resource:

```yaml
apiVersion: litellm.nwse.io/v1alpha2
kind: Request
metadata:
  name: example-request
spec:
  # Add your Request specification here
```

For more detailed examples and configuration options, refer to the [examples directory](examples/sample/).

## Developing locally

Run controller against the cluster:

```
make run
```

## Troubleshooting

If you encounter any issues during installation or usage, refer to the [troubleshooting guide](https://docs.crossplane.io/knowledge-base/guides/troubleshoot/) for common problems and solutions.
