# postfix
Postfix docker container (intended as a backup MX or for testing)


## Docker Image

Creates a Docker Image of Postfix. 
The Primary intention is to use this image as a backup MX, testing email sending, or as a relay where needed.

On every start, the container will re-run the transport postmap. SO if you need to change your transport maps, you just need to do a docker compose down and up. 


## Volumes

Volumes you may want to map are:

- /var/spool/postfix (Mail Queues)
- /config (BasicConfig Files)

Optional
- /var/log (Log Files)
- /etc/postfix (ALL Config Directory)

## Ports

Ports to expose

- 25 (SMTP relay)
- 587 (Mail submission)