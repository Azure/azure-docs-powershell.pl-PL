---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543808"
---
# <span data-ttu-id="1e886-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e886-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="1e886-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e886-102">SYNOPSIS</span></span>
<span data-ttu-id="1e886-103">Dodawanie punktu końcowego do centrum IoT</span><span class="sxs-lookup"><span data-stu-id="1e886-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e886-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e886-104">SYNTAX</span></span>

### <span data-ttu-id="1e886-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e886-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e886-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e886-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e886-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1e886-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e886-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e886-108">DESCRIPTION</span></span>
<span data-ttu-id="1e886-109">Dodaj nowy punkt końcowy w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1e886-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="1e886-110">Aby uzyskać informacje o obsługiwanych punktach końcowych, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="1e886-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="1e886-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e886-111">EXAMPLES</span></span>

### <span data-ttu-id="1e886-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e886-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="1e886-113">Dodaj nowy punkt końcowy "E2" typu EventHub do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="1e886-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="1e886-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1e886-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="1e886-115">Dodaj nowy punkt końcowy "S1" z typu AzureStorageContainer do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="1e886-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="1e886-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e886-116">PARAMETERS</span></span>

### <span data-ttu-id="1e886-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1e886-117">-ConnectionString</span></span>
<span data-ttu-id="1e886-118">Parametry połączenia punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="1e886-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e886-119">-DefaultProfile</span></span>
<span data-ttu-id="1e886-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e886-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e886-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1e886-121">-EndpointName</span></span>
<span data-ttu-id="1e886-122">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="1e886-122">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e886-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="1e886-124">Grupa zasobów w punkcie końcowym</span><span class="sxs-lookup"><span data-stu-id="1e886-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e886-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="1e886-126">Identyfikator subskrypcji zasobu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="1e886-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="1e886-127">-EndpointType</span></span>
<span data-ttu-id="1e886-128">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="1e886-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e886-129">-InputObject</span></span>
<span data-ttu-id="1e886-130">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="1e886-130">IotHub Object</span></span>

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

### <span data-ttu-id="1e886-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e886-131">-Name</span></span>
<span data-ttu-id="1e886-132">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="1e886-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1e886-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e886-133">-ResourceGroupName</span></span>
<span data-ttu-id="1e886-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1e886-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1e886-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e886-135">-ResourceId</span></span>
<span data-ttu-id="1e886-136">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="1e886-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1e886-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e886-137">-Confirm</span></span>
<span data-ttu-id="1e886-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e886-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e886-139">-WhatIf</span></span>
<span data-ttu-id="1e886-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e886-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e886-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e886-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e886-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e886-142">CommonParameters</span></span>
<span data-ttu-id="1e886-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e886-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e886-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e886-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e886-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e886-145">INPUTS</span></span>

### <span data-ttu-id="1e886-146">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1e886-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="1e886-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1e886-147">System.String</span></span>

## <span data-ttu-id="1e886-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e886-148">OUTPUTS</span></span>

### <span data-ttu-id="1e886-149">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e886-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="1e886-150">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Commands. IotHub. MODELES. PSRoutingServiceBusTopicEndpoint Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="1e886-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="1e886-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e886-151">NOTES</span></span>

## <span data-ttu-id="1e886-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e886-152">RELATED LINKS</span></span>
