---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: 91d7b92b7b52df20d69f53cddb98d6b9276b0b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176595"
---
# New-AzADDomainServiceForestTrust

## SYNOPSIS
Tworzenie obiektu w pamięci dla aplikacji ForestTrust

## SKŁADNIA

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## OPIS
Tworzenie obiektu w pamięci dla aplikacji ForestTrust

## PRZYKŁADY

### Przykład 1. Tworzenie oprogramowania ServiceForestTrust dla domeny ADDomain
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

Create ServiceForestTrust for ADDomain

## PARAMETERS

### -FriendlyName
Przyjazna nazwa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - RemoteDnsIP
Zdalne adresy IP DNS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustDirection
Kierunek zaufania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedDomainFqdn
Nazwa FQDN zaufanej domeny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustPassword
Hasło do zaufania.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.ForestTrust

## NOTATKI

ALIASY

## LINKI POKREWNE

