Interactive (in three shells)

```bash
ex3-sampler --id sampler --log-color false --mq-config ex3-dds-nodds.json
ex3-processor --id processor --config-key processor --log-color false --mq-config ex3-dds-nodds.json
ex3-sink --id sink --log-color false --mq-config ex3-dds-nodds.json
```

Local

```bash
dds-server start -s
dds-submit --rms localhost --config ex3-dds-hosts.cfg
dds-topology --activate ex3-dds-topology-local.xml
dds-agent-cmd getlog  (in ~/.DDS/log/agents/)
dds-topology --stop
```

Cloud

```bash
dds-server start -s
dds-submit --rms ssh --config ex3-dds-hosts-cloud.cfg
dds-topology --activate ex3-dds-topology.xml
```

