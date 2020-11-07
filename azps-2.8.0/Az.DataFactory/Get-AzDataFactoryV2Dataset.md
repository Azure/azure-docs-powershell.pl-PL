---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 1fb9b4a80faca7681154d375123b7e19be65e5c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706030"
---
# <span data-ttu-id="08b1f-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="08b1f-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="08b1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="08b1f-103">Pobiera informacje o zestawach danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="08b1f-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="08b1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08b1f-104">SYNTAX</span></span>

### <span data-ttu-id="08b1f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08b1f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08b1f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="08b1f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08b1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08b1f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08b1f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="08b1f-108">DESCRIPTION</span></span>
<span data-ttu-id="08b1f-109">Polecenie cmdlet Get-AzDataFactoryV2Dataset pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="08b1f-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="08b1f-110">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="08b1f-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="08b1f-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="08b1f-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="08b1f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08b1f-112">EXAMPLES</span></span>

### <span data-ttu-id="08b1f-113">Przykład 1: uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="08b1f-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="08b1f-114">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="08b1f-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="08b1f-115">Przykład 2: uzyskiwanie informacji na temat konkretnego zestawu danych</span><span class="sxs-lookup"><span data-stu-id="08b1f-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="08b1f-116">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="08b1f-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="08b1f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08b1f-117">PARAMETERS</span></span>

### <span data-ttu-id="08b1f-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="08b1f-118">-DataFactory</span></span>
<span data-ttu-id="08b1f-119">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="08b1f-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="08b1f-120">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="08b1f-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="08b1f-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="08b1f-121">-DataFactoryName</span></span>
<span data-ttu-id="08b1f-122">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="08b1f-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="08b1f-123">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="08b1f-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="08b1f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b1f-124">-DefaultProfile</span></span>
<span data-ttu-id="08b1f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08b1f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08b1f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08b1f-126">-Name</span></span>
<span data-ttu-id="08b1f-127">Określa nazwę zestawu danych, w którym mają zostać wyświetlone informacje.</span><span class="sxs-lookup"><span data-stu-id="08b1f-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="08b1f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b1f-128">-ResourceGroupName</span></span>
<span data-ttu-id="08b1f-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="08b1f-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="08b1f-130">To polecenie cmdlet umożliwia pobieranie zestawów danych należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="08b1f-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="08b1f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08b1f-131">-ResourceId</span></span>
<span data-ttu-id="08b1f-132">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="08b1f-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="08b1f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b1f-133">CommonParameters</span></span>
<span data-ttu-id="08b1f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b1f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b1f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b1f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b1f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08b1f-136">INPUTS</span></span>

### <span data-ttu-id="08b1f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="08b1f-137">System.String</span></span>

### <span data-ttu-id="08b1f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="08b1f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="08b1f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08b1f-139">OUTPUTS</span></span>

### <span data-ttu-id="08b1f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="08b1f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="08b1f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08b1f-141">NOTES</span></span>
<span data-ttu-id="08b1f-142">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="08b1f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="08b1f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08b1f-143">RELATED LINKS</span></span>

[<span data-ttu-id="08b1f-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="08b1f-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="08b1f-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="08b1f-145">Remove-AzDataFactoryV2Dataset</span></span>]()