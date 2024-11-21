# OpenMetrics compliance tester

While [OpenMetrics](https://openmetrics.io/) is an independent CNCF project, Prometheus designated it as the [official specification](https://github.com/OpenObservability/OpenMetrics/blob/main/specification/OpenMetrics.md) for Prometheus exposition. OpenMetrics is, and will remain, closely aligned to Prometheus.

The test suite can be found on [GitHub](https://github.com/OpenObservability/OpenMetrics/tree/main/src/cmd/openmetricstest). 

Depending on your implementation, the following might be of interest:
- [Scrape validator tool](https://github.com/OpenObservability/OpenMetrics/tree/main/src/cmd/scrapevalidator) to scrape an OpenMetrics HTTP endpoint and validate the exposition against the OpenMetrics specification.
- [Individual test cases](https://github.com/OpenObservability/OpenMetrics/tree/main/tests/testdata/parsers) to understand valid and invalid OpenMetric expositions.

Prometheus considers OpenMetrics compliance part of Prometheus compliance and compatibility.
