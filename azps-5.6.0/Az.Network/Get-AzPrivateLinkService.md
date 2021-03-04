---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 8b2e8902257566256ed41c38c90c31cb430d12d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954161"
---
# <span data-ttu-id="58acc-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="58acc-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="58acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58acc-102">SYNOPSIS</span></span>
<span data-ttu-id="58acc-103">Pobiera prywatną usługę linków</span><span class="sxs-lookup"><span data-stu-id="58acc-103">Gets private link service</span></span>

## <span data-ttu-id="58acc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58acc-104">SYNTAX</span></span>

### <span data-ttu-id="58acc-105">NoExpand (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="58acc-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58acc-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="58acc-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58acc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="58acc-107">DESCRIPTION</span></span>
<span data-ttu-id="58acc-108">Polecenie **cmdlet Get-AzPrivateLinkService** pobiera co najmniej jedną prywatną usługę linków.</span><span class="sxs-lookup"><span data-stu-id="58acc-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="58acc-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58acc-109">EXAMPLES</span></span>

### <span data-ttu-id="58acc-110">Przykład</span><span class="sxs-lookup"><span data-stu-id="58acc-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="58acc-111">To polecenie commandlet pobiera prywatną usługę linków w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="58acc-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="58acc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58acc-112">PARAMETERS</span></span>

### <span data-ttu-id="58acc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58acc-113">-DefaultProfile</span></span>
<span data-ttu-id="58acc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58acc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58acc-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="58acc-115">-ExpandResource</span></span>
<span data-ttu-id="58acc-116">Odwołanie do zasobu do rozwinięcia.</span><span class="sxs-lookup"><span data-stu-id="58acc-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58acc-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="58acc-117">-Name</span></span>
<span data-ttu-id="58acc-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="58acc-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58acc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58acc-119">-ResourceGroupName</span></span>
<span data-ttu-id="58acc-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58acc-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58acc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58acc-121">CommonParameters</span></span>
<span data-ttu-id="58acc-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58acc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58acc-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58acc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58acc-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58acc-124">INPUTS</span></span>

### <span data-ttu-id="58acc-125">System.String</span><span class="sxs-lookup"><span data-stu-id="58acc-125">System.String</span></span>

## <span data-ttu-id="58acc-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58acc-126">OUTPUTS</span></span>

### <span data-ttu-id="58acc-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="58acc-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="58acc-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58acc-128">NOTES</span></span>

## <span data-ttu-id="58acc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58acc-129">RELATED LINKS</span></span>
