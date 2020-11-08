---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051666"
---
# Get-AzAutomationDscNodeConfigurationDeployment

## STRESZCZENIe
Umożliwia pobieranie wdrożeń konfiguracji węzłów DSC w automatyzacji.

## POLECENIA

### ByAll (domyślny)
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** powoduje wdrożenie konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.

## Przykłady

### Przykład 1: pobieranie wdrożenia konfiguracji węzła
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01. Node1" na podstawie dwuwymiarowej tablicy nazw węzłów. Wdrożenie przebiega w sposób stopniowy.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.

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

### -EndTime
Filtr czasu zakończenia.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Określa identyfikator zadania istniejącego zadania wdrożenia.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.

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
Filtr czasu rozpoczęcia.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Stan filtru zadania.

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. GUID

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment

## INFORMACYJN

## LINKI POKREWNE

[Start — AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)

[Import — AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)

[Start — AzAutomationDscNodeConfigurationDeployment](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[Zatrzymaj — AzAutomationDscNodeConfigurationDeployment](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[Get-AzAutomationDscNodeConfigurationDeploymentSchedule](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
