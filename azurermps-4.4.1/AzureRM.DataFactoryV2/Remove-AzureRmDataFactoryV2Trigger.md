---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554386"
---
# <span data-ttu-id="4292d-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4292d-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="4292d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4292d-102">SYNOPSIS</span></span>
<span data-ttu-id="4292d-103">Usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4292d-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4292d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4292d-104">SYNTAX</span></span>

### <span data-ttu-id="4292d-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4292d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4292d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4292d-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4292d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4292d-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4292d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4292d-108">DESCRIPTION</span></span>
<span data-ttu-id="4292d-109">Polecenie cmdlet **Remove-AzureRmDataFactoryV2Trigger** usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4292d-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="4292d-110">Jeśli parametr _Force_ jest określony, przed usunięciem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4292d-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="4292d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4292d-111">EXAMPLES</span></span>

### <span data-ttu-id="4292d-112">Przykład 1: usuwanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="4292d-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="4292d-113">Usuwanie wyzwalacza o nazwie "ScheduledTrigger" z fabryki danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="4292d-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="4292d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4292d-114">PARAMETERS</span></span>

### <span data-ttu-id="4292d-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4292d-115">-Confirm</span></span>
<span data-ttu-id="4292d-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4292d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4292d-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4292d-117">-DataFactoryName</span></span>
<span data-ttu-id="4292d-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4292d-118">The data factory name.</span></span>

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

### <span data-ttu-id="4292d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4292d-119">-Force</span></span>
<span data-ttu-id="4292d-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4292d-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4292d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4292d-121">-Name</span></span>
<span data-ttu-id="4292d-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4292d-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4292d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4292d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4292d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4292d-124">The resource group name.</span></span>

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

### <span data-ttu-id="4292d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4292d-125">-ResourceId</span></span>
<span data-ttu-id="4292d-126">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4292d-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4292d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4292d-127">-InputObject</span></span>
<span data-ttu-id="4292d-128">Obiekt wyzwalacza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4292d-128">The Trigger object to remove.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4292d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4292d-129">-WhatIf</span></span>
<span data-ttu-id="4292d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4292d-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="4292d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4292d-131">INPUTS</span></span>

### <span data-ttu-id="4292d-132">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4292d-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="4292d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4292d-133">System.String</span></span>


## <span data-ttu-id="4292d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4292d-134">OUTPUTS</span></span>

### <span data-ttu-id="4292d-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="4292d-135">System.Object</span></span>

## <span data-ttu-id="4292d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4292d-136">NOTES</span></span>

## <span data-ttu-id="4292d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4292d-137">RELATED LINKS</span></span>
[<span data-ttu-id="4292d-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4292d-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4292d-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4292d-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4292d-140">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4292d-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4292d-141">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4292d-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

