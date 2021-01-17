---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386435"
---
# <span data-ttu-id="a18f8-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="a18f8-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="a18f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a18f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a18f8-103">Trasy testowe w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="a18f8-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="a18f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a18f8-104">SYNTAX</span></span>

### <span data-ttu-id="a18f8-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a18f8-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18f8-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="a18f8-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18f8-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="a18f8-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a18f8-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="a18f8-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18f8-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="a18f8-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a18f8-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="a18f8-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18f8-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="a18f8-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a18f8-112">Opis</span><span class="sxs-lookup"><span data-stu-id="a18f8-112">DESCRIPTION</span></span>
<span data-ttu-id="a18f8-113">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="a18f8-113">Test a specific route.</span></span>

## <span data-ttu-id="a18f8-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a18f8-114">EXAMPLES</span></span>

### <span data-ttu-id="a18f8-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a18f8-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="a18f8-116">Przetestuj wszystkie trasy ze źródłem "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="a18f8-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="a18f8-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a18f8-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="a18f8-118">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="a18f8-118">Test a specific route.</span></span>

### <span data-ttu-id="a18f8-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a18f8-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="a18f8-120">Przetestuj określoną trasę i pokazywanie przyczyny niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="a18f8-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="a18f8-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a18f8-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="a18f8-122">Przetestuj określoną trasę, korzystając z AppProperty i SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="a18f8-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="a18f8-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a18f8-123">PARAMETERS</span></span>

### <span data-ttu-id="a18f8-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="a18f8-124">-AppProperty</span></span>
<span data-ttu-id="a18f8-125">Właściwości aplikacji trasy</span><span class="sxs-lookup"><span data-stu-id="a18f8-125">App properties of the route message</span></span>

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

### <span data-ttu-id="a18f8-126">-Body</span><span class="sxs-lookup"><span data-stu-id="a18f8-126">-Body</span></span>
<span data-ttu-id="a18f8-127">Treść wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="a18f8-127">Body of the route message</span></span>

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

### <span data-ttu-id="a18f8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18f8-128">-DefaultProfile</span></span>
<span data-ttu-id="a18f8-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a18f8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18f8-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a18f8-130">-InputObject</span></span>
<span data-ttu-id="a18f8-131">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="a18f8-131">IotHub Object</span></span>

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

### <span data-ttu-id="a18f8-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a18f8-132">-Name</span></span>
<span data-ttu-id="a18f8-133">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="a18f8-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a18f8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18f8-134">-ResourceGroupName</span></span>
<span data-ttu-id="a18f8-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a18f8-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a18f8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18f8-136">-ResourceId</span></span>
<span data-ttu-id="a18f8-137">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="a18f8-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a18f8-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="a18f8-138">-RouteName</span></span>
<span data-ttu-id="a18f8-139">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="a18f8-139">Name of the Route</span></span>

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

### <span data-ttu-id="a18f8-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="a18f8-140">-ShowError</span></span>
<span data-ttu-id="a18f8-141">Pokaż szczegółowy błąd (jeśli istnieje)</span><span class="sxs-lookup"><span data-stu-id="a18f8-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="a18f8-142">-Source</span><span class="sxs-lookup"><span data-stu-id="a18f8-142">-Source</span></span>
<span data-ttu-id="a18f8-143">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="a18f8-143">Source of the route</span></span>

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

### <span data-ttu-id="a18f8-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="a18f8-144">-SystemProperty</span></span>
<span data-ttu-id="a18f8-145">Właściwości systemowe komunikatu o trasie</span><span class="sxs-lookup"><span data-stu-id="a18f8-145">System properties of the route message</span></span>

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

### <span data-ttu-id="a18f8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18f8-146">CommonParameters</span></span>
<span data-ttu-id="a18f8-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18f8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18f8-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18f8-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18f8-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a18f8-149">INPUTS</span></span>

### <span data-ttu-id="a18f8-150">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a18f8-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a18f8-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a18f8-151">System.String</span></span>

## <span data-ttu-id="a18f8-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a18f8-152">OUTPUTS</span></span>

### <span data-ttu-id="a18f8-153">Microsoft. Azure. Commands. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="a18f8-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="a18f8-154">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="a18f8-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="a18f8-155">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="a18f8-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="a18f8-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a18f8-156">NOTES</span></span>

## <span data-ttu-id="a18f8-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a18f8-157">RELATED LINKS</span></span>
