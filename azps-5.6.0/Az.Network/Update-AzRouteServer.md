---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 3cb1fe0fb72182e22c4f7653de26f356ecd823ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951617"
---
# <span data-ttu-id="95f68-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="95f68-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="95f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f68-102">SYNOPSIS</span></span>
<span data-ttu-id="95f68-103">Zaktualizuj serwer usługi Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="95f68-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="95f68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95f68-104">SYNTAX</span></span>

### <span data-ttu-id="95f68-105">RouteServerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="95f68-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95f68-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95f68-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95f68-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="95f68-107">DESCRIPTION</span></span>
<span data-ttu-id="95f68-108">Polecenie **cmdlet Update-AzRouteServer** przełącza ruch między gałęziami do serwera Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="95f68-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="95f68-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95f68-109">EXAMPLES</span></span>

### <span data-ttu-id="95f68-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95f68-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="95f68-111">Aby włączyć ruch gałęzi na serwerze tras.</span><span class="sxs-lookup"><span data-stu-id="95f68-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="95f68-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95f68-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="95f68-113">Aby wyłączyć ruch gałęzi na serwerze tras.</span><span class="sxs-lookup"><span data-stu-id="95f68-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="95f68-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95f68-114">PARAMETERS</span></span>

### <span data-ttu-id="95f68-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="95f68-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="95f68-116">Flaga zezwala na ruch gałęzi na serwerze tras.</span><span class="sxs-lookup"><span data-stu-id="95f68-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="95f68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f68-117">-DefaultProfile</span></span>
<span data-ttu-id="95f68-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95f68-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95f68-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f68-119">-ResourceGroupName</span></span>
<span data-ttu-id="95f68-120">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="95f68-120">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="95f68-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95f68-121">-ResourceId</span></span>
<span data-ttu-id="95f68-122">ResourceId serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="95f68-122">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="95f68-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="95f68-123">-RouteServerName</span></span>
<span data-ttu-id="95f68-124">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="95f68-124">The name of the route server.</span></span>

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

### <span data-ttu-id="95f68-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95f68-125">-Confirm</span></span>
<span data-ttu-id="95f68-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95f68-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95f68-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95f68-127">-WhatIf</span></span>
<span data-ttu-id="95f68-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95f68-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95f68-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95f68-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95f68-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f68-130">CommonParameters</span></span>
<span data-ttu-id="95f68-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f68-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f68-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95f68-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f68-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95f68-133">INPUTS</span></span>

### <span data-ttu-id="95f68-134">System.String</span><span class="sxs-lookup"><span data-stu-id="95f68-134">System.String</span></span>

## <span data-ttu-id="95f68-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95f68-135">OUTPUTS</span></span>

### <span data-ttu-id="95f68-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="95f68-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="95f68-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95f68-137">NOTES</span></span>

## <span data-ttu-id="95f68-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95f68-138">RELATED LINKS</span></span>
