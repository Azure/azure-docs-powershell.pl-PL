---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 2479336e2c646f82b6868ee2382af508d0404a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545423"
---
# <span data-ttu-id="868f7-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="868f7-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="868f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="868f7-102">SYNOPSIS</span></span>
<span data-ttu-id="868f7-103">Pobiera informacje o zestawach danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="868f7-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="868f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="868f7-104">SYNTAX</span></span>

### <span data-ttu-id="868f7-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="868f7-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="868f7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="868f7-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="868f7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="868f7-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="868f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="868f7-108">DESCRIPTION</span></span>
<span data-ttu-id="868f7-109">Polecenie cmdlet Get-AzureRmDataFactoryV2Dataset pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="868f7-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="868f7-110">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="868f7-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="868f7-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="868f7-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="868f7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="868f7-112">EXAMPLES</span></span>

### <span data-ttu-id="868f7-113">Przykład 1: uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="868f7-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="868f7-114">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="868f7-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="868f7-115">Przykład 2: uzyskiwanie informacji na temat konkretnego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="868f7-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="868f7-116">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="868f7-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="868f7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="868f7-117">PARAMETERS</span></span>

### <span data-ttu-id="868f7-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="868f7-118">-DataFactory</span></span>
<span data-ttu-id="868f7-119">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="868f7-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="868f7-120">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="868f7-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="868f7-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="868f7-121">-DataFactoryName</span></span>
<span data-ttu-id="868f7-122">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="868f7-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="868f7-123">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="868f7-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="868f7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868f7-124">-DefaultProfile</span></span>
<span data-ttu-id="868f7-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="868f7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="868f7-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="868f7-126">-Name</span></span>
<span data-ttu-id="868f7-127">Określa nazwę zestawu danych, w którym mają zostać wyświetlone informacje.</span><span class="sxs-lookup"><span data-stu-id="868f7-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="868f7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="868f7-128">-ResourceGroupName</span></span>
<span data-ttu-id="868f7-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="868f7-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="868f7-130">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="868f7-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="868f7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="868f7-131">-ResourceId</span></span>
<span data-ttu-id="868f7-132">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="868f7-132">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="868f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868f7-133">CommonParameters</span></span>
<span data-ttu-id="868f7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868f7-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="868f7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868f7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="868f7-136">INPUTS</span></span>

### <span data-ttu-id="868f7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="868f7-137">System.String</span></span>

### <span data-ttu-id="868f7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="868f7-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="868f7-139">Parametry: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="868f7-139">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="868f7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="868f7-140">OUTPUTS</span></span>

### <span data-ttu-id="868f7-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="868f7-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="868f7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="868f7-142">NOTES</span></span>
<span data-ttu-id="868f7-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="868f7-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="868f7-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="868f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="868f7-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="868f7-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="868f7-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="868f7-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
