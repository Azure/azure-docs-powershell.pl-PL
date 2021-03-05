---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 6020466feb5231c9634b01a5ccf5f8251616478f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005201"
---
# <span data-ttu-id="0bca5-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0bca5-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0bca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bca5-102">SYNOPSIS</span></span>
<span data-ttu-id="0bca5-103">Usuwa harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="0bca5-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="0bca5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0bca5-104">SYNTAX</span></span>

### <span data-ttu-id="0bca5-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0bca5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bca5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bca5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bca5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bca5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bca5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0bca5-108">DESCRIPTION</span></span>
<span data-ttu-id="0bca5-109">Polecenie **cmdlet Remove-AzStackEdgeBandwidthSchedule** usuwa harmonogram przepustowości dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="0bca5-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="0bca5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0bca5-110">EXAMPLES</span></span>

### <span data-ttu-id="0bca5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0bca5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="0bca5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bca5-112">PARAMETERS</span></span>

### <span data-ttu-id="0bca5-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0bca5-113">-AsJob</span></span>
<span data-ttu-id="0bca5-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0bca5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bca5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bca5-115">-DefaultProfile</span></span>
<span data-ttu-id="0bca5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0bca5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bca5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0bca5-117">-DeviceName</span></span>
<span data-ttu-id="0bca5-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0bca5-118">Device Name</span></span>

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

### <span data-ttu-id="0bca5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bca5-119">-InputObject</span></span>
<span data-ttu-id="0bca5-120">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="0bca5-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bca5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0bca5-121">-Name</span></span>
<span data-ttu-id="0bca5-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0bca5-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bca5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bca5-123">-PassThru</span></span>
<span data-ttu-id="0bca5-124">zwraca wartość prawda, jeśli pomyślnie</span><span class="sxs-lookup"><span data-stu-id="0bca5-124">returns true if successful</span></span>

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

### <span data-ttu-id="0bca5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bca5-125">-ResourceGroupName</span></span>
<span data-ttu-id="0bca5-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0bca5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0bca5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bca5-127">-ResourceId</span></span>
<span data-ttu-id="0bca5-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bca5-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bca5-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0bca5-129">-Confirm</span></span>
<span data-ttu-id="0bca5-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0bca5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bca5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bca5-131">-WhatIf</span></span>
<span data-ttu-id="0bca5-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bca5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bca5-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0bca5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bca5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bca5-134">CommonParameters</span></span>
<span data-ttu-id="0bca5-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bca5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bca5-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bca5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bca5-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bca5-137">INPUTS</span></span>

### <span data-ttu-id="0bca5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0bca5-138">System.String</span></span>

### <span data-ttu-id="0bca5-139">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0bca5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0bca5-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0bca5-140">OUTPUTS</span></span>

### <span data-ttu-id="0bca5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0bca5-141">System.Boolean</span></span>

## <span data-ttu-id="0bca5-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0bca5-142">NOTES</span></span>

## <span data-ttu-id="0bca5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0bca5-143">RELATED LINKS</span></span>
