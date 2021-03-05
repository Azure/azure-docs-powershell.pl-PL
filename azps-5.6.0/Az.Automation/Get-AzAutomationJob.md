---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 378bab1d62d5abcfb1eb2506e41d22bf26b217b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996955"
---
# Get-AzAutomationJob

## SYNOPSIS
Otrzymuje zadania podręcznika automatyzacji.

## SKŁADNIA

### ByAll (Domyślne)
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzAutomationJob** otrzymuje zadania podręcznika w usłudze Azure Automation.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie określonego zadania podręcznika
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

To polecenie otrzymuje zadanie o określonym identyfikatorze GUID.

### Przykład 2. Uzyskiwanie wszystkich zadań dla podręcznika uruchamiania
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

To polecenie pobiera wszystkie zadania skojarzone z podręcznikiem runbook o nazwie Runbook02.

### Przykład 3. Uzyskiwanie wszystkich uruchomionych zadań
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

To polecenie pobiera wszystkie uruchomione zadania na koncie automatyzacji o nazwie Contoso17.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet otrzymuje zadania.

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

### - EndTime
Określa czas zakończenia zadania jako obiekt **DateTimeOffset.**
Możesz określić ciąg, który może zostać przekonwertowany na prawidłowy **dateTimeOffset.**
To polecenie cmdlet pobiera zadania, które mają czas zakończenia na lub przed wartością, która określa ten parametr.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Identyfikator
Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której to polecenie cmdlet otrzymuje zadania.

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

### -RunbookName
Określa nazwę podręcznika, dla którego to polecenie cmdlet otrzymuje zadania.

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — StartTime
Określa czas rozpoczęcia zadania jako obiekt **DateTimeOffset.**
To polecenie cmdlet pobiera zadania, których godzina rozpoczęcia jest określana przez ten parametr lub po tej wartości.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Status
Określa stan zadania.
To polecenie cmdlet pobiera zadania, które mają stan zgodny z tym parametrem.
Prawidłowe wartości to: 
- Aktywacja
- Ukończono
- Niepowodzenie
- W kolejce
- Wznawianie
- Uruchomione
- Rozpoczynanie
- Zatrzymano
- Zatrzymywanie
- Wstrzymane
- Zawieszanie

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.Guid

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.Job

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)

[Resume-AzAutomationJob](./Resume-AzAutomationJob.md)

[Stop-AzAutomationJob](./Stop-AzAutomationJob.md)

[Suspend-AzAutomationJob](./Suspend-AzAutomationJob.md)


