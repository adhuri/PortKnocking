# PortKnocking

###Name     - Aniket Ramesh Dhuri
###Unity ID - adhuri
###Email    - adhuri@ncsu.edu

##Description
1. Run Make file using `make` - which sets executable permission to backdoor , knocker and read permission for configuration-file.
2. Start HTTP server by `chmod +x webserver/start-server.sh ; webserver/start-server.sh`
3. Run Backdoor using `sudo ./backdoor configuration-file http://<webserverIp>:8000`
4. Run Knocker using `sudo ./knocker configuration-file <ipofbackdoorserver>`
