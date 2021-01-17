---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: a54bfdb26b7013e490ca36e4ae5608da228d9d70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367801"
---
# <span data-ttu-id="43ec6-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="43ec6-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="43ec6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="43ec6-103">Aktualizowanie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="43ec6-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="43ec6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43ec6-104">SYNTAX</span></span>

### <span data-ttu-id="43ec6-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43ec6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ec6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43ec6-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ec6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43ec6-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ec6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="43ec6-108">DESCRIPTION</span></span>
<span data-ttu-id="43ec6-109">Edytowanie trasy.</span><span class="sxs-lookup"><span data-stu-id="43ec6-109">Edit a route.</span></span> <span data-ttu-id="43ec6-110">Możesz zaktualizować wszystkie pola w marszrucie, w tym źródło danych, punkt końcowy, zapytanie routingu, a także włączyć lub wyłączyć trasę.</span><span class="sxs-lookup"><span data-stu-id="43ec6-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="43ec6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43ec6-111">EXAMPLES</span></span>

### <span data-ttu-id="43ec6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43ec6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="43ec6-113">Aktualizowanie informacji o marszrucie.</span><span class="sxs-lookup"><span data-stu-id="43ec6-113">Updating the route information.</span></span>

### <span data-ttu-id="43ec6-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="43ec6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="43ec6-115">Aktualizowanie informacji o marszrucie.</span><span class="sxs-lookup"><span data-stu-id="43ec6-115">Updating the route information.</span></span>

### <span data-ttu-id="43ec6-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="43ec6-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="43ec6-117">Aktualizowanie informacji o marszrucie.</span><span class="sxs-lookup"><span data-stu-id="43ec6-117">Updating the route information.</span></span>

## <span data-ttu-id="43ec6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43ec6-118">PARAMETERS</span></span>

### <span data-ttu-id="43ec6-119">-Warunek</span><span class="sxs-lookup"><span data-stu-id="43ec6-119">-Condition</span></span>
<span data-ttu-id="43ec6-120">Warunek, który ma zostać oceniony w celu zastosowania reguły routingu</span><span class="sxs-lookup"><span data-stu-id="43ec6-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="43ec6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ec6-121">-DefaultProfile</span></span>
<span data-ttu-id="43ec6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43ec6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ec6-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="43ec6-123">-Enabled</span></span>
<span data-ttu-id="43ec6-124">Włączanie trasy</span><span class="sxs-lookup"><span data-stu-id="43ec6-124">Enable route</span></span>

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

### <span data-ttu-id="43ec6-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="43ec6-125">-EndpointName</span></span>
<span data-ttu-id="43ec6-126">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="43ec6-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="43ec6-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43ec6-127">-InputObject</span></span>
<span data-ttu-id="43ec6-128">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="43ec6-128">IotHub Object</span></span>

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

### <span data-ttu-id="43ec6-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43ec6-129">-Name</span></span>
<span data-ttu-id="43ec6-130">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="43ec6-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="43ec6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ec6-131">-ResourceGroupName</span></span>
<span data-ttu-id="43ec6-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="43ec6-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43ec6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43ec6-133">-ResourceId</span></span>
<span data-ttu-id="43ec6-134">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="43ec6-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="43ec6-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="43ec6-135">-RouteName</span></span>
<span data-ttu-id="43ec6-136">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="43ec6-136">Name of the Route</span></span>

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

### <span data-ttu-id="43ec6-137">-Source</span><span class="sxs-lookup"><span data-stu-id="43ec6-137">-Source</span></span>
<span data-ttu-id="43ec6-138">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="43ec6-138">Source of the route</span></span>

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

### <span data-ttu-id="43ec6-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43ec6-139">-Confirm</span></span>
<span data-ttu-id="43ec6-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ec6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ec6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ec6-141">-WhatIf</span></span>
<span data-ttu-id="43ec6-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ec6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ec6-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43ec6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ec6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ec6-144">CommonParameters</span></span>
<span data-ttu-id="43ec6-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ec6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ec6-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ec6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ec6-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43ec6-147">INPUTS</span></span>

### <span data-ttu-id="43ec6-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="43ec6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="43ec6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="43ec6-149">System.String</span></span>

## <span data-ttu-id="43ec6-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43ec6-150">OUTPUTS</span></span>

### <span data-ttu-id="43ec6-151">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="43ec6-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="43ec6-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43ec6-152">NOTES</span></span>

## <span data-ttu-id="43ec6-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43ec6-153">RELATED LINKS</span></span>
