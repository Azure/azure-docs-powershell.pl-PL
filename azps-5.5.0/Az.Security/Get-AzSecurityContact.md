---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189195"
---
# Get-AzSecurityContact

## SYNOPSIS
Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji

## SKŁADNIA

### SubscriptionScope (domyślne)
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Pobiera kontakty zabezpieczeń, które zostały skonfigurowane w tej subskrypcji.
Kontakt zabezpieczeń może otrzymywać powiadomienia o alertach zabezpieczeń, które są wysyłane w ramach subskrypcji.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

Pobiera wszystkie skonfigurowane kontakty zabezpieczeń w subskrypcji

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
Nazwa zasobu.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu.

```yaml
Type: System.String
Parameter Sets: ResourceId
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

## OUTPUTS

### Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact

## NOTATKI

## LINKI POKREWNE
