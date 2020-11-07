---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 17460bf1fbba1e6c336f720744a8795f0be2bd89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891366"
---
# <span data-ttu-id="b291e-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="b291e-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="b291e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b291e-102">SYNOPSIS</span></span>
<span data-ttu-id="b291e-103">Uzyskiwanie informacji na temat trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="b291e-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="b291e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b291e-104">SYNTAX</span></span>

### <span data-ttu-id="b291e-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b291e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b291e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b291e-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b291e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b291e-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b291e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b291e-108">DESCRIPTION</span></span>
<span data-ttu-id="b291e-109">Uzyskaj informacje na temat trasy. Możesz pobrać wszystkie trasy z Centrum IoT, pobrać trasy do punktu końcowego lub uzyskać trasy do określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="b291e-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="b291e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b291e-110">EXAMPLES</span></span>

### <span data-ttu-id="b291e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b291e-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="b291e-112">Pobierz całą trasę z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b291e-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="b291e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b291e-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="b291e-114">Pobierz informacje o marszrucie z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b291e-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b291e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b291e-115">PARAMETERS</span></span>

### <span data-ttu-id="b291e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b291e-116">-DefaultProfile</span></span>
<span data-ttu-id="b291e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b291e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b291e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b291e-118">-InputObject</span></span>
<span data-ttu-id="b291e-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="b291e-119">IotHub Object</span></span>

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

### <span data-ttu-id="b291e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b291e-120">-Name</span></span>
<span data-ttu-id="b291e-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="b291e-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b291e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b291e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b291e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b291e-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b291e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b291e-124">-ResourceId</span></span>
<span data-ttu-id="b291e-125">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="b291e-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b291e-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="b291e-126">-RouteName</span></span>
<span data-ttu-id="b291e-127">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="b291e-127">Name of the Route</span></span>

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

### <span data-ttu-id="b291e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b291e-128">CommonParameters</span></span>
<span data-ttu-id="b291e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b291e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b291e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b291e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b291e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b291e-131">INPUTS</span></span>

### <span data-ttu-id="b291e-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b291e-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b291e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b291e-133">System.String</span></span>

## <span data-ttu-id="b291e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b291e-134">OUTPUTS</span></span>

### <span data-ttu-id="b291e-135">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="b291e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="b291e-136">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="b291e-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="b291e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b291e-137">NOTES</span></span>

## <span data-ttu-id="b291e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b291e-138">RELATED LINKS</span></span>
