---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959786"
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

Pobierz wszystkie konta rozliczeniowe, do których użytkownik ma dostęp, i uwzględnij adres w wynikach.

### Przykład 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Uzyskaj dostęp do wszystkich kont rozliczeniowych i uwzględnij profile rozliczeniowe w wynikach.

### Przykład 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Uzyskaj dostęp do wszystkich kont rozliczeniowych, do których ma dostęp użytkownik, oraz uwzględnij w wynikach sekcje dotyczące faktur i profile rozliczeniowe.

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

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## NOTATKI

## LINKI POKREWNE
