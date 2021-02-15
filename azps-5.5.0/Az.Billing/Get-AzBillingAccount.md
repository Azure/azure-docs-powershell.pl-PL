---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182018"
---
# Get-AzBillingAccount

## SYNOPSIS
Uzyskaj konta rozliczeniowe.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzBillingAccount** pobiera konta rozliczeniowe, użytkownik ma do nich dostęp. 

## PRZYKŁADY

### Przykład 1
```
PS C:\> Get-AzBillingAccount
```

Uzyskaj dostęp do wszystkich kont rozliczeniowych, do których ma dostęp użytkownik.

### Przykład 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Pobierz konto rozliczeniowe o podanej nazwie.

### Przykład 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Pobierz wszystkie konta rozliczeniowe, do których użytkownik ma dostęp, i uwzględnij adres w wyniku.

### Przykład 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Uzyskaj dostęp do wszystkich kont rozliczeniowych i uwzględnij profile rozliczeniowe w wynikach.

### Przykład 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Uzyskaj dostęp do wszystkich kont rozliczeniowych i uwzględnij w wynikach sekcje dotyczące profilów rozliczeń i faktur.

### Przykład 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Uzyskaj konto rozliczeniowe o podanej nazwie i uwzględnij w wynikach sekcje adresu, profilów rozliczeń i faktur.

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
Uwzględnij profile rozliczeniowe w obszarze konta rozliczeniowego.

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
Uwzględnij profile rozliczeniowe w sekcjach konta rozliczeniowego i faktur pod nimi.

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

### — Nazwa
Nazwa konkretnego konta rozliczeniowego.

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
Utwórz listę jednostek rozliczeniowych w obszarze konta rozliczeniowego, których można użyć jako danych wejściowych do utworzenia subskrypcji.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## NOTATKI

## LINKI POKREWNE
