# headscale-project

Refer to [headscale/setup.md](https://github.com/juanfont/headscale/blob/main/docs/running-headscale-container.md) for how to setup and register a machine onto the headscale server

Note:
- Be aware that the [main documentation website on docker setup](https://headscale.net/running-headscale-container/) is not up to date. Refer to the above link for more up to date documentation
- When the server prompt you to do (YOU_+MACHINE_KEY will be given on an attempt to register to the server): 
    - ``` headscale --user myfirstuser nodes register --key <YOU_+MACHINE_KEY> ```
    
    What you actually need to put is:
    - ``` headscale --user <HOST_USER> nodes register --key <YOU_+MACHINE_KEY> ```
    
    HOST_USER comes from:
    - ``` docker exec headscale headscale users create <HOST_USER> ```
    
    during the server setup

<br>

### TODO:
- Automate the process so that the user only needs to click the given link so that the server recieve the link and automatically run the headscale register command
- Bind the URl from localhost to an active Domain Name
- Figure out how to have a sqlitedb in the vpn be hosted on different dns