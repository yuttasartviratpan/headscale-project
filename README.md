# headscale-project

Refer to [https://github.com/juanfont/headscale/blob/main/docs/running-headscale-container.md](headscale/setup.md) for how to setup and register a machine onto the headscale server

Note:
- When the server prompt you to do (YOU_+MACHINE_KEY will be given on an attempt to register to the server): 
    - ``` headscale --user myfirstuser nodes register --key <YOU_+MACHINE_KEY> ```
    What you actually need to put is:
    - ``` headscale --user <HOST_USER> nodes register --key <YOU_+MACHINE_KEY> ```
    HOST_USER comes from:
    - ``` docker exec headscale headscale users create <HOST_USER> ```
    during the server setup


TODO:
- Automate the process so that the user only needs to click the given link so that the server recieve the link and automatically run the headscale register command
- Figure out how to have a sqlitedb in the vpn be hosted on different dns