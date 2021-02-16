---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188650"
---
# Get-AzDataFactoryPipeline

## SYNOPSIS
Pobiera informacje o potokach w usłudze Azure Data Factory.

## SKŁADNIA

### ByFactoryName (Default)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDataFactoryPipeline** pobiera informacje o potokach w usłudze Azure Data Factory.
Jeśli określisz nazwę potoku, to polecenie cmdlet pobiera informacje o tym potoku.
Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich potokach w zakładzie danych.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji o wszystkich potokach
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

To polecenie pobiera informacje o wszystkich potokach w fabrycznej układzie danych o nazwie WikiADF.
Możesz użyć jednego z poniższych poleceń przykładowych.
Drugi obiekt korzysta z **obiektu DataFactory** jako parametru.

### Przykład 2. Uzyskiwanie informacji o określonym potoku
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

To polecenie pobiera informacje o potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF.
Polecenie przekazuje te informacje do Format-List cmdlet przy użyciu operatora potoku.
To polecenie cmdlet s formatuje wyniki.
Aby uzyskać więcej informacji, wpisz `Get-Help Format-List` .

### Przykład 3. Uzyskiwanie właściwości określonego potoku
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości **Properties** skojarzonej z tym potokiem.

### Przykład 4. Uzyskiwanie działań dla określonego potoku
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w zakładzie danych o  nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.

### Przykład 5. Uzyskiwanie informacji dotyczących środowiska uruchomieniowego dla określonego potoku
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample w zakładzie danych o nazwie WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości **RuntimeInfo** skojarzonej z tym potokiem.

### Przykład 6. Uzyskiwanie informacji o danych wejściowych dla pierwszego działania
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

To polecenie pobiera informacje dotyczące potoku o nazwie DPWikisample z fabryki danych o nazwie  WikiADF, a następnie używa standardowej notacji kropki w celu wyświetlenia właściwości Działania skojarzonej z tym potokiem.
Polecenie wyświetla właściwość **Dane wejściowe** pierwszego elementu tablicy Działania **przy** użyciu opcji **Format-Lista.**

## PARAMETERS

### -DataFactory
Określa obiekt **PSDataFactory.**
To polecenie cmdlet pobiera potoki, które należą do fabryki danych, które określa ten parametr.

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
To polecenie cmdlet pobiera potoki należące do fabrycznych danych, które określa ten parametr.

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

### — Nazwa
Określa nazwę potoku, o którym mają być informacje.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet pobiera potoki, które należą do grupy, której parametr określa.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## OUTPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSPipeline

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Resume-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


