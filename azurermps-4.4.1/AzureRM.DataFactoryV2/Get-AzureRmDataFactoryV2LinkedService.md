---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: 7466ad5617fb78d48deb92ac2d623fc05ad90634
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553941"
---
# Get-AzureRmDataFactoryV2LinkedService

## STRESZCZENIe
Pobiera informacje o usługach połączonych w fabryce danych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByFactoryName (domyślny)
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
```
## Opis
Polecenie cmdlet Get-AzureRmDataFactoryV2LinkedService pobiera informacje o usługach połączonych w usłudze Azure Data Factory.
Jeśli określisz nazwę połączonej usługi, to polecenie cmdlet będzie pobierać informacje dotyczące tej połączonej usługi.
Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich usług połączonych w fabryce danych.

## Przykłady

### Przykład 1: uzyskiwanie informacji o wszystkich usługach połączonych
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

To polecenie pobiera informacje dotyczące wszystkich usług połączonych w fabryce danych o nazwie WikiADF, a następnie przekazuje połączone usługi do polecenia cmdlet Format-List przy użyciu operatora potoku.
To polecenie cmdlet programu Windows PowerShell formatuje wyniki.
Aby uzyskać więcej informacji, wpisz Get-Help format-lista.

Możesz użyć jednego z następujących sposobów:

### Przykład 2: uzyskiwanie informacji o konkretnej połączonej usłudze
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

To polecenie pobiera informacje o połączonej usłudze o nazwie LinkedServiceCuratedWikiData w fabryce danych o nazwie WikiADF.

### Przykład 3: uzyskiwanie informacji o konkretnej połączonej usłudze przez określenie parametru DataFactory
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Pierwsze polecenie używa polecenia cmdlet Get-AzureRmDataFactoryV2, aby uzyskać fabrykę danych o nazwie ContosoFactory, a następnie przechowywać ją w zmiennej $DataFactory.

Drugie polecenie pobiera informacje o połączonej usłudze dla fabryki danych przechowywanej w $DataFactory, a następnie przekazuje te informacje do polecenia cmdlet Format-Table za pomocą operatora potoku.
Polecenie cmdlet Format-Table formatuje dane wyjściowe jako zestaw danych o określonych właściwościach jako kolumny zestawu danych.

## PARAMETRÓW

### -DataFactory
Określa obiekt PSDataFactory.
To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Datafactoryname
Określa nazwę fabryki danych.
To polecenie cmdlet umożliwia pobieranie połączonych usług należących do fabryki danych, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę połączonej usługi, o której należy uzyskać informacje.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet umożliwia pobieranie połączonych usług należących do grupy, którą określa ten parametr.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## WEJŚCIOWE

### System. String
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory


## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService


## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE
[Set-AzureRmDataFactoryV2LinkedService]()

[Remove-AzureRmDataFactoryV2LinkedService]()
