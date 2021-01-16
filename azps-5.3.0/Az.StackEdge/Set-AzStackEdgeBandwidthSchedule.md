---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374297"
---
# <span data-ttu-id="5a588-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5a588-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="5a588-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a588-102">SYNOPSIS</span></span>
<span data-ttu-id="5a588-103">Aktualizuje harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="5a588-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="5a588-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a588-104">SYNTAX</span></span>

### <span data-ttu-id="5a588-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5a588-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a588-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a588-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5a588-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5a588-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a588-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5a588-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5a588-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5a588-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a588-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="5a588-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a588-114">Opis</span><span class="sxs-lookup"><span data-stu-id="5a588-114">DESCRIPTION</span></span>
<span data-ttu-id="5a588-115">Polecenie cmdlet **Set-AzStackEdgeBandwidthSchedule** aktualizuje harmonogram przepustowości urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="5a588-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="5a588-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a588-116">EXAMPLES</span></span>

### <span data-ttu-id="5a588-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a588-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="5a588-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5a588-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="5a588-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a588-119">PARAMETERS</span></span>

### <span data-ttu-id="5a588-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a588-120">-AsJob</span></span>
<span data-ttu-id="5a588-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5a588-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a588-122">-Przepustowość</span><span class="sxs-lookup"><span data-stu-id="5a588-122">-Bandwidth</span></span>
<span data-ttu-id="5a588-123">Przepustowość w MB/s</span><span class="sxs-lookup"><span data-stu-id="5a588-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="5a588-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="5a588-124">-DaysOfWeek</span></span>
<span data-ttu-id="5a588-125">Zaplanowane DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="5a588-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="5a588-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a588-126">-DefaultProfile</span></span>
<span data-ttu-id="5a588-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a588-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a588-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5a588-128">-DeviceName</span></span>
<span data-ttu-id="5a588-129">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="5a588-129">Device Name</span></span>

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

### <span data-ttu-id="5a588-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a588-130">-InputObject</span></span>
<span data-ttu-id="5a588-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a588-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="5a588-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a588-132">-Name</span></span>
<span data-ttu-id="5a588-133">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="5a588-133">Resource Name</span></span>

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

### <span data-ttu-id="5a588-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a588-134">-ResourceGroupName</span></span>
<span data-ttu-id="5a588-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5a588-135">Resource Group Name</span></span>

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

### <span data-ttu-id="5a588-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a588-136">-ResourceId</span></span>
<span data-ttu-id="5a588-137">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a588-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="5a588-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5a588-138">-StartTime</span></span>
<span data-ttu-id="5a588-139">Planowanie godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="5a588-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="5a588-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="5a588-140">-StopTime</span></span>
<span data-ttu-id="5a588-141">Planowanie godziny zakończenia</span><span class="sxs-lookup"><span data-stu-id="5a588-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="5a588-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="5a588-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="5a588-143">Ustawia przepustowość bez ograniczeń</span><span class="sxs-lookup"><span data-stu-id="5a588-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="5a588-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a588-144">-Confirm</span></span>
<span data-ttu-id="5a588-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a588-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a588-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a588-146">-WhatIf</span></span>
<span data-ttu-id="5a588-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a588-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a588-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5a588-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a588-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a588-149">CommonParameters</span></span>
<span data-ttu-id="5a588-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a588-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a588-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a588-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a588-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a588-152">INPUTS</span></span>

### <span data-ttu-id="5a588-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5a588-153">None</span></span>

## <span data-ttu-id="5a588-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a588-154">OUTPUTS</span></span>

### <span data-ttu-id="5a588-155">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="5a588-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="5a588-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a588-156">NOTES</span></span>

## <span data-ttu-id="5a588-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a588-157">RELATED LINKS</span></span>
