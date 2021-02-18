---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201203"
---
# Get-AzAutomationDscCompilationJobOutput

## SYNOPSIS
Pobiera strumienie rejestrowania zadania kompilacji dsc automatyzacji.

## SKŁADNIA

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzAutomationDscCompilationJobOutput** pobiera rekordy strumienia zadania kompilacji APS Desired State Configuration (DSC) w usłudze Azure Automation.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie dzienników dla zadania kompilacji dsc
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

Pierwsze polecenie pobiera zadania kompilacji na koncie automatyzacji o nazwie Contoso17 przy użyciu Get-AzAutomationDscCompilationJob cmdlet.
Polecenie przechowuje te obiekty w $Jobs zmienną.
Drugie polecenie pobiera dane wyjściowe zadania kompilacji dla dowolnego strumienia dla pierwszego członka $Jobs tablicy.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji zawierającego zadanie kompilacji dsc.

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

### — Identyfikator
Określa unikatowy identyfikator zadania kompilacji dsc, dla którego jest wyprowadzone to polecenie cmdlet.

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
Określa nazwę grupy zasobów zawierającej zadanie kompilacji dsc, dla którego to polecenie cmdlet pobiera rekordy strumienia.

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

### — StartTime
Określa czas rozpoczęcia.
To polecenie cmdlet pobiera rekordy strumieniowe, których dane wyjściowe zadania kompilacji dsc są po tym czasie.

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

### — Stream
Określa typ strumienia dla wyniku, który otrzymuje to polecenie cmdlet.
Prawidłowe wartości to: 
- Dowolna 
- Ostrzeżenie 
- Błąd 
- Pełne słownictwo

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.Guid

### Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType

### System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.JobStream

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationDscCompilationJob](./Get-AzAutomationDscCompilationJob.md)

[Start-AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)


