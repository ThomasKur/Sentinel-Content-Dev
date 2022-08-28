# Import-TI-ThreatViewIPBlocklist

author: Alex Verboon

This playbook ingest threat indicators into Microsoft Sentinel.

Threat Intellgience Source: [ThreatView](https://threatview.io/) [IP Blocklist](https://threatview.io/Downloads/IP-High-Confidence-Feed.txt)

## Prerequisites

1. This playbook has a dependency on the BatchImport playbook
2. Create a service principal that has access to the Sentinel Log Analytics workspace

## Configurations

* After importing the playbook, open the playbook and configure the connection for the Azure Monitor connector.

![](https://github.com/alexverboon/Sentinel-Content-Dev/blob/59c92c63e8b4e3dc7bbfeda66b634aee40211cf7/Playbooks/ThreatView_IPBlockList/images/azuremonitor-connection.png)




[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https://raw.githubusercontent.com/alexverboon/Sentinel-Content-Dev/main/Playbooks/ThreatView_IPBlockList/azuredeploy.json) [![Deploy to Azure Gov](https://aka.ms/deploytoazuregovbutton)](https://portal.azure.us/#create/Microsoft.Template/uri/https://raw.githubusercontent.com/alexverboon/Sentinel-Content-Dev/main/Playbooks/ThreatView_IPBlockList/azuredeploy.json)