---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: ca1e2032b312a7d0805811fb638c95777ba8ae75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199514"
---
# Get-AzBillingInvoice

## SYNOPSIS
Uzyskaj faktury za subskrypcję.
Uzyskiwanie faktur rozliczeniowych konta rozliczeniowego i profilu rozliczeniowego

## SKŁADNIA

### Lista (domyślna)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### Najnowsze
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Single
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzBillingInvoice** pobiera faktury za subskrypcję. 

## PRZYKŁADY

### Przykład 1
```
PS C:\> Get-AzBillingInvoice -Latest
```

Pobierz najnowszą fakturę za subskrypcję.

### Przykład 2
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Pobierz fakturę subskrypcji o określonej nazwie.

### Przykład 3
```
PS C:\> Get-AzBillingInvoice
```

Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, począwszy od najnowszej faktury bez pobierania adresu URL. 

### Przykład 4
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Uzyskaj najnowsze 10 faktur subskrypcji i uwzględnij w wyniku adres URL pobierania.

### Przykład 5
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Uzyskaj określoną fakturę według nazwy i dołącz adres URL pobierania w wyniku.

### Przykład 6
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Pobieraj faktury według nazwy konta rozliczeniowego i uwzględnij w wyniku adres URL każdej faktury.

### Przykład 7
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Uzyskaj określoną fakturę według nazwy faktury i nazwy konta rozliczeniowego oraz dołącz adres URL pobierania każdej faktury w wyniku.

### Przykład 8
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Uzyskaj najnowszą fakturę według nazwy konta rozliczeniowego i uwzględnij w wyniku adres URL faktury.

### Przykład 9
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Uzyskaj najnowsze 10 faktur z konkretnego konta rozliczeniowego i określonego profilu rozliczeniowego oraz uwzględnij w wynikach adres URL pobierania.

### Przykład 10
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

Uzyskaj najnowszą fakturę według nazwy konta rozliczeniowego i nazwy profilu rozliczeniowego oraz uwzględnij w wyniku adres URL pobierania faktury.

### Przykład 10
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

Uzyskaj faktury według nazwy konta rozliczeniowego i nazwy profilu rozliczeniowego dla okresu rozliczeniowego określonego przez datę rozpoczęcia i datę zakończenia okresu.


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

### — najnowsza wersja
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
Określa maksymalną liczbę rekordów do zwrócenia.

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

### — Nazwa
Nazwa określonej faktury do uzyskania lub najnowsza, jeśli nie jest określona.

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
Nazwa konkretnego konta rozliczeniowego, na które chcesz uzyskać faktury.

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
Nazwa konkretnego profilu rozliczeniowego, za który chcesz uzyskać faktury.

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
Data zakończenia faktury.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### Microsoft.Azure.Commands.Billing.Models.PSInvoice

## NOTATKI

## LINKI POKREWNE
