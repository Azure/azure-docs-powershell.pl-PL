---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 0ce0a651444bd30a1bf6c766083b0a8584c5cd71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995492"
---
# <span data-ttu-id="35e90-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="35e90-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="35e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e90-102">SYNOPSIS</span></span>
<span data-ttu-id="35e90-103">Usuwanie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="35e90-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="35e90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35e90-104">SYNTAX</span></span>

### <span data-ttu-id="35e90-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35e90-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35e90-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35e90-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35e90-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35e90-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e90-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="35e90-108">DESCRIPTION</span></span>
<span data-ttu-id="35e90-109">Usuwanie tras do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="35e90-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="35e90-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35e90-110">EXAMPLES</span></span>

### <span data-ttu-id="35e90-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35e90-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="35e90-112">Usuń trasę "R1" z centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="35e90-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="35e90-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35e90-113">PARAMETERS</span></span>

### <span data-ttu-id="35e90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e90-114">-DefaultProfile</span></span>
<span data-ttu-id="35e90-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35e90-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e90-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35e90-116">-InputObject</span></span>
<span data-ttu-id="35e90-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="35e90-117">IotHub Object</span></span>

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

### <span data-ttu-id="35e90-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35e90-118">-Name</span></span>
<span data-ttu-id="35e90-119">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="35e90-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="35e90-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35e90-120">-PassThru</span></span>
<span data-ttu-id="35e90-121">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="35e90-121">Allows to return the boolean object.</span></span> <span data-ttu-id="35e90-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="35e90-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35e90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e90-123">-ResourceGroupName</span></span>
<span data-ttu-id="35e90-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="35e90-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="35e90-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35e90-125">-ResourceId</span></span>
<span data-ttu-id="35e90-126">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="35e90-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="35e90-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="35e90-127">-RouteName</span></span>
<span data-ttu-id="35e90-128">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="35e90-128">Name of the Route</span></span>

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

### <span data-ttu-id="35e90-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35e90-129">-Confirm</span></span>
<span data-ttu-id="35e90-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="35e90-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e90-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e90-131">-WhatIf</span></span>
<span data-ttu-id="35e90-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e90-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e90-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="35e90-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e90-134">CommonParameters</span></span>
<span data-ttu-id="35e90-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e90-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35e90-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e90-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35e90-137">INPUTS</span></span>

### <span data-ttu-id="35e90-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="35e90-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="35e90-139">System.String</span><span class="sxs-lookup"><span data-stu-id="35e90-139">System.String</span></span>

## <span data-ttu-id="35e90-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35e90-140">OUTPUTS</span></span>

### <span data-ttu-id="35e90-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35e90-141">System.Boolean</span></span>

## <span data-ttu-id="35e90-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35e90-142">NOTES</span></span>

## <span data-ttu-id="35e90-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35e90-143">RELATED LINKS</span></span>
