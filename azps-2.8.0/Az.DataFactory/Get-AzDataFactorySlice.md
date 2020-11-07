---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a4f83bf560af1643d2971ed7644089cee26759c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706038"
---
# Get-AzDataFactorySlice

## STRESZCZENIe
Pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.

## POLECENIA

### ByFactoryName (domyślny)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDataFactorySlice** pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.
Określ godzinę rozpoczęcia i godzinę zakończenia w celu zdefiniowania zakresu wycinków danych do wyświetlenia.
Stan wycinka danych jest jednym z następujących wartości: 
- PendingExecution.
Nie rozpoczęto przetwarzania danych. 
- W trakcie.
Trwa przetwarzanie danych. 
- Dostarczenia.
Przetwarzanie danych zostało zakończone.
Wycinek danych jest gotowy do użycia w wycinkach zależnych. 
- Nie powiodło się.
Uruchomienie tego wycinka nie powiodło się. 
- Przeskok.
Fabryka danych pomija przetwarzanie wycinka. 
- Ponów.
Ponowna instalacja fabryki danych, która tworzy plasterek. 
- Przekroczenie limitu czasu. Upłynął limit czasu przetwarzania danych. 
- PendingValidation.
Przed przetworzeniem wycinka danych czeka na sprawdzenie poprawności. 
- Spróbuj ponownie wykonać weryfikację.
Fabryka danych ponawia weryfikację wycinka. 
- Sprawdzanie poprawności nie powiodło się.
Sprawdzanie poprawności wycinka nie powiodło się.
W przypadku każdego wycinka możesz wyświetlić więcej informacji na temat uruchamiania, które tworzą plasterek przy użyciu Get-AzDataFactoryRun polecenia cmdlet.

## Przykłady

### Przykład 1: pobieranie wycinków danych dla zestawu danych
```
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

To polecenie pobiera wszystkie wycinki danych dla zestawu danych o nazwie WikiAggregatedData w fabryce danych o nazwie WikiADF.
Polecenie pobiera wycinków wygenerowanych po upływie czasu, który określa parametr StartDateTime.
Poniższy przykładowy kod określa dostępność tego zestawu danych co godzinę w pliku notacji języka JavaScript (kod JSON).
dostępność: {period: "godzina"; periodMultiplier: 1} Niektóre wyniki są gotowe, a inne są PendingExecution.
Gotowe plasterki są już uruchomione.
Oczekujące plasterki oczekują na wykonanie na końcu każdej godziny w interwale, w którym określono polecenie cmdlet Set-AzDataFactoryPipelineActivePeriod.
W tym przykładzie zarówno okresy rozpoczęcia i zakończenia rurociągu oraz wycinka mają wartość jednego dnia (24 godziny).

## PARAMETRÓW

### -DataFactory
Określa obiekt **PSDataFactory** .
To polecenie cmdlet umożliwia pobieranie wycinków należących do fabryki danych, którą określa ten parametr.

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
To polecenie cmdlet umożliwia pobieranie wycinków należących do fabryki danych, którą określa ten parametr.

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
Określa nazwę zestawu danych, dla którego to polecenie cmdlet pobiera plasterki.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -EndDateTime
Określa koniec okresu jako obiekt **DateTime** .
To polecenie cmdlet umożliwia pobieranie wycinków wyprodukowanych przed upływem czasu, jaki ten parametr określi.
Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .
*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00 – 08:00 (czas standardowy)

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet umożliwia pobieranie wycinków należących do grupy, którą określa ten parametr.

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
To polecenie cmdlet umożliwia pobieranie wycinków wygenerowanych po upływie czasu, jaki ten parametr określa.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## WYSYŁA

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


