# Chart for turborepo-remote-cache

This project is an open-source implementation of the Turborepo custom remote cache server. If Vercel’s official cache server isn’t a viable option, this server is an alternative for self-hosted deployments. It supports several storage providers and deploys environments. Moreover, the project provides “deploy to “ buttons for one-click deployments whenever possible.

## Installation

To install the chart with the release name `my-release`:

```bash
$ helm install --name my-release .
```

## Configuration
The following table lists the configurable parameters of the chart and their default values.

| Parameter	| Description |	Default |
| ----------- | ----------- | ----------- |
| image.repository	| The image repository	myregistry/| mychart
| image.tag	| The image tag	| latest
| image.pullPolicy |The image pull policy |	IfNotPresent
| service.type |	The type of service to create	| ClusterIP
| service.port|	The port to expose|	80
| replicaCount	|The number of replicas|	1
| ingress.enabled|	Enable ingress	|false
| ingress.annotations|	ingress annotations|	{}
| ingress.path|	ingress path	|/
| ingress.hosts|	ingress hosts|	[]
| ingress.tls|	ingress tls|	[]
Specify each parameter using the --set key=value[,key=value] argument to helm install.

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart. For example,

```
$ helm install --name my-release -f values.yaml .
```
Tip: You can use the default values.yaml

## Values overwriting priority
```
command line options
--values options
--set-file options
values.yaml in chart
default values
```
It's a basic template you can start with and edit according to your use case. Also, it gives an idea on how to use `values.yaml`, `--set`,`--set-file` to customize the chart.

Please let me know if you want further customizations or if you have any question about above example.
