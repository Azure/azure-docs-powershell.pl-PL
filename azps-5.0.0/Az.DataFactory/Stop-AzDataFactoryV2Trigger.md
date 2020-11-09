---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305940"
---
# <span data-ttu-id="5725b-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5725b-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5725b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5725b-102">SYNOPSIS</span></span>
<span data-ttu-id="5725b-103">Zatrzymuje wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5725b-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="5725b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5725b-104">SYNTAX</span></span>

### <span data-ttu-id="5725b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5725b-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5725b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5725b-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5725b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5725b-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5725b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5725b-108">DESCRIPTION</span></span>
<span data-ttu-id="5725b-109">Polecenie cmdlet **stop-AzDataFactoryV2Trigger** zatrzymuje wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="5725b-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="5725b-110">Jeśli wyzwalacz jest w stanie "uruchomiony", polecenie cmdlet zatrzymuje wyzwalacz i nie wywoła już potoków.</span><span class="sxs-lookup"><span data-stu-id="5725b-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="5725b-111">Jeśli wyzwalacz jest już w stanie "zatrzymany", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="5725b-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="5725b-112">Jeśli parametr Force jest określony, polecenie cmdlet nie jest wyświetlane przed zatrzymaniem wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5725b-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="5725b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5725b-113">EXAMPLES</span></span>

### <span data-ttu-id="5725b-114">Przykład 1. zatrzymanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="5725b-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5725b-115">Zatrzymuje wyzwalacz o nazwie "ScheduledTrigger" w fabryce danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5725b-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="5725b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5725b-116">PARAMETERS</span></span>

### <span data-ttu-id="5725b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5725b-117">-DataFactoryName</span></span>
<span data-ttu-id="5725b-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5725b-118">The data factory name.</span></span>

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

### <span data-ttu-id="5725b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5725b-119">-DefaultProfile</span></span>
<span data-ttu-id="5725b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5725b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5725b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5725b-121">-Force</span></span>
<span data-ttu-id="5725b-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5725b-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5725b-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5725b-123">-InputObject</span></span>
<span data-ttu-id="5725b-124">Uruchamianie obiektu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5725b-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="5725b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5725b-125">-Name</span></span>
<span data-ttu-id="5725b-126">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5725b-126">The trigger name.</span></span>

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

### <span data-ttu-id="5725b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5725b-127">-ResourceGroupName</span></span>
<span data-ttu-id="5725b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5725b-128">The resource group name.</span></span>

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

### <span data-ttu-id="5725b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5725b-129">-ResourceId</span></span>
<span data-ttu-id="5725b-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5725b-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5725b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5725b-131">-Confirm</span></span>
<span data-ttu-id="5725b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5725b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5725b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5725b-133">-WhatIf</span></span>
<span data-ttu-id="5725b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5725b-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5725b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5725b-135">CommonParameters</span></span>
<span data-ttu-id="5725b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5725b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5725b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5725b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5725b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5725b-138">INPUTS</span></span>

### <span data-ttu-id="5725b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5725b-139">System.String</span></span>

### <span data-ttu-id="5725b-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5725b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5725b-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5725b-141">OUTPUTS</span></span>

### <span data-ttu-id="5725b-142">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5725b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5725b-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5725b-143">NOTES</span></span>

## <span data-ttu-id="5725b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5725b-144">RELATED LINKS</span></span>

[<span data-ttu-id="5725b-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5725b-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5725b-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5725b-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5725b-147">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5725b-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5725b-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5725b-148">Remove-AzDataFactoryV2Trigger</span></span>]()
