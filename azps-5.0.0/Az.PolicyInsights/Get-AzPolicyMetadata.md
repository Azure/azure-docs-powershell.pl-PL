---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224998"
---
# Get-AzPolicyMetadata

## STRESZCZENIe
Pobiera zasoby metadanych zasad

## POLECENIA

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzPolicyRemediation** pobiera wszystkie zasoby metadanych zasad lub konkretny zasób metadanych zasad.

## Przykłady

### Przykład 1. pobieranie wszystkich zasobów metadanych zasad
```powershell
PS C:\> Get-AzPolicyMetadata
```

To polecenie pobiera wszystkie zasoby metadanych zasad

### Przykład 2: uzyskiwanie zbioru 10 zasobów metadanych zasad
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

To polecenie pobiera zbiór 10 zasobów metadanych zasad

### Przykład 3: uzyskiwanie pojedynczego zasobu metadanych zasad o nazwie "ACF1348"
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

To polecenie pobiera jeden zasób metadanych zasad o nazwie "ACF1348"

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Początek
Maksymalna liczba zasobów metadanych zasad, które mają zostać zwrócone.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. PolicyInsights. models. PSPolicyMetadata

## INFORMACYJN

## LINKI POKREWNE
