---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 56ac931259de9705e0d6703e1387853aba77b028
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004081"
---
# <span data-ttu-id="35244-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="35244-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="35244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35244-102">SYNOPSIS</span></span>
<span data-ttu-id="35244-103">Testowanie tras w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="35244-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="35244-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35244-104">SYNTAX</span></span>

### <span data-ttu-id="35244-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35244-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35244-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="35244-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35244-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="35244-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35244-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="35244-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35244-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="35244-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35244-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="35244-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35244-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="35244-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35244-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="35244-112">DESCRIPTION</span></span>
<span data-ttu-id="35244-113">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="35244-113">Test a specific route.</span></span>

## <span data-ttu-id="35244-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35244-114">EXAMPLES</span></span>

### <span data-ttu-id="35244-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35244-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="35244-116">Przetestuj całą trasę za pomocą źródłowego "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="35244-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="35244-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="35244-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="35244-118">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="35244-118">Test a specific route.</span></span>

### <span data-ttu-id="35244-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="35244-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="35244-120">Przetestuj konkretną trasę i pokaż przyczynę niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="35244-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="35244-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="35244-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="35244-122">Przetestuj określoną trasę za pomocą właściwości AppProperty i SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="35244-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="35244-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35244-123">PARAMETERS</span></span>

### <span data-ttu-id="35244-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="35244-124">-AppProperty</span></span>
<span data-ttu-id="35244-125">Właściwości aplikacji wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="35244-125">App properties of the route message</span></span>

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

### <span data-ttu-id="35244-126">— Treść</span><span class="sxs-lookup"><span data-stu-id="35244-126">-Body</span></span>
<span data-ttu-id="35244-127">Treść wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="35244-127">Body of the route message</span></span>

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

### <span data-ttu-id="35244-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35244-128">-DefaultProfile</span></span>
<span data-ttu-id="35244-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35244-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35244-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35244-130">-InputObject</span></span>
<span data-ttu-id="35244-131">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="35244-131">IotHub Object</span></span>

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

### <span data-ttu-id="35244-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35244-132">-Name</span></span>
<span data-ttu-id="35244-133">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="35244-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="35244-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35244-134">-ResourceGroupName</span></span>
<span data-ttu-id="35244-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="35244-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="35244-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35244-136">-ResourceId</span></span>
<span data-ttu-id="35244-137">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="35244-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="35244-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="35244-138">-RouteName</span></span>
<span data-ttu-id="35244-139">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="35244-139">Name of the Route</span></span>

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

### <span data-ttu-id="35244-140">- ShowError</span><span class="sxs-lookup"><span data-stu-id="35244-140">-ShowError</span></span>
<span data-ttu-id="35244-141">Wyświetlanie szczegółowych informacji o błędzie, jeśli istnieją</span><span class="sxs-lookup"><span data-stu-id="35244-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="35244-142">— Źródło</span><span class="sxs-lookup"><span data-stu-id="35244-142">-Source</span></span>
<span data-ttu-id="35244-143">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="35244-143">Source of the route</span></span>

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

### <span data-ttu-id="35244-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="35244-144">-SystemProperty</span></span>
<span data-ttu-id="35244-145">Właściwości systemowe wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="35244-145">System properties of the route message</span></span>

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

### <span data-ttu-id="35244-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35244-146">CommonParameters</span></span>
<span data-ttu-id="35244-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35244-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35244-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35244-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35244-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35244-149">INPUTS</span></span>

### <span data-ttu-id="35244-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="35244-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="35244-151">System.String</span><span class="sxs-lookup"><span data-stu-id="35244-151">System.String</span></span>

## <span data-ttu-id="35244-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35244-152">OUTPUTS</span></span>

### <span data-ttu-id="35244-153">Microsoft.Azure.Commands.Management.iotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="35244-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="35244-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="35244-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="35244-155">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="35244-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="35244-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35244-156">NOTES</span></span>

## <span data-ttu-id="35244-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35244-157">RELATED LINKS</span></span>
