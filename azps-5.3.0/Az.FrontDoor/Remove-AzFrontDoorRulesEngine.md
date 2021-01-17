---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489701"
---
# <span data-ttu-id="5523c-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="5523c-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="5523c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5523c-102">SYNOPSIS</span></span>
<span data-ttu-id="5523c-103">Usunięcie aparatu reguł z przodu drzwi</span><span class="sxs-lookup"><span data-stu-id="5523c-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="5523c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5523c-104">SYNTAX</span></span>

### <span data-ttu-id="5523c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5523c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5523c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5523c-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5523c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5523c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5523c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5523c-108">DESCRIPTION</span></span>
<span data-ttu-id="5523c-109">Usunięcie aparatu reguł z przodu drzwi</span><span class="sxs-lookup"><span data-stu-id="5523c-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="5523c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5523c-110">EXAMPLES</span></span>

### <span data-ttu-id="5523c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5523c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="5523c-112">Usuwanie reguł konfiguracji aparatu.</span><span class="sxs-lookup"><span data-stu-id="5523c-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="5523c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5523c-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="5523c-114">Oczekiwano wyniku usunięcia nieistniejącej konfiguracji aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="5523c-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="5523c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5523c-115">PARAMETERS</span></span>

### <span data-ttu-id="5523c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5523c-116">-DefaultProfile</span></span>
<span data-ttu-id="5523c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5523c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5523c-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="5523c-118">-FrontDoorName</span></span>
<span data-ttu-id="5523c-119">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="5523c-119">Front Door name.</span></span>

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

### <span data-ttu-id="5523c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5523c-120">-InputObject</span></span>
<span data-ttu-id="5523c-121">Obiekt aparatu reguł do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="5523c-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="5523c-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5523c-122">-Name</span></span>
<span data-ttu-id="5523c-123">Nazwa aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="5523c-123">Rules engine name.</span></span>

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

### <span data-ttu-id="5523c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5523c-124">-PassThru</span></span>
<span data-ttu-id="5523c-125">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="5523c-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="5523c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5523c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5523c-127">Nazwa grupy zasobów, w której zostaną utworzone drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="5523c-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="5523c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5523c-128">-ResourceId</span></span>
<span data-ttu-id="5523c-129">Identyfikator zasobu RulesEngine do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="5523c-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="5523c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5523c-130">-Confirm</span></span>
<span data-ttu-id="5523c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5523c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5523c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5523c-132">-WhatIf</span></span>
<span data-ttu-id="5523c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5523c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5523c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5523c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5523c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5523c-135">CommonParameters</span></span>
<span data-ttu-id="5523c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5523c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5523c-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5523c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5523c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5523c-138">INPUTS</span></span>

### <span data-ttu-id="5523c-139">Microsoft. Azure. Commands. FrontDoor. models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="5523c-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="5523c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5523c-140">System.String</span></span>

## <span data-ttu-id="5523c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5523c-141">OUTPUTS</span></span>

### <span data-ttu-id="5523c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5523c-142">System.Boolean</span></span>

## <span data-ttu-id="5523c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5523c-143">NOTES</span></span>

## <span data-ttu-id="5523c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5523c-144">RELATED LINKS</span></span>
