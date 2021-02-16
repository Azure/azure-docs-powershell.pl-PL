---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185610"
---
# <span data-ttu-id="93e00-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="93e00-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="93e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e00-102">SYNOPSIS</span></span>
<span data-ttu-id="93e00-103">Aktualizowanie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="93e00-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="93e00-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93e00-104">SYNTAX</span></span>

### <span data-ttu-id="93e00-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="93e00-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e00-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="93e00-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e00-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="93e00-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e00-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="93e00-108">DESCRIPTION</span></span>
<span data-ttu-id="93e00-109">Edytowanie trasy.</span><span class="sxs-lookup"><span data-stu-id="93e00-109">Edit a route.</span></span> <span data-ttu-id="93e00-110">Możesz zaktualizować wszystkie pola w trasy, w tym źródło danych, punkt końcowy, zapytanie routingu, a także włączyć lub wyłączyć trasę.</span><span class="sxs-lookup"><span data-stu-id="93e00-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="93e00-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93e00-111">EXAMPLES</span></span>

### <span data-ttu-id="93e00-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="93e00-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="93e00-113">Aktualizowanie informacji o rozsyłaniu.</span><span class="sxs-lookup"><span data-stu-id="93e00-113">Updating the route information.</span></span>

### <span data-ttu-id="93e00-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="93e00-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="93e00-115">Aktualizowanie informacji o rozsyłaniu.</span><span class="sxs-lookup"><span data-stu-id="93e00-115">Updating the route information.</span></span>

### <span data-ttu-id="93e00-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="93e00-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="93e00-117">Aktualizowanie informacji o rozsyłaniu.</span><span class="sxs-lookup"><span data-stu-id="93e00-117">Updating the route information.</span></span>

## <span data-ttu-id="93e00-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e00-118">PARAMETERS</span></span>

### <span data-ttu-id="93e00-119">— Warunek</span><span class="sxs-lookup"><span data-stu-id="93e00-119">-Condition</span></span>
<span data-ttu-id="93e00-120">Warunek oceniany w celu zastosowania reguły routingu</span><span class="sxs-lookup"><span data-stu-id="93e00-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="93e00-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e00-121">-DefaultProfile</span></span>
<span data-ttu-id="93e00-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93e00-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e00-123">— włączone</span><span class="sxs-lookup"><span data-stu-id="93e00-123">-Enabled</span></span>
<span data-ttu-id="93e00-124">Włącz trasę</span><span class="sxs-lookup"><span data-stu-id="93e00-124">Enable route</span></span>

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

### <span data-ttu-id="93e00-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="93e00-125">-EndpointName</span></span>
<span data-ttu-id="93e00-126">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="93e00-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="93e00-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93e00-127">-InputObject</span></span>
<span data-ttu-id="93e00-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="93e00-128">IotHub Object</span></span>

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

### <span data-ttu-id="93e00-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93e00-129">-Name</span></span>
<span data-ttu-id="93e00-130">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="93e00-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="93e00-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e00-131">-ResourceGroupName</span></span>
<span data-ttu-id="93e00-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="93e00-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="93e00-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e00-133">-ResourceId</span></span>
<span data-ttu-id="93e00-134">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="93e00-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="93e00-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="93e00-135">-RouteName</span></span>
<span data-ttu-id="93e00-136">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="93e00-136">Name of the Route</span></span>

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

### <span data-ttu-id="93e00-137">— Źródło</span><span class="sxs-lookup"><span data-stu-id="93e00-137">-Source</span></span>
<span data-ttu-id="93e00-138">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="93e00-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e00-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93e00-139">-Confirm</span></span>
<span data-ttu-id="93e00-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93e00-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e00-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e00-141">-WhatIf</span></span>
<span data-ttu-id="93e00-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93e00-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e00-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93e00-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e00-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e00-144">CommonParameters</span></span>
<span data-ttu-id="93e00-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e00-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e00-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e00-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e00-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93e00-147">INPUTS</span></span>

### <span data-ttu-id="93e00-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="93e00-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="93e00-149">System.String</span><span class="sxs-lookup"><span data-stu-id="93e00-149">System.String</span></span>

## <span data-ttu-id="93e00-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93e00-150">OUTPUTS</span></span>

### <span data-ttu-id="93e00-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="93e00-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="93e00-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93e00-152">NOTES</span></span>

## <span data-ttu-id="93e00-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93e00-153">RELATED LINKS</span></span>
