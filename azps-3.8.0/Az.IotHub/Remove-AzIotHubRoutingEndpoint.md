---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050382"
---
# <span data-ttu-id="808f7-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="808f7-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="808f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="808f7-102">SYNOPSIS</span></span>
<span data-ttu-id="808f7-103">Usuwanie punktu końcowego Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="808f7-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="808f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="808f7-104">SYNTAX</span></span>

### <span data-ttu-id="808f7-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="808f7-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="808f7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="808f7-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="808f7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="808f7-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="808f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="808f7-108">DESCRIPTION</span></span>
<span data-ttu-id="808f7-109">Usuwanie punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="808f7-109">Delete an endpoint.</span></span> <span data-ttu-id="808f7-110">Pamiętaj, aby usunąć wszystkie trasy korzystające z tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="808f7-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="808f7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="808f7-111">EXAMPLES</span></span>

### <span data-ttu-id="808f7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="808f7-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="808f7-113">Usuń punkt końcowy "E2" z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="808f7-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="808f7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="808f7-114">PARAMETERS</span></span>

### <span data-ttu-id="808f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808f7-115">-DefaultProfile</span></span>
<span data-ttu-id="808f7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="808f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808f7-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="808f7-117">-EndpointName</span></span>
<span data-ttu-id="808f7-118">Nazwa punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="808f7-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="808f7-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="808f7-119">-EndpointType</span></span>
<span data-ttu-id="808f7-120">Typ punktu końcowego routingu</span><span class="sxs-lookup"><span data-stu-id="808f7-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="808f7-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="808f7-121">-InputObject</span></span>
<span data-ttu-id="808f7-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="808f7-122">IotHub Object</span></span>

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

### <span data-ttu-id="808f7-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="808f7-123">-Name</span></span>
<span data-ttu-id="808f7-124">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="808f7-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="808f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="808f7-125">-PassThru</span></span>
<span data-ttu-id="808f7-126">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="808f7-126">Allows to return the boolean object.</span></span> <span data-ttu-id="808f7-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="808f7-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="808f7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808f7-128">-ResourceGroupName</span></span>
<span data-ttu-id="808f7-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="808f7-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="808f7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="808f7-130">-ResourceId</span></span>
<span data-ttu-id="808f7-131">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="808f7-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="808f7-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="808f7-132">-Confirm</span></span>
<span data-ttu-id="808f7-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808f7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="808f7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808f7-134">-WhatIf</span></span>
<span data-ttu-id="808f7-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808f7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808f7-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="808f7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="808f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808f7-137">CommonParameters</span></span>
<span data-ttu-id="808f7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808f7-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808f7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808f7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="808f7-140">INPUTS</span></span>

### <span data-ttu-id="808f7-141">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="808f7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="808f7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="808f7-142">System.String</span></span>

## <span data-ttu-id="808f7-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="808f7-143">OUTPUTS</span></span>

### <span data-ttu-id="808f7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="808f7-144">System.Boolean</span></span>

## <span data-ttu-id="808f7-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="808f7-145">NOTES</span></span>

## <span data-ttu-id="808f7-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="808f7-146">RELATED LINKS</span></span>
