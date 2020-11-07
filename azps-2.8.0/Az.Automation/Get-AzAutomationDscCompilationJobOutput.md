---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 7a39d010759228e15dd5aee36788f9373ab879bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706830"
---
# Get-AzAutomationDscCompilationJobOutput

## STRESZCZENIe
Pobiera strumienie rejestrowania zadania kompilacji DSC usługi Automation.

## POLECENIA

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationDscCompilationJobOutput** pobiera rekordy strumieniowe zadania kompilacji DSC (żądana konfiguracja stanu) w usłudze Azure Automation.

## Przykłady

### Przykład 1. Pobierz dzienniki zadania kompilacji DSC
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

Pierwsze polecenie pobiera zadania kompilacji na koncie usługi Automation o nazwie Contoso17 przy użyciu polecenia cmdlet Get-AzAutomationDscCompilationJob.
Polecenie zapisuje te obiekty w zmiennej $Jobs.
Drugie polecenie pobiera dane wyjściowe zadania kompilacji dla dowolnego strumienia dla pierwszego członka tablicy $Jobs.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji zawierającego zadanie kompilacji DSC.

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

### -ID
Określa unikatowy identyfikator zadania kompilacji DSC, dla którego to polecenie cmdlet pobiera dane wyjściowe.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej zadanie kompilacji DSC, dla którego to polecenie cmdlet pobiera rekordy strumieniowe.

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
To polecenie cmdlet pobiera rekordy strumieniowe, które zadanie kompilacji DSC jest wyprowadzane po upływie tego czasu.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stream
Określa typ strumienia danych wyjściowych, które są pobierane przez to polecenie cmdlet.
Prawidłowe wartości: 
- Jakieś 
- Ostrzeżenie 
- Błędów 
- Pełne

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. GUID

### Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType

### System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. JobStream

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAutomationDscCompilationJob](./Get-AzAutomationDscCompilationJob.md)

[Start — AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


