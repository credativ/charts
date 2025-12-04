# credativ Charts

A collection of Helm charts that we use ourselves or at our customers' sites.

## Usage

We provide the charts as OCI artifacts on GitHub Container Registry. To install or pull a chart:

```bash
helm pull oci://ghcr.io/credativ/charts/<chart-name>
helm install my-release oci://ghcr.io/credativ/charts/<chart-name>
```

Please have a look into the chart specific READMEs.

## Development

* Use EditorConfig
* Use `pre-commit`
* Use Conventional Commits

## Copyright

All product names, logos, and brands are property of their respective owners.

* [GitHub](https://www.github.com) is a trademark of GitHub, Inc.
* [Helm](https://helm.sh) is a trademark of [The Linux Foundation](https://www.linuxfoundation.org).
* [Seatsurfing](https://seatsurfing.io) is a trademark of Seatsurfing GmbH.
