
Local

```bash
dds-server start -s

dds-submit --rms localhost -n 6

dds-topology --activate tutorial1_topo.xml
```

Cloud

```bash
dds-server start -s

dds-submit --rms ssh --config tutorial1_hosts_cloud.cfg

dds-topology --activate tutorial1_topo.xml
```

