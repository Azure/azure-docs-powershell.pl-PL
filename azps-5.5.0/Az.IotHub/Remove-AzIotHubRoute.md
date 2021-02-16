---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185635"
---
# <span data-ttu-id="8666a-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="8666a-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="8666a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8666a-102">SYNOPSIS</span></span>
<span data-ttu-id="8666a-103">Usuwanie trasy w centrum IoT</span><span class="sxs-lookup"><span data-stu-id="8666a-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="8666a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8666a-104">SYNTAX</span></span>

### <span data-ttu-id="8666a-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8666a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8666a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8666a-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8666a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8666a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8666a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8666a-108">DESCRIPTION</span></span>
<span data-ttu-id="8666a-109">Usuwanie tras do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="8666a-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="8666a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8666a-110">EXAMPLES</span></span>

### <span data-ttu-id="8666a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8666a-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="8666a-112">Usuń trasę "R1" z centrum IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="8666a-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="8666a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8666a-113">PARAMETERS</span></span>

### <span data-ttu-id="8666a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8666a-114">-DefaultProfile</span></span>
<span data-ttu-id="8666a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8666a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8666a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8666a-116">-InputObject</span></span>
<span data-ttu-id="8666a-117">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="8666a-117">IotHub Object</span></span>

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

### <span data-ttu-id="8666a-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8666a-118">-Name</span></span>
<span data-ttu-id="8666a-119">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="8666a-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8666a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8666a-120">-PassThru</span></span>
<span data-ttu-id="8666a-121">Zwraca obiekt logiczny.</span><span class="sxs-lookup"><span data-stu-id="8666a-121">Allows to return the boolean object.</span></span> <span data-ttu-id="8666a-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8666a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8666a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8666a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8666a-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8666a-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8666a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8666a-125">-ResourceId</span></span>
<span data-ttu-id="8666a-126">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="8666a-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8666a-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8666a-127">-RouteName</span></span>
<span data-ttu-id="8666a-128">Nazwa trasy</span><span class="sxs-lookup"><span data-stu-id="8666a-128">Name of the Route</span></span>

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

### <span data-ttu-id="8666a-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8666a-129">-Confirm</span></span>
<span data-ttu-id="8666a-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8666a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8666a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8666a-131">-WhatIf</span></span>
<span data-ttu-id="8666a-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8666a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8666a-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8666a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8666a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8666a-134">CommonParameters</span></span>
<span data-ttu-id="8666a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8666a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8666a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8666a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8666a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8666a-137">INPUTS</span></span>

### <span data-ttu-id="8666a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8666a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8666a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8666a-139">System.String</span></span>

## <span data-ttu-id="8666a-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8666a-140">OUTPUTS</span></span>

### <span data-ttu-id="8666a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8666a-141">System.Boolean</span></span>

## <span data-ttu-id="8666a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8666a-142">NOTES</span></span>

## <span data-ttu-id="8666a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8666a-143">RELATED LINKS</span></span>
