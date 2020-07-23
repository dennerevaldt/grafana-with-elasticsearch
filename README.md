## Grafana with Elasticsearch

## Instructions

### Step one
- docker-compose up

### Step two
- npm install
- npm run makelogs (Populate elasticsearch, index 'logstash-*', with fake data logs)

### Step three
Configuring Grafana:

- Access http://localhost:3000
- Login with user and pwd 'admin'
- Access the menu: Configuration -> Data sources
- Go to Add data source and Select Elasticsearch
- Configs:

HTTP:
- Url: http://es01:9200
- Access: Server

Elasticsearch details:
- Index name: logstash-*
- Pattern: No pattern
- Time field name: @timestamp
- Version: 7.0+

6 - Press Save & Test

7 - Now we are ready to create dashboards
