---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 990cd9d10dd90ee68c179fa65ea4d0575bdda1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527178"
---
# Stop-AzureRmStreamAnalyticsJob

## STRESZCZENIe
Zatrzymuje zadanie analizy strumienia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **stop-AzureRmStreamAnalyticsJob** asynchronicznie zatrzymuje działanie funkcji Stream Analytics na platformie Azure i derezerwuje zasoby, które były używane.
Definicja zadania i metadane pozostają dostępne w ramach abonamentu za pośrednictwem interfejsów API portalu i zarządzania Azure, takich jak zadanie można edytować i ponownie uruchomić.
Nie zostanie naliczona opłata za zadanie w stanie zatrzymania.

## Przykłady

### PRZYKŁAD 1: Zatrzymywanie uruchomionego zadania
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

To polecenie zatrzymuje zadanie StreamingJob.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać zatrzymane.

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

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.

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

### System. Object

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[Get-AzureRmStreamAnalyticsJob](./Get-AzureRmStreamAnalyticsJob.md)

[Nowe — AzureRmStreamAnalyticsJob](./New-AzureRmStreamAnalyticsJob.md)

[Remove-AzureRmStreamAnalyticsJob](./Remove-AzureRmStreamAnalyticsJob.md)

[Start — AzureRmStreamAnalyticsJob](./Start-AzureRmStreamAnalyticsJob.md)


