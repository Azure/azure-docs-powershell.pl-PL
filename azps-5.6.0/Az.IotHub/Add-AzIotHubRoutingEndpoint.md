---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 74ec300e1189cd93ac29fba917ee44590da0d650
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988219"
---
# <span data-ttu-id="49a0b-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="49a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="49a0b-103">Dodawanie punktu końcowego do centrum IoT</span><span class="sxs-lookup"><span data-stu-id="49a0b-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="49a0b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49a0b-104">SYNTAX</span></span>

### <span data-ttu-id="49a0b-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49a0b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49a0b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49a0b-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a0b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="49a0b-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a0b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="49a0b-108">DESCRIPTION</span></span>
<span data-ttu-id="49a0b-109">Dodaj nowy punkt końcowy w Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="49a0b-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="49a0b-110">Aby dowiedzieć się więcej o obsługiwanych punktach końcowych, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="49a0b-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="49a0b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49a0b-111">EXAMPLES</span></span>

### <span data-ttu-id="49a0b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49a0b-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="49a0b-113">Dodaj nowy punkt końcowy "E2" typu Aplikacja EventHub do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="49a0b-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="49a0b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="49a0b-114">Example 2</span></span>
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

<span data-ttu-id="49a0b-115">Dodaj nowy punkt końcowy "S1" typu AzureStorageContainer do centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="49a0b-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="49a0b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49a0b-116">PARAMETERS</span></span>

### <span data-ttu-id="49a0b-117">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="49a0b-117">-ConnectionString</span></span>
<span data-ttu-id="49a0b-118">Connection string of the Routing Endpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="49a0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a0b-119">-DefaultProfile</span></span>
<span data-ttu-id="49a0b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49a0b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a0b-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="49a0b-121">-EndpointName</span></span>
<span data-ttu-id="49a0b-122">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="49a0b-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="49a0b-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49a0b-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="49a0b-124">Grupa zasobów zasobu punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="49a0b-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="49a0b-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49a0b-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="49a0b-126">SubscriptionId zasobu Endpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="49a0b-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="49a0b-127">-EndpointType</span></span>
<span data-ttu-id="49a0b-128">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="49a0b-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="49a0b-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="49a0b-129">-ContainerName</span></span>
<span data-ttu-id="49a0b-130">Nazwa kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="49a0b-130">Name of the storage container</span></span>

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

### <span data-ttu-id="49a0b-131">— Kodowanie</span><span class="sxs-lookup"><span data-stu-id="49a0b-131">-Encoding</span></span>
<span data-ttu-id="49a0b-132">Wybierz format, w którym chcesz rozsyłać dane.</span><span class="sxs-lookup"><span data-stu-id="49a0b-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="49a0b-133">Możesz wybrać JSON lub AVRO.</span><span class="sxs-lookup"><span data-stu-id="49a0b-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="49a0b-134">Wartość domyślna to AVRO.</span><span class="sxs-lookup"><span data-stu-id="49a0b-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="49a0b-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49a0b-135">-InputObject</span></span>
<span data-ttu-id="49a0b-136">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="49a0b-136">IotHub Object</span></span>

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

### <span data-ttu-id="49a0b-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49a0b-137">-Name</span></span>
<span data-ttu-id="49a0b-138">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="49a0b-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="49a0b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a0b-139">-ResourceGroupName</span></span>
<span data-ttu-id="49a0b-140">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="49a0b-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="49a0b-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49a0b-141">-ResourceId</span></span>
<span data-ttu-id="49a0b-142">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="49a0b-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="49a0b-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49a0b-143">-Confirm</span></span>
<span data-ttu-id="49a0b-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49a0b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a0b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a0b-145">-WhatIf</span></span>
<span data-ttu-id="49a0b-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49a0b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a0b-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49a0b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a0b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a0b-148">CommonParameters</span></span>
<span data-ttu-id="49a0b-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a0b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a0b-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a0b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a0b-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49a0b-151">INPUTS</span></span>

### <span data-ttu-id="49a0b-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="49a0b-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="49a0b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="49a0b-153">System.String</span></span>

## <span data-ttu-id="49a0b-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49a0b-154">OUTPUTS</span></span>

### <span data-ttu-id="49a0b-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="49a0b-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="49a0b-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="49a0b-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49a0b-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="49a0b-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49a0b-159">NOTES</span></span>

## <span data-ttu-id="49a0b-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49a0b-160">RELATED LINKS</span></span>
