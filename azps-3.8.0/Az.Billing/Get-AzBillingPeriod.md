---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051385"
---
# Get-AzBillingPeriod

## STRESZCZENIe
Uzyskaj okresy rozliczeniowe abonamentu.

## POLECENIA

### Lista (domyślna)
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Jedn
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzBillingPeriod** pobiera okresy rozliczeniowe abonamentu.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzBillingPeriod
```

Uzyskaj wszystkie dostępne okresy rozliczeniowe abonamentu.

### Przykład 2
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

Pobierz okres rozliczeniowy abonamentu o określonej nazwie.

### Przykład 3
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

Uzyskaj co najwyżej 2 okresy rozliczeniowe abonamentu.

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

### -MaxCount
Określ maksymalną liczbę zwracanych rekordów.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa określonego okresu rozliczeniowego do pobrania.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod

## INFORMACYJN

## LINKI POKREWNE
