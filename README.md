# elasticsearch-kibana

This is a simple project for running both elastic search, influxdb, and kibana/grafana in a docker container.

```
docker-compose up -d
```

###Change Docker Machine Max Memory (Github)
```bash
sudo sysctl -w vm.max_map_count=262144
```

##InfluxDB
```
curl -G 'http://192.168.99.100:8086/query?db=NOAA_water_database&pretty=true'
    --data-urlencode 'q=SELECT mean(water_level) FROM "h2o_feet" group by location'
```

##Log Stash
cat nyc_collision_data.csv | ../logstash/bin/logstash -f
wget https://raw.githubusercontent.com/elastic/examples/master/ElasticStack_nyc_traffic_accidents/nyc_collision_logstash.conf
https://github.com/elastic/examples/tree/master/ElasticStack_nyc_traffic_accidents
https://www.elastic.co/guide/en/logstash/current/installing-logstash.html
curl -XPOST 'localhost:9200/bank/account/_bulk?pretty&refresh' --data-binary "@accounts.json"

##Grafana
http://docs.grafana.org/alerting/rules/

##Data Sources
###Jira
https://github.com/steves/node-jira