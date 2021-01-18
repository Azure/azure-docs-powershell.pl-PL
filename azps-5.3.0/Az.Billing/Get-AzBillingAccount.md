---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504279"
---
# Get-AzBillingAccount

## STRESZCZENIe
Pobierz konta rozliczeniowe.

## POLECENIA

### Lista (domyślna)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Jedn
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzBillingAccount** pobiera konta rozliczeniowe, do których użytkownik ma dostęp. 

## Przykłady

### Przykład 1
```
PS C:\> Get-AzBillingAccount
```

Pobierz wszystkie konta rozliczeniowe, do których ma dostęp użytkownik.

### Przykład 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Pobierz konto rozliczeniowe o określonej nazwie.

### Przykład 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Pobierz wszystkie konta rozliczeniowe, do których użytkownik ma dostęp, i Dołącz ten adres do wyniku.

### Przykład 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Pobierz wszystkie konta rozliczeniowe, do których jest dostęp, i Dołącz do nich profile rozliczeń.

### Przykład 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Pobierz wszystkie konta rozliczeniowe, do których masz dostęp, i Dołącz do nich sekcje Profile rozliczeń i faktury.

### Przykład 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Pobierz konto rozliczeniowe o określonej nazwie, a następnie w wynikach Uwzględnij adres, profile rozliczeń i faktury.

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

### -IncludeAddress
Uwzględnij adres konta rozliczeniowego.

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

### -ExpandBillingProfile
Uwzględnij profile rozliczeń w obszarze konto rozliczeniowe.

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

### -ExpandInvoiceSection
Uwzględnij profile rozliczeń w sekcji konto rozliczeniowe i faktury pod nimi.

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

### -Name (nazwa)
Nazwa określonego konta rozliczeniowego.

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

### -ListEntitiesToCreateSubscription
Wystaw jednostki rozliczeniowe w obszarze konto rozliczeniowe, których można użyć jako danych wejściowych w celu utworzenia subskrypcji.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
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

### Microsoft. Azure. Commands. rozliczenia. modele. PSBillingAccount

## INFORMACYJN

## LINKI POKREWNE
