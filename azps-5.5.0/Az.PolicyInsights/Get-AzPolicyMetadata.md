---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193178"
---
# Get-AzPolicyMetadata

## SYNOPSIS
Pobiera zasoby metadanych zasad

## SKŁADNIA

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzPolicyRemediation** pobiera wszystkie zasoby metadanych zasad lub określony zasób metadanych zasad.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich zasobów metadanych zasad
```powershell
PS C:\> Get-AzPolicyMetadata
```

To polecenie pobiera wszystkie zasoby metadanych zasad

### Przykład 2. Uzyskiwanie kolekcji 10 zasobów metadanych zasad
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

To polecenie otrzymuje kolekcję 10 zasobów metadanych zasad

### Przykład 3. Uzyskiwanie zasobu metadanych zasad o nazwie "ACF1348"
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

To polecenie otrzymuje pojedynczy zasób metadanych zasad o nazwie "ACF1348"

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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Na górze
Maksymalna liczba zwracanych zasobów metadanych zasad.

```yaml
Type: System.Int32
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

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata

## NOTATKI

## LINKI POKREWNE
