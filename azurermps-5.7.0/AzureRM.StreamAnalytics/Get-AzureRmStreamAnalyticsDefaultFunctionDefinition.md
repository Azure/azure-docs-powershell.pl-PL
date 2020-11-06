---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: bc04c78538e808ce67813a3d706c35817102cfc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542135"
---
# Get-AzureRmStreamAnalyticsDefaultFunctionDefinition

## STRESZCZENIe
Pobiera domyślną definicję funkcji w analizie strumienia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** pobiera domyślną definicję funkcji w usłudze Azure Stream Analytics.
Do tworzenia funkcji można użyć definicji domyślnej i polecenia cmdlet New-AzureRmStreamAnalyticsFunction.
Możesz zmodyfikować definicję domyślną przed utworzeniem funkcji.

## Przykłady

### Przykład 1: uzyskiwanie domyślnej definicji funkcji Stream Analytics
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

To polecenie pobiera domyślną definicję funkcji o nazwie ScoreTweet przy użyciu parametrów określonych w RetrieveDefaultDefinitionRequest.jsw pliku.

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

### -File (plik)
Określa ścieżkę pliku JSON zawierającego reprezentację treści żądania dla żądania pobrania definicji funkcji domyślnej (JSON).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Określa nazwę zadania Stream Analytics, do którego należą funkcje.
To polecenie cmdlet pobiera domyślną definicję funkcji w zadaniu, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę funkcji Stream Analytics, dla której to polecenie cmdlet pobiera definicję domyślną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należą funkcje funkcji Analiza strumienia.
To polecenie cmdlet umożliwia pobieranie definicji funkcji dla grupy, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. StreamAnalytics. models. PSFunction

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmStreamAnalyticsFunction](./New-AzureRmStreamAnalyticsFunction.md)


