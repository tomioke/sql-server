# Setup SQL Server 2019 free from VPS

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

 > Select 3 for Express, free edition
 >
 > yes
 
 > Enter password, example ManiakSQL@123

 ## Cek status sql server
 
 ```bash
systemctl status mssql-server --no-pager
```

## Check the listening port for MSSQL server

 ```bash
sudo apt install net-tools
```

## Cek port number

```bash
sudo netstat -tnlp | grep sqlservr
```

## Allow firewall

```bash
sudo ufw allow 22
sudo ufw allow 1433
sudo ufw allow 1434
sudo ufw enable 
```
> type y

