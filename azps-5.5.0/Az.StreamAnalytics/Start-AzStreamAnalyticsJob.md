---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182915"
---
# Start-AzStreamAnalyticsJob

## SYNOPSIS
Uruchamia zadanie analizy strumieniowej.

## SKŁADNIA

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Start-AzStreamAnalyticsJob** asynchronicznie wdraża i uruchamia zadanie analizy strumienia na platformie Azure.

## PRZYKŁADY

### Przykład 1. Uruchamianie zadania analizy strumieniowej
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

To polecenie uruchamia zadanie StreamingJob i określa, że strumienie zdarzeń wyjściowych powinny rozpoczynać się w sygnaturze czasowej 2014-07-03T01:00Z.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Nazwa
Określa nazwę zadania Azure Stream Analytics, które ma się rozpocząć.

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

### -OutputStartMode
Określa tryb uruchamiania zadania.
Prawidłowe wartości to: 
- JobStartTime — ta wartość wskazuje, że punkt początkowy wyjściowego strumienia zdarzeń powinien się rozpocząć po uruchomieniu zadania.
- CustomTime — ta wartość wskazuje, że punkt początkowy strumieniowego zdarzenia wyjściowego powinien rozpoczynać się w niestandardowej godzinie określonej w parametrze *OutputStartTime.* 
 - LastOutputEventTime — ta wartość wskazuje, że punkt początkowy strumieniowego zdarzenia wyjściowego powinien rozpoczynać się od ostatniego czasu wyjściowego zdarzenia.
Jeśli właściwość jest nieobecna, wartością domyślną jest JobStartTime.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputStartTime
Określa czas rozpoczęcia.
Ta wartość jest albo sformatowaną sygnaturą czasową ISO-8601, która wskazuje punkt początkowy wyjściowego strumienia zdarzeń, albo $Null, aby wskazać, że wyjściowy strumień zdarzeń będzie odtwarzany po każdym uruchomieniu zadania przesyłania strumieniowego.
Jeśli dla właściwości *OutputStartMode* ustawiono wartość CustomTime, ta właściwość musi mieć wartość.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy zadanie Azure Stream Analytics.

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

### System.String

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUTS

### System.Boolean

## NOTATKI

## LINKI POKREWNE

[Get-AzStreamAnalyticsJob](./Get-AzStreamAnalyticsJob.md)

[New-AzStreamAnalyticsJob](./New-AzStreamAnalyticsJob.md)

[Remove-AzStreamAnalyticsJob](./Remove-AzStreamAnalyticsJob.md)

[Stop-AzStreamAnalyticsJob](./Stop-AzStreamAnalyticsJob.md)


