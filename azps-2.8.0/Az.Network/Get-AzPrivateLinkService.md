---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 9f40d9ce99db8640fcf98d48f8dc3920a8517b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870644"
---
# <span data-ttu-id="f8dfe-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8dfe-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="f8dfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="f8dfe-103">Pobiera usługę link prywatny</span><span class="sxs-lookup"><span data-stu-id="f8dfe-103">Gets private link service</span></span>

## <span data-ttu-id="f8dfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8dfe-104">SYNTAX</span></span>

### <span data-ttu-id="f8dfe-105">NOEXPAND (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f8dfe-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8dfe-106">Większa</span><span class="sxs-lookup"><span data-stu-id="f8dfe-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8dfe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8dfe-107">DESCRIPTION</span></span>
<span data-ttu-id="f8dfe-108">Polecenie cmdlet **Get-AzPrivateLinkService umożliwia pobranie** jednej lub kilku prywatnych usług linków.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="f8dfe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8dfe-109">EXAMPLES</span></span>

### <span data-ttu-id="f8dfe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8dfe-110">Example</span></span>
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

<span data-ttu-id="f8dfe-111">Ta unifiedgroup uzyskuje usługę link prywatny w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="f8dfe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8dfe-112">PARAMETERS</span></span>

### <span data-ttu-id="f8dfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8dfe-113">-DefaultProfile</span></span>
<span data-ttu-id="f8dfe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8dfe-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f8dfe-115">-ExpandResource</span></span>
<span data-ttu-id="f8dfe-116">Odwołanie do zasobu, które ma zostać rozwinięte.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="f8dfe-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8dfe-117">-Name</span></span>
<span data-ttu-id="f8dfe-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-118">The resource name.</span></span>

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

### <span data-ttu-id="f8dfe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8dfe-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8dfe-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-120">The resource group name.</span></span>

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

### <span data-ttu-id="f8dfe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8dfe-121">CommonParameters</span></span>
<span data-ttu-id="f8dfe-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8dfe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8dfe-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8dfe-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8dfe-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8dfe-124">INPUTS</span></span>

### <span data-ttu-id="f8dfe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f8dfe-125">System.String</span></span>

## <span data-ttu-id="f8dfe-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8dfe-126">OUTPUTS</span></span>

### <span data-ttu-id="f8dfe-127">Microsoft. Azure. Commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f8dfe-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f8dfe-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8dfe-128">NOTES</span></span>

## <span data-ttu-id="f8dfe-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8dfe-129">RELATED LINKS</span></span>
