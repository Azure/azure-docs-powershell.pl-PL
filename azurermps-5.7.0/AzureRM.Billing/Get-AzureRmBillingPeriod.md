---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553032"
---
# Get-AzureRmBillingPeriod

## STRESZCZENIe
Uzyskaj okresy rozliczeniowe abonamentu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Lista (domyślna)
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Jedn
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmBillingPeriod** pobiera okresy rozliczeniowe abonamentu.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmBillingPeriod
```

Uzyskaj wszystkie dostępne okresy rozliczeniowe abonamentu.

### Przykład 2
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

Pobierz okres rozliczeniowy abonamentu o określonej nazwie.

### Przykład 3
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

Uzyskaj co najwyżej 2 okresy rozliczeniowe abonamentu.

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

### -MaxCount
Określ maksymalną liczbę zwracanych rekordów.

```yaml
Type: Int32
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod, Microsoft. Azure. Commands. rozliczenia, wersja = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod

## INFORMACYJN

## LINKI POKREWNE

