---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bce1969ed951f196b1ff2c6d5bcc359ee68bc3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552956"
---
# Get-AzureRmDataFactoryV2Pipeline

## STRESZCZENIe
Pobiera informacje o rurociągach w fabryce danych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByFactoryName (domyślny)
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzureRmDataFactoryV2Pipeline -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzureRmDataFactoryV2Pipeline pobiera informacje o rurociągach w usłudze Azure Data Factory.
Jeśli określisz nazwę potoku, to polecenie cmdlet będzie pobierać informacje o tym potoku.
Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich rurociągach w fabryce danych.

## Przykłady

### Przykład 1: uzyskiwanie informacji o wszystkich rurociągach
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

To polecenie pobiera informacje o wszystkich rurociągach w fabryce danych o nazwie WikiADF.
Możesz użyć jednego z poniższych poleceń przykładowych.
Druga z nich używa obiektu DataFactory jako parametru.

### Przykład 2: uzyskiwanie informacji na temat konkretnego procesu
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

To polecenie pobiera informacje o potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF.
Polecenie przekazuje te informacje do polecenia cmdlet Format-List przy użyciu operatora potoku.
To polecenie cmdlet programu Windows PowerShell formatuje wyniki.
Aby uzyskać więcej informacji, wpisz Get-Help format-lista.

### Przykład 3: uzyskiwanie właściwości dla konkretnego potoku
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości aktywności skojarzonej z tym potokiem.

### Przykład 6: uzyskiwanie informacji o danych wejściowych dla pierwszej aktywności
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego w celu wyświetlenia właściwości aktywności skojarzonej z tym potokiem.
Polecenie wyświetla właściwość dane wejściowe pierwszego elementu tablicy aktywności przy użyciu polecenia cmdlet Format-List.

## PARAMETRÓW

### -DataFactory
Określa obiekt PSDataFactory.
To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.

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
To polecenie cmdlet umożliwia pobieranie potoków należących do fabryki danych, którą określa ten parametr.

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
Określa nazwę potoku, w którym należy uzyskać informacje.

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet umożliwia pobieranie potoków należących do grupy, którą określa ten parametr.

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

### -ResourceId
Identyfikator zasobu platformy Azure.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String
Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Set-AzureRmDataFactoryV2Pipeline]()

[Remove-AzureRmDataFactoryV2Pipeline]()

[Invoke-AzureRmDataFactoryV2Pipeline]()
