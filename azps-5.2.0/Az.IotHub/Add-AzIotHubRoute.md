---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352729"
---
# <span data-ttu-id="5850b-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="5850b-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="5850b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5850b-102">SYNOPSIS</span></span>
<span data-ttu-id="5850b-103">Tworzenie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5850b-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="5850b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5850b-104">SYNTAX</span></span>

### <span data-ttu-id="5850b-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5850b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5850b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5850b-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5850b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5850b-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5850b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5850b-108">DESCRIPTION</span></span>
<span data-ttu-id="5850b-109">Utwórz trasę, aby wysłać określone źródło danych i warunek do odpowiedniego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="5850b-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="5850b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5850b-110">EXAMPLES</span></span>

### <span data-ttu-id="5850b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5850b-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="5850b-112">Tworzenie nowej trasy "R1".</span><span class="sxs-lookup"><span data-stu-id="5850b-112">Create a new route "R1".</span></span>

## <span data-ttu-id="5850b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5850b-113">PARAMETERS</span></span>

### <span data-ttu-id="5850b-114">-Warunek</span><span class="sxs-lookup"><span data-stu-id="5850b-114">-Condition</span></span>
<span data-ttu-id="5850b-115">Warunek, który ma zostać oceniony w celu zastosowania reguły routingu</span><span class="sxs-lookup"><span data-stu-id="5850b-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="5850b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5850b-116">-DefaultProfile</span></span>
<span data-ttu-id="5850b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5850b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5850b-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5850b-118">-Enabled</span></span>
<span data-ttu-id="5850b-119">Włączanie trasy</span><span class="sxs-lookup"><span data-stu-id="5850b-119">Enable route</span></span>

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

### <span data-ttu-id="5850b-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5850b-120">-EndpointName</span></span>
<span data-ttu-id="5850b-121">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="5850b-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="5850b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5850b-122">-InputObject</span></span>
<span data-ttu-id="5850b-123">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="5850b-123">IotHub Object</span></span>

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

### <span data-ttu-id="5850b-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5850b-124">-Name</span></span>
<span data-ttu-id="5850b-125">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="5850b-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5850b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5850b-126">-ResourceGroupName</span></span>
<span data-ttu-id="5850b-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5850b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5850b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5850b-128">-ResourceId</span></span>
<span data-ttu-id="5850b-129">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="5850b-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5850b-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="5850b-130">-RouteName</span></span>
<span data-ttu-id="5850b-131">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="5850b-131">Name of the Route</span></span>

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

### <span data-ttu-id="5850b-132">-Source</span><span class="sxs-lookup"><span data-stu-id="5850b-132">-Source</span></span>
<span data-ttu-id="5850b-133">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="5850b-133">Source of the route</span></span>

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

### <span data-ttu-id="5850b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5850b-134">-Confirm</span></span>
<span data-ttu-id="5850b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5850b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5850b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5850b-136">-WhatIf</span></span>
<span data-ttu-id="5850b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5850b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5850b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5850b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5850b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5850b-139">CommonParameters</span></span>
<span data-ttu-id="5850b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5850b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5850b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5850b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5850b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5850b-142">INPUTS</span></span>

### <span data-ttu-id="5850b-143">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5850b-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5850b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5850b-144">System.String</span></span>

## <span data-ttu-id="5850b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5850b-145">OUTPUTS</span></span>

### <span data-ttu-id="5850b-146">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="5850b-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="5850b-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5850b-147">NOTES</span></span>

## <span data-ttu-id="5850b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5850b-148">RELATED LINKS</span></span>
