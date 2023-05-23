
# Maestro

Maestro is a powerful Bash script designed to streamline various Kubernetes operations and facilitate management tasks. It provides a set of options and commands to simplify the configuration and administration of your Kubernetes cluster. Whether you need to create tokens, grant permissions, retrieve information, or create and manage master and worker nodes, Maestro has got you covered.

## Prerequisites

Before using Maestro, ensure that you have the following:

- A working Bash environment.
- Access to a Kubernetes cluster with the necessary privileges.


## Installation

You can install this script globally in your machine by doing the following. In this example we use the latest version of the script.

```bash
  wget https://github.com/joseareia/maestro/archive/refs/tags/v1.2.1.tar.gz
  tar -xvf v1.2.1.tar.gz & cd maestro-1.2.1
  sudo chmod +x maestro.sh
  mv maestro.sh /usr/local/bin/maestro
```

After following the steps above, Maestro is ready to use globally in your machine.

## Usage

Using Maestro is simple. You just need to run the script with the options that you want. Below is an example of you can use it for creating a K3S master node.

```bash
maestro master -n my-master-node
```

In the section below you can find all the options and available commands that Maestro can offer you.

### Available options

```bash
-h, --help
    Display help for the given command. When no command is specified, it displays help for the list command.

-c, --create-token
    Create a new bearer token for the default Kubernetes account.

-r, --retrieve-token
    Retrieve the existing bearer token for the default Kubernetes account.

-p, --permissions
    Grant the necessary permissions for the default Kubernetes user to access the REST API.

-m, --master-token
    Retrieve the existing master token for the current node master.
```

### Available commands

```bash
about
    Shows a short information about Maestro.

list
    Lists all the commands and useful information.

master
    Creates a k3s master node with a given name.

worker
    Creates a k3s worker node with a given name, master node address, and token.
```

Maestro simplifies Kubernetes management by providing an intuitive interface to perform common tasks. It automates repetitive operations and helps you save time and effort in administering your Kubernetes cluster. With Maestro, you can focus on developing and deploying applications without getting bogged down by complex Kubernetes configurations.


## Contributing

Contributions to Maestro are welcome! If you encounter any issues, have suggestions for improvements, or would like to add new features, please submit a pull request. We appreciate your feedback and contributions to make Maestro even better.


## License

This project is under the [GNU GPLv3](https://choosealicense.com/licenses/gpl-3.0/) license.
