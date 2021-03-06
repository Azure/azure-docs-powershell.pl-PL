---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710898"
---
# Get-AzOperationalInsightsWorkspaceUsage

## STRESZCZENIe
Pobiera dane dotyczące użycia obszaru roboczego.

## POLECENIA

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzOperationalInsightsWorkspaceUsage** pobiera dane dotyczące użycia obszaru roboczego.
Dzięki temu jest to, ile danych zostało przeanalizowanych przez obszar roboczy w określonym czasie.

## Przykłady

### Przykład 1: pobieranie danych użycia według nazwy obszaru roboczego
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

To polecenie pobiera szczegóły użycia obszaru roboczego o nazwie Moja przestrzeń robocza w określonej grupie zasobów.

### Przykład 2: uzyskiwanie danych dotyczących użycia przy użyciu rurociągu
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

To polecenie pobiera obszar roboczy o nazwie webworkspace za pomocą polecenia cmdlet Get-AzOperationalInsightsWorkspace, a następnie przekazuje obszar roboczy do bieżącego polecenia cmdlet.
Polecenie pobiera dane dotyczące użycia tego obszaru roboczego.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Name (nazwa)
Określa nazwę obszaru roboczego.

```yaml
Type: System.String
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
Type: System.String
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

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. OperationalInsights. models. PSUsageMetric

## INFORMACYJN

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Operations Insights](/powershell/module/az.operationalinsights)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


