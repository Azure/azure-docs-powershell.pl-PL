---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554388"
---
# <span data-ttu-id="c0d1b-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c0d1b-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="c0d1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d1b-103">Usuwa połączoną usługę z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0d1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0d1b-104">SYNTAX</span></span>

### <span data-ttu-id="c0d1b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c0d1b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c0d1b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0d1b-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c0d1b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d1b-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c0d1b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c0d1b-108">DESCRIPTION</span></span>
<span data-ttu-id="c0d1b-109">Polecenie cmdlet Remove-AzureRmDataFactoryV2LinkedService powoduje usunięcie połączonej usługi z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="c0d1b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0d1b-110">EXAMPLES</span></span>

### <span data-ttu-id="c0d1b-111">Przykład 1: usuwanie połączonej usługi</span><span class="sxs-lookup"><span data-stu-id="c0d1b-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="c0d1b-112">To polecenie powoduje usunięcie połączonej usługi o nazwie LinkedServiceTest z fabryki danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="c0d1b-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="c0d1b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0d1b-114">PARAMETERS</span></span>

### <span data-ttu-id="c0d1b-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0d1b-115">-Confirm</span></span>
<span data-ttu-id="c0d1b-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d1b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c0d1b-117">-DataFactoryName</span></span>
<span data-ttu-id="c0d1b-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c0d1b-119">To polecenie cmdlet umożliwia usunięcie połączonej usługi z fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0d1b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c0d1b-120">-Force</span></span>
<span data-ttu-id="c0d1b-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c0d1b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c0d1b-122">-InputObject</span></span>
<span data-ttu-id="c0d1b-123">Określa obiekt LinkedService, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d1b-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0d1b-124">-Name</span></span>
<span data-ttu-id="c0d1b-125">Określa nazwę połączonej usługi, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="c0d1b-126">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0d1b-128">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c0d1b-129">To polecenie cmdlet powoduje usunięcie połączonej usługi z grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="c0d1b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d1b-130">-ResourceId</span></span>
<span data-ttu-id="c0d1b-131">Identyfikator zasobu platformy Azure połączonej usługi do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="c0d1b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d1b-132">-WhatIf</span></span>
<span data-ttu-id="c0d1b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0d1b-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="c0d1b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0d1b-134">INPUTS</span></span>

### <span data-ttu-id="c0d1b-135">Microsoft. Azure. Commands. DataFactoryV2. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="c0d1b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="c0d1b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d1b-136">System.String</span></span>


## <span data-ttu-id="c0d1b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0d1b-137">OUTPUTS</span></span>

### <span data-ttu-id="c0d1b-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="c0d1b-138">System.Object</span></span>

## <span data-ttu-id="c0d1b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0d1b-139">NOTES</span></span>
<span data-ttu-id="c0d1b-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="c0d1b-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c0d1b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0d1b-141">RELATED LINKS</span></span>
[<span data-ttu-id="c0d1b-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c0d1b-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="c0d1b-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="c0d1b-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

