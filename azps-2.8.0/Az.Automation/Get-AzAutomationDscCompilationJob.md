---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 8742b9967720948118f132de23fd07dbfdcb5f0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706828"
---
# Get-AzAutomationDscCompilationJob

## STRESZCZENIe
Pobiera zadania kompilacji DSC w automatyzacji.

## POLECENIA

### ByAll (domyślny)
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationDscCompilationJob** pobiera zadania kompilacji pożądanej konfiguracji stanu (DSC) w usłudze Azure Automation.

## Przykłady

### Przykład 1: pobieranie wszystkich zadań kompilacji DSC
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

To polecenie pobiera wszystkie zadania kompilacji na koncie usługi Automation o nazwie Contoso17.

### Przykład 2: pobieranie zadań kompilacji DSC dla konfiguracji
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

To polecenie pobiera wszystkie zadania kompilacji dla konfiguracji DSC o nazwie ContosoConfiguration na koncie automatyzacji o nazwie Contoso17.

### Przykład 3: uzyskiwanie określonego zadania kompilacji DSC
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

To polecenie pobiera zadanie kompilacji z określonym IDENTYFIKATORem na koncie usługi Automation o nazwie Contoso17.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji zawierającego zadania kompilacji DSC, które są dostępne w tym poleceniu cmdlet.

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

### -ConfigurationName
Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera zadania kompilacji.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -EndTime
Określa godzinę zakończenia.
To polecenie cmdlet umożliwia pobieranie zadań kompilacji, które zostały uruchomione do momentu, gdy ten parametr określi.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Określa unikatowy identyfikator zadania kompilacji DSC, które jest pobierane przez to polecenie cmdlet.

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
Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania kompilacji DSC.

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

### -StartTime
Określa godzinę rozpoczęcia.
To polecenie cmdlet pobiera zadania, które zaczynają się od godziny lub po upływie tego parametru.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Określa stan zadań pobieranych przez to polecenie cmdlet.
Prawidłowe wartości: 
- Zakończyć 
- Nie powiodło się 
- Oczekuje 
- Czynając 
- Działanie 
- Wykonywania 
- Trzymywanie 
- Trzymywany 
- Zawiesin 
- Zawieszeniem 
- Ponownego
- Nowy

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. GUID

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. CompilationJob

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAutomationDscCompilationJobOutput](./Get-AzAutomationDscCompilationJobOutput.md)

[Start — AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


