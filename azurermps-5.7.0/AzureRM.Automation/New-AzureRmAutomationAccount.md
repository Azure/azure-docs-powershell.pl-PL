---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527137"
---
# New-AzureRmAutomationAccount

## STRESZCZENIe
Tworzy konto usługi Automation.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmAutomationAccount** tworzy konto usługi Azure Automation w grupie zasobów.

Konto usługi Automation to kontener zasobów automatyzacji odizolowanych od zasobów innych kont automatyzacji. Zasoby automatyzacji obejmują elementy Runbook, konfiguracje (wymagane) konfiguracji stanu (DSC), zadania i zasoby.

## Przykłady

### Przykład 1. Tworzenie konta usługi Automation
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

To polecenie tworzy nowe konto usługi Automation o nazwie ContosoAutomationAccount w regionie wschód USA.

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

### — Lokalizacja
Określa lokalizację, w której to polecenie cmdlet tworzy konto automatyzacji.
Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRMLocation.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konta automatyzacji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Określa plan konta automatyzacji.
Prawidłowe wartości:

- Podstawowym
- Niezależnych

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której to polecenie cmdlet dodaje konto usługi Automation.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagi
Pary klucz-wartość w formie tabeli skrótów. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. AutomationAccount

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmAutomationAccount](./Get-AzureRmAutomationAccount.md)

[Remove-AzureRmAutomationAccount](./Remove-AzureRmAutomationAccount.md)

[Set-AzureRmAutomationAccount](./Set-AzureRmAutomationAccount.md)
