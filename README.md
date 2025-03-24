# AzSQLMaint

AzSQLMaint is a PowerShell-based Azure Function designed to simplify and automate maintenance tasks for Azure SQL databases. It streamlines routine database management activities, ensuring optimal performance and reliability within your Azure environment.

## Features

- **Automated Maintenance**: Schedule and perform routine maintenance tasks automatically.
- **Customizable Tasks**: Easily tailor maintenance tasks to fit your specific database management requirements.
- **Scalable Solution**: Effectively manage maintenance across multiple Azure SQL databases.

## Prerequisites

Before deploying AzSQLMaint, ensure you have:

- An active **Azure subscription**.
- At least one **Azure SQL Database**.
- An **Azure Functions** environment configured for PowerShell.

## Deployment

Follow these steps to deploy AzSQLMaint:

### 1. Clone the Repository

```bash
git clone https://github.com/joshargy/AzSQLMaint.git
cd AzSQLMaint
```

### 2. Deploy to Azure Functions

Create an Azure Function App using Azure CLI:

```bash
az functionapp create \
  --resource-group <ResourceGroupName> \
  --consumption-plan-location <Location> \
  --runtime powershell \
  --functions-version 3 \
  --name <FunctionAppName> \
  --storage-account <StorageAccountName>
```

Deploy function code:

```bash
az functionapp deployment source config-zip \
  --resource-group <ResourceGroupName> \
  --name <FunctionAppName> \
  --src AzSQLMaint.zip
```

## Configuration

Adjust the following configurations:

- **Application Settings**: Update database connection strings, schedules, and maintenance parameters in your Azure Function App settings.
- **Function Triggers**: Configure triggers (e.g., timer-based) to automate the execution schedule.

## Usage

Once configured:

- **Monitor** your maintenance tasks via the Azure Portal or Application Insights.
- Review **logs** regularly to ensure successful execution and troubleshoot as necessary.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Submit a detailed Pull Request.

## License

AzSQLMaint is licensed under the MIT License. Refer to the [LICENSE](LICENSE) file for more information.

## Contact

For issues, support, or suggestions, open an issue in the repository or contact [joshargy](https://github.com/joshargy).

---

*For the most detailed and accurate instructions, please refer to the [AzSQLMaint GitHub repository](https://github.com/joshargy/AzSQLMaint).*
