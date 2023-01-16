# Zabbix and Grafana with Docker

[Zabbix](https://www.zabbix.com/) and [Grafana](https://grafana.com/) with [Docker](https://www.docker.com/) for tests.

## Requirements

- Docker installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed

## Configuring environment variables

Create `.env` file:

```
cp .env.example .env
```

## Running

```
docker-compose up -d
```

| Service | Port | Address | User | Password |
|---      |---   | ---     | ---  | ---            |
| Grafana | 3000 | http://localhost:3000 | `admin` | `admin` (1) |
| MySQL Server | 3306 | - | `root` | (2) |
| Zabbix Agent | - | - | - | - |
| Zabbix Server | 10051 | - | - | - | - |
| Zabbix Web Interface | 8080 | http://localhost:8080 | `Admin` | `zabbix` (1) |

1. Default password. 
2. Value setting in `.env` file.

## References

- https://hub.docker.com/_/mysql
- https://hub.docker.com/r/grafana/grafana
- https://hub.docker.com/r/zabbix/zabbix-agent
- https://hub.docker.com/r/zabbix/zabbix-server-mysql/
- https://hub.docker.com/r/zabbix/zabbix-web-nginx-mysql
- https://www.zabbix.com/documentation/6.2/en/manual/appendix/install/db_scripts#mysql
- https://github.com/zabbix/zabbix-docker/issues/999
