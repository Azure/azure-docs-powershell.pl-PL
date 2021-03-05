---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 84bcc64127636adc318935d1a7fd97f7ce79d760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015233"
---
# <span data-ttu-id="a35c1-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="a35c1-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="a35c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a35c1-103">Usuwanie aparatu reguł z drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="a35c1-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="a35c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a35c1-104">SYNTAX</span></span>

### <span data-ttu-id="a35c1-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a35c1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a35c1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35c1-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a35c1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a35c1-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a35c1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a35c1-108">DESCRIPTION</span></span>
<span data-ttu-id="a35c1-109">Usuwanie aparatu reguł z drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="a35c1-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="a35c1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a35c1-110">EXAMPLES</span></span>

### <span data-ttu-id="a35c1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a35c1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="a35c1-112">Usuń konfigurację aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="a35c1-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="a35c1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a35c1-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="a35c1-114">Oczekiwany wynik w przypadku usunięcia nieunikomej konfiguracji aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="a35c1-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="a35c1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a35c1-115">PARAMETERS</span></span>

### <span data-ttu-id="a35c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35c1-116">-DefaultProfile</span></span>
<span data-ttu-id="a35c1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a35c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a35c1-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a35c1-118">-FrontDoorName</span></span>
<span data-ttu-id="a35c1-119">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="a35c1-119">Front Door name.</span></span>

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

### <span data-ttu-id="a35c1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a35c1-120">-InputObject</span></span>
<span data-ttu-id="a35c1-121">Obiekt Aparat reguł do aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a35c1-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="a35c1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a35c1-122">-Name</span></span>
<span data-ttu-id="a35c1-123">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="a35c1-123">Rules engine name.</span></span>

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

### <span data-ttu-id="a35c1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a35c1-124">-PassThru</span></span>
<span data-ttu-id="a35c1-125">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="a35c1-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="a35c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a35c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="a35c1-127">Nazwa grupy zasobów, w przypadku których zostanie utworzona brama frontowa.</span><span class="sxs-lookup"><span data-stu-id="a35c1-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="a35c1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a35c1-128">-ResourceId</span></span>
<span data-ttu-id="a35c1-129">Identyfikator zasobu reguły do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a35c1-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="a35c1-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a35c1-130">-Confirm</span></span>
<span data-ttu-id="a35c1-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a35c1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a35c1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a35c1-132">-WhatIf</span></span>
<span data-ttu-id="a35c1-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a35c1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a35c1-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a35c1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a35c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35c1-135">CommonParameters</span></span>
<span data-ttu-id="a35c1-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35c1-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a35c1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35c1-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a35c1-138">INPUTS</span></span>

### <span data-ttu-id="a35c1-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="a35c1-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="a35c1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a35c1-140">System.String</span></span>

## <span data-ttu-id="a35c1-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a35c1-141">OUTPUTS</span></span>

### <span data-ttu-id="a35c1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a35c1-142">System.Boolean</span></span>

## <span data-ttu-id="a35c1-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a35c1-143">NOTES</span></span>

## <span data-ttu-id="a35c1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a35c1-144">RELATED LINKS</span></span>
