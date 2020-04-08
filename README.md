# Blazemeter Service for Keptn
This is a Sandbox Keptn Service integrates [Blazemeter](https://www.blazemeter.com/) by invoking tests and reporting test result

**ATTENTION: THIS REPO IS CURRENTLY UNDER DEVELOPMENT. Expecting a first version soon!**

## Compatibility Matrix

| Keptn Version    | [Blazemeter Service for Keptn] |
|:----------------:|:----------------------------------------:|
|       0.6.1      | TBD/blazemeter-service:0.1.0 |

## Installation

The *blazemeter-service* can be installed as a part of [Keptn's uniform](https://keptn.sh).

### Deploy in your Kubernetes cluster

To deploy the current version of the *blazemeter-service* in your Keptn Kubernetes cluster, apply the [`deploy/service.yaml`](deploy/service.yaml) file:

```console
kubectl apply -f deploy/service.yaml
```

This should install the `blazemeter-service` together with a Keptn `distributor` into the `keptn` namespace, which you can verify using

```console
kubectl -n keptn get deployment blazemeter-service -o wide
kubectl -n keptn get pods -l run=blazemeter-service
```

### Up- or Downgrading

Adapt and use the following command in case you want to up- or downgrade your installed version (specified by the `$VERSION` placeholder):

```console
kubectl -n keptn set image deployment/blazemeter-service blazemeter-service=your-username/blazemeter-service:$VERSION --record
```

### Uninstall

To delete a deployed *blazemeter-service*, use the file `deploy/*.yaml` files from this repository and delete the Kubernetes resources:

```console
kubectl delete -f deploy/service.yaml
```

## Usage


## License

Please find more information in the [LICENSE](LICENSE) file.