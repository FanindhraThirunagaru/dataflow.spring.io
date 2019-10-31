---
path: 'concepts/monitoring/'
title: 'Monitoring'
description: 'Runtime monitoring of Stream data pipelines'
---

# Monitoring

The Data Flow metrics architecture is designed around the Micrometer library, which is a vendor-neutral application metrics facade.
It provides a simple facade over the instrumentation clients for the most popular monitoring systems.
The Micrometer instrumentation library powers the delivery of application metrics from Spring Boot and includes metrics for message rates and errors, which is critical to the monitoring of deployed streams.

The prebuilt applications are configured to support two of the most popular monitoring systems, Prometheus and InfluxDB. You can declaratively select which monitoring system to use.

To help you get started monitoring Streams, Data Flow provides Grafana Dashboards that you can customize for your needs.

The following image shows the general architecture of how the Stream applications are monitored:

![Data Flow Stream Monitoring Architecture](images/SCDF-stream-metrics-architecture.png)

The following image shows the creation of two streams defined with the `time | filter | log` DSL expression:

![Two stream definitions](images/monitoring-stream-defs.png)

The following image shows the Stream applications view in the Grafana dashboard:

![Grafana Streams Dashboard](images/grafana-dashboard.png)

The [Stream Monitoring Feature Guide](%currentPath%/feature-guides/streams/monitoring/) contains detailed information on how to set up the monitoring infrastructure.
