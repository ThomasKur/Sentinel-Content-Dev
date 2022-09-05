# Watchlist-NetWork-Addresses

## Description

The playbook ***Watchlist-NetWork-Addresses*** check if any of the Incident IP Address entities is within the range of the ***Network Addresses*** watchlist.

![watchlist-network-addresses-flow](./images/watchlist-network-addresses-flow.png)

## Prerequisites

1. Managed Identity must have Sentinel Contribor role.
2. The Service principal must have access to the Sentinel Log Analytics workspace
3. The watchlist 'Network addresses' must be present and have IP ranges of known networks defined

## Deployment

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Falexverboon%2FSentinel-Content-Dev%2Fmain%2FPlaybooks%2FWatchlist-NetworkAddresses%2Fazuredeploy.json)

[![Deploy to Azure Gov](https://aka.ms/deploytoazuregovbutton)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Falexverboon%2FSentinel-Content-Dev%2Fmain%2FPlaybooks%2FWatchlist-NetworkAddresses%2Fazuredeploy.json)

## Configuration

### Assign the Sentinel contributor role to the Managed Identity

![assign role](./images/Identity_role1.png)

![assign role](./images/identity_role2.png)

### Configure the connections

Configure the connection to use the Managed Identity
![Get Entities connection](./images/configure_conn1.png)

![Get entities connection](./images/configure_conn2.png)

Configure the connection to use the Service Principal that you have setup for Sentinel Playbooks.
> Note! the service principal must have access to the Sentinel Log Analytics workspace

![log anlytics connection](./images/azmon-conn1.png)

![log anlytics connection](./images/azmon-conn2.png)

![log anlytics connection](./images/azmon-conn3.png)

![log anlytics connection](./images/azmon-conn4.png)

![log anlytics connection](./images/azmon-conn5.png)

## Results

The playbook writes the results into the incident comment

![playbook result](./images/watchlist-network-address-result.png)
