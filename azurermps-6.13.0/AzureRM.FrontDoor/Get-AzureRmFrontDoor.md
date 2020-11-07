---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717404"
---
# <span data-ttu-id="493c9-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="493c9-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="493c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="493c9-102">SYNOPSIS</span></span>
<span data-ttu-id="493c9-103">Pobierz przednią stację równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="493c9-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="493c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="493c9-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="493c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="493c9-105">DESCRIPTION</span></span>
<span data-ttu-id="493c9-106">Na karcie **Get-AzureRmFrontDoor** cmdletGet są pobierane wszystkie istniejące drzwi przednie w bieżącej subskrypcji, które pasują do podanych informacji.</span><span class="sxs-lookup"><span data-stu-id="493c9-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="493c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="493c9-107">EXAMPLES</span></span>

### <span data-ttu-id="493c9-108">Przykład 1: Uzyskaj wszystkie FrontDoors w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="493c9-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="493c9-109">Pobierz wszystkie FrontDoors w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="493c9-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="493c9-110">Przykład 2: Pobierz wszystkie FrontDoors w grupie zasobów "RG1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="493c9-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="493c9-111">Pobierz wszystkie FrontDoors w grupie zasobów "RG1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="493c9-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="493c9-112">Przykład 3: Pobierz FrontDoors w grupie zasobów "RG1" o nazwie "frontDoor1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="493c9-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="493c9-113">Pobierz FrontDoors w grupie zasobów "RG1" o nazwie "frontDoor1" w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="493c9-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="493c9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="493c9-114">PARAMETERS</span></span>

### <span data-ttu-id="493c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493c9-115">-DefaultProfile</span></span>
<span data-ttu-id="493c9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="493c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="493c9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="493c9-117">-Name</span></span>
<span data-ttu-id="493c9-118">Imię i nazwisko drzwi przednie.</span><span class="sxs-lookup"><span data-stu-id="493c9-118">Front Door name.</span></span>

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

### <span data-ttu-id="493c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="493c9-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="493c9-120">The resource group name.</span></span>

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

### <span data-ttu-id="493c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493c9-121">CommonParameters</span></span>
<span data-ttu-id="493c9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493c9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="493c9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493c9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="493c9-124">INPUTS</span></span>

### <span data-ttu-id="493c9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="493c9-125">System.String</span></span>

## <span data-ttu-id="493c9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="493c9-126">OUTPUTS</span></span>

### <span data-ttu-id="493c9-127">Microsoft. Azure. Commands. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="493c9-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="493c9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="493c9-128">NOTES</span></span>

## <span data-ttu-id="493c9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="493c9-129">RELATED LINKS</span></span>

<span data-ttu-id="493c9-130">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="493c9-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
