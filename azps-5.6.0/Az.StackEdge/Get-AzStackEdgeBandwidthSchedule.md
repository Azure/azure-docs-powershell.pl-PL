---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: e13992fdd8a14a75c859312b62833dc66b2e539a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011457"
---
# <span data-ttu-id="25be4-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="25be4-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="25be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25be4-102">SYNOPSIS</span></span>
<span data-ttu-id="25be4-103">Pobiera informacje na temat harmonogramów przepustowości</span><span class="sxs-lookup"><span data-stu-id="25be4-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="25be4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25be4-104">SYNTAX</span></span>

### <span data-ttu-id="25be4-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="25be4-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25be4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25be4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25be4-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25be4-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25be4-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25be4-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="25be4-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="25be4-109">DESCRIPTION</span></span>
<span data-ttu-id="25be4-110">Polecenie **cmdlet Get-AzStackEdgeBandwidthSchedule** pobiera informacje o harmonogramach przepustowości.</span><span class="sxs-lookup"><span data-stu-id="25be4-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="25be4-111">Możesz określić nazwę harmonogramu wraz z nazwą grupy zasobów i nazwą urządzenia, aby uzyskać informacje o określonym harmonogramie przepustowości</span><span class="sxs-lookup"><span data-stu-id="25be4-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="25be4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25be4-112">EXAMPLES</span></span>

### <span data-ttu-id="25be4-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25be4-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="25be4-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="25be4-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="25be4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25be4-115">PARAMETERS</span></span>

### <span data-ttu-id="25be4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25be4-116">-DefaultProfile</span></span>
<span data-ttu-id="25be4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25be4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25be4-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="25be4-118">-DeviceName</span></span>
<span data-ttu-id="25be4-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="25be4-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25be4-120">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="25be4-120">-DeviceObject</span></span>
<span data-ttu-id="25be4-121">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="25be4-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25be4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25be4-122">-Name</span></span>
<span data-ttu-id="25be4-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="25be4-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25be4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25be4-124">-ResourceGroupName</span></span>
<span data-ttu-id="25be4-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="25be4-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25be4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25be4-126">-ResourceId</span></span>
<span data-ttu-id="25be4-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="25be4-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25be4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25be4-128">CommonParameters</span></span>
<span data-ttu-id="25be4-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25be4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25be4-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25be4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25be4-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25be4-131">INPUTS</span></span>

### <span data-ttu-id="25be4-132">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="25be4-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="25be4-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25be4-133">OUTPUTS</span></span>

### <span data-ttu-id="25be4-134">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="25be4-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="25be4-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25be4-135">NOTES</span></span>

## <span data-ttu-id="25be4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25be4-136">RELATED LINKS</span></span>
