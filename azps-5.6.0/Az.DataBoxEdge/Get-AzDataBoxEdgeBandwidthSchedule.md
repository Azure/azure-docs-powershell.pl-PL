---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: bf41be0619998c030a6aec859ff433a3909af083
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998656"
---
# <span data-ttu-id="bd224-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="bd224-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="bd224-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd224-102">SYNOPSIS</span></span>
<span data-ttu-id="bd224-103">Pobiera informacje na temat harmonogramów przepustowości</span><span class="sxs-lookup"><span data-stu-id="bd224-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="bd224-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd224-104">SYNTAX</span></span>

### <span data-ttu-id="bd224-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bd224-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd224-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd224-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd224-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd224-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd224-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd224-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="bd224-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd224-109">DESCRIPTION</span></span>
<span data-ttu-id="bd224-110">Polecenie **cmdlet Get-AzDataBoxEdgeBandwidthSchedule** pobiera informacje o harmonogramach przepustowości.</span><span class="sxs-lookup"><span data-stu-id="bd224-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="bd224-111">Możesz określić nazwę harmonogramu wraz z nazwą grupy zasobów i nazwą urządzenia, aby uzyskać informacje o określonym harmonogramie przepustowości</span><span class="sxs-lookup"><span data-stu-id="bd224-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="bd224-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd224-112">EXAMPLES</span></span>

### <span data-ttu-id="bd224-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd224-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="bd224-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bd224-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="bd224-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd224-115">PARAMETERS</span></span>

### <span data-ttu-id="bd224-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd224-116">-DefaultProfile</span></span>
<span data-ttu-id="bd224-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd224-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd224-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bd224-118">-DeviceName</span></span>
<span data-ttu-id="bd224-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="bd224-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd224-120">— DeviceObject</span><span class="sxs-lookup"><span data-stu-id="bd224-120">-DeviceObject</span></span>
<span data-ttu-id="bd224-121">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="bd224-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd224-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bd224-122">-Name</span></span>
<span data-ttu-id="bd224-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="bd224-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd224-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd224-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd224-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bd224-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd224-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd224-126">-ResourceId</span></span>
<span data-ttu-id="bd224-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd224-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="bd224-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd224-128">CommonParameters</span></span>
<span data-ttu-id="bd224-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd224-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd224-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd224-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd224-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd224-131">INPUTS</span></span>

### <span data-ttu-id="bd224-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="bd224-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="bd224-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd224-133">OUTPUTS</span></span>

### <span data-ttu-id="bd224-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="bd224-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="bd224-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd224-135">NOTES</span></span>

## <span data-ttu-id="bd224-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd224-136">RELATED LINKS</span></span>
