# Ansible Playbooks for Apache and CSR1000v

This repository contains Ansible playbooks for automating the deployment and management of Apache web server and Cisco CSR1000v routers. These playbooks are designed to streamline the configuration process, enabling quick and consistent setup across environments.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Usage](#usage)
3. [Playbooks](#playbooks)
4. [Contributing](#contributing)
5. [License](#license)

## Prerequisites

Before using these playbooks, ensure that you have the following prerequisites installed:

- **Ansible**: Install Ansible on the control node from where you'll execute the playbooks. Refer to the [Ansible documentation](https://docs.ansible.com/ansible/latest/installation_guide/index.html) for installation instructions.
- **Python**: Ansible requires Python to be installed on both the control node and managed nodes. Ensure Python is installed and accessible.
- **SSH Access**: Ensure SSH access to the target servers (Apache servers and CSR1000v routers) from the control node. Set up passwordless SSH authentication or provide necessary credentials in the inventory file.
- **Cisco CSR1000v**: If managing CSR1000v routers, ensure they are deployed and accessible in your network environment.

## Usage

1. **Clone the Repository**: Clone this repository to your local machine using the following command:

    ```bash
    git clone https://github.com/MrHackerz/ansible.git
    ```
2. **Navigate to the Ansible Directory**: Enter the Ansible directory:

    ```bash
    cd ansible/labs/devnet-src/ansible/ansible-apache
    ```

3. **Update Inventory**: Update the `inventory` file with the IP addresses or hostnames of your Apache servers and CSR1000v routers.

4. **Configure Variables**: Customize variables in the playbook YAML files located in the `playbooks` directory according to your environment requirements.

5. **Execute Playbooks**: Run the desired playbook using the `ansible-playbook` command:

    ```bash
    ansible-playbook -i inventory playbook.yml
    ```

   Replace `playbook.yml` with the name of the playbook you want to execute.

## Playbooks

- **`apache_playbook.yml`**: Installs and configures Apache web server on specified hosts.
- **`configure_router.yml`**: Configures Cisco CSR1000v routers with specified settings.
- **`backup_cisco_router_playbook.yml`**: Automatically backs up the running-config of CSR1000v routers.

## Contributing

Contributions to improve this repository are welcome! If you find any issues or have suggestions for enhancements, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

