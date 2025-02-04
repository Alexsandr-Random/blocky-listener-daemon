# Blocky Listener Daemon

Based on [Blocky](https://github.com/0xERR0R/blocky). Blocky is a DNS proxy and ad-blocker for the local network written in Go with following features

## Features

- **Blocking** - Blocking of DNS queries with external lists (Ad-block, malware) and whitelisting

    * Definition of black and white lists per client group (Kids, Smart home devices, etc.)
    * Periodical reload of external black and white lists
    * Blocking of request domain, response CNAME (deep CNAME inspection) and response IP addresses (against IP lists)

- **Advanced DNS configuration** - not just an ad-blocker

    * Custom DNS resolution for certain domain names
    * Conditional forwarding to external DNS server
    * Upstream resolvers can be defined per client group

- **Performance** - Improves speed and performance in your network

    * Customizable caching of DNS answers for queries -> improves DNS resolution speed and reduces amount of external DNS
    queries
    * Prefetching and caching of often used queries
    * Using multiple external resolver simultaneously
    * Low memory footprint

- **Various Protocols** - Supports modern DNS protocols

    * DNS over UDP and TCP
    * DNS over HTTPS (aka DoH)
    * DNS over TLS (aka DoT)

- **Security and Privacy** - Secure communication

    * Supports modern DNS extensions: DNSSEC, eDNS, ...
    * Free configurable blocking lists - no hidden filtering etc.
    * Provides DoH Endpoint
    * Uses random upstream resolvers from the configuration - increases you privacy though the distribution of your DNS
    traffic over multiple provider
    * Blocky does **NOT** collect any user data, telemetry, statistics etc.

- **Integration** - various integration

    * [Prometheus](https://prometheus.io/) metrics
    * Prepared [Grafana](https://grafana.com/) dashboard
    * Logging of DNS queries per day / per client in CSV format - easy to analyze
    * Statistics report via CLI
    * Various REST API endpoints
    * CLI tool

- **Simple configuration** - single configuration file in YAML format

    * Simple to maintain
    * Simple to backup

- **Simple installation/configuration** - blocky was designed for simple installation

    * Stateless (no database, no temporary files)
    * Docker image with Multi-arch support
    * Single binary
    * Supports x86-64 and ARM architectures -> runs fine on Raspberry PI
    * Community supported Helm chart for k8s deployment

## Quick start

You can jump to [Installation](https://0xerr0r.github.io/blocky/installation/) chapter in the documentation.

## Full documentation

You can find full documentation and configuration examples
at: [https://0xERR0R.github.io/blocky/](https://0xERR0R.github.io/blocky/)

## Contribution

Issues, feature suggestions and pull requests are welcome!

## Additional links

* https://github.com/m0zgen/blocky-installer.git
* https://github.com/m0zgen/prometheus-stack-installer.git
* https://github.com/m0zgen/dns-hole.git
* https://github.com/m0zgen/dns-tester.git
