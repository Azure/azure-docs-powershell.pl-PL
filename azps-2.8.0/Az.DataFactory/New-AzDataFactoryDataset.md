---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 1d03ba1e4b025be933fd9cd409270d8deb93d1d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705997"
---
# New-AzDataFactoryDataset

## STRESZCZENIe
Tworzy zestaw danych w fabryce danych.

## POLECENIA

### ByFactoryName (domyślny)
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzDataFactoryDataset** tworzy zestaw danych w fabryce Azure Data Factory.
Jeśli określisz nazwę dla zestawu danych, który już istnieje, to polecenie cmdlet monituje o potwierdzenie przed zastąpieniem zestawu danych.
Jeśli określisz parametr *Force* , polecenie cmdlet zastępuje istniejący zestaw danych bez potwierdzenia.
Wykonuj następujące operacje w następującej kolejności: 
- Tworzenie fabryki danych. 
- Tworzenie połączonych usług. 
- Tworzenie zestawów danych. 
- Utwórz rurociąg.
Jeśli zestaw danych o takiej samej nazwie już istnieje w fabryce danych, to polecenie cmdlet wyświetli monit o potwierdzenie zamiaru zastąpienia istniejącego zestawu danych nowym zestawem danych.
Jeśli potwierdzisz zastąpienie istniejącego zestawu danych, definicja zestawu danych również zostanie zastąpiona.

## Przykłady

### Przykład 1. Tworzenie zestawu danych
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

To polecenie tworzy zestaw danych o nazwie DA_WikipediaClickEvents w fabryce danych o nazwie WikiADF.
Polecenie opiera się na zestawie danych na temat informacji zawartych w DAWikipediaClickEvents.jspliku.

### Przykład 2: Wyświetlanie dostępności nowego zestawu danych
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

Pierwsze polecenie powoduje utworzenie zestawu danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisanie tego zestawu danych do zmiennej $Dataset.
Drugie polecenie używa standardowego zapisu kropkowego, aby wyświetlić szczegółowe informacje o właściwości dostępności zestawu danych.

### Przykład 3: Wyświetlanie lokalizacji nowego zestawu danych
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

Pierwsze polecenie powoduje utworzenie zestawu danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisanie tego zestawu danych do zmiennej $Dataset.
Drugie polecenie wyświetla szczegółowe informacje dotyczące właściwości lokalizacja zestawu danych.

### Przykład 4: Wyświetlanie reguł sprawdzania poprawności dla nowego zestawu danych
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

Pierwsze polecenie powoduje utworzenie zestawu danych o nazwie DA_WikipediaClickEvents, tak jak w poprzednim przykładzie, a następnie przypisanie tego zestawu danych do zmiennej $Dataset.
Drugie polecenie pobiera szczegóły dotyczące reguł poprawności dla zestawu danych, a następnie przekazuje je do polecenia cmdlet Format-List przy użyciu operatora potoku.
To polecenie cmdlet programu Windows PowerShell formatuje wyniki.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Format-List` .

## PARAMETRÓW

### -DataFactory
Określa obiekt **PSDataFactory** .
To polecenie cmdlet powoduje utworzenie zestawu danych w fabryce danych, który określa ten parametr.

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
To polecenie cmdlet powoduje utworzenie zestawu danych w fabryce danych, który określa ten parametr.

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

### -File (plik)
Określa pełną ścieżkę do pliku notacji JavaScript (kod JSON) zawierającego opis zestawu danych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wskazuje, że to polecenie cmdlet Zamienia istniejący zestaw danych bez monitowania o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę zestawu danych, który ma zostać utworzony.

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

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet powoduje utworzenie zestawu danych w grupie, którą ten parametr określa.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## WYSYŁA

### Microsoft.Azure.Commands.DataFactories.Models.PSDataset

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Get-AzDataFactoryDataset](./Get-AzDataFactoryDataset.md)

[Remove-AzDataFactoryDataset](./Remove-AzDataFactoryDataset.md)


