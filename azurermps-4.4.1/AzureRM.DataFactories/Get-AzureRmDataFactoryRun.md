---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: db3992a8df2cbd27c560827a702f9562e64ddcb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719350"
---
# Get-AzureRmDataFactoryRun

## STRESZCZENIe
Powoduje uruchomienie wycinka danych zestawu danych w fabryce Azure Data Factory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByFactoryName (domyślny)
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDataFactoryRun** pobiera wycinek danych dla zestawu danych w usłudze Azure Data Factory.
Zestaw danych w fabryce danych składa się z wycinków na osi czasu.
Szerokość wycinka jest określana przez harmonogram — co godzinę lub codziennie.
Uruchomienie to jednostka przetwarzania wycinka.
W przypadku ponowienia prób lub ponownego uruchomienia wycinka z powodu błędów można wykonać co najmniej jeden z nich.
Plasterek jest identyfikowany według godziny rozpoczęcia.
Aby uzyskać godzinę rozpoczęcia wycinka, użyj polecenia cmdlet Get-AzureRmDataFactorySlice.

Aby na przykład uzyskać dostęp do następującego wycinka, użyj godziny rozpoczęcia 2015-04 — 02T20:00:00.

ResourceGroupName: ADF datafactoryname: SPDataFactory0924 DataSetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM koniec: 5/3/2014 8:00:00 PM RetryCount: 0 status: gotowe LatencyStatus:

## Przykłady

### Przykład 1: uzyskiwanie zestawu danych
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

To polecenie pobiera wszystkie działania dla wycinków zestawu danych o nazwie DAWikiAggregatedData w fabryce danych o nazwie WikiADF, które zaczynają się od 4 PM GMT w 05/21/2014.

## PARAMETRÓW

### -DataFactory
Określa obiekt **PSDataFactory** .
To polecenie cmdlet jest uruchamiane dla wycinków należących do fabryki danych, którą określa ten parametr.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datafactoryname
Określa nazwę fabryki danych.
To polecenie cmdlet jest uruchamiane dla wycinków należących do fabryki danych, którą określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataSetName
Określa nazwę zestawu danych.
To polecenie cmdlet jest uruchamiane dla wycinków należących do zestawu danych, który określa ten parametr.

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
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet umożliwia uruchomienie fabryki dla wycinków należących do grupy, której ten parametr określa.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDateTime
Określa początek okresu jako obiekt **DateTime** .
To polecenie cmdlet zostanie uruchomione dla wycinków danych, które pasują do tego przedziału czasu.

*StartDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00 – 08 – 00 (pacyficzny czas standardowy)

Domyślnym wyznaczaniem strefy czasowej jest czas UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
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

### System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft. platformy windowsazure. Commands. Commands, Version = 0.8.2.0, Culture = neutral; PublicKeyToken = 31bf3856ad364e35]]

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Get-AzureRmDataFactorySlice](./Get-AzureRmDataFactorySlice.md)


