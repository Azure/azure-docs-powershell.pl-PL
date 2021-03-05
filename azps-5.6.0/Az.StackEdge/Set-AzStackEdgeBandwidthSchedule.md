---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 17221e2d4f88e2f59ee13f73fb18132c01f6632e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994890"
---
# <span data-ttu-id="dd076-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="dd076-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="dd076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd076-102">SYNOPSIS</span></span>
<span data-ttu-id="dd076-103">Aktualizuje harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="dd076-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="dd076-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd076-104">SYNTAX</span></span>

### <span data-ttu-id="dd076-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dd076-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd076-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd076-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dd076-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dd076-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd076-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dd076-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dd076-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dd076-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd076-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dd076-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd076-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd076-114">DESCRIPTION</span></span>
<span data-ttu-id="dd076-115">Polecenie **cmdlet Set-AzStackEdgeBandwidthSchedule** aktualizuje harmonogram przepustowości dla urządzenia Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="dd076-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="dd076-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd076-116">EXAMPLES</span></span>

### <span data-ttu-id="dd076-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd076-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="dd076-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dd076-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="dd076-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd076-119">PARAMETERS</span></span>

### <span data-ttu-id="dd076-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="dd076-120">-AsJob</span></span>
<span data-ttu-id="dd076-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dd076-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd076-122">— Przepustowość</span><span class="sxs-lookup"><span data-stu-id="dd076-122">-Bandwidth</span></span>
<span data-ttu-id="dd076-123">Przepustowość w Mb/s</span><span class="sxs-lookup"><span data-stu-id="dd076-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dd076-124">-DaysOfWeek</span></span>
<span data-ttu-id="dd076-125">Zaplanowane dniWeek</span><span class="sxs-lookup"><span data-stu-id="dd076-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd076-126">-DefaultProfile</span></span>
<span data-ttu-id="dd076-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd076-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd076-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dd076-128">-DeviceName</span></span>
<span data-ttu-id="dd076-129">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="dd076-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd076-130">-InputObject</span></span>
<span data-ttu-id="dd076-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd076-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd076-132">-Name</span></span>
<span data-ttu-id="dd076-133">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="dd076-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd076-134">-ResourceGroupName</span></span>
<span data-ttu-id="dd076-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dd076-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd076-136">-ResourceId</span></span>
<span data-ttu-id="dd076-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd076-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-138">— StartTime</span><span class="sxs-lookup"><span data-stu-id="dd076-138">-StartTime</span></span>
<span data-ttu-id="dd076-139">Zaplanuj czas rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="dd076-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="dd076-140">- StopTime</span><span class="sxs-lookup"><span data-stu-id="dd076-140">-StopTime</span></span>
<span data-ttu-id="dd076-141">Zaplanuj czas zatrzymania</span><span class="sxs-lookup"><span data-stu-id="dd076-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="dd076-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="dd076-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="dd076-143">Ustawi nieograniczoną przepustowość</span><span class="sxs-lookup"><span data-stu-id="dd076-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd076-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd076-144">-Confirm</span></span>
<span data-ttu-id="dd076-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd076-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd076-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd076-146">-WhatIf</span></span>
<span data-ttu-id="dd076-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd076-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd076-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd076-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd076-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd076-149">CommonParameters</span></span>
<span data-ttu-id="dd076-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd076-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd076-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd076-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd076-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd076-152">INPUTS</span></span>

### <span data-ttu-id="dd076-153">Brak</span><span class="sxs-lookup"><span data-stu-id="dd076-153">None</span></span>

## <span data-ttu-id="dd076-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd076-154">OUTPUTS</span></span>

### <span data-ttu-id="dd076-155">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="dd076-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="dd076-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd076-156">NOTES</span></span>

## <span data-ttu-id="dd076-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd076-157">RELATED LINKS</span></span>
