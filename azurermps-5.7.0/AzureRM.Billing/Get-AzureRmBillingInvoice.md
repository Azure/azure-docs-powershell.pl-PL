---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527054"
---
# Get-AzureRmBillingInvoice

## STRESZCZENIe
Pobierz faktury rozliczeniowe dla subskrypcji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Lista (domyślna)
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Późniejsza
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Jedn
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu. 

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

Pobierz najnowszą fakturę z abonamentu.

### Przykład 2
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

Pobierz fakturę abonamentu o określonej nazwie.

### Przykład 3
```
PS C:\> Get-AzureRmBillingInvoice
```

Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania. 

### Przykład 4
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.

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

### -GenerateDownloadUrl
Wygeneruj adres URL pobierania faktur.

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Najnowsze
Pobierz najnowszą fakturę.

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Określa maksymalną liczbę zwracanych rekordów.

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
Nazwa konkretnej faktury do pobrania lub ostatniej, jeśli nie została określona.

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

### System. Collections. Generic. list "1 [[Microsoft. Azure. Management. rozliczenia. modele. Invoice, Microsoft. Azure. Commands. rozliczenia, wersja = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Management. rozliczenia. modele, faktura

## INFORMACYJN

## LINKI POKREWNE

