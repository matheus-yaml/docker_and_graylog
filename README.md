# docker_and_graylog

http://localhost:9000/system/inputs
create a GELF INPUT UDP on port 12201

http://localhost:9000/streams
create a stream to filter logs

manage your stream and create a rule to your stream
statements:
field: image_name
type: contain
value: your container_name #container-01

docker run --rm --name container-01 --log-driver=gelf --log-opt gelf-address=udp://<GRAYLOG-SERVER>:12201 nginx bash

