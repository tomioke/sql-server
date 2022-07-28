# Setup SQL Server 2019 free from VPS

[![Discord][discord-image]][discord-url]

## Minimum System Requipments:
- Ubuntu 20.04
- CPU 1 Core
- RAM 2 GB
- Hardisk 20 GB

## Import the public repository GPG keys:

```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
```

## Register the SQL Server Ubuntu repository:

```bash
sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"
```

## Run the following commands to install SQL Server:

```bash
sudo apt-get update
sudo apt-get install -y mssql-server
```

 After the package installation finishes, run mssql-conf setup and follow the prompts to set the SA password and choose your edition. 
 As a reminder, the following SQL Server editions are freely licensed: Evaluation, Developer, and Express.
 
 ## Settings editions packages
```bash
sudo /opt/mssql/bin/mssql-conf setup
```
