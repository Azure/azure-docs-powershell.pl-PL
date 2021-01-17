---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371133"
---
# <span data-ttu-id="f9f11-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9f11-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="f9f11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9f11-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f11-103">Uzyskaj informacje na temat wszystkich punktów końcowych Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="f9f11-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="f9f11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9f11-104">SYNTAX</span></span>

### <span data-ttu-id="f9f11-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9f11-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9f11-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f9f11-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9f11-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f9f11-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9f11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f9f11-108">DESCRIPTION</span></span>
<span data-ttu-id="f9f11-109">Uzyskaj informacje o punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="f9f11-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="f9f11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9f11-110">EXAMPLES</span></span>

### <span data-ttu-id="f9f11-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9f11-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="f9f11-112">Pobierz wszystkie punkty końcowe z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f9f11-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f9f11-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9f11-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="f9f11-114">Pobierz wszystkie punkty końcowe typu EventHub z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f9f11-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="f9f11-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9f11-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="f9f11-116">Pobierz wszystkie punkty końcowe typu EventHub z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f9f11-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="f9f11-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f9f11-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="f9f11-118">Uzyskaj informacje o punkcie końcowym z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f9f11-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="f9f11-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9f11-119">PARAMETERS</span></span>

### <span data-ttu-id="f9f11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f11-120">-DefaultProfile</span></span>
<span data-ttu-id="f9f11-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f11-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f9f11-122">-EndpointName</span></span>
<span data-ttu-id="f9f11-123">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="f9f11-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="f9f11-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f9f11-124">-EndpointType</span></span>
<span data-ttu-id="f9f11-125">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="f9f11-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="f9f11-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9f11-126">-InputObject</span></span>
<span data-ttu-id="f9f11-127">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="f9f11-127">IotHub Object</span></span>

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

### <span data-ttu-id="f9f11-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9f11-128">-Name</span></span>
<span data-ttu-id="f9f11-129">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="f9f11-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f9f11-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f11-130">-ResourceGroupName</span></span>
<span data-ttu-id="f9f11-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f9f11-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f9f11-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9f11-132">-ResourceId</span></span>
<span data-ttu-id="f9f11-133">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="f9f11-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f9f11-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f11-134">CommonParameters</span></span>
<span data-ttu-id="f9f11-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f11-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f11-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f11-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f11-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9f11-137">INPUTS</span></span>

### <span data-ttu-id="f9f11-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f9f11-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f9f11-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f9f11-139">System.String</span></span>

## <span data-ttu-id="f9f11-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9f11-140">OUTPUTS</span></span>

### <span data-ttu-id="f9f11-141">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9f11-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="f9f11-142">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Management. IotHub. MODELES. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdlet. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f9f11-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f9f11-143">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9f11-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="f9f11-144">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="f9f11-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="f9f11-145">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9f11-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="f9f11-146">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="f9f11-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="f9f11-147">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9f11-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="f9f11-148">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="f9f11-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="f9f11-149">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="f9f11-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="f9f11-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9f11-150">NOTES</span></span>

## <span data-ttu-id="f9f11-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9f11-151">RELATED LINKS</span></span>
