---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049964"
---
# <span data-ttu-id="0abd1-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0abd1-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="0abd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0abd1-102">SYNOPSIS</span></span>
<span data-ttu-id="0abd1-103">Tworzy nowy harmonogram przepustowości</span><span class="sxs-lookup"><span data-stu-id="0abd1-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="0abd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0abd1-104">SYNTAX</span></span>

### <span data-ttu-id="0abd1-105">UnlimitedBandwidthParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0abd1-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0abd1-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="0abd1-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0abd1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0abd1-107">DESCRIPTION</span></span>
<span data-ttu-id="0abd1-108">Polecenie cmdlet **New-AzStackEdgeBandwidthSchedule** tworzy nowy harmonogram przepustowości dla urządzenia ze stosem, aby ułatwić zarządzanie użyciem przepustowości.</span><span class="sxs-lookup"><span data-stu-id="0abd1-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="0abd1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0abd1-109">EXAMPLES</span></span>

### <span data-ttu-id="0abd1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0abd1-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="0abd1-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0abd1-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="0abd1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0abd1-112">PARAMETERS</span></span>

### <span data-ttu-id="0abd1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0abd1-113">-AsJob</span></span>
<span data-ttu-id="0abd1-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0abd1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0abd1-115">-Przepustowość</span><span class="sxs-lookup"><span data-stu-id="0abd1-115">-Bandwidth</span></span>
<span data-ttu-id="0abd1-116">Przepustowość w MB/s</span><span class="sxs-lookup"><span data-stu-id="0abd1-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="0abd1-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0abd1-117">-DaysOfWeek</span></span>
<span data-ttu-id="0abd1-118">Zaplanowane DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0abd1-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="0abd1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abd1-119">-DefaultProfile</span></span>
<span data-ttu-id="0abd1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0abd1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0abd1-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0abd1-121">-DeviceName</span></span>
<span data-ttu-id="0abd1-122">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="0abd1-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd1-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0abd1-123">-Name</span></span>
<span data-ttu-id="0abd1-124">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="0abd1-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0abd1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0abd1-125">-ResourceGroupName</span></span>
<span data-ttu-id="0abd1-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0abd1-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0abd1-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0abd1-127">-StartTime</span></span>
<span data-ttu-id="0abd1-128">Planowanie godziny rozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="0abd1-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="0abd1-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="0abd1-129">-StopTime</span></span>
<span data-ttu-id="0abd1-130">Planowanie godziny zakończenia</span><span class="sxs-lookup"><span data-stu-id="0abd1-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="0abd1-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="0abd1-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="0abd1-132">Ustawienie przepustowości jako bez ograniczeń</span><span class="sxs-lookup"><span data-stu-id="0abd1-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0abd1-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0abd1-133">-Confirm</span></span>
<span data-ttu-id="0abd1-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0abd1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0abd1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0abd1-135">-WhatIf</span></span>
<span data-ttu-id="0abd1-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0abd1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0abd1-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0abd1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0abd1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abd1-138">CommonParameters</span></span>
<span data-ttu-id="0abd1-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0abd1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abd1-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0abd1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abd1-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0abd1-141">INPUTS</span></span>

### <span data-ttu-id="0abd1-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0abd1-142">None</span></span>

## <span data-ttu-id="0abd1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0abd1-143">OUTPUTS</span></span>

### <span data-ttu-id="0abd1-144">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="0abd1-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="0abd1-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0abd1-145">NOTES</span></span>

## <span data-ttu-id="0abd1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0abd1-146">RELATED LINKS</span></span>
