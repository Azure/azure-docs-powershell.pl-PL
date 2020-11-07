---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: f761a84fe994f0da68b4d3a86b513ba333b06573
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891562"
---
# <span data-ttu-id="afa87-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="afa87-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="afa87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afa87-102">SYNOPSIS</span></span>
<span data-ttu-id="afa87-103">Aktualizuje harmonogram przepustowości.</span><span class="sxs-lookup"><span data-stu-id="afa87-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="afa87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afa87-104">SYNTAX</span></span>

### <span data-ttu-id="afa87-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="afa87-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa87-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afa87-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="afa87-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="afa87-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa87-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="afa87-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="afa87-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="afa87-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa87-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="afa87-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afa87-114">Opis</span><span class="sxs-lookup"><span data-stu-id="afa87-114">DESCRIPTION</span></span>
<span data-ttu-id="afa87-115">Polecenie cmdlet **Set-AzDataBoxEdgeBandwidthSchedule** aktualizuje harmonogram przepustowości dla urządzenia z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="afa87-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="afa87-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afa87-116">EXAMPLES</span></span>

### <span data-ttu-id="afa87-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afa87-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="afa87-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="afa87-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="afa87-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afa87-119">PARAMETERS</span></span>

### <span data-ttu-id="afa87-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afa87-120">-AsJob</span></span>
<span data-ttu-id="afa87-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="afa87-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afa87-122">-Przepustowość</span><span class="sxs-lookup"><span data-stu-id="afa87-122">-Bandwidth</span></span>
<span data-ttu-id="afa87-123">Przepustowość w MB/s</span><span class="sxs-lookup"><span data-stu-id="afa87-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="afa87-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="afa87-124">-DaysOfWeek</span></span>
<span data-ttu-id="afa87-125">Zaplanowane DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="afa87-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="afa87-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa87-126">-DefaultProfile</span></span>
<span data-ttu-id="afa87-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afa87-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa87-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="afa87-128">-DeviceName</span></span>
<span data-ttu-id="afa87-129">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="afa87-129">Device Name</span></span>

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

### <span data-ttu-id="afa87-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afa87-130">-InputObject</span></span>
<span data-ttu-id="afa87-131">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="afa87-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="afa87-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afa87-132">-Name</span></span>
<span data-ttu-id="afa87-133">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="afa87-133">Resource Name</span></span>

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

### <span data-ttu-id="afa87-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa87-134">-ResourceGroupName</span></span>
<span data-ttu-id="afa87-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="afa87-135">Resource Group Name</span></span>

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

### <span data-ttu-id="afa87-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afa87-136">-ResourceId</span></span>
<span data-ttu-id="afa87-137">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="afa87-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="afa87-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="afa87-138">-StartTime</span></span>
<span data-ttu-id="afa87-139">Planowanie godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="afa87-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="afa87-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="afa87-140">-StopTime</span></span>
<span data-ttu-id="afa87-141">Planowanie godziny zakończenia</span><span class="sxs-lookup"><span data-stu-id="afa87-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="afa87-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="afa87-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="afa87-143">Ustawia przepustowość bez ograniczeń</span><span class="sxs-lookup"><span data-stu-id="afa87-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="afa87-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afa87-144">-Confirm</span></span>
<span data-ttu-id="afa87-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa87-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa87-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa87-146">-WhatIf</span></span>
<span data-ttu-id="afa87-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa87-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afa87-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afa87-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa87-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa87-149">CommonParameters</span></span>
<span data-ttu-id="afa87-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa87-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa87-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afa87-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa87-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afa87-152">INPUTS</span></span>

### <span data-ttu-id="afa87-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="afa87-153">None</span></span>

## <span data-ttu-id="afa87-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afa87-154">OUTPUTS</span></span>

### <span data-ttu-id="afa87-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="afa87-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="afa87-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afa87-156">NOTES</span></span>

## <span data-ttu-id="afa87-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afa87-157">RELATED LINKS</span></span>
