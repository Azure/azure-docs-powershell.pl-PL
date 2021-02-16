---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184986"
---
# Add-AzLogProfile

## SYNOPSIS
Tworzy nowy profil dziennika aktywności. Ten profil służy do archiwizowania dziennika aktywności na koncie magazynu platformy Azure lub strumieniowego przesyłania go do centrum zdarzeń platformy Azure w tej samej subskrypcji. 

## SKŁADNIA

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzLogProfile** tworzy profil dziennika.
- **Konto magazynu** — obsługiwane jest tylko standardowe konto magazynu (konto magazynu premium nie jest obsługiwane). Może to być typ ARM klasyczny. Jeśli jest on zalogowany na koncie magazynu, koszt przechowywania dziennika działań jest rozliczany przy normalnych standardowych stawkach przestrzeni dyskowej. W konsekwencji do wyeksportowania dziennika aktywności może być użyte tylko jedno konto magazynu na subskrypcję. 
- **Centrum zdarzeń** — w ramach jednej subskrypcji może być tylko jeden profil dziennika, w konsekwencji tylko jedno centrum zdarzeń na subskrypcję może zostać użyte do wyeksportowania dziennika aktywności. Jeśli dziennik aktywności jest przesyłany strumieniowo do centrum zdarzeń, będą obowiązywały standardowe ceny centrum wydarzeń. W dzienniku aktywności zdarzenia mogą dotyczyć regionu lub mogą być "globalne". Globalnie oznacza, że te zdarzenia są agnostykami regionów i są niezależne od regionu, w rzeczywistości większość zdarzeń należy do tej kategorii. Jeśli profil dziennika aktywności jest ustawiony w portalu, niejawnie dodaje on wartość "Global" wraz z dowolnym innym regionem wybranym w interfejsie użytkownika. Podczas korzystania z polecenia cmdlet należy jawnie wspomnieć o lokalizacji jako "globalnej" poza dowolnym innym regionem. 
**Uwaga** :- **Jeśli nie ustawisz pozycji "Global"** w lokalizacjach, większość dziennika aktywności nie zostanie wyeksportowana. To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed jego utworzeniem, zmodyfikowaniem lub usunięciem.

## PRZYKŁADY

### Przykład 1. Dodawanie nowego profilu dziennika w celu wyeksportowania dziennika działań spełniającego warunek lokalizacji do konta magazynu
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### Przykład 2

Tworzy nowy profil dziennika aktywności. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETERS

### — Kategoria
Określa listę kategorii.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### — Lokalizacja
Określa lokalizację profilu dziennika.
Prawidłowe wartości: Uruchom poniżej polecenia cmdlet, aby uzyskać najnowszą listę lokalizacji. Get-AzLocation | Wybierz pozycję DisplayName (Nazwa wyświetlana)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę profilu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Określa zasady przechowywania w dniach. Jest to liczba dni zachowywania dzienników na określonym koncie magazynu. Aby zachować dane na zawsze, ustaw wartość **0.** Jeśli nie zostanie określone, wartość domyślna to **0.** W przypadku przechowywania danych będą obowiązywały standardowe stawki za magazyn lub centrum wydarzeń.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Określa identyfikator reguły autobusu usług.

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

### - StorageAccountId
Określa identyfikator konta magazynu. Identyfikator to w pełni kwalifikowany identyfikator zasobu konta magazynu, na przykład  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## NOTATKI

## LINKI POKREWNE

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


