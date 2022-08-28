# Import-TI-ThreatViewIPBlocklist

author: Alex Verboon

This playbook ingest threat indicators into Microsoft Sentinel.

Threat Intellgience Source: [ThreatView](https://threatview.io/) [IP Blocklist](https://threatview.io/Downloads/IP-High-Confidence-Feed.txt)

## Prerequisites

1. This playbook has a dependency on the BatchImport playbook
2. Create a service principal that has access to the Sentinel Log Analytics workspace

## Configurations

* After importing the playbook, open the playbook and configure the connection for the Azure Monitor connector.


![](https://raw.githubusercontent.com/Azure/Azure-Sentinel/master/Solutions/Watchlists%20Utilities/Playbooks/Watchlist-CloseIncidentKnownIPs/images/designerLight1.png)




[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FWatchlists%2520Utilities%2FPlaybooks%2FWatchlist-CloseIncidentKnownIPs%2Fazuredeploy.json) [![Deploy to Azure Gov](https://aka.ms/deploytoazuregovbutton)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FSolutions%2FWatchlists%2520Utilities%2FPlaybooks%2FWatchlist-CloseIncidentKnownIPs%2Fazuredeploy.json)