---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: ed4769c26363c60aace191d439d4a450a894eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717012"
---
# <span data-ttu-id="e5e1b-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="e5e1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e1b-103">Uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5e1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5e1b-104">SYNTAX</span></span>

### <span data-ttu-id="e5e1b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e5e1b-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e1b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5e1b-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e1b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e1b-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e1b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e5e1b-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e1b-109">Polecenie cmdlet **Start-AzureRmDataFactoryV2Trigger** uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="e5e1b-110">Jeśli wyzwalacz jest w stanie "zatrzymany", polecenie cmdlet rozpoczyna wyzwalacz i po pewnym czasie wywoła potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="e5e1b-111">Jeśli wyzwalacz jest już w stanie "uruchomiony", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="e5e1b-112">Jeśli parametr Force jest określony, przed uruchomieniem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="e5e1b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5e1b-113">EXAMPLES</span></span>

### <span data-ttu-id="e5e1b-114">Przykład 1. uruchomienie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="e5e1b-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="e5e1b-115">Uruchamia wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="e5e1b-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="e5e1b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5e1b-116">PARAMETERS</span></span>

### <span data-ttu-id="e5e1b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e5e1b-117">-DataFactoryName</span></span>
<span data-ttu-id="e5e1b-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-118">The data factory name.</span></span>

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

### <span data-ttu-id="e5e1b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e1b-119">-DefaultProfile</span></span>
<span data-ttu-id="e5e1b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e1b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e5e1b-121">-Force</span></span>
<span data-ttu-id="e5e1b-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e5e1b-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5e1b-123">-InputObject</span></span>
<span data-ttu-id="e5e1b-124">Uruchamianie obiektu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="e5e1b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5e1b-125">-Name</span></span>
<span data-ttu-id="e5e1b-126">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-126">The trigger name.</span></span>

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

### <span data-ttu-id="e5e1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5e1b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-128">The resource group name.</span></span>

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

### <span data-ttu-id="e5e1b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e1b-129">-ResourceId</span></span>
<span data-ttu-id="e5e1b-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e5e1b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5e1b-131">-Confirm</span></span>
<span data-ttu-id="e5e1b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e1b-133">-WhatIf</span></span>
<span data-ttu-id="e5e1b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e5e1b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e1b-135">CommonParameters</span></span>
<span data-ttu-id="e5e1b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e1b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e1b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e1b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e1b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5e1b-138">INPUTS</span></span>

### <span data-ttu-id="e5e1b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e1b-139">System.String</span></span>
<span data-ttu-id="e5e1b-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="e5e1b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5e1b-141">OUTPUTS</span></span>

### <span data-ttu-id="e5e1b-142">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. DataFactoryV2. MODELES. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e5e1b-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="e5e1b-143">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="e5e1b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5e1b-144">NOTES</span></span>

## <span data-ttu-id="e5e1b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5e1b-145">RELATED LINKS</span></span>

[<span data-ttu-id="e5e1b-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e5e1b-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e5e1b-148">Zatrzymaj — AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e5e1b-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e5e1b-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()