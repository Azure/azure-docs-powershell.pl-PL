---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 86330711dc9b35c85d87543d2b2ee55e9b1d4a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524485"
---
# <span data-ttu-id="e93e0-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e93e0-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="e93e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e93e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e93e0-103">Umożliwia usunięcie zestawu danych z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e93e0-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e93e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e93e0-104">SYNTAX</span></span>

### <span data-ttu-id="e93e0-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e93e0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93e0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e93e0-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e93e0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e93e0-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e93e0-108">DESCRIPTION</span></span>
<span data-ttu-id="e93e0-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2Dataset powoduje usunięcie zestawu danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e93e0-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="e93e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e93e0-110">EXAMPLES</span></span>

### <span data-ttu-id="e93e0-111">Przykład 1: usuwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="e93e0-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="e93e0-112">To polecenie usuwa zestaw danych o nazwie DAWikiAggregatedData z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e93e0-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="e93e0-113">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="e93e0-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="e93e0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e93e0-114">PARAMETERS</span></span>

### <span data-ttu-id="e93e0-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e93e0-115">-DataFactoryName</span></span>
<span data-ttu-id="e93e0-116">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e93e0-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e93e0-117">To polecenie cmdlet umożliwia usunięcie zestawu danych z fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e93e0-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e93e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93e0-118">-DefaultProfile</span></span>
<span data-ttu-id="e93e0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e93e0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93e0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e93e0-120">-Force</span></span>
<span data-ttu-id="e93e0-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e93e0-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e93e0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e93e0-122">-InputObject</span></span>
<span data-ttu-id="e93e0-123">Określa obiekt zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e93e0-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="e93e0-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e93e0-124">-Name</span></span>
<span data-ttu-id="e93e0-125">Określa nazwę zestawu danych, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e93e0-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="e93e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="e93e0-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e93e0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e93e0-128">To polecenie cmdlet umożliwia usunięcie zestawu danych z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="e93e0-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e93e0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e93e0-129">-ResourceId</span></span>
<span data-ttu-id="e93e0-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e93e0-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e93e0-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e93e0-131">-Confirm</span></span>
<span data-ttu-id="e93e0-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93e0-133">-WhatIf</span></span>
<span data-ttu-id="e93e0-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e93e0-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e93e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93e0-135">CommonParameters</span></span>
<span data-ttu-id="e93e0-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e93e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93e0-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93e0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93e0-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e93e0-138">INPUTS</span></span>

### <span data-ttu-id="e93e0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e93e0-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="e93e0-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e93e0-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e93e0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e93e0-141">System.String</span></span>

## <span data-ttu-id="e93e0-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e93e0-142">OUTPUTS</span></span>

### <span data-ttu-id="e93e0-143">System. void</span><span class="sxs-lookup"><span data-stu-id="e93e0-143">System.Void</span></span>

## <span data-ttu-id="e93e0-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e93e0-144">NOTES</span></span>
<span data-ttu-id="e93e0-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="e93e0-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e93e0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e93e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="e93e0-147">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e93e0-147">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="e93e0-148">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e93e0-148">Set-AzureRmDataFactoryV2Dataset</span></span>]()
