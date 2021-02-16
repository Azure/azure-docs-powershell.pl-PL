---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203905"
---
# <span data-ttu-id="cc91d-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="cc91d-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="cc91d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc91d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc91d-103">Uzyskiwanie informacji na temat trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="cc91d-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="cc91d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc91d-104">SYNTAX</span></span>

### <span data-ttu-id="cc91d-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc91d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc91d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc91d-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc91d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cc91d-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc91d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc91d-108">DESCRIPTION</span></span>
<span data-ttu-id="cc91d-109">Uzyskaj informacje na temat trasy. Możesz pobrać wszystkie trasy z centrum IoT, uzyskać trasy do określonego typu punktu końcowego lub uzyskać trasy do określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="cc91d-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="cc91d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc91d-110">EXAMPLES</span></span>

### <span data-ttu-id="cc91d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc91d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="cc91d-112">Pobierz całą trasę z centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cc91d-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cc91d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc91d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="cc91d-114">Uzyskiwanie informacji o rozsyłanych trasach z centrum IoT w aplikacji "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cc91d-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="cc91d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc91d-115">PARAMETERS</span></span>

### <span data-ttu-id="cc91d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc91d-116">-DefaultProfile</span></span>
<span data-ttu-id="cc91d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc91d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc91d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc91d-118">-InputObject</span></span>
<span data-ttu-id="cc91d-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="cc91d-119">IotHub Object</span></span>

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

### <span data-ttu-id="cc91d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cc91d-120">-Name</span></span>
<span data-ttu-id="cc91d-121">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="cc91d-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cc91d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc91d-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc91d-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cc91d-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cc91d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc91d-124">-ResourceId</span></span>
<span data-ttu-id="cc91d-125">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="cc91d-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cc91d-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="cc91d-126">-RouteName</span></span>
<span data-ttu-id="cc91d-127">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="cc91d-127">Name of the Route</span></span>

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

### <span data-ttu-id="cc91d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc91d-128">CommonParameters</span></span>
<span data-ttu-id="cc91d-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc91d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc91d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc91d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc91d-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc91d-131">INPUTS</span></span>

### <span data-ttu-id="cc91d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cc91d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cc91d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cc91d-133">System.String</span></span>

## <span data-ttu-id="cc91d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc91d-134">OUTPUTS</span></span>

### <span data-ttu-id="cc91d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="cc91d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="cc91d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="cc91d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="cc91d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc91d-137">NOTES</span></span>

## <span data-ttu-id="cc91d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc91d-138">RELATED LINKS</span></span>
