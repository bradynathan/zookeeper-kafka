Zookeeper Kafka
=========

Installs zookeeper and kafka

Requirements
------------


Role Variables
--------------


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - zookeeper_kafka

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Testing
--------
Create Topic
/opt/kafka/current/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test
Start Consumer
/opt/kafka/current/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning
Send Message
/opt/kafka/current/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
