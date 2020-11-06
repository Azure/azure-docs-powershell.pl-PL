---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 36ee24fea327828247336d7f9c983515ced9deb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548308"
---
# <span data-ttu-id="6db6e-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6db6e-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="6db6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6db6e-102">SYNOPSIS</span></span>
<span data-ttu-id="6db6e-103">Umożliwia usunięcie zestawu danych z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6db6e-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6db6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6db6e-104">SYNTAX</span></span>

### <span data-ttu-id="6db6e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6db6e-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6db6e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6db6e-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6db6e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6db6e-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6db6e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6db6e-108">DESCRIPTION</span></span>
<span data-ttu-id="6db6e-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2Dataset powoduje usunięcie zestawu danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="6db6e-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="6db6e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6db6e-110">EXAMPLES</span></span>

### <span data-ttu-id="6db6e-111">Przykład 1: usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="6db6e-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="6db6e-112">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6db6e-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="6db6e-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="6db6e-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="6db6e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6db6e-114">PARAMETERS</span></span>

### <span data-ttu-id="6db6e-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6db6e-115">-Confirm</span></span>
<span data-ttu-id="6db6e-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db6e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db6e-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6db6e-117">-DataFactoryName</span></span>
<span data-ttu-id="6db6e-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6db6e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6db6e-119">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6db6e-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6db6e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6db6e-120">-InputObject</span></span>
<span data-ttu-id="6db6e-121">Określa obiekt zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="6db6e-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db6e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6db6e-122">-Force</span></span>
<span data-ttu-id="6db6e-123">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6db6e-123">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db6e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6db6e-124">-Name</span></span>
<span data-ttu-id="6db6e-125">Określa nazwę zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="6db6e-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db6e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db6e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6db6e-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6db6e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6db6e-128">To polecenie cmdlet umożliwia usunięcie zestawu danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6db6e-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6db6e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db6e-129">-ResourceId</span></span>
<span data-ttu-id="6db6e-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6db6e-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6db6e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db6e-131">-WhatIf</span></span>
<span data-ttu-id="6db6e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db6e-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db6e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db6e-133">-DefaultProfile</span></span>
<span data-ttu-id="6db6e-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6db6e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db6e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db6e-135">CommonParameters</span></span>
<span data-ttu-id="6db6e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db6e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db6e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db6e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db6e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6db6e-138">INPUTS</span></span>

### <span data-ttu-id="6db6e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="6db6e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="6db6e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6db6e-140">System.String</span></span>

## <span data-ttu-id="6db6e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6db6e-141">OUTPUTS</span></span>

### <span data-ttu-id="6db6e-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="6db6e-142">System.Object</span></span>

## <span data-ttu-id="6db6e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6db6e-143">NOTES</span></span>
<span data-ttu-id="6db6e-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="6db6e-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6db6e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6db6e-145">RELATED LINKS</span></span>

[<span data-ttu-id="6db6e-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6db6e-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="6db6e-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="6db6e-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
