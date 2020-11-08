---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052786"
---
# <span data-ttu-id="97c43-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="97c43-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="97c43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97c43-102">SYNOPSIS</span></span>
<span data-ttu-id="97c43-103">Uzyskaj informacje na temat wszystkich punktów końcowych Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="97c43-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="97c43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97c43-104">SYNTAX</span></span>

### <span data-ttu-id="97c43-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="97c43-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c43-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97c43-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c43-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="97c43-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97c43-108">Opis</span><span class="sxs-lookup"><span data-stu-id="97c43-108">DESCRIPTION</span></span>
<span data-ttu-id="97c43-109">Uzyskaj informacje o punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="97c43-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="97c43-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97c43-110">EXAMPLES</span></span>

### <span data-ttu-id="97c43-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97c43-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="97c43-112">Pobierz wszystkie punkty końcowe z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="97c43-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="97c43-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="97c43-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="97c43-114">Pobierz wszystkie punkty końcowe typu EventHub z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="97c43-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="97c43-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="97c43-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="97c43-116">Pobierz wszystkie punkty końcowe typu EventHub z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="97c43-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="97c43-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="97c43-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="97c43-118">Uzyskaj informacje o punkcie końcowym z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="97c43-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="97c43-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97c43-119">PARAMETERS</span></span>

### <span data-ttu-id="97c43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c43-120">-DefaultProfile</span></span>
<span data-ttu-id="97c43-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97c43-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c43-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="97c43-122">-EndpointName</span></span>
<span data-ttu-id="97c43-123">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="97c43-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="97c43-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="97c43-124">-EndpointType</span></span>
<span data-ttu-id="97c43-125">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="97c43-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c43-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="97c43-126">-InputObject</span></span>
<span data-ttu-id="97c43-127">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="97c43-127">IotHub Object</span></span>

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

### <span data-ttu-id="97c43-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97c43-128">-Name</span></span>
<span data-ttu-id="97c43-129">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="97c43-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="97c43-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c43-130">-ResourceGroupName</span></span>
<span data-ttu-id="97c43-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="97c43-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="97c43-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97c43-132">-ResourceId</span></span>
<span data-ttu-id="97c43-133">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="97c43-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="97c43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c43-134">CommonParameters</span></span>
<span data-ttu-id="97c43-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c43-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c43-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c43-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97c43-137">INPUTS</span></span>

### <span data-ttu-id="97c43-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="97c43-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="97c43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97c43-139">System.String</span></span>

## <span data-ttu-id="97c43-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97c43-140">OUTPUTS</span></span>

### <span data-ttu-id="97c43-141">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="97c43-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="97c43-142">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Management. IotHub. MODELES. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdlet. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="97c43-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="97c43-143">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="97c43-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="97c43-144">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="97c43-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="97c43-145">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="97c43-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="97c43-146">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="97c43-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="97c43-147">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="97c43-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="97c43-148">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="97c43-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="97c43-149">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="97c43-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="97c43-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97c43-150">NOTES</span></span>

## <span data-ttu-id="97c43-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97c43-151">RELATED LINKS</span></span>
