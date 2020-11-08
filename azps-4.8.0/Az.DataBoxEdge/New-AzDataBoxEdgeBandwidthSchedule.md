---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221324"
---
# <span data-ttu-id="0f136-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0f136-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0f136-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f136-102">SYNOPSIS</span></span>
<span data-ttu-id="0f136-103">Tworzy nowy harmonogram przepustowości</span><span class="sxs-lookup"><span data-stu-id="0f136-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="0f136-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f136-104">SYNTAX</span></span>

### <span data-ttu-id="0f136-105">BandwidthParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f136-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f136-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f136-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f136-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0f136-107">DESCRIPTION</span></span>
<span data-ttu-id="0f136-108">Polecenie cmdlet **New-AzDataBoxEdgeBandwidthSchedule** tworzy nowy harmonogram przepustowości dla urządzenia z polem danych, aby ułatwić zarządzanie użyciem przepustowości.</span><span class="sxs-lookup"><span data-stu-id="0f136-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="0f136-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f136-109">EXAMPLES</span></span>

### <span data-ttu-id="0f136-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f136-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="0f136-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0f136-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="0f136-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f136-112">PARAMETERS</span></span>

### <span data-ttu-id="0f136-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f136-113">-AsJob</span></span>
<span data-ttu-id="0f136-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0f136-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f136-115">-Przepustowość</span><span class="sxs-lookup"><span data-stu-id="0f136-115">-Bandwidth</span></span>
<span data-ttu-id="0f136-116">Przepustowość w MB/s</span><span class="sxs-lookup"><span data-stu-id="0f136-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="0f136-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0f136-117">-DaysOfWeek</span></span>
<span data-ttu-id="0f136-118">Zaplanowane DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0f136-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="0f136-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f136-119">-DefaultProfile</span></span>
<span data-ttu-id="0f136-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f136-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f136-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0f136-121">-DeviceName</span></span>
<span data-ttu-id="0f136-122">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0f136-122">Device Name</span></span>

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

### <span data-ttu-id="0f136-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f136-123">-Name</span></span>
<span data-ttu-id="0f136-124">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0f136-124">Resource Name</span></span>

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

### <span data-ttu-id="0f136-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f136-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f136-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0f136-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0f136-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0f136-127">-StartTime</span></span>
<span data-ttu-id="0f136-128">Planowanie godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="0f136-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="0f136-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="0f136-129">-StopTime</span></span>
<span data-ttu-id="0f136-130">Planowanie godziny zakończenia</span><span class="sxs-lookup"><span data-stu-id="0f136-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="0f136-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="0f136-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="0f136-132">Ustawia przepustowość bez ograniczeń, jeśli ustawiono wartość FAŁSZ, ustawienie wartości domyślnej jako 20 MB/s</span><span class="sxs-lookup"><span data-stu-id="0f136-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="0f136-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f136-133">-Confirm</span></span>
<span data-ttu-id="0f136-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f136-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f136-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f136-135">-WhatIf</span></span>
<span data-ttu-id="0f136-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f136-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f136-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f136-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f136-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f136-138">CommonParameters</span></span>
<span data-ttu-id="0f136-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f136-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f136-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f136-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f136-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f136-141">INPUTS</span></span>

### <span data-ttu-id="0f136-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0f136-142">None</span></span>

## <span data-ttu-id="0f136-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f136-143">OUTPUTS</span></span>

### <span data-ttu-id="0f136-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0f136-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0f136-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f136-145">NOTES</span></span>

## <span data-ttu-id="0f136-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f136-146">RELATED LINKS</span></span>
