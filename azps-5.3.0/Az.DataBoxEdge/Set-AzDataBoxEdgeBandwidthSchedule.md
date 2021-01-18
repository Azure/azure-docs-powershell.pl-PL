---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503711"
---
# <span data-ttu-id="0de21-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0de21-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0de21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0de21-102">SYNOPSIS</span></span>
<span data-ttu-id="0de21-103">Aktualizuje harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="0de21-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="0de21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0de21-104">SYNTAX</span></span>

### <span data-ttu-id="0de21-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0de21-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de21-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0de21-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0de21-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0de21-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0de21-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0de21-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0de21-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0de21-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="0de21-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de21-114">Opis</span><span class="sxs-lookup"><span data-stu-id="0de21-114">DESCRIPTION</span></span>
<span data-ttu-id="0de21-115">Polecenie cmdlet **Set-AzDataBoxEdgeBandwidthSchedule** aktualizuje harmonogram przepustowości dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="0de21-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="0de21-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0de21-116">EXAMPLES</span></span>

### <span data-ttu-id="0de21-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0de21-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="0de21-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0de21-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="0de21-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0de21-119">PARAMETERS</span></span>

### <span data-ttu-id="0de21-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0de21-120">-AsJob</span></span>
<span data-ttu-id="0de21-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0de21-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0de21-122">-Przepustowość</span><span class="sxs-lookup"><span data-stu-id="0de21-122">-Bandwidth</span></span>
<span data-ttu-id="0de21-123">Przepustowość w MB/s</span><span class="sxs-lookup"><span data-stu-id="0de21-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="0de21-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0de21-124">-DaysOfWeek</span></span>
<span data-ttu-id="0de21-125">Zaplanowane DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0de21-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="0de21-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de21-126">-DefaultProfile</span></span>
<span data-ttu-id="0de21-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0de21-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0de21-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0de21-128">-DeviceName</span></span>
<span data-ttu-id="0de21-129">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0de21-129">Device Name</span></span>

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

### <span data-ttu-id="0de21-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0de21-130">-InputObject</span></span>
<span data-ttu-id="0de21-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0de21-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="0de21-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0de21-132">-Name</span></span>
<span data-ttu-id="0de21-133">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0de21-133">Resource Name</span></span>

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

### <span data-ttu-id="0de21-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de21-134">-ResourceGroupName</span></span>
<span data-ttu-id="0de21-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0de21-135">Resource Group Name</span></span>

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

### <span data-ttu-id="0de21-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0de21-136">-ResourceId</span></span>
<span data-ttu-id="0de21-137">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0de21-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="0de21-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0de21-138">-StartTime</span></span>
<span data-ttu-id="0de21-139">Planowanie godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="0de21-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="0de21-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="0de21-140">-StopTime</span></span>
<span data-ttu-id="0de21-141">Planowanie godziny zakończenia</span><span class="sxs-lookup"><span data-stu-id="0de21-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="0de21-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="0de21-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="0de21-143">Ustawia przepustowość bez ograniczeń</span><span class="sxs-lookup"><span data-stu-id="0de21-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="0de21-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0de21-144">-Confirm</span></span>
<span data-ttu-id="0de21-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de21-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de21-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de21-146">-WhatIf</span></span>
<span data-ttu-id="0de21-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de21-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0de21-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0de21-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de21-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de21-149">CommonParameters</span></span>
<span data-ttu-id="0de21-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de21-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de21-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0de21-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de21-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0de21-152">INPUTS</span></span>

### <span data-ttu-id="0de21-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0de21-153">None</span></span>

## <span data-ttu-id="0de21-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0de21-154">OUTPUTS</span></span>

### <span data-ttu-id="0de21-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0de21-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0de21-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0de21-156">NOTES</span></span>

## <span data-ttu-id="0de21-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0de21-157">RELATED LINKS</span></span>
