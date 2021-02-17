---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192491"
---
# <span data-ttu-id="2ddff-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="2ddff-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="2ddff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ddff-102">SYNOPSIS</span></span>
<span data-ttu-id="2ddff-103">Utwórz nową konfigurację aparatu reguł dla określonych drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="2ddff-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="2ddff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ddff-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ddff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ddff-105">DESCRIPTION</span></span>
<span data-ttu-id="2ddff-106">Utwórz nową konfigurację aparatu reguł dla określonych przednich drzwi.</span><span class="sxs-lookup"><span data-stu-id="2ddff-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="2ddff-107">Użyj polecenia cmdlet "New-AzFrontDoorRulesEngineRule", aby skonstruować reguły aparatu reguł w celu przekazania do parametru "-Rules" tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ddff-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="2ddff-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ddff-108">EXAMPLES</span></span>

### <span data-ttu-id="2ddff-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ddff-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="2ddff-110">Utwórz nową konfigurację aparatu reguł dla określonych drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="2ddff-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="2ddff-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ddff-111">PARAMETERS</span></span>

### <span data-ttu-id="2ddff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ddff-112">-DefaultProfile</span></span>
<span data-ttu-id="2ddff-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ddff-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ddff-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="2ddff-114">-FrontDoorName</span></span>
<span data-ttu-id="2ddff-115">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="2ddff-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ddff-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ddff-116">-Name</span></span>
<span data-ttu-id="2ddff-117">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="2ddff-117">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ddff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ddff-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ddff-119">Nazwa grupy zasobów, w przypadku których zostanie utworzona brama frontowa.</span><span class="sxs-lookup"><span data-stu-id="2ddff-119">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ddff-120">— reguła</span><span class="sxs-lookup"><span data-stu-id="2ddff-120">-Rule</span></span>
<span data-ttu-id="2ddff-121">Lista reguł definiująca określonej konfiguracji aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="2ddff-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="2ddff-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ddff-122">-Confirm</span></span>
<span data-ttu-id="2ddff-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ddff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ddff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ddff-124">-WhatIf</span></span>
<span data-ttu-id="2ddff-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ddff-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ddff-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ddff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ddff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ddff-127">CommonParameters</span></span>
<span data-ttu-id="2ddff-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ddff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ddff-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ddff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ddff-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ddff-130">INPUTS</span></span>

### <span data-ttu-id="2ddff-131">Brak</span><span class="sxs-lookup"><span data-stu-id="2ddff-131">None</span></span>

## <span data-ttu-id="2ddff-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ddff-132">OUTPUTS</span></span>

### <span data-ttu-id="2ddff-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="2ddff-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="2ddff-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ddff-134">NOTES</span></span>

## <span data-ttu-id="2ddff-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ddff-135">RELATED LINKS</span></span>
