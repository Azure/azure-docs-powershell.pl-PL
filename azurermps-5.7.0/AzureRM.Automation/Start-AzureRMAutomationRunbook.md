---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542752"
---
# Start-AzureRmAutomationRunbook

## STRESZCZENIe
Rozpoczyna zadanie elementu Runbook.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByAsynchronousReturnJob (domyślny)
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### BySynchronousReturnJobOutput
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureRmAutomationRunbook** rozpoczyna zadanie elementu Runbook usługi Azure Automation.
Określ identyfikator lub nazwę elementu Runbook.

## Przykłady

### Przykład 1. Rozpocznij zadanie elementu Runbook
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.

### Przykład 2: Rozpoczynanie zadania elementu Runbook i oczekiwanie na wyniki
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.
To polecenie określa parametr _oczekiwania_ .
Dlatego zwraca on wyniki po wykonaniu zadania.
Polecenie cmdlet czeka maksymalnie 1000 sekund na wyniki.

## PARAMETRÓW

### -AutomationAccountName
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -MaxWaitSeconds
Określa liczbę sekund, przez jaką to polecenie cmdlet oczekuje na zakończenie zadania, zanim odrzuca to zadanie.
Wartość domyślna to 10800 lub trzy godziny.

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Parametry
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
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

### -RunOn
Określa grupę hybrydowych procesów roboczych, na której ma zostać uruchomiony element Runbook.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Czekaj
Wskazuje, że to polecenie cmdlet oczekuje na ukończenie zadania, zawieszenie lub niepowodzenie, a następnie zwróci kontrolę do środowiska Azure PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
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

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. job
To polecenie cmdlet zwraca obiekt **zadania** , chyba że podano parametr _wait_ .

Jeśli nie określisz funkcji _czekaj_ , środowisko Azure PowerShell zwraca obiekt **zadania** natychmiast.
Jeśli określisz pozycję _czekaj_ , środowisko Azure PowerShell zakończy zadanie, a następnie zwróci wynik.
Wynik nie jest obiektem **zadania** .

## INFORMACYJN

## LINKI POKREWNE

[Eksportowanie — AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[Get-AzureRmAutomationRunbook](./Get-AzureRMAutomationRunbook.md)

[Import — AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[Nowe — AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Nowe — AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Publikowanie — AzureRmAutomationRunbook](./Publish-AzureRMAutomationRunbook.md)

[Remove-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)
