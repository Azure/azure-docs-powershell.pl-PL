---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: 2dbab7978716d6bb960c1804abf9e86246571e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975329"
---
# Get-AzDataFactoryRun

## SYNOPSIS
Działa dla wycinka danych zestawu danych w usłudze Azure Data Factory.

## SKŁADNIA

### ByFactoryName (Default)
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDataFactoryRun** pobiera uruchamiany dla wycinka danych zestawu danych w usłudze Azure Data Factory.
Zestaw danych w zakładzie danych składa się z wycinków na osi czasu.
Szerokość wycinka jest ustalana na podstawie harmonogramu co godzinę lub raz dziennie.
Uruchomienie to jednostka przetwarzania wycinka.
W przypadku ponownego uruchomień wycinków może być jedno lub więcej uruchomień dla wycinków w przypadku ponownego uruchomień z powodu niepowodzeń.
Wycinek jest oznaczony godziną rozpoczęcia.
Aby uzyskać czas rozpoczęcia wycinka, użyj Get-AzDataFactorySlice cmdlet.
Aby na przykład uruchomić poniższy wycinek, użyj godziny rozpoczęcia 2015-04-02T20:00:00.
ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingDataaignEffectivenessBlobDataset Start: 2014-05-02 8:00:00 End: 2014-05-03 8:00:00: 0 Status: Ready LatencyStatus:

## PRZYKŁADY

### Przykład 1. Uzyskiwanie zestawu danych
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

To polecenie pobiera wszystkie uruchomienia dla wycinków zestawu danych o nazwie DAWikiAggregatedData w fabrycznej bazie danych o nazwie WikiADF, których data rozpoczęcia się od 16:00 gmt 2014-05-21.

## PARAMETERS

### -DataFactory
Określa obiekt **PSDataFactory.**
To polecenie cmdlet jest uruchamiane dla wycinków należących do fabrycznych danych określanych przez ten parametr.

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

### -DataFactoryName
Określa nazwę fabryki danych.
To polecenie cmdlet jest uruchamiane dla wycinków należących do fabrycznych danych określanych przez ten parametr.

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

### -DatasetName
Określa nazwę zestawu danych.
To polecenie cmdlet jest uruchamiane dla wycinków należących do zestawu danych, który jest określany przez ten parametr.

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

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet powoduje, że jest uruchamiane fabryczne dla wycinków należących do grupy, które określono dla tego parametru.

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
Określa początek okresu jako obiekt **DateTime.**
To polecenie cmdlet jest uruchamiane dla wycinków danych, które pasują do tego okresu.
*Wartość StartDateTime* musi zostać określona w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01 01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (pacyficzny czas standardowy) Domyślnym projektem strefy czasowej jest czas UTC.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


