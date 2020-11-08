---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054623"
---
# Get-AzureAutomationRunbook

## STRESZCZENIe

Pobiera element Runbook.

## POLECENIA

### ByAll (domyślny)
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Polecenie cmdlet **Get-AzureAutomationRunbook** pobiera co najmniej jeden element Runbook usługi Microsoft Azure Automation.
Domyślnie zostaną zwrócone wszystkie elementy Runbook.
Aby uzyskać określony element Runbook, określ jego nazwę lub identyfikator.
Aby uzyskać dostęp do wszystkich elementów Runbook połączonych z określonym harmonogramem, określ nazwę harmonogramu.

## Przykłady

### Przykład 1. pobieranie wszystkich elementów Runbook
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

To polecenie pobiera wszystkie elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta usługi Azure Automation.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę elementu Runbook.

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. Runbook

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureAutomationRunbook](./New-AzureAutomationRunbook.md)

[Publikowanie — AzureAutomationRunbook](./Publish-AzureAutomationRunbook.md)

[Remove-AzureAutomationRunbook](./Remove-AzureAutomationRunbook.md)

[Set-AzureAutomationRunbook](./Set-AzureAutomationRunbook.md)

[Start — AzureAutomationRunbook](./Start-AzureAutomationRunbook.md)


