---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 7f24d7a7fc027e8d4411b12a3f04d24121af5354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969137"
---
# <span data-ttu-id="ae8a3-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ae8a3-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="ae8a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8a3-103">Aktualizowanie aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="ae8a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae8a3-104">SYNTAX</span></span>

### <span data-ttu-id="ae8a3-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ae8a3-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae8a3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae8a3-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae8a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae8a3-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae8a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae8a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ae8a3-109">Aktualizowanie aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="ae8a3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae8a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ae8a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae8a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="ae8a3-112">Pobierz istniejącą konfigurację aparatu reguł i dodaj do niego kolejną regułę aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="ae8a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae8a3-113">PARAMETERS</span></span>

### <span data-ttu-id="ae8a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8a3-114">-DefaultProfile</span></span>
<span data-ttu-id="ae8a3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae8a3-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ae8a3-116">-FrontDoorName</span></span>
<span data-ttu-id="ae8a3-117">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-117">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae8a3-118">-InputObject</span></span>
<span data-ttu-id="ae8a3-119">Obiekt Aparat reguł do aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-119">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8a3-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae8a3-120">-Name</span></span>
<span data-ttu-id="ae8a3-121">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-121">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae8a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae8a3-123">Nazwa grupy zasobów, w przypadku których zostanie utworzona brama frontowa.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-123">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae8a3-124">-ResourceId</span></span>
<span data-ttu-id="ae8a3-125">Identyfikator zasobu reguły do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="ae8a3-125">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8a3-126">— reguła</span><span class="sxs-lookup"><span data-stu-id="ae8a3-126">-Rule</span></span>
<span data-ttu-id="ae8a3-127">Lista reguł definiująca określonej konfiguracji aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8a3-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae8a3-128">-Confirm</span></span>
<span data-ttu-id="ae8a3-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae8a3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae8a3-130">-WhatIf</span></span>
<span data-ttu-id="ae8a3-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae8a3-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae8a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8a3-133">CommonParameters</span></span>
<span data-ttu-id="ae8a3-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae8a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8a3-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae8a3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8a3-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae8a3-136">INPUTS</span></span>

### <span data-ttu-id="ae8a3-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ae8a3-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="ae8a3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ae8a3-138">System.String</span></span>

## <span data-ttu-id="ae8a3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae8a3-139">OUTPUTS</span></span>

### <span data-ttu-id="ae8a3-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ae8a3-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="ae8a3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae8a3-141">NOTES</span></span>

## <span data-ttu-id="ae8a3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae8a3-142">RELATED LINKS</span></span>
