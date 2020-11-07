---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 9715e7ee505fce0b34039d74d35e53b7138d7160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893118"
---
# <span data-ttu-id="4d333-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d333-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="4d333-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d333-102">SYNOPSIS</span></span>
<span data-ttu-id="4d333-103">Dodawanie punktu końcowego do centrum IoT</span><span class="sxs-lookup"><span data-stu-id="4d333-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="4d333-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d333-104">SYNTAX</span></span>

### <span data-ttu-id="4d333-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4d333-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d333-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d333-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d333-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d333-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d333-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4d333-108">DESCRIPTION</span></span>
<span data-ttu-id="4d333-109">Dodaj nowy punkt końcowy w centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="4d333-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="4d333-110">Aby uzyskać informacje o obsługiwanych punktach końcowych, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="4d333-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="4d333-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d333-111">EXAMPLES</span></span>

### <span data-ttu-id="4d333-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d333-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="4d333-113">Dodaj nowy punkt końcowy "E2" typu EventHub do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4d333-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="4d333-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4d333-114">Example 2</span></span>
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

<span data-ttu-id="4d333-115">Dodaj nowy punkt końcowy "S1" z typu AzureStorageContainer do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="4d333-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="4d333-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d333-116">PARAMETERS</span></span>

### <span data-ttu-id="4d333-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4d333-117">-ConnectionString</span></span>
<span data-ttu-id="4d333-118">Parametry połączenia punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="4d333-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4d333-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d333-119">-DefaultProfile</span></span>
<span data-ttu-id="4d333-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d333-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d333-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4d333-121">-EndpointName</span></span>
<span data-ttu-id="4d333-122">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="4d333-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4d333-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d333-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="4d333-124">Grupa zasobów zasobu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="4d333-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="4d333-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d333-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="4d333-126">Identyfikator subskrypcji zasobu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="4d333-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="4d333-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="4d333-127">-EndpointType</span></span>
<span data-ttu-id="4d333-128">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="4d333-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="4d333-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4d333-129">-ContainerName</span></span>
<span data-ttu-id="4d333-130">Nazwa kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="4d333-130">Name of the storage container</span></span>

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

### <span data-ttu-id="4d333-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="4d333-131">-Encoding</span></span>
<span data-ttu-id="4d333-132">Wybierz format, w którym chcesz rozesłać dane.</span><span class="sxs-lookup"><span data-stu-id="4d333-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="4d333-133">Możesz wybrać pozycję JSON lub AVRO.</span><span class="sxs-lookup"><span data-stu-id="4d333-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="4d333-134">Domyślnym ustawieniem jest AVRO.</span><span class="sxs-lookup"><span data-stu-id="4d333-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="4d333-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d333-135">-InputObject</span></span>
<span data-ttu-id="4d333-136">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="4d333-136">IotHub Object</span></span>

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

### <span data-ttu-id="4d333-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d333-137">-Name</span></span>
<span data-ttu-id="4d333-138">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="4d333-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4d333-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d333-139">-ResourceGroupName</span></span>
<span data-ttu-id="4d333-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4d333-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4d333-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d333-141">-ResourceId</span></span>
<span data-ttu-id="4d333-142">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="4d333-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4d333-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d333-143">-Confirm</span></span>
<span data-ttu-id="4d333-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d333-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d333-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d333-145">-WhatIf</span></span>
<span data-ttu-id="4d333-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d333-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d333-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d333-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d333-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d333-148">CommonParameters</span></span>
<span data-ttu-id="4d333-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d333-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d333-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d333-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d333-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d333-151">INPUTS</span></span>

### <span data-ttu-id="4d333-152">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4d333-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4d333-153">System. String</span><span class="sxs-lookup"><span data-stu-id="4d333-153">System.String</span></span>

## <span data-ttu-id="4d333-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d333-154">OUTPUTS</span></span>

### <span data-ttu-id="4d333-155">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d333-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="4d333-156">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d333-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="4d333-157">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d333-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="4d333-158">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d333-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="4d333-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d333-159">NOTES</span></span>

## <span data-ttu-id="4d333-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d333-160">RELATED LINKS</span></span>
