---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: b5b14cbf816a7872abf431f787f9e3102006901c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003281"
---
# Get-AzOperationalInsightsWorkspaceUsage

## SYNOPSIS
Pobiera dane dotyczące użycia dla obszaru roboczego.

## SKŁADNIA

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzOperationalInsightsWorkspaceUsage** pobiera dane użycia dla obszaru roboczego.
Udostępnia to informacje o tym, jaka część danych była analizowana przez obszar roboczy w określonym okresie.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie danych dotyczących użycia według nazwy obszaru roboczego
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

To polecenie pobiera szczegóły użycia dla obszaru roboczego o nazwie MyWorkspace w określonej grupie zasobów.

### Przykład 2. Uzyskiwanie danych dotyczących użycia przy użyciu potoku
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

To polecenie pobiera obszar roboczy o nazwie MyWorkSpace za Get-AzOperationalInsightsWorkspace cmdlet, a następnie przekazuje go do bieżącego polecenia cmdlet.
Polecenie pobiera szczegóły użycia dla tego obszaru roboczego.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric

## NOTATKI

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Operational Insights](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


