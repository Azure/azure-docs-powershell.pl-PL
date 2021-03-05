---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997991"
---
# Get-AzIotCentralApp

## SYNOPSIS
Pobiera właściwości jednej lub kilku aplikacji centralnych IoT.

## SKŁADNIA

### ListIotCentralAppsParameterSet (domyślne)
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Pobiera metadane dla określonej aplikacji centralnej IoT lub wszystkich aplikacji w grupie zasobów lub subskrypcji, w zależności od zestawu parametrów. 

## PRZYKŁADY

### Przykład 1. Uzyskiwanie konkretnej aplikacji centralnej IoT.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Pobiera metadane dla określonej aplikacji centralnej IoT.

Przykładowe dane wyjściowe:

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName

### Przykład 2. Uzyskiwanie aplikacji centralnej aplikacji IoT w subskrypcji.
```powershell
PS C:\> Get-AzIotCentralApp
```

Pobiera metadane dla wszystkich aplikacji centralnych IoT w bieżącej subskrypcji.

Przykładowe dane wyjściowe:

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName

ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa nazwa wyświetlana 2 poddomena: Szablon MyAppSubDomain2: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName2

### Przykład 3. Uzyskiwanie aplikacji centralnej aplikacji IoT w grupie zasobów.
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Pobiera metadane dla wszystkich aplikacji centralnych IoT w podanej grupie zasobów.

Przykładowe dane wyjściowe:

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa poddomena nazwa wyświetlana: Szablon MyAppSubDomain: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName

ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name: MyAppResourceName2 Type: Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppskuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Nazwa wyświetlana: Moja niestandardowa nazwa wyświetlana 2 poddomena: Szablon MyAppSubDomain2: iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa centralnego zasobu aplikacji IOT.

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu aplikacji centralnej.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp

## NOTATKI

## LINKI POKREWNE
