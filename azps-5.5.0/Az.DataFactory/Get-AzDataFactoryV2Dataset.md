---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238319"
---
# <span data-ttu-id="73cd9-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="73cd9-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="73cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="73cd9-103">Pobiera informacje o zestawach danych w układzie Data Factory.</span><span class="sxs-lookup"><span data-stu-id="73cd9-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="73cd9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73cd9-104">SYNTAX</span></span>

### <span data-ttu-id="73cd9-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="73cd9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73cd9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="73cd9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73cd9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="73cd9-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73cd9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="73cd9-108">DESCRIPTION</span></span>
<span data-ttu-id="73cd9-109">Polecenie Get-AzDataFactoryV2Dataset pobiera informacje o zestawach danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="73cd9-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="73cd9-110">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet pobiera informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="73cd9-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="73cd9-111">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich zestawach danych w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="73cd9-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="73cd9-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73cd9-112">EXAMPLES</span></span>

### <span data-ttu-id="73cd9-113">Przykład 1. Uzyskiwanie informacji o wszystkich zestawach danych</span><span class="sxs-lookup"><span data-stu-id="73cd9-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="73cd9-114">To polecenie pobiera informacje o wszystkich zestawach danych w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="73cd9-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="73cd9-115">Przykład 2. Uzyskiwanie informacji o określonym zestawie danych</span><span class="sxs-lookup"><span data-stu-id="73cd9-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="73cd9-116">To polecenie pobiera informacje o zestawie danych o nazwie DAWikipediaClickEvents w fabrycznej bazie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="73cd9-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="73cd9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73cd9-117">PARAMETERS</span></span>

### <span data-ttu-id="73cd9-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="73cd9-118">-DataFactory</span></span>
<span data-ttu-id="73cd9-119">Określa obiekt PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="73cd9-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="73cd9-120">To polecenie cmdlet pobiera zestawy danych, które należą do fabrycznej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="73cd9-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="73cd9-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="73cd9-121">-DataFactoryName</span></span>
<span data-ttu-id="73cd9-122">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="73cd9-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="73cd9-123">To polecenie cmdlet pobiera zestawy danych, które należą do fabrycznej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="73cd9-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="73cd9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cd9-124">-DefaultProfile</span></span>
<span data-ttu-id="73cd9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73cd9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73cd9-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73cd9-126">-Name</span></span>
<span data-ttu-id="73cd9-127">Określa nazwę zestawu danych, o którym mają być uzyskiwanie informacji.</span><span class="sxs-lookup"><span data-stu-id="73cd9-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="73cd9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73cd9-128">-ResourceGroupName</span></span>
<span data-ttu-id="73cd9-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="73cd9-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="73cd9-130">To polecenie cmdlet pobiera zestawy danych, które należą do grupy, której parametr określa.</span><span class="sxs-lookup"><span data-stu-id="73cd9-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="73cd9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73cd9-131">-ResourceId</span></span>
<span data-ttu-id="73cd9-132">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="73cd9-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="73cd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cd9-133">CommonParameters</span></span>
<span data-ttu-id="73cd9-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cd9-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73cd9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cd9-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73cd9-136">INPUTS</span></span>

### <span data-ttu-id="73cd9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="73cd9-137">System.String</span></span>

### <span data-ttu-id="73cd9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="73cd9-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="73cd9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73cd9-139">OUTPUTS</span></span>

### <span data-ttu-id="73cd9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="73cd9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="73cd9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73cd9-141">NOTES</span></span>
<span data-ttu-id="73cd9-142">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="73cd9-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="73cd9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73cd9-143">RELATED LINKS</span></span>

[<span data-ttu-id="73cd9-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="73cd9-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="73cd9-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="73cd9-145">Remove-AzDataFactoryV2Dataset</span></span>]()
