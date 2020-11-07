---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 1cc1bb46909260bd23cfa3f72e675251a011072d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705232"
---
# <span data-ttu-id="44419-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="44419-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="44419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44419-102">SYNOPSIS</span></span>
<span data-ttu-id="44419-103">Uzyskiwanie informacji na temat trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="44419-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="44419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44419-104">SYNTAX</span></span>

### <span data-ttu-id="44419-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44419-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44419-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44419-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44419-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44419-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44419-108">Opis</span><span class="sxs-lookup"><span data-stu-id="44419-108">DESCRIPTION</span></span>
<span data-ttu-id="44419-109">Uzyskaj informacje na temat trasy. Możesz pobrać wszystkie trasy z Centrum IoT, pobrać trasy do punktu końcowego lub uzyskać trasy do określonego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="44419-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="44419-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44419-110">EXAMPLES</span></span>

### <span data-ttu-id="44419-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44419-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="44419-112">Pobierz całą trasę z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="44419-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="44419-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="44419-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="44419-114">Pobierz informacje o marszrucie z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="44419-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="44419-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44419-115">PARAMETERS</span></span>

### <span data-ttu-id="44419-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44419-116">-DefaultProfile</span></span>
<span data-ttu-id="44419-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44419-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44419-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44419-118">-InputObject</span></span>
<span data-ttu-id="44419-119">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="44419-119">IotHub Object</span></span>

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

### <span data-ttu-id="44419-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44419-120">-Name</span></span>
<span data-ttu-id="44419-121">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="44419-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="44419-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44419-122">-ResourceGroupName</span></span>
<span data-ttu-id="44419-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="44419-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44419-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44419-124">-ResourceId</span></span>
<span data-ttu-id="44419-125">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="44419-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="44419-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="44419-126">-RouteName</span></span>
<span data-ttu-id="44419-127">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="44419-127">Name of the Route</span></span>

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

### <span data-ttu-id="44419-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44419-128">CommonParameters</span></span>
<span data-ttu-id="44419-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44419-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44419-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44419-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44419-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44419-131">INPUTS</span></span>

### <span data-ttu-id="44419-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="44419-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="44419-133">System. String</span><span class="sxs-lookup"><span data-stu-id="44419-133">System.String</span></span>

## <span data-ttu-id="44419-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44419-134">OUTPUTS</span></span>

### <span data-ttu-id="44419-135">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="44419-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="44419-136">Microsoft. Azure. Commands. Management. IotHub. models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="44419-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="44419-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44419-137">NOTES</span></span>

## <span data-ttu-id="44419-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44419-138">RELATED LINKS</span></span>
