# Nats Cluster Example

This repository serves as an example for setting up a NATS cluster using Docker Compose. NATS is a simple, secure, and high-performance open-source messaging system for cloud-native applications, IoT messaging, and microservices architectures. This example provides a straightforward way to get started with NATS clustering.

## Getting Started
Follow these instructions to get the NATS cluster up and running on your local machine.

## Prerequisites
- Docker
- Docker Compose
## Installation
1. Clone this repository to your local machine:
```bash
Copy code
git clone https://github.com/HiWay-Media/nats-cluster-example.git
```

1. Navigate to the cloned directory:
```bash
Copy code
cd nats-cluster-example
```
## Usage
1. Start the NATS cluster using Docker Compose:
```bash
Copy code
docker-compose up -d
```
1. Verify that the cluster is running:
```bash
Copy code
docker-compose ps
```
This command should display three containers running, each representing a member of the NATS cluster.

## Testing
You can test the functionality of the NATS cluster by publishing and subscribing to messages.

1. Publish a message:
```bash
Copy code
docker-compose exec nats1 nats-pub -s nats://nats1:4222 subject "Hello NATS!"
```

1. Subscribe to the message:
```bash
Copy code
docker-compose exec nats2 nats-sub -s nats://nats2:4222 subject
```
You should see the message "Hello NATS!" being received in the subscriber's console.

## Configuration
The NATS cluster configuration is defined in the docker-compose.yml file. You can modify this file to adjust settings such as the number of nodes, ports, and clustering parameters.

## Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- NATS - For providing a lightweight and efficient messaging system.
- Docker - For simplifying the deployment of the NATS cluster using containers.

## Contact
For any inquiries or assistance, please contact HiWay Media.

Thank you for using the NATS cluster example! 🚀
