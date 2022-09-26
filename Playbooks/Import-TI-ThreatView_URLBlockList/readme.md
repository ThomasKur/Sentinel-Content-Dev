# Import-TI-ThreatView URL Block List

author: Alex Verboon

This playbook ingest threat indicators into Microsoft Sentinel.

Threat Intellgience Source: [ThreatView](https://threatview.io/) [URL Blocklist](https://threatview.io/Downloads/URL-High-Confidence-Feed.txt)

![Playbook](./images/importthreatviewurlblocklist_flow.png)

## Prerequisites

1. This playbook has a dependency on the [BatchImportToSentinel](../TIBatchImportSentinel/readme.md) playbook
2. The Service principal must have access to the Sentinel Log Analytics workspace
![Service Principal workspace permissions](./images/la_app_permissions.png)

## Deployment

Before deploying this playbook, make sure you have the [BatchImportToSentinel](../TIBatchImportSentinel/readme.md) playbook deployed

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Falexverboon%2FSentinel-Content-Dev%2Fmain%2FPlaybooks%2FThreatView_URLBlockList%2Fazuredeploy.json)

[![Deploy to Azure Gov](https://aka.ms/deploytoazuregovbutton)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Falexverboon%2FSentinel-Content-Dev%2Fmain%2FPlaybooks%2FThreatView_URLBlockList%2Fazuredeploy.json)

## Configuration

* After importing the playbook, open the playbook and configure the connection for the Azure Monitor connector. Configure the API connection to connect with a service principal.

![Azure Monitor Connection](./images/azuremonitor-connection.png)

* Optionally, configure the Threat Intelligence data import settings, such as the expiration time for the imported TI.

![TI settings](./images/ti_data.png)


## Result

```kusto
ThreatIntelligenceIndicator
| where SourceSystem == "SecurityGraph"
| where Description == "ThreatView-IPBlockList"
```


