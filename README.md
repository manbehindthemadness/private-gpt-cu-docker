# private-gpt-cu-docker

Automated creation of one or more private-gpt client instances in docker containers using a single host ollama server.

```
git clone https://github.com/manbehindthemadness/private-gpt-cu-docker
cd private-gpt-cu-docker
chmod +x private-gpt-docker
./private-gpt-docker <desired listening port> <desired instance name>
```

Notes:
 - The listening port will be mapped to the host system, ensure is doesn't conflict with an existing service.
 - We assume that the host system is presented as 172.17.0.1 on the virtual LAN.
 - We assume that ollama is listening on port 11434.
 - Unit files are placed within the service_units folder and then syslinked to systemd.
 - Unit files will reflect the name of the instance specified.
 - flush_all_docker does exactly what it's name suggests, it's mainly for testing use.
