---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339769"
---
# Get-AzBillingInvoice

## STRESZCZENIe
Pobierz faktury rozliczeniowe dla subskrypcji.
Pobieranie faktur rozliczeniowych dotyczących konta rozliczeniowego i profilu rozliczeń

## POLECENIA

### Lista (domyślna)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### Późniejsza
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Jedn
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu. 

## Przykłady

### Przykład 1
```
PS C:\> Get-AzBillingInvoice -Latest
```

Pobierz najnowszą fakturę z abonamentu.

### Przykład 2
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Pobierz fakturę abonamentu o określonej nazwie.

### Przykład 3
```
PS C:\> Get-AzBillingInvoice
```

Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania. 

### Przykład 4
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.

### Przykład 5
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Pobierz określoną fakturę według nazwy i Dołącz adres URL pobierania w wyniku.

### Przykład 6
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Pobierz faktury według nazwy konta rozliczeniowego i Dołącz adres URL pobierania dla każdej faktury w wyniku.

### Przykład 7
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Pobierz określoną fakturę według nazwy faktury i nazwy konta rozliczeniowego i Dołącz adres URL pobierania dla każdej faktury w wyniku.

### Przykład 8
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Pobierz najnowszą fakturę według nazwy konta rozliczeniowego i Dołącz adres URL pobierania dla faktury w wyniku.

### Przykład 9
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Pobierz najnowsze 10 faktur z określonego konta rozliczeniowego i konkretnego profilu rozliczeń i Dołącz do wyników adres URL pobierania.

### Przykład 10
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

Pobierz najnowszą fakturę według nazwy konta rozliczeniowego oraz nazwy profilu rozliczeń i Dołącz adres URL pobierania dla faktury w wyniku.

### Przykład 10
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

Pobierz faktury według nazwy konta rozliczeniowego i nazwy profilu rozliczeń dla okresu rozliczeniowego określonego przez datę perioStart i datę periodEnd.


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

### -GenerateDownloadUrl
Wygeneruj adres URL pobierania faktur.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
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
Type: System.Management.Automation.SwitchParameter
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

### -BillingAccountName
Nazwa określonego konta rozliczeniowego, za pomocą którego można uzyskać faktury.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BillingProfileName
Nazwa określonego profilu rozliczeń, za pomocą którego można uzyskać faktury.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodStartDate
Data rozpoczęcia faktury.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodEndDate
Data zakończenia fakturowania.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. rozliczenia. modele. PSInvoice

## INFORMACYJN

## LINKI POKREWNE
