---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719539"
---
# Get-AzureRmAutomationJobOutput

## STRESZCZENIe
Pobiera dane wyjściowe zadania automatyzacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmAutomationJobOutput** pobiera dane wyjściowe zadania usługi Azure Automation.

## Przykłady

### Przykład 1. Pobieranie danych wyjściowych zadania automatyzacji
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

To polecenie pobiera wszystkie dane wyjściowe zadania o określonym IDENTYFIKATORze.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera dane wyjściowe zadania.

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

### -ID
Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera dane wyjściowe.

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
Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera dane wyjściowe zadania.

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
Określa godzinę rozpoczęcia jako obiekt **DateTimeOffset** .
Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.
Polecenie cmdlet umożliwia pobranie danych wyjściowych utworzonych po tym czasie.

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
Określa typ danych wyjściowych.
Prawidłowe wartości: 

- Jakieś
- Wykrywanie
- Błędów
- Prowadzone
- Okres
- Pełne
- Ostrzeżenie

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. JobStream

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmAutomationJob](./Get-AzureRMAutomationJob.md)

[Życiorys — AzureRmAutomationJob](./Resume-AzureRMAutomationJob.md)

[Zatrzymaj — AzureRmAutomationJob](./Stop-AzureRMAutomationJob.md)

[Suspend — AzureRmAutomationJob](./Suspend-AzureRMAutomationJob.md)


