---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502682"
---
# Get-AzStreamAnalyticsTransformation

## STRESZCZENIe
Pobiera informacje o transformacji zadania Stream Analytics.

## POLECENIA

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzStreamAnalyticsTransformation** pobiera informacje o transformacji zdefiniowanej w zadaniu Stream Analytics.

## Przykłady

### PRZYKŁAD 1: uzyskiwanie informacji o przekształceń analizy strumienia
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

To polecenie zwraca informacje o transformacji o nazwie StreamingJob w przypadku zadania o nazwie StreamingJob.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -JobName
Określa nazwę zadania usługi Azure Stream Analytics, do którego należy transformacja analizy strumienia Azure.

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

### -Name (nazwa)
Określa nazwę przekształcenia usługi Analiza strumienia Azure do pobrania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy transformacja analizy strumienia Azure.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. StreamAnalytics. models. PSTransformation

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzStreamAnalyticsTransformation](./New-AzStreamAnalyticsTransformation.md)


