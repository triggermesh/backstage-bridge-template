## ${{ values.name }}

${{ values.description }}

This integration reads messages on an AWS Simple Queue Service (SQS) queue and
forwards these messages as cloudevents to a Tranformation object for processing.
The Transformed message is then delivered to the specified service.

### Manifests

The `manifests/` directory of the reposotory consists of the kubernetes YAML 
manifests which are rendered and deployed to the cluster using the `kapp` tool 
by the Github Actions CI/CD workflows.

```console
manifests
├── broker.yaml
├── service-trigger.yaml
├── service.yaml
├── sqssecret.yaml
├── sqssource.yaml
├── transformation-trigger.yaml
└── transformation.yaml
```

### Metrics

The `metrics/` directory contains some sample dashboards that can be imported 
into your Grafana instance to visualize the metrics of the components used in
this integration.

```console
metrics
└── dashboards
    ├── ${{ values.name }}-broker.json
    └── ${{ values.name }}-sqs.json
```

### Docs

The `docs/` directory contains the documentation for the integration. 
