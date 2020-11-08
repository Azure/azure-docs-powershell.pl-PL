---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050857"
---
# <span data-ttu-id="339ff-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="339ff-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="339ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="339ff-102">SYNOPSIS</span></span>
<span data-ttu-id="339ff-103">Trasy testowe w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="339ff-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="339ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="339ff-104">SYNTAX</span></span>

### <span data-ttu-id="339ff-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="339ff-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="339ff-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="339ff-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="339ff-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="339ff-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="339ff-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="339ff-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="339ff-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="339ff-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="339ff-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="339ff-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="339ff-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="339ff-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="339ff-112">Opis</span><span class="sxs-lookup"><span data-stu-id="339ff-112">DESCRIPTION</span></span>
<span data-ttu-id="339ff-113">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="339ff-113">Test a specific route.</span></span>

## <span data-ttu-id="339ff-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="339ff-114">EXAMPLES</span></span>

### <span data-ttu-id="339ff-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="339ff-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="339ff-116">Przetestuj wszystkie trasy ze źródłem "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="339ff-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="339ff-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="339ff-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="339ff-118">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="339ff-118">Test a specific route.</span></span>

### <span data-ttu-id="339ff-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="339ff-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="339ff-120">Przetestuj określoną trasę i pokazywanie przyczyny niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="339ff-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="339ff-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="339ff-121">PARAMETERS</span></span>

### <span data-ttu-id="339ff-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="339ff-122">-AppProperty</span></span>
<span data-ttu-id="339ff-123">Właściwości aplikacji trasy</span><span class="sxs-lookup"><span data-stu-id="339ff-123">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-124">-Body</span><span class="sxs-lookup"><span data-stu-id="339ff-124">-Body</span></span>
<span data-ttu-id="339ff-125">Treść wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="339ff-125">Body of the route message</span></span>

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

### <span data-ttu-id="339ff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339ff-126">-DefaultProfile</span></span>
<span data-ttu-id="339ff-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="339ff-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339ff-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="339ff-128">-InputObject</span></span>
<span data-ttu-id="339ff-129">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="339ff-129">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="339ff-130">-Name</span></span>
<span data-ttu-id="339ff-131">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="339ff-131">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339ff-132">-ResourceGroupName</span></span>
<span data-ttu-id="339ff-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="339ff-133">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="339ff-134">-ResourceId</span></span>
<span data-ttu-id="339ff-135">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="339ff-135">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="339ff-136">-RouteName</span></span>
<span data-ttu-id="339ff-137">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="339ff-137">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="339ff-138">-ShowError</span></span>
<span data-ttu-id="339ff-139">Pokaż szczegółowy błąd (jeśli istnieje)</span><span class="sxs-lookup"><span data-stu-id="339ff-139">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-140">-Source</span><span class="sxs-lookup"><span data-stu-id="339ff-140">-Source</span></span>
<span data-ttu-id="339ff-141">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="339ff-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="339ff-142">-SystemProperty</span></span>
<span data-ttu-id="339ff-143">Właściwości systemowe komunikatu o trasie</span><span class="sxs-lookup"><span data-stu-id="339ff-143">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339ff-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339ff-144">CommonParameters</span></span>
<span data-ttu-id="339ff-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339ff-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339ff-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339ff-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339ff-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="339ff-147">INPUTS</span></span>

### <span data-ttu-id="339ff-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="339ff-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="339ff-149">System. String</span><span class="sxs-lookup"><span data-stu-id="339ff-149">System.String</span></span>

## <span data-ttu-id="339ff-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="339ff-150">OUTPUTS</span></span>

### <span data-ttu-id="339ff-151">Microsoft. Azure. Commands. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="339ff-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="339ff-152">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="339ff-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="339ff-153">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="339ff-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="339ff-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="339ff-154">NOTES</span></span>

## <span data-ttu-id="339ff-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="339ff-155">RELATED LINKS</span></span>
