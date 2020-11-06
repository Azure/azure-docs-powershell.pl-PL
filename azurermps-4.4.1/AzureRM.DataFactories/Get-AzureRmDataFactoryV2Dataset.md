---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 01c2849c69cfbdd785fae092aeed63117a07b1ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528221"
---
# <span data-ttu-id="ba3d2-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ba3d2-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="ba3d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3d2-103">Pobiera informacje o zestawach danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba3d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba3d2-104">SYNTAX</span></span>

### <span data-ttu-id="ba3d2-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ba3d2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba3d2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ba3d2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba3d2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba3d2-107">DESCRIPTION</span></span>
<span data-ttu-id="ba3d2-108">Polecenie cmdlet Get-AzureRmDataFactoryV2Dataset pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="ba3d2-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="ba3d2-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="ba3d2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba3d2-111">EXAMPLES</span></span>

### <span data-ttu-id="ba3d2-112">Przykład 1: uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="ba3d2-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="ba3d2-113">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="ba3d2-114">Przykład 2: uzyskiwanie informacji na temat konkretnego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="ba3d2-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="ba3d2-115">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="ba3d2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba3d2-116">PARAMETERS</span></span>

### <span data-ttu-id="ba3d2-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ba3d2-117">-DataFactory</span></span>
<span data-ttu-id="ba3d2-118">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="ba3d2-119">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="ba3d2-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ba3d2-120">-DataFactoryName</span></span>
<span data-ttu-id="ba3d2-121">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ba3d2-122">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba3d2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba3d2-123">-Name</span></span>
<span data-ttu-id="ba3d2-124">Określa nazwę zestawu danych, w którym mają zostać wyświetlone informacje.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba3d2-126">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ba3d2-127">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba3d2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3d2-128">-DefaultProfile</span></span>
<span data-ttu-id="ba3d2-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba3d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3d2-130">CommonParameters</span></span>
<span data-ttu-id="ba3d2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3d2-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3d2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3d2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba3d2-133">INPUTS</span></span>

### <span data-ttu-id="ba3d2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba3d2-134">System.String</span></span>
<span data-ttu-id="ba3d2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ba3d2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ba3d2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba3d2-136">OUTPUTS</span></span>

### <span data-ttu-id="ba3d2-137">System. Collections. Generic. list "1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ba3d2-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ba3d2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="ba3d2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="ba3d2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba3d2-139">NOTES</span></span>
<span data-ttu-id="ba3d2-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="ba3d2-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ba3d2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba3d2-141">RELATED LINKS</span></span>

[<span data-ttu-id="ba3d2-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ba3d2-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="ba3d2-143">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="ba3d2-143">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
