---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 988f63d9f894de95c4206dc05bcda66e68f3c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710076"
---
# <span data-ttu-id="fb864-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb864-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="fb864-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb864-102">SYNOPSIS</span></span>
<span data-ttu-id="fb864-103">Uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="fb864-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="fb864-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb864-104">SYNTAX</span></span>

### <span data-ttu-id="fb864-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb864-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb864-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb864-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb864-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb864-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb864-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fb864-108">DESCRIPTION</span></span>
<span data-ttu-id="fb864-109">Polecenie cmdlet **Start-AzDataFactoryV2Trigger** uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="fb864-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="fb864-110">Jeśli wyzwalacz jest w stanie "zatrzymany", polecenie cmdlet rozpoczyna wyzwalacz i po pewnym czasie wywoła potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="fb864-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="fb864-111">Jeśli wyzwalacz jest już w stanie "uruchomiony", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="fb864-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="fb864-112">Jeśli parametr Force jest określony, przed uruchomieniem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb864-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="fb864-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb864-113">EXAMPLES</span></span>

### <span data-ttu-id="fb864-114">Przykład 1. uruchomienie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="fb864-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="fb864-115">Uruchamia wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="fb864-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="fb864-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb864-116">PARAMETERS</span></span>

### <span data-ttu-id="fb864-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fb864-117">-DataFactoryName</span></span>
<span data-ttu-id="fb864-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="fb864-118">The data factory name.</span></span>

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

### <span data-ttu-id="fb864-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb864-119">-DefaultProfile</span></span>
<span data-ttu-id="fb864-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb864-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb864-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fb864-121">-Force</span></span>
<span data-ttu-id="fb864-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fb864-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fb864-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fb864-123">-InputObject</span></span>
<span data-ttu-id="fb864-124">Uruchamianie obiektu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="fb864-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb864-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb864-125">-Name</span></span>
<span data-ttu-id="fb864-126">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="fb864-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb864-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb864-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb864-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fb864-128">The resource group name.</span></span>

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

### <span data-ttu-id="fb864-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb864-129">-ResourceId</span></span>
<span data-ttu-id="fb864-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb864-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fb864-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb864-131">-Confirm</span></span>
<span data-ttu-id="fb864-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb864-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb864-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb864-133">-WhatIf</span></span>
<span data-ttu-id="fb864-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb864-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fb864-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb864-135">CommonParameters</span></span>
<span data-ttu-id="fb864-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb864-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb864-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb864-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb864-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb864-138">INPUTS</span></span>

### <span data-ttu-id="fb864-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fb864-139">System.String</span></span>

### <span data-ttu-id="fb864-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="fb864-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fb864-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb864-141">OUTPUTS</span></span>

### <span data-ttu-id="fb864-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="fb864-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fb864-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb864-143">NOTES</span></span>

## <span data-ttu-id="fb864-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb864-144">RELATED LINKS</span></span>

[<span data-ttu-id="fb864-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb864-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fb864-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb864-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fb864-147">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb864-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fb864-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb864-148">Remove-AzDataFactoryV2Trigger</span></span>]()
