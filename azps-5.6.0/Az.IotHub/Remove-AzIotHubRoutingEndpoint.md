---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1b14ce37d03e1840336696792493e30701a09bfe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997830"
---
# <span data-ttu-id="69bd2-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="69bd2-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="69bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="69bd2-103">Usuwanie punktu końcowego dla centrum IoT</span><span class="sxs-lookup"><span data-stu-id="69bd2-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="69bd2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69bd2-104">SYNTAX</span></span>

### <span data-ttu-id="69bd2-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69bd2-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69bd2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="69bd2-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69bd2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69bd2-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69bd2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="69bd2-108">DESCRIPTION</span></span>
<span data-ttu-id="69bd2-109">Usuwanie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="69bd2-109">Delete an endpoint.</span></span> <span data-ttu-id="69bd2-110">Pamiętaj, aby usunąć wszystkie trasy, które używają tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="69bd2-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="69bd2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69bd2-111">EXAMPLES</span></span>

### <span data-ttu-id="69bd2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69bd2-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="69bd2-113">Usuń punkt końcowy "E2" z centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="69bd2-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="69bd2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69bd2-114">PARAMETERS</span></span>

### <span data-ttu-id="69bd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bd2-115">-DefaultProfile</span></span>
<span data-ttu-id="69bd2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69bd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69bd2-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="69bd2-117">-EndpointName</span></span>
<span data-ttu-id="69bd2-118">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="69bd2-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="69bd2-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="69bd2-119">-EndpointType</span></span>
<span data-ttu-id="69bd2-120">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="69bd2-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="69bd2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69bd2-121">-InputObject</span></span>
<span data-ttu-id="69bd2-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="69bd2-122">IotHub Object</span></span>

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

### <span data-ttu-id="69bd2-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69bd2-123">-Name</span></span>
<span data-ttu-id="69bd2-124">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="69bd2-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="69bd2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69bd2-125">-PassThru</span></span>
<span data-ttu-id="69bd2-126">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="69bd2-126">Allows to return the boolean object.</span></span> <span data-ttu-id="69bd2-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="69bd2-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69bd2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bd2-128">-ResourceGroupName</span></span>
<span data-ttu-id="69bd2-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="69bd2-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="69bd2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69bd2-130">-ResourceId</span></span>
<span data-ttu-id="69bd2-131">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="69bd2-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="69bd2-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69bd2-132">-Confirm</span></span>
<span data-ttu-id="69bd2-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69bd2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bd2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bd2-134">-WhatIf</span></span>
<span data-ttu-id="69bd2-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69bd2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bd2-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69bd2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bd2-137">CommonParameters</span></span>
<span data-ttu-id="69bd2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bd2-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bd2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bd2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69bd2-140">INPUTS</span></span>

### <span data-ttu-id="69bd2-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="69bd2-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="69bd2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="69bd2-142">System.String</span></span>

## <span data-ttu-id="69bd2-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69bd2-143">OUTPUTS</span></span>

### <span data-ttu-id="69bd2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69bd2-144">System.Boolean</span></span>

## <span data-ttu-id="69bd2-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69bd2-145">NOTES</span></span>

## <span data-ttu-id="69bd2-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69bd2-146">RELATED LINKS</span></span>
