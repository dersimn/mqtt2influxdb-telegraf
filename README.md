Telegraf-based Docker Image to store raw data from MQTT into InfluxDB.

## Build

    make docker-image

## Run

Configure environment variables according to your needs:

    MQTT_HOST="mqtt"
    MQTT_PORT="1883"
    INFLUXDB_URL="http://influxdb:8086"
    INFLUXDB_DB_NAME="raw_mqtt"
    INFLUXDB_MEASUREMENT_NAME="string_data"

Example:

    docker run -d --restart=always --name=mqtt2influxdb -e "MQTT_HOST=10.1.1.50" -e "INFLUXDB_URL=http://10.1.1.50:8086" dersimn/mqtt2influxdb