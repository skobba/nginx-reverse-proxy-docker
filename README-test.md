# Python test webserver
python -m SimpleHTTPServer 80


# Docker container som viser IP

## Dynamisk port
docker run -P -d nginxdemos/hello

## Port 8181
docker run -p 8181:80 -d nginxdemos/hello

## Port 10.10.4.33:8181
docker run -p 10.10.4.33:8181:80 -d nginxdemos/hello


# IP in Docker
When you invoke docker run you can use either:
 -p IP:host_port:container_port 
 
 or 
 
 -p IP::port
 
to specify the external interface for one particular binding.
