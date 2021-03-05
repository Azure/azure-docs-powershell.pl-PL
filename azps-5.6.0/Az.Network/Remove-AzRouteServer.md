---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 5fc8f30a2ef8a0ee276c9fb7ac3f1e2a503f6ec4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992545"
---
# <span data-ttu-id="ff16c-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="ff16c-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="ff16c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff16c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff16c-103">Usuwa serwer azure routeserver.</span><span class="sxs-lookup"><span data-stu-id="ff16c-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="ff16c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff16c-104">SYNTAX</span></span>

### <span data-ttu-id="ff16c-105">RouteServerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ff16c-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff16c-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff16c-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff16c-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff16c-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff16c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff16c-108">DESCRIPTION</span></span>
<span data-ttu-id="ff16c-109">Polecenie **cmdlet Remove-AzRouteServer** usuwa serwer Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="ff16c-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="ff16c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff16c-110">EXAMPLES</span></span>

### <span data-ttu-id="ff16c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff16c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="ff16c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ff16c-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="ff16c-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ff16c-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="ff16c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff16c-114">PARAMETERS</span></span>

### <span data-ttu-id="ff16c-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ff16c-115">-AsJob</span></span>
<span data-ttu-id="ff16c-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ff16c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff16c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff16c-117">-DefaultProfile</span></span>
<span data-ttu-id="ff16c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff16c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff16c-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ff16c-119">-Force</span></span>
<span data-ttu-id="ff16c-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="ff16c-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ff16c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff16c-121">-InputObject</span></span>
<span data-ttu-id="ff16c-122">Obiekt wejściowy serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="ff16c-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff16c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff16c-123">-PassThru</span></span>
<span data-ttu-id="ff16c-124">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="ff16c-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ff16c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff16c-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff16c-126">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="ff16c-126">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff16c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff16c-127">-ResourceId</span></span>
<span data-ttu-id="ff16c-128">Identyfikator zasobu serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="ff16c-128">The route server resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff16c-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="ff16c-129">-RouteServerName</span></span>
<span data-ttu-id="ff16c-130">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="ff16c-130">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff16c-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff16c-131">-Confirm</span></span>
<span data-ttu-id="ff16c-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff16c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff16c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff16c-133">-WhatIf</span></span>
<span data-ttu-id="ff16c-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff16c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff16c-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ff16c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff16c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff16c-136">CommonParameters</span></span>
<span data-ttu-id="ff16c-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff16c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff16c-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff16c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff16c-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff16c-139">INPUTS</span></span>

### <span data-ttu-id="ff16c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ff16c-140">System.String</span></span>

### <span data-ttu-id="ff16c-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="ff16c-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="ff16c-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff16c-142">OUTPUTS</span></span>

### <span data-ttu-id="ff16c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff16c-143">System.Boolean</span></span>

## <span data-ttu-id="ff16c-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff16c-144">NOTES</span></span>

## <span data-ttu-id="ff16c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff16c-145">RELATED LINKS</span></span>
