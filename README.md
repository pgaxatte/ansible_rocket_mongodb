# Rocket.Chat mongodb -- Ubuntu 18.04 ansible role

This ansible role is directly based on the official (non-working)
[RocketChat ansible role](https://github.com/RocketChat/Rocket.Chat.Ansible).

It deploys only the MongoDB server (see the [RocketChat server
role](https://github.com/pgaxatte/ansible_rocket_server) for the actual server part) and only works on Ubuntu
18.04.

## Role Variables

All defaults are set in [`defaults/main.yml`](defaults/main.yml)

### MongoDB configuration

|     Name     |     Default Value    |    Description     |
|---------------------------|-----------------------|------------------------------------|
| `rocket_chat_mongodb_packages` | mongodb | Package used to install MongoDB. |
| `rocket_chat_mongodb_service_name` | mongodb | Name of the service to user. |
| `rocket_chat_mongodb_service_user` | mongodb | Name of the user used in the service. |
| `rocket_chat_mongodb_user` | not used by default | Username to be used when connecting to MongoDB. If you set this, you should also define `rocket_chat_mongodb_password`, otherwise no user/pass is used to connect to MongoDB |
| `rocket_chat_mongodb_password` | not used by default | Password to be used when connecting to MongoDB. If you set this, you should also define `rocket_chat_mongodb_user`, otherwise no user/pass is used to connect to MongoDB |
| `rocket_chat_mongodb_server` | 0.0.0.0 | The IP/FQDN of the MongoDB host |
| `rocket_chat_mongodb_port` | 27017 | The TCP port to contact the MongoDB host host via |
| `rocket_chat_mongodb_database` | rocketchat |  The MongoDB database to be used for Rocket.Chat |
| `rocket_chat_mongodb_use_tls`   | false  | Whether or not to use TLS to connect to the MongoDB DB  |
