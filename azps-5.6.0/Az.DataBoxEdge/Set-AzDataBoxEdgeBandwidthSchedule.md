---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: d0f5d0d71f35df5bb36ea86a1ec20ca009256f67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983185"
---
# <span data-ttu-id="b4d50-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4d50-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b4d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d50-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d50-103">Aktualizuje harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="b4d50-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="b4d50-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4d50-104">SYNTAX</span></span>

### <span data-ttu-id="b4d50-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4d50-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d50-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d50-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="b4d50-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d50-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4d50-114">DESCRIPTION</span></span>
<span data-ttu-id="b4d50-115">Polecenie **cmdlet Set-AzDataBoxEdgeBandwidthSchedule** aktualizuje harmonogram przepustowości dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="b4d50-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="b4d50-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4d50-116">EXAMPLES</span></span>

### <span data-ttu-id="b4d50-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4d50-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="b4d50-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4d50-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="b4d50-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4d50-119">PARAMETERS</span></span>

### <span data-ttu-id="b4d50-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b4d50-120">-AsJob</span></span>
<span data-ttu-id="b4d50-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4d50-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4d50-122">— Przepustowość</span><span class="sxs-lookup"><span data-stu-id="b4d50-122">-Bandwidth</span></span>
<span data-ttu-id="b4d50-123">Przepustowość w Mb/s</span><span class="sxs-lookup"><span data-stu-id="b4d50-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="b4d50-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b4d50-124">-DaysOfWeek</span></span>
<span data-ttu-id="b4d50-125">Zaplanowane dniWeek</span><span class="sxs-lookup"><span data-stu-id="b4d50-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="b4d50-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d50-126">-DefaultProfile</span></span>
<span data-ttu-id="b4d50-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d50-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d50-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b4d50-128">-DeviceName</span></span>
<span data-ttu-id="b4d50-129">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b4d50-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d50-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d50-130">-InputObject</span></span>
<span data-ttu-id="b4d50-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d50-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d50-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b4d50-132">-Name</span></span>
<span data-ttu-id="b4d50-133">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="b4d50-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d50-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d50-134">-ResourceGroupName</span></span>
<span data-ttu-id="b4d50-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b4d50-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d50-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d50-136">-ResourceId</span></span>
<span data-ttu-id="b4d50-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d50-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d50-138">— StartTime</span><span class="sxs-lookup"><span data-stu-id="b4d50-138">-StartTime</span></span>
<span data-ttu-id="b4d50-139">Zaplanuj czas rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="b4d50-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="b4d50-140">- StopTime</span><span class="sxs-lookup"><span data-stu-id="b4d50-140">-StopTime</span></span>
<span data-ttu-id="b4d50-141">Zaplanuj czas zatrzymania</span><span class="sxs-lookup"><span data-stu-id="b4d50-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="b4d50-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="b4d50-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b4d50-143">Ustawi nieograniczoną przepustowość</span><span class="sxs-lookup"><span data-stu-id="b4d50-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d50-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4d50-144">-Confirm</span></span>
<span data-ttu-id="b4d50-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b4d50-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d50-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d50-146">-WhatIf</span></span>
<span data-ttu-id="b4d50-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d50-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4d50-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b4d50-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d50-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d50-149">CommonParameters</span></span>
<span data-ttu-id="b4d50-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d50-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d50-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4d50-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d50-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4d50-152">INPUTS</span></span>

### <span data-ttu-id="b4d50-153">Brak</span><span class="sxs-lookup"><span data-stu-id="b4d50-153">None</span></span>

## <span data-ttu-id="b4d50-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4d50-154">OUTPUTS</span></span>

### <span data-ttu-id="b4d50-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b4d50-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b4d50-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4d50-156">NOTES</span></span>

## <span data-ttu-id="b4d50-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4d50-157">RELATED LINKS</span></span>
