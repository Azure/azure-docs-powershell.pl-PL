---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6dd40ff6bdf94d95b9fe31ead7ce6bde53c7042b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705402"
---
# <span data-ttu-id="fd4e5-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="fd4e5-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="fd4e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4e5-103">Pobierz przednią stację równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fd4e5-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="fd4e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd4e5-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd4e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd4e5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4e5-106">Na karcie **Get-AzFrontDoor** cmdletGet są pobierane wszystkie istniejące drzwi przednie w bieżącej subskrypcji, które pasują do podanych informacji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="fd4e5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd4e5-107">EXAMPLES</span></span>

### <span data-ttu-id="fd4e5-108">Przykład 1: Uzyskaj wszystkie FrontDoors w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
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

<span data-ttu-id="fd4e5-109">Pobierz wszystkie FrontDoors w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="fd4e5-110">Przykład 2: Pobierz wszystkie FrontDoors w grupie zasobów "RG1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
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

<span data-ttu-id="fd4e5-111">Pobierz wszystkie FrontDoors w grupie zasobów "RG1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="fd4e5-112">Przykład 3: Pobierz FrontDoors w grupie zasobów "RG1" o nazwie "frontDoor1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
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

<span data-ttu-id="fd4e5-113">Pobierz FrontDoors w grupie zasobów "RG1" o nazwie "frontDoor1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="fd4e5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd4e5-114">PARAMETERS</span></span>

### <span data-ttu-id="fd4e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4e5-115">-DefaultProfile</span></span>
<span data-ttu-id="fd4e5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd4e5-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd4e5-117">-Name</span></span>
<span data-ttu-id="fd4e5-118">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-118">Front Door name.</span></span>

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

### <span data-ttu-id="fd4e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd4e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd4e5-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-120">The resource group name.</span></span>

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

### <span data-ttu-id="fd4e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4e5-121">CommonParameters</span></span>
<span data-ttu-id="fd4e5-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4e5-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd4e5-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4e5-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd4e5-124">INPUTS</span></span>

### <span data-ttu-id="fd4e5-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fd4e5-125">None</span></span>

## <span data-ttu-id="fd4e5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd4e5-126">OUTPUTS</span></span>

### <span data-ttu-id="fd4e5-127">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="fd4e5-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="fd4e5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd4e5-128">NOTES</span></span>

## <span data-ttu-id="fd4e5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd4e5-129">RELATED LINKS</span></span>

<span data-ttu-id="fd4e5-130">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="fd4e5-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
