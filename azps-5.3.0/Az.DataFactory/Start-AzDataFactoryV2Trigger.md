---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503633"
---
# <span data-ttu-id="3d346-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d346-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="3d346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d346-102">SYNOPSIS</span></span>
<span data-ttu-id="3d346-103">Uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="3d346-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="3d346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d346-104">SYNTAX</span></span>

### <span data-ttu-id="3d346-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3d346-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d346-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d346-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d346-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d346-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d346-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3d346-108">DESCRIPTION</span></span>
<span data-ttu-id="3d346-109">Polecenie cmdlet **Start-AzDataFactoryV2Trigger** uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="3d346-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="3d346-110">Jeśli wyzwalacz jest w stanie "zatrzymany", polecenie cmdlet rozpoczyna wyzwalacz i po pewnym czasie wywoła potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="3d346-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="3d346-111">Jeśli wyzwalacz jest już w stanie "uruchomiony", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="3d346-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="3d346-112">Jeśli parametr Force jest określony, przed uruchomieniem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d346-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="3d346-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d346-113">EXAMPLES</span></span>

### <span data-ttu-id="3d346-114">Przykład 1. uruchomienie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="3d346-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="3d346-115">Uruchamia wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="3d346-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="3d346-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d346-116">PARAMETERS</span></span>

### <span data-ttu-id="3d346-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3d346-117">-DataFactoryName</span></span>
<span data-ttu-id="3d346-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="3d346-118">The data factory name.</span></span>

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

### <span data-ttu-id="3d346-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d346-119">-DefaultProfile</span></span>
<span data-ttu-id="3d346-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d346-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d346-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3d346-121">-Force</span></span>
<span data-ttu-id="3d346-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3d346-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3d346-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d346-123">-InputObject</span></span>
<span data-ttu-id="3d346-124">Uruchamianie obiektu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3d346-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="3d346-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d346-125">-Name</span></span>
<span data-ttu-id="3d346-126">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3d346-126">The trigger name.</span></span>

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

### <span data-ttu-id="3d346-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d346-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d346-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d346-128">The resource group name.</span></span>

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

### <span data-ttu-id="3d346-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d346-129">-ResourceId</span></span>
<span data-ttu-id="3d346-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d346-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3d346-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d346-131">-Confirm</span></span>
<span data-ttu-id="3d346-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d346-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d346-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d346-133">-WhatIf</span></span>
<span data-ttu-id="3d346-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d346-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3d346-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d346-135">CommonParameters</span></span>
<span data-ttu-id="3d346-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d346-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d346-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d346-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d346-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d346-138">INPUTS</span></span>

### <span data-ttu-id="3d346-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3d346-139">System.String</span></span>

### <span data-ttu-id="3d346-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3d346-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3d346-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d346-141">OUTPUTS</span></span>

### <span data-ttu-id="3d346-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3d346-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3d346-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d346-143">NOTES</span></span>

## <span data-ttu-id="3d346-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d346-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d346-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d346-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3d346-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d346-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3d346-147">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d346-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3d346-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d346-148">Remove-AzDataFactoryV2Trigger</span></span>]()
