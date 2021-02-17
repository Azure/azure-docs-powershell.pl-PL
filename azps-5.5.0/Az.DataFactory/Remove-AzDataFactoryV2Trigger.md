---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198834"
---
# <span data-ttu-id="5b01f-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b01f-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5b01f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b01f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b01f-103">Usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5b01f-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="5b01f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b01f-104">SYNTAX</span></span>

### <span data-ttu-id="5b01f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5b01f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b01f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b01f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b01f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b01f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b01f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b01f-108">DESCRIPTION</span></span>
<span data-ttu-id="5b01f-109">Polecenie **cmdlet Remove-AzDataFactoryV2Trigger** usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5b01f-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="5b01f-110">Jeśli parametr _Force_ jest określony, polecenie cmdlet nie wyświetla monitu przed usunięciem wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5b01f-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="5b01f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b01f-111">EXAMPLES</span></span>

### <span data-ttu-id="5b01f-112">Przykład 1. Usuwanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="5b01f-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5b01f-113">Usuwanie wyzwalacza o nazwie "ScheduledTrigger" z fabrycznej witryny danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5b01f-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="5b01f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b01f-114">PARAMETERS</span></span>

### <span data-ttu-id="5b01f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5b01f-115">-DataFactoryName</span></span>
<span data-ttu-id="5b01f-116">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="5b01f-116">The data factory name.</span></span>

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

### <span data-ttu-id="5b01f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b01f-117">-DefaultProfile</span></span>
<span data-ttu-id="5b01f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b01f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b01f-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5b01f-119">-Force</span></span>
<span data-ttu-id="5b01f-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b01f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b01f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b01f-121">-InputObject</span></span>
<span data-ttu-id="5b01f-122">Obiekt Trigger do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5b01f-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="5b01f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5b01f-123">-Name</span></span>
<span data-ttu-id="5b01f-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5b01f-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b01f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b01f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b01f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5b01f-126">The resource group name.</span></span>

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

### <span data-ttu-id="5b01f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b01f-127">-ResourceId</span></span>
<span data-ttu-id="5b01f-128">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="5b01f-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b01f-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b01f-129">-Confirm</span></span>
<span data-ttu-id="5b01f-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b01f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b01f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b01f-131">-WhatIf</span></span>
<span data-ttu-id="5b01f-132">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b01f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5b01f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b01f-133">CommonParameters</span></span>
<span data-ttu-id="5b01f-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b01f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b01f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b01f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b01f-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b01f-136">INPUTS</span></span>

### <span data-ttu-id="5b01f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5b01f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="5b01f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5b01f-138">System.String</span></span>

## <span data-ttu-id="5b01f-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b01f-139">OUTPUTS</span></span>

### <span data-ttu-id="5b01f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b01f-140">System.Boolean</span></span>

## <span data-ttu-id="5b01f-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b01f-141">NOTES</span></span>

## <span data-ttu-id="5b01f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b01f-142">RELATED LINKS</span></span>

[<span data-ttu-id="5b01f-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b01f-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b01f-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b01f-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b01f-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b01f-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5b01f-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5b01f-146">Stop-AzDataFactoryV2Trigger</span></span>]()

