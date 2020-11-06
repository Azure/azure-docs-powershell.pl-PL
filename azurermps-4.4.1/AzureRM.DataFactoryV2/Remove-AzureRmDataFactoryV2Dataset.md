---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551904"
---
# <span data-ttu-id="99da7-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="99da7-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="99da7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99da7-102">SYNOPSIS</span></span>
<span data-ttu-id="99da7-103">Umożliwia usunięcie zestawu danych z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="99da7-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99da7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99da7-104">SYNTAX</span></span>

### <span data-ttu-id="99da7-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99da7-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99da7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="99da7-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="99da7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99da7-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="99da7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="99da7-108">DESCRIPTION</span></span>
<span data-ttu-id="99da7-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2Dataset powoduje usunięcie zestawu danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="99da7-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="99da7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99da7-110">EXAMPLES</span></span>

### <span data-ttu-id="99da7-111">Przykład 1: usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="99da7-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="99da7-112">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="99da7-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="99da7-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="99da7-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="99da7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99da7-114">PARAMETERS</span></span>

### <span data-ttu-id="99da7-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99da7-115">-Confirm</span></span>
<span data-ttu-id="99da7-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99da7-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99da7-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="99da7-117">-DataFactoryName</span></span>
<span data-ttu-id="99da7-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="99da7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="99da7-119">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="99da7-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="99da7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="99da7-120">-InputObject</span></span>
<span data-ttu-id="99da7-121">Określa obiekt zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="99da7-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99da7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="99da7-122">-Force</span></span>
<span data-ttu-id="99da7-123">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99da7-123">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99da7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99da7-124">-Name</span></span>
<span data-ttu-id="99da7-125">Określa nazwę zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="99da7-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99da7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99da7-126">-ResourceGroupName</span></span>
<span data-ttu-id="99da7-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99da7-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="99da7-128">To polecenie cmdlet umożliwia usunięcie zestawu danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="99da7-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="99da7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99da7-129">-ResourceId</span></span>
<span data-ttu-id="99da7-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="99da7-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99da7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99da7-131">-WhatIf</span></span>
<span data-ttu-id="99da7-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99da7-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="99da7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99da7-133">INPUTS</span></span>

### <span data-ttu-id="99da7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="99da7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="99da7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="99da7-135">System.String</span></span>


## <span data-ttu-id="99da7-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99da7-136">OUTPUTS</span></span>

### <span data-ttu-id="99da7-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="99da7-137">System.Object</span></span>

## <span data-ttu-id="99da7-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99da7-138">NOTES</span></span>
<span data-ttu-id="99da7-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="99da7-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="99da7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99da7-140">RELATED LINKS</span></span>
[<span data-ttu-id="99da7-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="99da7-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="99da7-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="99da7-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
