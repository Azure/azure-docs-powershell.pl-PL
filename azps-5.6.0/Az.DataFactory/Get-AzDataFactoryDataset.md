---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: c31a8bb3ef09eb190a7a4c77aef0c44fadbf8960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992797"
---
# <span data-ttu-id="cf6c6-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="cf6c6-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="cf6c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="cf6c6-103">Pobiera informacje o zestawach danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="cf6c6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf6c6-104">SYNTAX</span></span>

### <span data-ttu-id="cf6c6-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="cf6c6-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf6c6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cf6c6-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf6c6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf6c6-107">DESCRIPTION</span></span>
<span data-ttu-id="cf6c6-108">Polecenie **cmdlet Get-AzDataFactoryDataset** pobiera informacje o zestawach danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="cf6c6-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet pobiera informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="cf6c6-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich zestawach danych w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="cf6c6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf6c6-111">EXAMPLES</span></span>

### <span data-ttu-id="cf6c6-112">Przykład 1. Uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="cf6c6-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="cf6c6-113">To polecenie pobiera informacje o wszystkich zestawach danych w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="cf6c6-114">Przykład 2. Uzyskiwanie informacji o określonym zestawie danych</span><span class="sxs-lookup"><span data-stu-id="cf6c6-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="cf6c6-115">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabrycznej bazie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="cf6c6-116">Przykład 3. Uzyskiwanie lokalizacji dla określonego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="cf6c6-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="cf6c6-117">To polecenie pobiera informacje dotyczące zestawu danych o nazwie DAWikipediaClickEvents w fabrycznej bazie  danych o nazwie WikiADF, a następnie wyświetla lokalizację skojarzoną z tym zestawem danych przy użyciu standardowej notacji kropki.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="cf6c6-118">Możesz również przypisać dane wyjściowe polecenia cmdlet **Get-AzDataFactoryDataset** do zmiennej, a następnie użyć notacji kropki w celu wyświetlenia właściwości Location skojarzonej z obiektem zestawu danych przechowywanym w tej zmiennej.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="cf6c6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf6c6-119">PARAMETERS</span></span>

### <span data-ttu-id="cf6c6-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cf6c6-120">-DataFactory</span></span>
<span data-ttu-id="cf6c6-121">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="cf6c6-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cf6c6-122">To polecenie cmdlet pobiera zestawy danych, które należą do fabrycznej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf6c6-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf6c6-123">-DataFactoryName</span></span>
<span data-ttu-id="cf6c6-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cf6c6-125">To polecenie cmdlet pobiera zestawy danych, które należą do fabrycznej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf6c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf6c6-126">-DefaultProfile</span></span>
<span data-ttu-id="cf6c6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cf6c6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf6c6-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf6c6-128">-Name</span></span>
<span data-ttu-id="cf6c6-129">Określa nazwę zestawu danych, o którym to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="cf6c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf6c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf6c6-131">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cf6c6-132">To polecenie cmdlet pobiera zestawy danych, które należą do grupy, której parametr określa.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf6c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf6c6-133">CommonParameters</span></span>
<span data-ttu-id="cf6c6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf6c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf6c6-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf6c6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf6c6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf6c6-136">INPUTS</span></span>

### <span data-ttu-id="cf6c6-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cf6c6-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cf6c6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cf6c6-138">System.String</span></span>

## <span data-ttu-id="cf6c6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf6c6-139">OUTPUTS</span></span>

### <span data-ttu-id="cf6c6-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="cf6c6-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="cf6c6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf6c6-141">NOTES</span></span>
* <span data-ttu-id="cf6c6-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cf6c6-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cf6c6-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf6c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="cf6c6-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="cf6c6-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="cf6c6-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="cf6c6-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


