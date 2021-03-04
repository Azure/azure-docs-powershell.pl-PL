---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: d627460da42d5d5710aa9931d2e831320378b082
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987883"
---
# <span data-ttu-id="59ca4-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="59ca4-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="59ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="59ca4-103">Uzyskiwanie informacji na temat trasy w centrum IoT Hub</span><span class="sxs-lookup"><span data-stu-id="59ca4-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="59ca4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59ca4-104">SYNTAX</span></span>

### <span data-ttu-id="59ca4-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59ca4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59ca4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59ca4-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59ca4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59ca4-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59ca4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="59ca4-108">DESCRIPTION</span></span>
<span data-ttu-id="59ca4-109">Uzyskaj informacje na temat trasy. Możesz pobrać wszystkie trasy z centrum IoT, uzyskać trasy do określonego typu punktu końcowego lub uzyskać trasy do określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="59ca4-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="59ca4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59ca4-110">EXAMPLES</span></span>

### <span data-ttu-id="59ca4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59ca4-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="59ca4-112">Pobierz całą trasę z centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="59ca4-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="59ca4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59ca4-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="59ca4-114">Uzyskiwanie informacji o trasach z centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="59ca4-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="59ca4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59ca4-115">PARAMETERS</span></span>

### <span data-ttu-id="59ca4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ca4-116">-DefaultProfile</span></span>
<span data-ttu-id="59ca4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59ca4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59ca4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59ca4-118">-InputObject</span></span>
<span data-ttu-id="59ca4-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="59ca4-119">IotHub Object</span></span>

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

### <span data-ttu-id="59ca4-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59ca4-120">-Name</span></span>
<span data-ttu-id="59ca4-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="59ca4-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="59ca4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ca4-122">-ResourceGroupName</span></span>
<span data-ttu-id="59ca4-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="59ca4-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="59ca4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59ca4-124">-ResourceId</span></span>
<span data-ttu-id="59ca4-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="59ca4-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="59ca4-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="59ca4-126">-RouteName</span></span>
<span data-ttu-id="59ca4-127">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="59ca4-127">Name of the Route</span></span>

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

### <span data-ttu-id="59ca4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ca4-128">CommonParameters</span></span>
<span data-ttu-id="59ca4-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ca4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ca4-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ca4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ca4-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59ca4-131">INPUTS</span></span>

### <span data-ttu-id="59ca4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="59ca4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="59ca4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="59ca4-133">System.String</span></span>

## <span data-ttu-id="59ca4-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59ca4-134">OUTPUTS</span></span>

### <span data-ttu-id="59ca4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="59ca4-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="59ca4-136">Microsoft.Azure.Commands.Management.iotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="59ca4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="59ca4-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59ca4-137">NOTES</span></span>

## <span data-ttu-id="59ca4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59ca4-138">RELATED LINKS</span></span>
