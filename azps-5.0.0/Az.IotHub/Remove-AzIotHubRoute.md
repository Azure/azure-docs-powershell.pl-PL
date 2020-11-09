---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304692"
---
# <span data-ttu-id="bd3a5-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="bd3a5-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="bd3a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="bd3a5-103">Usuwanie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="bd3a5-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="bd3a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd3a5-104">SYNTAX</span></span>

### <span data-ttu-id="bd3a5-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd3a5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd3a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd3a5-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd3a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bd3a5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd3a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bd3a5-108">DESCRIPTION</span></span>
<span data-ttu-id="bd3a5-109">Usuwanie tras do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="bd3a5-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="bd3a5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd3a5-110">EXAMPLES</span></span>

### <span data-ttu-id="bd3a5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd3a5-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="bd3a5-112">Usuń trasę "R1" z Centrum IoT firmy "myiothub".</span><span class="sxs-lookup"><span data-stu-id="bd3a5-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="bd3a5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd3a5-113">PARAMETERS</span></span>

### <span data-ttu-id="bd3a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd3a5-114">-DefaultProfile</span></span>
<span data-ttu-id="bd3a5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd3a5-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd3a5-116">-InputObject</span></span>
<span data-ttu-id="bd3a5-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="bd3a5-117">IotHub Object</span></span>

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

### <span data-ttu-id="bd3a5-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd3a5-118">-Name</span></span>
<span data-ttu-id="bd3a5-119">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="bd3a5-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bd3a5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd3a5-120">-PassThru</span></span>
<span data-ttu-id="bd3a5-121">Umożliwia zwrócenie obiektu logicznego.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-121">Allows to return the boolean object.</span></span> <span data-ttu-id="bd3a5-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bd3a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd3a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd3a5-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bd3a5-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bd3a5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd3a5-125">-ResourceId</span></span>
<span data-ttu-id="bd3a5-126">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="bd3a5-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bd3a5-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="bd3a5-127">-RouteName</span></span>
<span data-ttu-id="bd3a5-128">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="bd3a5-128">Name of the Route</span></span>

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

### <span data-ttu-id="bd3a5-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd3a5-129">-Confirm</span></span>
<span data-ttu-id="bd3a5-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd3a5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd3a5-131">-WhatIf</span></span>
<span data-ttu-id="bd3a5-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd3a5-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd3a5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd3a5-134">CommonParameters</span></span>
<span data-ttu-id="bd3a5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd3a5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd3a5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd3a5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd3a5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd3a5-137">INPUTS</span></span>

### <span data-ttu-id="bd3a5-138">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bd3a5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bd3a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bd3a5-139">System.String</span></span>

## <span data-ttu-id="bd3a5-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd3a5-140">OUTPUTS</span></span>

### <span data-ttu-id="bd3a5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd3a5-141">System.Boolean</span></span>

## <span data-ttu-id="bd3a5-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd3a5-142">NOTES</span></span>

## <span data-ttu-id="bd3a5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd3a5-143">RELATED LINKS</span></span>
