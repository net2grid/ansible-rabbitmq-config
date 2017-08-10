# rabbitmq-config

This role configures a RabbitMQ cluster

Requirements
------------

All dependencies are listed in the metadata file.

Role Variables
--------------

The following variables can be passed to this role:

    # The credentials for the RabbitMQ server we're configuring
    rabbitmq_config_user: admin
    rabbitmq_config_password: admin
    rabbitmq_config_host: localhost
    
    # Exchanges
    rabbitmq_config_exchanges:
      - name: hello_world
        exchange_type: topic
    
    # Queues
    rabbitmq_config_queus:
      - name: hello_world
        durable: true
        message_ttl: 60000
    
    # Bindings
    rabbitmq_config_bindings:
      - name: hello_world
        destination: hello_world
        destination_type: queue

License
-------

MIT

Author Information
------------------

- Remco Brink, NET2GRID
