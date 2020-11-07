---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 2444579c8a155cc2957ab8432eb63cc28300bfe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706800"
---
# Get-AzAutomationScheduledRunbook

## STRESZCZENIe
Pobiera elementy Runbook funkcji Automation i skojarzone harmonogramy.

## POLECENIA

### ByAll (domyślny)
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationScheduledRunbook** pobiera co najmniej jeden element Runbook usługi Azure Automation i skojarzone harmonogramy.
Domyślnie to polecenie cmdlet pobiera wszystkie zaplanowane elementy Runbook.
Określ nazwę elementu Runbook lub harmonogram albo oba te elementy, aby wyświetlić określone harmonogramy elementu Runbook.

## Przykłady

### Przykład 1: pobieranie wszystkich zaplanowanych elementów Runbook
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

To polecenie pobiera wszystkie zaplanowane elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.

### Przykład 2: pobieranie wszystkich harmonogramów skojarzonych z elementem Runbook
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

To polecenie pobiera wszystkie zaplanowane elementy Runbook dla elementu Runbook Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.

### Przykład 3: pobieranie wszystkich elementów Runbook skojarzonych z harmonogramem
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

To polecenie pobiera wszystkie zaplanowane elementy Runbook dla Schedule01 harmonogram na koncie usługi Azure Automation o nazwie Contoso17.

## PARAMETRÓW

### -AutomationAccountName
Określa konto usługi Automation dla elementu Runbook, dla którego działa to polecenie cmdlet.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobScheduleId
Określa identyfikator zaplanowanego zadania, które jest pobierane przez to polecenie cmdlet.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów dla zaplanowanych elementów Runbook, które są pobierane przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Element runbookname
Określa nazwę elementu Runbook, dla którego ten aplet polecenia pobiera zaplanowane elementy Runbook.

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Określa nazwę harmonogramu, dla którego ten aplet polecenia pobiera zaplanowane elementy Runbook.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. JobSchedule

## INFORMACYJN

## LINKI POKREWNE

[Rejestr — AzAutomationScheduledRunbook](./Register-AzAutomationScheduledRunbook.md)

[Wyrejestrowanie — AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md)


