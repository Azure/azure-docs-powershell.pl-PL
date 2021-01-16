---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354589"
---
# <span data-ttu-id="cd920-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="cd920-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="cd920-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd920-102">SYNOPSIS</span></span>
<span data-ttu-id="cd920-103">Pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cd920-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="cd920-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd920-104">SYNTAX</span></span>

### <span data-ttu-id="cd920-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd920-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd920-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cd920-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd920-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd920-107">DESCRIPTION</span></span>
<span data-ttu-id="cd920-108">Polecenie cmdlet **Get-AzDataFactoryDataset** pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cd920-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="cd920-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="cd920-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="cd920-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="cd920-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="cd920-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd920-111">EXAMPLES</span></span>

### <span data-ttu-id="cd920-112">Przykład 1: uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="cd920-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="cd920-113">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cd920-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="cd920-114">Przykład 2: uzyskiwanie informacji na temat konkretnego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="cd920-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="cd920-115">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cd920-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="cd920-116">Przykład 3: Uzyskiwanie lokalizacji dla określonego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="cd920-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="cd920-117">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF, a następnie używa standardowego zapisu kropkowego do wyświetlania **lokalizacji** skojarzonej z tym zestawem danych.</span><span class="sxs-lookup"><span data-stu-id="cd920-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="cd920-118">Możesz też przypisać dane wyjściowe polecenia cmdlet **Get-AzDataFactoryDataset** do zmiennej, a następnie za pomocą notacji kropkowej wyświetlić Właściwość lokalizacji skojarzoną z obiektem zestawu danych przechowywanym w tej zmiennej.</span><span class="sxs-lookup"><span data-stu-id="cd920-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="cd920-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd920-119">PARAMETERS</span></span>

### <span data-ttu-id="cd920-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd920-120">-DataFactory</span></span>
<span data-ttu-id="cd920-121">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="cd920-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cd920-122">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cd920-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd920-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cd920-123">-DataFactoryName</span></span>
<span data-ttu-id="cd920-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cd920-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cd920-125">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cd920-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd920-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd920-126">-DefaultProfile</span></span>
<span data-ttu-id="cd920-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cd920-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd920-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd920-128">-Name</span></span>
<span data-ttu-id="cd920-129">Określa nazwę zestawu danych, w którym ten aplet polecenia pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="cd920-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="cd920-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd920-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd920-131">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd920-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cd920-132">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="cd920-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd920-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd920-133">CommonParameters</span></span>
<span data-ttu-id="cd920-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd920-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd920-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd920-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd920-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd920-136">INPUTS</span></span>

### <span data-ttu-id="cd920-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cd920-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cd920-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cd920-138">System.String</span></span>

## <span data-ttu-id="cd920-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd920-139">OUTPUTS</span></span>

### <span data-ttu-id="cd920-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="cd920-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="cd920-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd920-141">NOTES</span></span>
* <span data-ttu-id="cd920-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cd920-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cd920-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd920-143">RELATED LINKS</span></span>

[<span data-ttu-id="cd920-144">Nowe — AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="cd920-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="cd920-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="cd920-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


