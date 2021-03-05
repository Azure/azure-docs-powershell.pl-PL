---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: fbb0801dd586731a938c773711d72847e7a96e50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997809"
---
# <span data-ttu-id="7f444-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="7f444-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="7f444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f444-102">SYNOPSIS</span></span>
<span data-ttu-id="7f444-103">Tworzenie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="7f444-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="7f444-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f444-104">SYNTAX</span></span>

### <span data-ttu-id="7f444-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f444-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f444-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7f444-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f444-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7f444-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f444-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f444-108">DESCRIPTION</span></span>
<span data-ttu-id="7f444-109">Utwórz trasę, aby wysłać określone źródło danych i warunek do odpowiedniego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="7f444-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="7f444-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f444-110">EXAMPLES</span></span>

### <span data-ttu-id="7f444-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f444-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="7f444-112">Utwórz nową trasę "R1".</span><span class="sxs-lookup"><span data-stu-id="7f444-112">Create a new route "R1".</span></span>

## <span data-ttu-id="7f444-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f444-113">PARAMETERS</span></span>

### <span data-ttu-id="7f444-114">— Warunek</span><span class="sxs-lookup"><span data-stu-id="7f444-114">-Condition</span></span>
<span data-ttu-id="7f444-115">Warunek oceniany w celu zastosowania reguły routingu</span><span class="sxs-lookup"><span data-stu-id="7f444-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="7f444-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f444-116">-DefaultProfile</span></span>
<span data-ttu-id="7f444-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f444-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f444-118">— włączone</span><span class="sxs-lookup"><span data-stu-id="7f444-118">-Enabled</span></span>
<span data-ttu-id="7f444-119">Włącz trasę</span><span class="sxs-lookup"><span data-stu-id="7f444-119">Enable route</span></span>

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

### <span data-ttu-id="7f444-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f444-120">-EndpointName</span></span>
<span data-ttu-id="7f444-121">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="7f444-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="7f444-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f444-122">-InputObject</span></span>
<span data-ttu-id="7f444-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="7f444-123">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f444-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7f444-124">-Name</span></span>
<span data-ttu-id="7f444-125">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="7f444-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f444-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f444-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f444-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7f444-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f444-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f444-128">-ResourceId</span></span>
<span data-ttu-id="7f444-129">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="7f444-129">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f444-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="7f444-130">-RouteName</span></span>
<span data-ttu-id="7f444-131">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="7f444-131">Name of the Route</span></span>

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

### <span data-ttu-id="7f444-132">— Źródło</span><span class="sxs-lookup"><span data-stu-id="7f444-132">-Source</span></span>
<span data-ttu-id="7f444-133">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="7f444-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f444-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f444-134">-Confirm</span></span>
<span data-ttu-id="7f444-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f444-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f444-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f444-136">-WhatIf</span></span>
<span data-ttu-id="7f444-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f444-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f444-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f444-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f444-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f444-139">CommonParameters</span></span>
<span data-ttu-id="7f444-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f444-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f444-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f444-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f444-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f444-142">INPUTS</span></span>

### <span data-ttu-id="7f444-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7f444-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7f444-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7f444-144">System.String</span></span>

## <span data-ttu-id="7f444-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f444-145">OUTPUTS</span></span>

### <span data-ttu-id="7f444-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="7f444-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="7f444-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f444-147">NOTES</span></span>

## <span data-ttu-id="7f444-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f444-148">RELATED LINKS</span></span>
