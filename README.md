# glances-web-docker
Glances Monitoring

isterseniz run.sh çalıştırarak kurabilirsiniz isterseniz bu kodu kendiniz çalıştırarak yapabilirsiniz. Kurduktan sonra http://ip-adresi:61208 adresinden kontrol edebilirsiniz.

Glances Web Docker Kodu
```bash
docker run -d --restart="always" --name glances-web -p 61208-61209:61208-61209 -e TZ="${TZ}" -e GLANCES_OPT="-w" -v /var/run/docker.sock:/var/run/docker.sock:ro -v /run/user/1000/podman/podman.sock:/run/user/1000/podman/podman.sock:ro --pid host nicolargo/glances:latest-full
```
