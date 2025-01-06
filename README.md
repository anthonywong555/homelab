# homelab
My own personal homelab

## Diagram

![](./assets/homelab-architecture-diagram.png)


## Temporal

To setup Temporal, you want to use the [docker compose examples](https://github.com/temporalio/docker-compose/blob/main/docker-compose-mysql-es.yml). The reason for this is because the [temporalio/auto-setup](https://hub.docker.com/r/temporalio/auto-setup) sets up the database. 

I add `DEFAULT_NAMESPACE_RETENTION=90d` as part of the environment variable for the `temporalio/auto-setup`.

After that, you can replace the auto-setup with the [temporalio/server](https://hub.docker.com/r/temporalio/server).

## Tip & Tricks

>How come I'm can't access my reverse proxy?

*Add your reverse proxy URL into the PiHole Local DNS Records. It should be.*

Domain: Machine IP Address.

## Resources
- [Temporal Docker Compose](https://github.com/anthonywong555/temporalio-docker-compose)
- [Ansible Playbook for my Ubuntu Server](https://github.com/anthonywong555/ansible-homelab)