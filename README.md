# CS2 helm chart using steamcmd docker image

this chart uses a pvc to store the game files located in /home/steam/cs2-ds/, i use nfs-client in ReadWriteMany so pods dont get stuck waiting to other pod to be terminated, also uses loadBalancer IP to publish udp (game) and tcp (rcon) ports, you can use nodePort or other aproach but it needs to be modified.

## GAME TOKEN
Get Game Server Token from https://steamcommunity.com/dev/managegameservers

You need to create a token and specify it in the values.

## SERVER CFG
you can customize your server.cfg file in the values too.