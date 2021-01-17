---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361748"
---
# <span data-ttu-id="c2d26-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c2d26-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="c2d26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2d26-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d26-103">Trasy testowe w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="c2d26-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="c2d26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2d26-104">SYNTAX</span></span>

### <span data-ttu-id="c2d26-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c2d26-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d26-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="c2d26-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d26-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="c2d26-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d26-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="c2d26-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d26-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="c2d26-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d26-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="c2d26-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2d26-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="c2d26-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2d26-112">Opis</span><span class="sxs-lookup"><span data-stu-id="c2d26-112">DESCRIPTION</span></span>
<span data-ttu-id="c2d26-113">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="c2d26-113">Test a specific route.</span></span>

## <span data-ttu-id="c2d26-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2d26-114">EXAMPLES</span></span>

### <span data-ttu-id="c2d26-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2d26-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="c2d26-116">Przetestuj wszystkie trasy ze źródłem "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="c2d26-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="c2d26-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c2d26-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="c2d26-118">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="c2d26-118">Test a specific route.</span></span>

### <span data-ttu-id="c2d26-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c2d26-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="c2d26-120">Przetestuj określoną trasę i pokazywanie przyczyny niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="c2d26-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="c2d26-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c2d26-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="c2d26-122">Przetestuj określoną trasę, korzystając z AppProperty i SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="c2d26-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="c2d26-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2d26-123">PARAMETERS</span></span>

### <span data-ttu-id="c2d26-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="c2d26-124">-AppProperty</span></span>
<span data-ttu-id="c2d26-125">Właściwości aplikacji trasy</span><span class="sxs-lookup"><span data-stu-id="c2d26-125">App properties of the route message</span></span>

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

### <span data-ttu-id="c2d26-126">-Body</span><span class="sxs-lookup"><span data-stu-id="c2d26-126">-Body</span></span>
<span data-ttu-id="c2d26-127">Treść wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="c2d26-127">Body of the route message</span></span>

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

### <span data-ttu-id="c2d26-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d26-128">-DefaultProfile</span></span>
<span data-ttu-id="c2d26-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d26-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d26-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2d26-130">-InputObject</span></span>
<span data-ttu-id="c2d26-131">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="c2d26-131">IotHub Object</span></span>

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

### <span data-ttu-id="c2d26-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c2d26-132">-Name</span></span>
<span data-ttu-id="c2d26-133">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="c2d26-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c2d26-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d26-134">-ResourceGroupName</span></span>
<span data-ttu-id="c2d26-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c2d26-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c2d26-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d26-136">-ResourceId</span></span>
<span data-ttu-id="c2d26-137">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="c2d26-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c2d26-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c2d26-138">-RouteName</span></span>
<span data-ttu-id="c2d26-139">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="c2d26-139">Name of the Route</span></span>

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

### <span data-ttu-id="c2d26-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="c2d26-140">-ShowError</span></span>
<span data-ttu-id="c2d26-141">Pokaż szczegółowy błąd (jeśli istnieje)</span><span class="sxs-lookup"><span data-stu-id="c2d26-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="c2d26-142">-Source</span><span class="sxs-lookup"><span data-stu-id="c2d26-142">-Source</span></span>
<span data-ttu-id="c2d26-143">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="c2d26-143">Source of the route</span></span>

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

### <span data-ttu-id="c2d26-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="c2d26-144">-SystemProperty</span></span>
<span data-ttu-id="c2d26-145">Właściwości systemowe komunikatu o trasie</span><span class="sxs-lookup"><span data-stu-id="c2d26-145">System properties of the route message</span></span>

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

### <span data-ttu-id="c2d26-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d26-146">CommonParameters</span></span>
<span data-ttu-id="c2d26-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2d26-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d26-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2d26-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d26-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2d26-149">INPUTS</span></span>

### <span data-ttu-id="c2d26-150">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c2d26-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c2d26-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c2d26-151">System.String</span></span>

## <span data-ttu-id="c2d26-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2d26-152">OUTPUTS</span></span>

### <span data-ttu-id="c2d26-153">Microsoft. Azure. Commands. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="c2d26-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="c2d26-154">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="c2d26-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="c2d26-155">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="c2d26-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="c2d26-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2d26-156">NOTES</span></span>

## <span data-ttu-id="c2d26-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2d26-157">RELATED LINKS</span></span>
