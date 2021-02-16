---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188666"
---
# <span data-ttu-id="864e8-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="864e8-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="864e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="864e8-102">SYNOPSIS</span></span>
<span data-ttu-id="864e8-103">Tworzy nowy harmonogram przepustowości</span><span class="sxs-lookup"><span data-stu-id="864e8-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="864e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="864e8-104">SYNTAX</span></span>

### <span data-ttu-id="864e8-105">BandwidthParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="864e8-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="864e8-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="864e8-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864e8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="864e8-107">DESCRIPTION</span></span>
<span data-ttu-id="864e8-108">Polecenie cmdlet **New-AzDataBoxEdgeBandwidthSchedule** tworzy nowy harmonogram przepustowości dla urządzenia z krawędzią pola danych, aby ułatwić zarządzanie użyciem przepustowości.</span><span class="sxs-lookup"><span data-stu-id="864e8-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="864e8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="864e8-109">EXAMPLES</span></span>

### <span data-ttu-id="864e8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="864e8-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="864e8-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="864e8-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="864e8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="864e8-112">PARAMETERS</span></span>

### <span data-ttu-id="864e8-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="864e8-113">-AsJob</span></span>
<span data-ttu-id="864e8-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="864e8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="864e8-115">— Przepustowość</span><span class="sxs-lookup"><span data-stu-id="864e8-115">-Bandwidth</span></span>
<span data-ttu-id="864e8-116">Przepustowość w mb/s</span><span class="sxs-lookup"><span data-stu-id="864e8-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="864e8-117">-DaysOfWeek</span></span>
<span data-ttu-id="864e8-118">Zaplanowane dniWeek</span><span class="sxs-lookup"><span data-stu-id="864e8-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864e8-119">-DefaultProfile</span></span>
<span data-ttu-id="864e8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="864e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="864e8-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="864e8-121">-DeviceName</span></span>
<span data-ttu-id="864e8-122">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="864e8-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="864e8-123">-Name</span></span>
<span data-ttu-id="864e8-124">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="864e8-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="864e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="864e8-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="864e8-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-127">— StartTime</span><span class="sxs-lookup"><span data-stu-id="864e8-127">-StartTime</span></span>
<span data-ttu-id="864e8-128">Zaplanuj czas rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="864e8-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-129">- StopTime</span><span class="sxs-lookup"><span data-stu-id="864e8-129">-StopTime</span></span>
<span data-ttu-id="864e8-130">Zaplanuj czas zatrzymania</span><span class="sxs-lookup"><span data-stu-id="864e8-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="864e8-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="864e8-132">Ustawi nieograniczoną przepustowość, jeśli zostanie ustawiona wartość fałsz, ustawi wartość domyślną na 20 Mb/s</span><span class="sxs-lookup"><span data-stu-id="864e8-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e8-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="864e8-133">-Confirm</span></span>
<span data-ttu-id="864e8-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="864e8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="864e8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864e8-135">-WhatIf</span></span>
<span data-ttu-id="864e8-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="864e8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="864e8-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="864e8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="864e8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864e8-138">CommonParameters</span></span>
<span data-ttu-id="864e8-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="864e8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864e8-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="864e8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864e8-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="864e8-141">INPUTS</span></span>

### <span data-ttu-id="864e8-142">Brak</span><span class="sxs-lookup"><span data-stu-id="864e8-142">None</span></span>

## <span data-ttu-id="864e8-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="864e8-143">OUTPUTS</span></span>

### <span data-ttu-id="864e8-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="864e8-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="864e8-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="864e8-145">NOTES</span></span>

## <span data-ttu-id="864e8-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="864e8-146">RELATED LINKS</span></span>
