---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServer.md
ms.openlocfilehash: 20021b2d557b4590a9853d3124930db27286313a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184674"
---
# <span data-ttu-id="1708c-101">Get-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="1708c-101">Get-AzRouteServer</span></span>

## <span data-ttu-id="1708c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1708c-102">SYNOPSIS</span></span>
<span data-ttu-id="1708c-103">Uzyskiwanie serwera usługi Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="1708c-103">Get an Azure RouteServer</span></span>

## <span data-ttu-id="1708c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1708c-104">SYNTAX</span></span>

### <span data-ttu-id="1708c-105">RouteServerSubscriptionIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1708c-105">RouteServerSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzRouteServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1708c-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1708c-106">RouteServerNameParameterSet</span></span>
```
Get-AzRouteServer -ResourceGroupName <String> [-RouteServerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1708c-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1708c-107">RouteServerResourceIdParameterSet</span></span>
```
Get-AzRouteServer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1708c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1708c-108">DESCRIPTION</span></span>
<span data-ttu-id="1708c-109">Polecenie **cmdlet Get-AzRouteServer** otrzymuje serwer Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="1708c-109">The **Get-AzRouteServer** cmdlet gets an Azure RouteServer</span></span>

## <span data-ttu-id="1708c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1708c-110">EXAMPLES</span></span>

### <span data-ttu-id="1708c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1708c-111">Example 1</span></span>
```powershell
Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="1708c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1708c-112">Example 2</span></span>
```powershell
$routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Get-AzRouteServer -ResourceId $routeServerId
```
## <span data-ttu-id="1708c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1708c-113">PARAMETERS</span></span>

### <span data-ttu-id="1708c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1708c-114">-DefaultProfile</span></span>
<span data-ttu-id="1708c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1708c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1708c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1708c-116">-ResourceGroupName</span></span>
<span data-ttu-id="1708c-117">Nazwa grupy zasobów serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="1708c-117">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="1708c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1708c-118">-ResourceId</span></span>
<span data-ttu-id="1708c-119">ResourceId serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="1708c-119">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="1708c-120">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="1708c-120">-RouteServerName</span></span>
<span data-ttu-id="1708c-121">Nazwa serwera trasy.</span><span class="sxs-lookup"><span data-stu-id="1708c-121">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1708c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1708c-122">CommonParameters</span></span>
<span data-ttu-id="1708c-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1708c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1708c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1708c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1708c-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1708c-125">INPUTS</span></span>

### <span data-ttu-id="1708c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1708c-126">System.String</span></span>

## <span data-ttu-id="1708c-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1708c-127">OUTPUTS</span></span>

### <span data-ttu-id="1708c-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="1708c-128">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="1708c-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1708c-129">NOTES</span></span>

## <span data-ttu-id="1708c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1708c-130">RELATED LINKS</span></span>
