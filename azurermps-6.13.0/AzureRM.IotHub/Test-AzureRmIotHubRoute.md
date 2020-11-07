---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/test-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
ms.openlocfilehash: f51ba85215d252959b974a39ea864b1c98fce460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718851"
---
# <span data-ttu-id="24aad-101">Test-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="24aad-101">Test-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="24aad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24aad-102">SYNOPSIS</span></span>
<span data-ttu-id="24aad-103">Trasy testowe w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="24aad-103">Test routes in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24aad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24aad-104">SYNTAX</span></span>

### <span data-ttu-id="24aad-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24aad-105">ResourceSet (Default)</span></span>
```
Test-AzureRmIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24aad-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="24aad-106">InputObjectTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24aad-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="24aad-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24aad-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="24aad-108">TestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24aad-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="24aad-109">TestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource>
 [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24aad-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="24aad-110">ResourceIdTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24aad-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="24aad-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24aad-112">Opis</span><span class="sxs-lookup"><span data-stu-id="24aad-112">DESCRIPTION</span></span>
<span data-ttu-id="24aad-113">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="24aad-113">Test a specific route.</span></span>

## <span data-ttu-id="24aad-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24aad-114">EXAMPLES</span></span>

### <span data-ttu-id="24aad-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24aad-115">Example 1</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="24aad-116">Przetestuj wszystkie trasy ze źródłem "DeviceMessges".</span><span class="sxs-lookup"><span data-stu-id="24aad-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="24aad-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="24aad-117">Example 2</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="24aad-118">Przetestuj określoną trasę.</span><span class="sxs-lookup"><span data-stu-id="24aad-118">Test a specific route.</span></span>

### <span data-ttu-id="24aad-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="24aad-119">Example 3</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="24aad-120">Przetestuj określoną trasę i pokazywanie przyczyny niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="24aad-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="24aad-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24aad-121">PARAMETERS</span></span>

### <span data-ttu-id="24aad-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="24aad-122">-AppProperty</span></span>
<span data-ttu-id="24aad-123">Właściwości aplikacji trasy</span><span class="sxs-lookup"><span data-stu-id="24aad-123">App properties of the route message</span></span>

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

### <span data-ttu-id="24aad-124">-Body</span><span class="sxs-lookup"><span data-stu-id="24aad-124">-Body</span></span>
<span data-ttu-id="24aad-125">Treść wiadomości trasy</span><span class="sxs-lookup"><span data-stu-id="24aad-125">Body of the route message</span></span>

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

### <span data-ttu-id="24aad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24aad-126">-DefaultProfile</span></span>
<span data-ttu-id="24aad-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24aad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24aad-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24aad-128">-InputObject</span></span>
<span data-ttu-id="24aad-129">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="24aad-129">IotHub Object</span></span>

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

### <span data-ttu-id="24aad-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24aad-130">-Name</span></span>
<span data-ttu-id="24aad-131">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="24aad-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="24aad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24aad-132">-ResourceGroupName</span></span>
<span data-ttu-id="24aad-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="24aad-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="24aad-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24aad-134">-ResourceId</span></span>
<span data-ttu-id="24aad-135">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="24aad-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="24aad-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="24aad-136">-RouteName</span></span>
<span data-ttu-id="24aad-137">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="24aad-137">Name of the Route</span></span>

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

### <span data-ttu-id="24aad-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="24aad-138">-ShowError</span></span>
<span data-ttu-id="24aad-139">Pokaż szczegółowy błąd (jeśli istnieje)</span><span class="sxs-lookup"><span data-stu-id="24aad-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="24aad-140">-Source</span><span class="sxs-lookup"><span data-stu-id="24aad-140">-Source</span></span>
<span data-ttu-id="24aad-141">Źródło trasy</span><span class="sxs-lookup"><span data-stu-id="24aad-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24aad-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="24aad-142">-SystemProperty</span></span>
<span data-ttu-id="24aad-143">Właściwości systemowe komunikatu o trasie</span><span class="sxs-lookup"><span data-stu-id="24aad-143">System properties of the route message</span></span>

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

### <span data-ttu-id="24aad-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24aad-144">CommonParameters</span></span>
<span data-ttu-id="24aad-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24aad-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24aad-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24aad-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24aad-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24aad-147">INPUTS</span></span>

### <span data-ttu-id="24aad-148">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="24aad-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="24aad-149">System. String</span><span class="sxs-lookup"><span data-stu-id="24aad-149">System.String</span></span>

## <span data-ttu-id="24aad-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24aad-150">OUTPUTS</span></span>

### <span data-ttu-id="24aad-151">Microsoft. Azure. Commands. Management. IotHub. models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="24aad-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>
<span data-ttu-id="24aad-152">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteCompilationError system. Collections.. "1 [[Microsoft. Azure. polecenia. Management. IotHub. MODELES. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="24aad-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="24aad-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24aad-153">NOTES</span></span>

## <span data-ttu-id="24aad-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24aad-154">RELATED LINKS</span></span>
