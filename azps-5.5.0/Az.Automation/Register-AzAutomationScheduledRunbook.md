---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6f53573c6eb737d280ac24182ed84158d63d132f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239611"
---
# Register-AzAutomationScheduledRunbook

## SYNOPSIS
Kojarzy podręcznik z harmonogramem.

## SKŁADNIA

### ByRunbookName (Domyślna)
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Register-AzAutomationScheduledRunbook** kojarzy podręcznik Azure Automation z harmonogramem.
Runbook zostanie uruchomiony na podstawie harmonogramu, który określisz przy użyciu *parametru ScheduleName.*

## PRZYKŁADY

### Przykład 1. Kojarzenie podręcznika z harmonogramem
```powershell
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

To polecenie skojarzy podręcznik o nazwie Runbk01 z harmonogramem o nazwie Sched01 na koncie usługi Azure Automation o nazwie Contoso17.

### Przykład 2

Kojarzy podręcznik z harmonogramem. (wygenerowane automatycznie)

<!-- Aladdin Generated Example -->
```powershell
Register-AzAutomationScheduledRunbook -AutomationAccountName 'Contoso17' -Parameters <IDictionary> -ResourceGroupName 'ResourceGroup01' -RunbookName 'Runbk01' -ScheduleName 'Sched01'
```

## PARAMETERS

### -AutomationAccountName
Określa konto automatyzacji dla podręcznika, na którym działa to polecenie cmdlet.

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

### — Parametry
Określa tabelę skrótów par klucz/wartość.
Klucze to nazwy parametrów podręcznika uruchamiania.
Wartości są wartościami parametrów podręcznika uruchamiania.
Po uruchomieniu podręcznika w odpowiedzi na skojarzony harmonogram te parametry są przekazywane do podręcznika.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów dla zaplanowanego podręcznika.

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
Określa nazwę podręcznika, który skojarzy to polecenie cmdlet z harmonogramem.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - RunOn
Nazwa grupy pracowników hybrydowego podręcznika.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Określa nazwę harmonogramu, z którym to polecenie cmdlet skojarzy podręcznik.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.JobSchedule

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationScheduledRunbook](./Get-AzAutomationScheduledRunbook.md)

[Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md)


