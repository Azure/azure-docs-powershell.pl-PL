---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 2b50d49c108408e1639b5f5f490c2aaafc7bbd82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191722"
---
# <span data-ttu-id="275ec-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="275ec-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="275ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="275ec-102">SYNOPSIS</span></span>
<span data-ttu-id="275ec-103">Usuwa serwer usługi Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="275ec-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="275ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="275ec-104">SYNTAX</span></span>

### <span data-ttu-id="275ec-105">RouteServerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="275ec-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275ec-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275ec-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275ec-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="275ec-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275ec-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="275ec-108">DESCRIPTION</span></span>
<span data-ttu-id="275ec-109">Polecenie **cmdlet Remove-AzRouteServer** usuwa serwer Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="275ec-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="275ec-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="275ec-110">EXAMPLES</span></span>

### <span data-ttu-id="275ec-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="275ec-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="275ec-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="275ec-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="275ec-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="275ec-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="275ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="275ec-114">PARAMETERS</span></span>

### <span data-ttu-id="275ec-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="275ec-115">-AsJob</span></span>
<span data-ttu-id="275ec-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="275ec-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="275ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275ec-117">-DefaultProfile</span></span>
<span data-ttu-id="275ec-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="275ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275ec-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="275ec-119">-Force</span></span>
<span data-ttu-id="275ec-120">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="275ec-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="275ec-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="275ec-121">-InputObject</span></span>
<span data-ttu-id="275ec-122">Obiekt wejściowy serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="275ec-122">The route server input object.</span></span>

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

### <span data-ttu-id="275ec-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="275ec-123">-PassThru</span></span>
<span data-ttu-id="275ec-124">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="275ec-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="275ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="275ec-126">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="275ec-126">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="275ec-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="275ec-127">-ResourceId</span></span>
<span data-ttu-id="275ec-128">Identyfikator zasobu serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="275ec-128">The route server resource Id.</span></span>

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

### <span data-ttu-id="275ec-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="275ec-129">-RouteServerName</span></span>
<span data-ttu-id="275ec-130">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="275ec-130">The name of the route server.</span></span>

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

### <span data-ttu-id="275ec-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="275ec-131">-Confirm</span></span>
<span data-ttu-id="275ec-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="275ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275ec-133">-WhatIf</span></span>
<span data-ttu-id="275ec-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275ec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275ec-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="275ec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275ec-136">CommonParameters</span></span>
<span data-ttu-id="275ec-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275ec-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="275ec-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275ec-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275ec-139">INPUTS</span></span>

### <span data-ttu-id="275ec-140">System.String</span><span class="sxs-lookup"><span data-stu-id="275ec-140">System.String</span></span>

### <span data-ttu-id="275ec-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="275ec-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="275ec-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275ec-142">OUTPUTS</span></span>

### <span data-ttu-id="275ec-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="275ec-143">System.Boolean</span></span>

## <span data-ttu-id="275ec-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="275ec-144">NOTES</span></span>

## <span data-ttu-id="275ec-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="275ec-145">RELATED LINKS</span></span>
