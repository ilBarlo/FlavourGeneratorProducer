# FlavourGenerator
This repository contains a Kubernetes controller implemented using the controller-runtime library. The controller continuously watches the Kubernetes cluster for any changes in the resources and retrieves the metrics of the node where the resource is being added/modified/deleted. The metrics are then processed and sent to RabbitMQ for further consumption by other systems. The producer has been implemented using Golang, and the RabbitMQ client library used is AMQP.

In order to use this repository, the following steps need to be taken:

1. Set up a RabbitMQ server.
2. To run it locally execute the run command in a console where you previously exported a KUBECONFIG variable.

      ```bash
      go run cmd/main.go
      ```

## About
For the repo of the consumer, click this [link](https://github.com/ilBarlo/FlavourGeneratorConsumer)
