Vector
=========

This role install vector.

## Requirements
-------

- Ansible >= 2.10
- Target host: Ubuntu 22.04 / 24.04
- Root/sudo access


## Role Variables
-------

| Variable | Default | Description |
|----------|---------|-------------|
| `vector_version` | `"0.35.1"` | Version of Vector to install |


## Dependencies
-------

None.


### Example `vector_config` structure:
-------

```yaml
vector_config:
  sources:
    dummy_logs:
      type: demo_logs
      format: syslog
  sinks:
    to_clickhouse:
      type: clickhouse
      endpoint: "http://127.0.0.1:8123"
      database: logs
      table: dummy_logs
```

## License
-------

MIT

## Author Information
------------------

Viktor M.
