---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 2f4fd8c81cadd890cd17f2dd8d6db77c0eef5283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996941"
---
# Get-AzAutomationJobOutputRecord

## SYNOPSIS
Pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.

## SKŁADNIA

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzAutomationJobOutputRecord** pobiera pełne dane wyjściowe rekordu wyjściowego zadania automatyzacji.
Mimo że **polecenie cmdlet Get-AzAutomationJobOutput** wyświetla jeden lub więcej rekordów wyjściowych zadań, zwraca tylko podsumowanie wartości dowolnego rekordu wyjściowego jako ciąg.
Nie zwraca pełnej wartości wartości wyjściowej rekordu wyjściowego w oryginalnym typie.
Ponadto podsumowanie ma maksymalną długość, która może przekraczać pełną wartość w wynikach tego polecenia cmdlet.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie pełnych wyników zadania automatyzacji
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

To polecenie pobiera pełne dane wyjściowe zadania o określonym identyfikatorze zadania.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet uzyskuje rekord wyjściowy zadania.

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
Określa identyfikator rekordu wyjściowego zadania dla tego polecenia cmdlet do pobrania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - JobId
Określa identyfikator zadania, dla którego to polecenie cmdlet uzyskuje rekord wyjściowy.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, dla której to polecenie cmdlet uzyskuje rekord wyjściowy zadania.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.Guid

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.JobStreamRecord

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)


