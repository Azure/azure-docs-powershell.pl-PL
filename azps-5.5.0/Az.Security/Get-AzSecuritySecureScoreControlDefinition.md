---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189139"
---
# Get-AzSecuritySecureScoreControlDefinition

## SYNOPSIS
Pobiera definicje bezpiecznej kontroli wyników w subskrypcji

## SKŁADNIA

### SubscriptionScope (domyślne)
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

Pobiera wszystkie definicje kontroli wyników bezpiecznego zabezpieczeń w subskrypcji

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition

## NOTATKI

## LINKI POKREWNE
