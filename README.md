# CoreOS Graphite

Set of unit files for running [docker-graphite](https://github.com/ejholmes/docker-graphite), [docker-carbon](https://github.com/ejholmes/docker-carbon), and [docker-statsd](https://github.com/ejholmes/docker-statsd).

## Usage

Assuming you have a CoreOS cluster running and you've set the `FLEETCTL_TUNNEL` environment variable:

```bash
$ fleetctl submit units/*.service
$ fleetctl start units/*.service
```

Once the docker images are pulled, and started, you should have a full functioning Graphite + StatsD
service running on CoreOS.
