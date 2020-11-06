---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528158"
---
# Sync-AzureAnalysisServicesInstance

## STRESZCZENIe

Synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w aktualnie zalogowanym środowisku określonym w Add-AzureAnalysisServicesAccount polecenia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## Opis

Polecenie cmdlet Sync-AzureAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami ScaleOut zapytań w obecnie zarejestrowaniu środowisku określonym w Add-AzureAnalysisServicesAccount polecenie

## Przykłady

### Przykład 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

To polecenie zsynchronizuje bazę danych o nazwie SalesOrders na serwerze o nazwie "contoso" w westus.asazure.windows.net środowiska, pod warunkiem że użytkownik zarejestrował się do tego środowiska przy użyciu Add-AzureAnalysisServicesAccount polecenia.

## PARAMETRÓW

### -Instance

Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

Tożsamość bazy danych do zsynchronizowania

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### System. Boolean

## INFORMACYJN

Alias: Sync-AzureAsInstance

## LINKI POKREWNE
