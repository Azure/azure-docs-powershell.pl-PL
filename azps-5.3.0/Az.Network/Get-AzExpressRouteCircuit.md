---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498738"
---
# <span data-ttu-id="867be-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="867be-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="867be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="867be-102">SYNOPSIS</span></span>
<span data-ttu-id="867be-103">Pobiera obwód ExpressRoute platformy Azure z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="867be-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="867be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="867be-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="867be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="867be-105">DESCRIPTION</span></span>
<span data-ttu-id="867be-106">Polecenie cmdlet **Get-AzExpressRouteCircuit** służy do pobierania obiektu obwodu ExpressRoute z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="867be-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="867be-107">Zwracany obiekt obwodu może być wykorzystywany jako wejście dla innych poleceń cmdlet, które działają na obwodach ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="867be-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="867be-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="867be-108">EXAMPLES</span></span>

### <span data-ttu-id="867be-109">Przykład 1: uzyskiwanie obwodu ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="867be-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="867be-110">Uzyskiwanie określonego obwodu ExpressRoute o nazwie "testrg" i ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="867be-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="867be-111">Przykład 2: wykaz obwodów ExpressRoute przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="867be-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="867be-112">Pobierz wszystkie obwody ExpressRoute, których nazwa zaczyna się od tekstu "test".</span><span class="sxs-lookup"><span data-stu-id="867be-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="867be-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="867be-113">PARAMETERS</span></span>

### <span data-ttu-id="867be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867be-114">-DefaultProfile</span></span>
<span data-ttu-id="867be-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="867be-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="867be-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="867be-116">-Name</span></span>
<span data-ttu-id="867be-117">Nazwa obwodu ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="867be-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="867be-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867be-118">-ResourceGroupName</span></span>
<span data-ttu-id="867be-119">Nazwa grupy zasobów zawierającej obwód ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="867be-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="867be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867be-120">CommonParameters</span></span>
<span data-ttu-id="867be-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867be-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="867be-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867be-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="867be-123">INPUTS</span></span>

### <span data-ttu-id="867be-124">System. String</span><span class="sxs-lookup"><span data-stu-id="867be-124">System.String</span></span>

## <span data-ttu-id="867be-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="867be-125">OUTPUTS</span></span>

### <span data-ttu-id="867be-126">Microsoft. Azure. Commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="867be-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="867be-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="867be-127">NOTES</span></span>

## <span data-ttu-id="867be-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="867be-128">RELATED LINKS</span></span>

[<span data-ttu-id="867be-129">Przenieś — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="867be-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="867be-130">Nowe — AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="867be-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="867be-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="867be-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="867be-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="867be-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
