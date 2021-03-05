---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993098"
---
# <span data-ttu-id="6c4b5-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="6c4b5-101">Update-AzActionRule</span></span>

## <span data-ttu-id="6c4b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4b5-103">Aktualizuje właściwości reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-103">Updates action rule properties.</span></span>

## <span data-ttu-id="6c4b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c4b5-104">SYNTAX</span></span>

### <span data-ttu-id="6c4b5-105">ByNameSimplifiedPatch (Default)</span><span class="sxs-lookup"><span data-stu-id="6c4b5-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4b5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4b5-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4b5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6c4b5-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c4b5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c4b5-108">DESCRIPTION</span></span>
<span data-ttu-id="6c4b5-109">**Polecenie cmdlet Update-AzActionRule** aktualizuje właściwości reguły akcji — stan i tagi.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="6c4b5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c4b5-110">EXAMPLES</span></span>

### <span data-ttu-id="6c4b5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c4b5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="6c4b5-112">To polecenie cmdlet wyłącza regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="6c4b5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c4b5-113">PARAMETERS</span></span>

### <span data-ttu-id="6c4b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4b5-114">-DefaultProfile</span></span>
<span data-ttu-id="6c4b5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4b5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c4b5-116">-InputObject</span></span>
<span data-ttu-id="6c4b5-117">Zasób reguły akcji</span><span class="sxs-lookup"><span data-stu-id="6c4b5-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b5-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6c4b5-118">-Name</span></span>
<span data-ttu-id="6c4b5-119">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="6c4b5-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4b5-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c4b5-121">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="6c4b5-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4b5-122">-ResourceId</span></span>
<span data-ttu-id="6c4b5-123">Identyfikator zasobu reguły akcji</span><span class="sxs-lookup"><span data-stu-id="6c4b5-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b5-124">— Status</span><span class="sxs-lookup"><span data-stu-id="6c4b5-124">-Status</span></span>
<span data-ttu-id="6c4b5-125">Stan reguły akcji</span><span class="sxs-lookup"><span data-stu-id="6c4b5-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b5-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="6c4b5-126">-Tag</span></span>
<span data-ttu-id="6c4b5-127">Tagi reguł akcji</span><span class="sxs-lookup"><span data-stu-id="6c4b5-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b5-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c4b5-128">-Confirm</span></span>
<span data-ttu-id="6c4b5-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c4b5-130">-WhatIf</span></span>
<span data-ttu-id="6c4b5-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c4b5-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4b5-133">CommonParameters</span></span>
<span data-ttu-id="6c4b5-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4b5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c4b5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4b5-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c4b5-136">INPUTS</span></span>

### <span data-ttu-id="6c4b5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6c4b5-137">System.String</span></span>

### <span data-ttu-id="6c4b5-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6c4b5-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6c4b5-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c4b5-139">OUTPUTS</span></span>

### <span data-ttu-id="6c4b5-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6c4b5-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6c4b5-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c4b5-141">NOTES</span></span>

## <span data-ttu-id="6c4b5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c4b5-142">RELATED LINKS</span></span>
