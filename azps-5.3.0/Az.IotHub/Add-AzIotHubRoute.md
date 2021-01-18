---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503510"
---
# <span data-ttu-id="aa041-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="aa041-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="aa041-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa041-102">SYNOPSIS</span></span>
<span data-ttu-id="aa041-103">Tworzenie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="aa041-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="aa041-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa041-104">SYNTAX</span></span>

### <span data-ttu-id="aa041-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa041-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa041-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa041-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa041-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa041-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa041-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa041-108">DESCRIPTION</span></span>
<span data-ttu-id="aa041-109">Utwórz trasę, aby wysłać określone źródło danych i warunek do odpowiedniego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="aa041-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="aa041-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa041-110">EXAMPLES</span></span>

### <span data-ttu-id="aa041-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa041-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="aa041-112">Tworzenie nowej trasy "R1".</span><span class="sxs-lookup"><span data-stu-id="aa041-112">Create a new route "R1".</span></span>

## <span data-ttu-id="aa041-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa041-113">PARAMETERS</span></span>

### <span data-ttu-id="aa041-114">-Warunek</span><span class="sxs-lookup"><span data-stu-id="aa041-114">-Condition</span></span>
<span data-ttu-id="aa041-115">Warunek, który ma zostać oceniony w celu zastosowania reguły routingu</span><span class="sxs-lookup"><span data-stu-id="aa041-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="aa041-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa041-116">-DefaultProfile</span></span>
<span data-ttu-id="aa041-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa041-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa041-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="aa041-118">-Enabled</span></span>
<span data-ttu-id="aa041-119">Włączanie trasy</span><span class="sxs-lookup"><span data-stu-id="aa041-119">Enable route</span></span>

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

### <span data-ttu-id="aa041-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="aa041-120">-EndpointName</span></span>
<span data-ttu-id="aa041-121">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="aa041-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="aa041-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa041-122">-InputObject</span></span>
<span data-ttu-id="aa041-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="aa041-123">IotHub Object</span></span>

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

### <span data-ttu-id="aa041-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa041-124">-Name</span></span>
<span data-ttu-id="aa041-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="aa041-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aa041-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa041-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa041-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa041-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aa041-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa041-128">-ResourceId</span></span>
<span data-ttu-id="aa041-129">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="aa041-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aa041-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="aa041-130">-RouteName</span></span>
<span data-ttu-id="aa041-131">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="aa041-131">Name of the Route</span></span>

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

### <span data-ttu-id="aa041-132">-Source</span><span class="sxs-lookup"><span data-stu-id="aa041-132">-Source</span></span>
<span data-ttu-id="aa041-133">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="aa041-133">Source of the route</span></span>

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

### <span data-ttu-id="aa041-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa041-134">-Confirm</span></span>
<span data-ttu-id="aa041-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa041-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa041-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa041-136">-WhatIf</span></span>
<span data-ttu-id="aa041-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa041-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa041-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa041-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa041-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa041-139">CommonParameters</span></span>
<span data-ttu-id="aa041-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa041-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa041-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa041-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa041-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa041-142">INPUTS</span></span>

### <span data-ttu-id="aa041-143">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="aa041-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aa041-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aa041-144">System.String</span></span>

## <span data-ttu-id="aa041-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa041-145">OUTPUTS</span></span>

### <span data-ttu-id="aa041-146">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="aa041-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="aa041-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa041-147">NOTES</span></span>

## <span data-ttu-id="aa041-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa041-148">RELATED LINKS</span></span>
