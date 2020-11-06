---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554377"
---
# <span data-ttu-id="6bd81-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6bd81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6bd81-102">SYNOPSIS</span></span>

<span data-ttu-id="6bd81-103">Uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="6bd81-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6bd81-104">SYNTAX</span></span>

### <span data-ttu-id="6bd81-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6bd81-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6bd81-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6bd81-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6bd81-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd81-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6bd81-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6bd81-108">DESCRIPTION</span></span>

<span data-ttu-id="6bd81-109">Polecenie cmdlet **Start-AzureRmDataFactoryV2Trigger** uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="6bd81-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="6bd81-110">Jeśli wyzwalacz jest w stanie "zatrzymany", polecenie cmdlet rozpoczyna wyzwalacz i po pewnym czasie wywoła potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="6bd81-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="6bd81-111">Jeśli wyzwalacz jest już w stanie "uruchomiony", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="6bd81-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="6bd81-112">Jeśli parametr Force jest określony, przed uruchomieniem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd81-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="6bd81-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6bd81-113">EXAMPLES</span></span>

### <span data-ttu-id="6bd81-114">Przykład 1. uruchomienie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="6bd81-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="6bd81-115">Uruchamia wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6bd81-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="6bd81-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6bd81-116">PARAMETERS</span></span>

### <span data-ttu-id="6bd81-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bd81-117">-Confirm</span></span>
<span data-ttu-id="6bd81-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd81-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd81-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6bd81-119">-DataFactoryName</span></span>
<span data-ttu-id="6bd81-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6bd81-120">The data factory name.</span></span>

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

### <span data-ttu-id="6bd81-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6bd81-121">-Force</span></span>
<span data-ttu-id="6bd81-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6bd81-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6bd81-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6bd81-123">-Name</span></span>
<span data-ttu-id="6bd81-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="6bd81-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bd81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd81-125">-ResourceGroupName</span></span>
<span data-ttu-id="6bd81-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bd81-126">The resource group name.</span></span>

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

### <span data-ttu-id="6bd81-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd81-127">-ResourceId</span></span>
<span data-ttu-id="6bd81-128">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6bd81-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6bd81-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6bd81-129">-InputObject</span></span>
<span data-ttu-id="6bd81-130">Uruchamianie obiektu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="6bd81-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="6bd81-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd81-131">-WhatIf</span></span>
<span data-ttu-id="6bd81-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bd81-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="6bd81-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bd81-133">INPUTS</span></span>

### <span data-ttu-id="6bd81-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6bd81-134">System.String</span></span>
<span data-ttu-id="6bd81-135">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="6bd81-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6bd81-136">OUTPUTS</span></span>

### <span data-ttu-id="6bd81-137">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6bd81-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="6bd81-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="6bd81-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6bd81-139">NOTES</span></span>

## <span data-ttu-id="6bd81-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bd81-140">RELATED LINKS</span></span>
[<span data-ttu-id="6bd81-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6bd81-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6bd81-143">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6bd81-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6bd81-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
