---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528006"
---
# Get-AzureRmOperationalInsightsWorkspaceSharedKeys

## STRESZCZENIe
Pobiera klucze współużytkowane dla obszaru roboczego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** zawiera listę kluczy współużytkowanych dla obszaru roboczego.
Klucze służą do łączenia agentów usługi Insights z obszarem roboczym.

## Przykłady

### Przykład 1: pobieranie kluczy współużytkowanych według nazwy obszaru roboczego
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

To polecenie pobiera klucze udostępnione dla obszaru roboczego o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.

### Przykład 2: pobieranie kluczy współużytkowanych za pomocą potoku
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzureRmOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do polecenia cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .
Polecenie pobiera klucze współużytkowane dla tego obszaru roboczego.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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
Określa nazwę obszaru roboczego.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspaceKeys

## INFORMACYJN

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Operations Insights](./AzureRM.OperationalInsights.md)

[Get-AzureRmOperationalInsightsWorkspace](./Get-AzureRmOperationalInsightsWorkspace.md)


