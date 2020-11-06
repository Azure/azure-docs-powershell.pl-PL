---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552807"
---
# <span data-ttu-id="01d58-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="01d58-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="01d58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01d58-102">SYNOPSIS</span></span>
<span data-ttu-id="01d58-103">Usuwanie punktu końcowego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="01d58-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01d58-104">SYNTAX</span></span>

### <span data-ttu-id="01d58-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="01d58-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01d58-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="01d58-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01d58-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="01d58-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01d58-108">Opis</span><span class="sxs-lookup"><span data-stu-id="01d58-108">DESCRIPTION</span></span>
<span data-ttu-id="01d58-109">Usuwanie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="01d58-109">Delete an endpoint.</span></span> <span data-ttu-id="01d58-110">Pamiętaj, aby usunąć wszystkie trasy korzystające z tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="01d58-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="01d58-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01d58-111">EXAMPLES</span></span>

### <span data-ttu-id="01d58-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01d58-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="01d58-113">Usuń punkt końcowy "E2" z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="01d58-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="01d58-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01d58-114">PARAMETERS</span></span>

### <span data-ttu-id="01d58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d58-115">-DefaultProfile</span></span>
<span data-ttu-id="01d58-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01d58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d58-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="01d58-117">-EndpointName</span></span>
<span data-ttu-id="01d58-118">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="01d58-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="01d58-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="01d58-119">-EndpointType</span></span>
<span data-ttu-id="01d58-120">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="01d58-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d58-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="01d58-121">-InputObject</span></span>
<span data-ttu-id="01d58-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="01d58-122">IotHub Object</span></span>

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

### <span data-ttu-id="01d58-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01d58-123">-Name</span></span>
<span data-ttu-id="01d58-124">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="01d58-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="01d58-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01d58-125">-PassThru</span></span>
<span data-ttu-id="01d58-126">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="01d58-126">Allows to return the boolean object.</span></span> <span data-ttu-id="01d58-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="01d58-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d58-128">-ResourceGroupName</span></span>
<span data-ttu-id="01d58-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="01d58-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="01d58-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01d58-130">-ResourceId</span></span>
<span data-ttu-id="01d58-131">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="01d58-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="01d58-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01d58-132">-Confirm</span></span>
<span data-ttu-id="01d58-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d58-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01d58-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01d58-134">-WhatIf</span></span>
<span data-ttu-id="01d58-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01d58-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01d58-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01d58-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01d58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d58-137">CommonParameters</span></span>
<span data-ttu-id="01d58-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d58-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d58-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d58-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01d58-140">INPUTS</span></span>

### <span data-ttu-id="01d58-141">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="01d58-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="01d58-142">System. String</span><span class="sxs-lookup"><span data-stu-id="01d58-142">System.String</span></span>

## <span data-ttu-id="01d58-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01d58-143">OUTPUTS</span></span>

### <span data-ttu-id="01d58-144">Microsoft. Azure. Commands. Management. IotHub. models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="01d58-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="01d58-145">System. Collections. Generic. list `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. MODELES. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Management. `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` Commands. Management. IotHub. MODELES. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] system. Collections; Generic. list ' 1 [[Microsoft. Azure. Commands. IotHub. Commands. = null]]</span><span class="sxs-lookup"><span data-stu-id="01d58-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="01d58-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01d58-146">NOTES</span></span>

## <span data-ttu-id="01d58-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01d58-147">RELATED LINKS</span></span>
