---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 5b3052682785a694b3fb0999bb5df761eb3b96be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705952"
---
# <span data-ttu-id="6aa7d-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6aa7d-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6aa7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa7d-103">Usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="6aa7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aa7d-104">SYNTAX</span></span>

### <span data-ttu-id="6aa7d-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6aa7d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa7d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6aa7d-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa7d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6aa7d-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aa7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6aa7d-108">DESCRIPTION</span></span>
<span data-ttu-id="6aa7d-109">Polecenie cmdlet **Remove-AzDataFactoryV2Trigger** usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="6aa7d-110">Jeśli parametr _Force_ jest określony, przed usunięciem wyzwalacza nie jest wyświetlany monit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="6aa7d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aa7d-111">EXAMPLES</span></span>

### <span data-ttu-id="6aa7d-112">Przykład 1: usuwanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="6aa7d-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="6aa7d-113">Usuwanie wyzwalacza o nazwie "ScheduledTrigger" z fabryki danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6aa7d-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="6aa7d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aa7d-114">PARAMETERS</span></span>

### <span data-ttu-id="6aa7d-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6aa7d-115">-DataFactoryName</span></span>
<span data-ttu-id="6aa7d-116">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-116">The data factory name.</span></span>

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

### <span data-ttu-id="6aa7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa7d-117">-DefaultProfile</span></span>
<span data-ttu-id="6aa7d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa7d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6aa7d-119">-Force</span></span>
<span data-ttu-id="6aa7d-120">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6aa7d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6aa7d-121">-InputObject</span></span>
<span data-ttu-id="6aa7d-122">Obiekt wyzwalacza do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="6aa7d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6aa7d-123">-Name</span></span>
<span data-ttu-id="6aa7d-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-124">The trigger name.</span></span>

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

### <span data-ttu-id="6aa7d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa7d-125">-ResourceGroupName</span></span>
<span data-ttu-id="6aa7d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-126">The resource group name.</span></span>

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

### <span data-ttu-id="6aa7d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aa7d-127">-ResourceId</span></span>
<span data-ttu-id="6aa7d-128">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6aa7d-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aa7d-129">-Confirm</span></span>
<span data-ttu-id="6aa7d-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa7d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa7d-131">-WhatIf</span></span>
<span data-ttu-id="6aa7d-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6aa7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa7d-133">CommonParameters</span></span>
<span data-ttu-id="6aa7d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa7d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa7d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa7d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aa7d-136">INPUTS</span></span>

### <span data-ttu-id="6aa7d-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6aa7d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="6aa7d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6aa7d-138">System.String</span></span>

## <span data-ttu-id="6aa7d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aa7d-139">OUTPUTS</span></span>

### <span data-ttu-id="6aa7d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6aa7d-140">System.Boolean</span></span>

## <span data-ttu-id="6aa7d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aa7d-141">NOTES</span></span>

## <span data-ttu-id="6aa7d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aa7d-142">RELATED LINKS</span></span>

[<span data-ttu-id="6aa7d-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6aa7d-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6aa7d-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6aa7d-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6aa7d-145">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6aa7d-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6aa7d-146">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6aa7d-146">Stop-AzDataFactoryV2Trigger</span></span>]()
