{
    "$schema": "http://schema.management.azure.com/schemas/2014-04-01-preview/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "dbServerName": {
            "type": "String"
        },
        "administratorLogin": {
            "type": "String"
        },
        "administratorLoginPassword": {
            "type": "SecureString"
        }
    },
    "variables": {
        "collation": "SQL_Latin1_General_CP1_CI_AS",
        "location": "[resourceGroup().location]",
        "sqlDBName": "AMPSaaSDB"
    },
    "resources": [],
    "outputs": {
        "SQL DB Server Name": {
            "type": "String",
            "value": "[concat(parameters('dbServerName'), '.database.windows.net')]"
        },
        "SQLDB Admin Login": {
            "type": "String",
            "value": "[parameters('administratorLogin')]"
        },
        "SQLDB Admin Password": {
            "type": "String",
            "value": "[parameters('administratorLoginPassword')]"
        }
    }
}
