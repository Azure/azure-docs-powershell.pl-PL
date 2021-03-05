---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: e7659c6437e9566a4793e12518a30067aa73297a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005073"
---
# <span data-ttu-id="97bdf-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="97bdf-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="97bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="97bdf-103">Usuwa istniejący wyzwalacz na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="97bdf-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="97bdf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97bdf-104">SYNTAX</span></span>

### <span data-ttu-id="97bdf-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="97bdf-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97bdf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97bdf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97bdf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97bdf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97bdf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="97bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="97bdf-109">Polecenie **cmdlet Remove-AzStackEdgeTrigger** usuwa istniejący wyzwalacz na urządzeniu Ze stosem Edge.</span><span class="sxs-lookup"><span data-stu-id="97bdf-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="97bdf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="97bdf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97bdf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="97bdf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97bdf-112">PARAMETERS</span></span>

### <span data-ttu-id="97bdf-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="97bdf-113">-AsJob</span></span>
<span data-ttu-id="97bdf-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="97bdf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97bdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97bdf-115">-DefaultProfile</span></span>
<span data-ttu-id="97bdf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97bdf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97bdf-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="97bdf-117">-DeviceName</span></span>
<span data-ttu-id="97bdf-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="97bdf-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97bdf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97bdf-119">-InputObject</span></span>
<span data-ttu-id="97bdf-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="97bdf-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97bdf-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97bdf-121">-Name</span></span>
<span data-ttu-id="97bdf-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="97bdf-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97bdf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97bdf-123">-PassThru</span></span>
<span data-ttu-id="97bdf-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="97bdf-124">returns true if successful</span></span>

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

### <span data-ttu-id="97bdf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97bdf-125">-ResourceGroupName</span></span>
<span data-ttu-id="97bdf-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="97bdf-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97bdf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97bdf-127">-ResourceId</span></span>
<span data-ttu-id="97bdf-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="97bdf-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97bdf-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97bdf-129">-Confirm</span></span>
<span data-ttu-id="97bdf-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97bdf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97bdf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97bdf-131">-WhatIf</span></span>
<span data-ttu-id="97bdf-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97bdf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97bdf-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="97bdf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97bdf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97bdf-134">CommonParameters</span></span>
<span data-ttu-id="97bdf-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97bdf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97bdf-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97bdf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97bdf-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97bdf-137">INPUTS</span></span>

### <span data-ttu-id="97bdf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="97bdf-138">System.String</span></span>

### <span data-ttu-id="97bdf-139">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="97bdf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="97bdf-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97bdf-140">OUTPUTS</span></span>

### <span data-ttu-id="97bdf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97bdf-141">System.Boolean</span></span>

## <span data-ttu-id="97bdf-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97bdf-142">NOTES</span></span>

## <span data-ttu-id="97bdf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97bdf-143">RELATED LINKS</span></span>
