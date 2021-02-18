---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239962"
---
# <span data-ttu-id="e84f9-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="e84f9-101">Update-AzActionRule</span></span>

## <span data-ttu-id="e84f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e84f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e84f9-103">Aktualizuje właściwości reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="e84f9-103">Updates action rule properties.</span></span>

## <span data-ttu-id="e84f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e84f9-104">SYNTAX</span></span>

### <span data-ttu-id="e84f9-105">ByNameSimplifiedPatch (Default)</span><span class="sxs-lookup"><span data-stu-id="e84f9-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e84f9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e84f9-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e84f9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e84f9-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e84f9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e84f9-108">DESCRIPTION</span></span>
<span data-ttu-id="e84f9-109">**Polecenie cmdlet Update-AzActionRule** aktualizuje właściwości reguły akcji — stan i tagi.</span><span class="sxs-lookup"><span data-stu-id="e84f9-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="e84f9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e84f9-110">EXAMPLES</span></span>

### <span data-ttu-id="e84f9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e84f9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="e84f9-112">To polecenie cmdlet wyłącza regułę akcji.</span><span class="sxs-lookup"><span data-stu-id="e84f9-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="e84f9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e84f9-113">PARAMETERS</span></span>

### <span data-ttu-id="e84f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84f9-114">-DefaultProfile</span></span>
<span data-ttu-id="e84f9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e84f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e84f9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e84f9-116">-InputObject</span></span>
<span data-ttu-id="e84f9-117">Zasób reguły akcji</span><span class="sxs-lookup"><span data-stu-id="e84f9-117">The action rule resource</span></span>

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

### <span data-ttu-id="e84f9-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e84f9-118">-Name</span></span>
<span data-ttu-id="e84f9-119">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="e84f9-119">Action rule name</span></span>

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

### <span data-ttu-id="e84f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e84f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="e84f9-121">Nazwa reguły akcji</span><span class="sxs-lookup"><span data-stu-id="e84f9-121">Action rule name</span></span>

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

### <span data-ttu-id="e84f9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e84f9-122">-ResourceId</span></span>
<span data-ttu-id="e84f9-123">Identyfikator zasobu reguły akcji</span><span class="sxs-lookup"><span data-stu-id="e84f9-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="e84f9-124">— Status</span><span class="sxs-lookup"><span data-stu-id="e84f9-124">-Status</span></span>
<span data-ttu-id="e84f9-125">Stan reguły akcji</span><span class="sxs-lookup"><span data-stu-id="e84f9-125">Action rule status</span></span>

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

### <span data-ttu-id="e84f9-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="e84f9-126">-Tag</span></span>
<span data-ttu-id="e84f9-127">Tagi reguł akcji</span><span class="sxs-lookup"><span data-stu-id="e84f9-127">Action rule tags</span></span>

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

### <span data-ttu-id="e84f9-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e84f9-128">-Confirm</span></span>
<span data-ttu-id="e84f9-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e84f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e84f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e84f9-130">-WhatIf</span></span>
<span data-ttu-id="e84f9-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e84f9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e84f9-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e84f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e84f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84f9-133">CommonParameters</span></span>
<span data-ttu-id="e84f9-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84f9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e84f9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84f9-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e84f9-136">INPUTS</span></span>

### <span data-ttu-id="e84f9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e84f9-137">System.String</span></span>

### <span data-ttu-id="e84f9-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e84f9-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e84f9-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e84f9-139">OUTPUTS</span></span>

### <span data-ttu-id="e84f9-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e84f9-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e84f9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e84f9-141">NOTES</span></span>

## <span data-ttu-id="e84f9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e84f9-142">RELATED LINKS</span></span>
