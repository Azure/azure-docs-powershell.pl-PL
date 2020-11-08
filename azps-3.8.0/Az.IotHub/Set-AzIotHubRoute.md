---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050365"
---
# <span data-ttu-id="81266-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="81266-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="81266-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81266-102">SYNOPSIS</span></span>
<span data-ttu-id="81266-103">Aktualizowanie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="81266-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="81266-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81266-104">SYNTAX</span></span>

### <span data-ttu-id="81266-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="81266-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81266-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="81266-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81266-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="81266-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81266-108">Opis</span><span class="sxs-lookup"><span data-stu-id="81266-108">DESCRIPTION</span></span>
<span data-ttu-id="81266-109">Edytowanie trasy.</span><span class="sxs-lookup"><span data-stu-id="81266-109">Edit a route.</span></span> <span data-ttu-id="81266-110">Możesz zaktualizować wszystkie pola w marszrucie, w tym źródło danych, punkt końcowy, zapytanie routingu, a także włączyć lub wyłączyć trasę.</span><span class="sxs-lookup"><span data-stu-id="81266-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="81266-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81266-111">EXAMPLES</span></span>

### <span data-ttu-id="81266-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="81266-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="81266-113">Aktualizowanie informacji o marszrucie.</span><span class="sxs-lookup"><span data-stu-id="81266-113">Updating the route information.</span></span>

### <span data-ttu-id="81266-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="81266-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="81266-115">Aktualizowanie informacji o marszrucie.</span><span class="sxs-lookup"><span data-stu-id="81266-115">Updating the route information.</span></span>

### <span data-ttu-id="81266-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="81266-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="81266-117">Aktualizowanie informacji o marszrucie.</span><span class="sxs-lookup"><span data-stu-id="81266-117">Updating the route information.</span></span>

## <span data-ttu-id="81266-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81266-118">PARAMETERS</span></span>

### <span data-ttu-id="81266-119">-Warunek</span><span class="sxs-lookup"><span data-stu-id="81266-119">-Condition</span></span>
<span data-ttu-id="81266-120">Warunek, który ma zostać oceniony w celu zastosowania reguły routingu</span><span class="sxs-lookup"><span data-stu-id="81266-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="81266-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81266-121">-DefaultProfile</span></span>
<span data-ttu-id="81266-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81266-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81266-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="81266-123">-Enabled</span></span>
<span data-ttu-id="81266-124">Włączanie trasy</span><span class="sxs-lookup"><span data-stu-id="81266-124">Enable route</span></span>

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

### <span data-ttu-id="81266-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="81266-125">-EndpointName</span></span>
<span data-ttu-id="81266-126">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="81266-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="81266-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81266-127">-InputObject</span></span>
<span data-ttu-id="81266-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="81266-128">IotHub Object</span></span>

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

### <span data-ttu-id="81266-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="81266-129">-Name</span></span>
<span data-ttu-id="81266-130">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="81266-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="81266-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81266-131">-ResourceGroupName</span></span>
<span data-ttu-id="81266-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="81266-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="81266-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81266-133">-ResourceId</span></span>
<span data-ttu-id="81266-134">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="81266-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="81266-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="81266-135">-RouteName</span></span>
<span data-ttu-id="81266-136">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="81266-136">Name of the Route</span></span>

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

### <span data-ttu-id="81266-137">-Source</span><span class="sxs-lookup"><span data-stu-id="81266-137">-Source</span></span>
<span data-ttu-id="81266-138">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="81266-138">Source of the route</span></span>

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

### <span data-ttu-id="81266-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81266-139">-Confirm</span></span>
<span data-ttu-id="81266-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81266-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81266-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81266-141">-WhatIf</span></span>
<span data-ttu-id="81266-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81266-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81266-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81266-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81266-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81266-144">CommonParameters</span></span>
<span data-ttu-id="81266-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81266-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81266-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81266-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81266-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81266-147">INPUTS</span></span>

### <span data-ttu-id="81266-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="81266-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="81266-149">System. String</span><span class="sxs-lookup"><span data-stu-id="81266-149">System.String</span></span>

## <span data-ttu-id="81266-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81266-150">OUTPUTS</span></span>

### <span data-ttu-id="81266-151">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="81266-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="81266-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81266-152">NOTES</span></span>

## <span data-ttu-id="81266-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81266-153">RELATED LINKS</span></span>
