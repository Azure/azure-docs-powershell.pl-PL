---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: f48fadb740fdca823c2513d68a2f77e0d34c4631
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954721"
---
# <span data-ttu-id="f73e1-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f73e1-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="f73e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f73e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f73e1-103">Uzyskaj równoważenie obciążenia drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="f73e1-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="f73e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f73e1-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f73e1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f73e1-105">DESCRIPTION</span></span>
<span data-ttu-id="f73e1-106">Polecenie **cmdlet Get-AzFrontDoor** pobiera wszystkie istniejące drzwi frontowe w bieżącej subskrypcji, które są takie, jak podane informacje.</span><span class="sxs-lookup"><span data-stu-id="f73e1-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="f73e1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f73e1-107">EXAMPLES</span></span>

### <span data-ttu-id="f73e1-108">Przykład 1. Pobierz wszystkie frontdoory w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f73e1-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="f73e1-109">Pobierz wszystkie frontoory w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f73e1-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="f73e1-110">Przykład 2. Uzyskiwanie wszystkich frontoorów w grupie zasobów "rg1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f73e1-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="f73e1-111">Pobierz wszystkich frontoorów w grupie zasobów "rg1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f73e1-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="f73e1-112">Przykład 3. Pobierz frontdoory z grupy zasobów "rg1" o nazwie "frontDoor1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f73e1-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="f73e1-113">Pobierz frontdoory w grupie zasobów "rg1" o nazwie "frontDoor1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f73e1-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="f73e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f73e1-114">PARAMETERS</span></span>

### <span data-ttu-id="f73e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73e1-115">-DefaultProfile</span></span>
<span data-ttu-id="f73e1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f73e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f73e1-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f73e1-117">-Name</span></span>
<span data-ttu-id="f73e1-118">Nazwa drzwi przednich.</span><span class="sxs-lookup"><span data-stu-id="f73e1-118">Front Door name.</span></span>

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

### <span data-ttu-id="f73e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="f73e1-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f73e1-120">The resource group name.</span></span>

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

### <span data-ttu-id="f73e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73e1-121">CommonParameters</span></span>
<span data-ttu-id="f73e1-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73e1-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f73e1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73e1-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f73e1-124">INPUTS</span></span>

### <span data-ttu-id="f73e1-125">Brak</span><span class="sxs-lookup"><span data-stu-id="f73e1-125">None</span></span>

## <span data-ttu-id="f73e1-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f73e1-126">OUTPUTS</span></span>

### <span data-ttu-id="f73e1-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f73e1-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="f73e1-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f73e1-128">NOTES</span></span>

## <span data-ttu-id="f73e1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f73e1-129">RELATED LINKS</span></span>

<span data-ttu-id="f73e1-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f73e1-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
