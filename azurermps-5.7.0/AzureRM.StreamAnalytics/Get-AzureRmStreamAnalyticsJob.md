---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542132"
---
# Get-AzureRmStreamAnalyticsJob

## STRESZCZENIe
Pobiera informacje o zadaniach analizy strumienia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByResourceGroup
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySubscription
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmStreamAnalyticsJob** wyświetla wszystkie zadania analizy strumienia zdefiniowane w subskrypcji platformy Azure lub określonej grupie zasobów albo pobiera informacje o zadaniach dotyczących określonego zadania w grupie zasobów.

## Przykłady

### PRZYKŁAD 1: uzyskiwanie informacji o wszystkich zadaniach w ramach abonamentu
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

To polecenie zwraca informacje na temat wszystkich zadań analizy strumienia w ramach subskrypcji platformy Azure.

### PRZYKŁAD 2: uzyskiwanie informacji o wszystkich zadaniach w grupie zasobów
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

To polecenie zwraca informacje na temat wszystkich zadań analizy strumienia w grupie zasób StreamAnalytics-default-zachód-my.

### PRZYKŁAD 3: uzyskiwanie informacji o konkretnym zadaniu w grupie zasobów
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

To polecenie zwraca informacje o zadaniu Stream Analytics StreamingJob w grupie zasób StreamAnalytics-default-zachód-USA.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać pobrane.

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NOEXPAND
Wskazuje, że polecenie cmdlet będzie pobierać zadanie usługi Azure Stream Analytics, ale nie zwraca informacji na temat danych wejściowych, wyjść i transformacji.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSJob, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSJob

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Start — AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)

[Zatrzymaj — AzureRmStreamAnalyticsJob](./Stop-AzureRmStreamAnalyticsJob.md)


