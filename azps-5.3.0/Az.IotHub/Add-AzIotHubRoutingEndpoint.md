---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503428"
---
# <span data-ttu-id="83afa-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="83afa-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="83afa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83afa-102">SYNOPSIS</span></span>
<span data-ttu-id="83afa-103">Dodawanie punktu końcowego do centrum IoT</span><span class="sxs-lookup"><span data-stu-id="83afa-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="83afa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83afa-104">SYNTAX</span></span>

### <span data-ttu-id="83afa-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83afa-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83afa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="83afa-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83afa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="83afa-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83afa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83afa-108">DESCRIPTION</span></span>
<span data-ttu-id="83afa-109">Dodaj nowy punkt końcowy w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="83afa-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="83afa-110">Aby uzyskać informacje o obsługiwanych punktach końcowych, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="83afa-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="83afa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83afa-111">EXAMPLES</span></span>

### <span data-ttu-id="83afa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83afa-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="83afa-113">Dodaj nowy punkt końcowy "E2" typu EventHub do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="83afa-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="83afa-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="83afa-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="83afa-115">Dodaj nowy punkt końcowy "S1" z typu AzureStorageContainer do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="83afa-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="83afa-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83afa-116">PARAMETERS</span></span>

### <span data-ttu-id="83afa-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="83afa-117">-ConnectionString</span></span>
<span data-ttu-id="83afa-118">Parametry połączenia punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="83afa-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83afa-119">-DefaultProfile</span></span>
<span data-ttu-id="83afa-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83afa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83afa-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="83afa-121">-EndpointName</span></span>
<span data-ttu-id="83afa-122">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="83afa-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="83afa-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83afa-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="83afa-124">Grupa zasobów zasobu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="83afa-124">Resource group of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83afa-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="83afa-126">Identyfikator subskrypcji zasobu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="83afa-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="83afa-127">-EndpointType</span></span>
<span data-ttu-id="83afa-128">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="83afa-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="83afa-129">-ContainerName</span></span>
<span data-ttu-id="83afa-130">Nazwa kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="83afa-130">Name of the storage container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="83afa-131">-Encoding</span></span>
<span data-ttu-id="83afa-132">Wybierz format, w którym chcesz rozesłać dane.</span><span class="sxs-lookup"><span data-stu-id="83afa-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="83afa-133">Możesz wybrać pozycję JSON lub AVRO.</span><span class="sxs-lookup"><span data-stu-id="83afa-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="83afa-134">Domyślnym ustawieniem jest AVRO.</span><span class="sxs-lookup"><span data-stu-id="83afa-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afa-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83afa-135">-InputObject</span></span>
<span data-ttu-id="83afa-136">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="83afa-136">IotHub Object</span></span>

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

### <span data-ttu-id="83afa-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83afa-137">-Name</span></span>
<span data-ttu-id="83afa-138">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="83afa-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="83afa-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83afa-139">-ResourceGroupName</span></span>
<span data-ttu-id="83afa-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="83afa-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="83afa-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83afa-141">-ResourceId</span></span>
<span data-ttu-id="83afa-142">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="83afa-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="83afa-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83afa-143">-Confirm</span></span>
<span data-ttu-id="83afa-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83afa-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83afa-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83afa-145">-WhatIf</span></span>
<span data-ttu-id="83afa-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83afa-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83afa-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83afa-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83afa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83afa-148">CommonParameters</span></span>
<span data-ttu-id="83afa-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83afa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83afa-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83afa-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83afa-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83afa-151">INPUTS</span></span>

### <span data-ttu-id="83afa-152">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="83afa-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="83afa-153">System. String</span><span class="sxs-lookup"><span data-stu-id="83afa-153">System.String</span></span>

## <span data-ttu-id="83afa-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83afa-154">OUTPUTS</span></span>

### <span data-ttu-id="83afa-155">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="83afa-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="83afa-156">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="83afa-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="83afa-157">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="83afa-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="83afa-158">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83afa-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="83afa-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83afa-159">NOTES</span></span>

## <span data-ttu-id="83afa-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83afa-160">RELATED LINKS</span></span>
