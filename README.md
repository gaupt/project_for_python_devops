# project_for_python_devops
## Start the stack:

```bash
docker-compose up -d
```
## Access Prometheus:

Open your browser and go to http://localhost:9090.
Verify that cadvisor is listed as a scrape target at Status > Targets.

## Access Grafana:

Open your browser and go to http://localhost:3000.
Log in with admin / admin (or the credentials you specified).
Add Prometheus as a data source:
Go to Configuration > Data Sources.
Click Add Data Source, select Prometheus, and set the URL to http://prometheus:9090.

## Import Docker Monitoring Dashboard:

Go to + > Import in Grafana.
Use the dashboard ID 893 (or any other Docker monitoring dashboard) and click Load.
Select your Prometheus data source and import the dashboard.

## Verify Monitoring:

View metrics like CPU, memory, disk usage, and network traffic for your Docker containers.