# Setting up RabbitMQ

The RabbitMQ is not available directly in the ubuntu repository, thus we add the repo and then install it.

To install RabbitMQ follow these steps:

1. Install Erlang Repo Package
2. Add an Erlang Solution public key
3. Install Erlang
Note: Here we will be making use of "update_cache: yes" this will work same as "apt update" ... This step is needed because we have added a new repo


Note: For adding a repo using ansible we make use of "deb" module inside apt module
