---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718244"
---
# <span data-ttu-id="657b2-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="657b2-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="657b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="657b2-102">SYNOPSIS</span></span>

<span data-ttu-id="657b2-103">Zatrzymuje wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="657b2-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="657b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="657b2-104">SYNTAX</span></span>

### <span data-ttu-id="657b2-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="657b2-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="657b2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="657b2-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="657b2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="657b2-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="657b2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="657b2-108">DESCRIPTION</span></span>

<span data-ttu-id="657b2-109">Polecenie cmdlet **stop-AzureRmDataFactoryV2Trigger** zatrzymuje wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="657b2-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="657b2-110">Jeśli wyzwalacz jest w stanie "uruchomiony", polecenie cmdlet zatrzymuje wyzwalacz i nie wywoła już potoków.</span><span class="sxs-lookup"><span data-stu-id="657b2-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="657b2-111">Jeśli wyzwalacz jest już w stanie "zatrzymany", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="657b2-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="657b2-112">Jeśli parametr Force jest określony, polecenie cmdlet nie jest wyświetlane przed zatrzymaniem wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="657b2-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>


## <span data-ttu-id="657b2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="657b2-113">EXAMPLES</span></span>

### <span data-ttu-id="657b2-114">Przykład 1. zatrzymanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="657b2-114">Example 1: Stop a trigger</span></span>

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="657b2-115">Zatrzymuje wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="657b2-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="657b2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="657b2-116">PARAMETERS</span></span>

### <span data-ttu-id="657b2-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="657b2-117">-Confirm</span></span>
<span data-ttu-id="657b2-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="657b2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="657b2-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="657b2-119">-DataFactoryName</span></span>
<span data-ttu-id="657b2-120">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="657b2-120">The data factory name.</span></span>

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

### <span data-ttu-id="657b2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="657b2-121">-Force</span></span>
<span data-ttu-id="657b2-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="657b2-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="657b2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="657b2-123">-Name</span></span>
<span data-ttu-id="657b2-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="657b2-124">The trigger name.</span></span>

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

### <span data-ttu-id="657b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="657b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="657b2-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="657b2-126">The resource group name.</span></span>

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

### <span data-ttu-id="657b2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="657b2-127">-ResourceId</span></span>
<span data-ttu-id="657b2-128">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="657b2-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="657b2-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="657b2-129">-InputObject</span></span>
<span data-ttu-id="657b2-130">Uruchamianie obiektu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="657b2-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="657b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="657b2-131">-WhatIf</span></span>
<span data-ttu-id="657b2-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="657b2-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="657b2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="657b2-133">INPUTS</span></span>

### <span data-ttu-id="657b2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="657b2-134">System.String</span></span>
<span data-ttu-id="657b2-135">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="657b2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="657b2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="657b2-136">OUTPUTS</span></span>

### <span data-ttu-id="657b2-137">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="657b2-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="657b2-138">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="657b2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="657b2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="657b2-139">NOTES</span></span>

## <span data-ttu-id="657b2-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="657b2-140">RELATED LINKS</span></span>
[<span data-ttu-id="657b2-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="657b2-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="657b2-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="657b2-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="657b2-143">Start — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="657b2-143">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="657b2-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="657b2-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
