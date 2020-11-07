---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719425"
---
# Get-AzureRmIotCentralApp

## STRESZCZENIe
Pobiera właściwości jednego lub kilku aplikacji centralnych IoT.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ListIotCentralAppsParameterSet (domyślny)
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Pobiera metadane dla konkretnej aplikacji centralnej usługi IoT albo wszystkie aplikacje w grupie zasobów lub subskrypcji, w zależności od zestawu parametrów. 

## Przykłady

### Przykład 1 Pobierz określoną aplikację centralną IoT.
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

Pobiera metadane określonej aplikacji Centrum IoT.

Przykładowe dane wyjściowe:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-xxxxxxxxxxxx DisplayName: Moja niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

### Przykład 2 Uzyskaj w ramach abonamentu aplikację centralną IoT.
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

Pobiera metadane wszystkich aplikacji centralnych IoT w bieżącej subskrypcji.

Przykładowe dane wyjściowe:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-xxxxxxxxxxxx DisplayName: Moja niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2: typ MyAppResourceName2: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. MODELES. PSIotCentralAppSkuInfo: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Moja niestandardowa nazwa wyświetlana 2 poddomena: MyAppSubdomain2: iotc-default@1.0.0 ResourceGroupName

### Przykład 3 Uzyskaj aplikacje centralne programu IoT w grupie zasób.
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

Pobiera metadane wszystkich aplikacji centralnych IoT w podanej grupie zasobów.

Przykładowe dane wyjściowe:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName: MyAppResourceName typ: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. modele. PSIotCentralAppSkuInfo identyfikator: XXXXXXXX-XXXX-XXXX-XXXX-xxxxxxxxxxxx DisplayName: Moja niestandardowa nazwa wyświetlana: MyAppSubdomain szablon: identyfikator iotc-default@1.0.0 subskrypcji: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2: typ MyAppResourceName2: Microsoft. IoTCentral/IoTApps Location: tag zachód: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. MODELES. PSIotCentralAppSkuInfo: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Moja niestandardowa nazwa wyświetlana 2 poddomena: MyAppSubdomain2: iotc-default@1.0.0 ResourceGroupName

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa zasobu aplikacji centralnej IoT.

```yaml
Type: String
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
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu aplikacji centralnej IoT.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String
## WYSYŁA

### Microsoft. Azure. Commands. IotCentral. models. PSIotCentralApp
## INFORMACYJN

## LINKI POKREWNE
