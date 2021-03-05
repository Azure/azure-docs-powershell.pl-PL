---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 961edb46c71b60f0c3c43523d8d88486f1414d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006401"
---
# <span data-ttu-id="f0d3d-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0d3d-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f0d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d3d-103">Pobiera lokalną bramę sieciową</span><span class="sxs-lookup"><span data-stu-id="f0d3d-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="f0d3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0d3d-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d3d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d3d-106">Lokalna brama sieciowa to obiekt reprezentujący lokalne urządzenie sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="f0d3d-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f0d3d-107">Polecenie **cmdlet Get-AzLocalNetworkGateway** zwraca obiekt reprezentujący wejściową bramę na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0d3d-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f0d3d-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0d3d-108">EXAMPLES</span></span>

### <span data-ttu-id="f0d3d-109">Przykład 1. Uzyskiwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="f0d3d-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="f0d3d-110">Zwraca obiekt lokalnej bramy sieciowej o nazwie "myLocalGW1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="f0d3d-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="f0d3d-111">Przykład 2. Uzyskiwanie lokalnych bram sieciowych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="f0d3d-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="f0d3d-112">Zwraca obiekt lokalnej bramy sieciowej o nazwie zaczynającej się od ciągu "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="f0d3d-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="f0d3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0d3d-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d3d-114">-DefaultProfile</span></span>
<span data-ttu-id="f0d3d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d3d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d3d-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f0d3d-116">-Name</span></span>
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

### <span data-ttu-id="f0d3d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d3d-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f0d3d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d3d-118">CommonParameters</span></span>
<span data-ttu-id="f0d3d-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d3d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d3d-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0d3d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d3d-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0d3d-121">INPUTS</span></span>

### <span data-ttu-id="f0d3d-122">System.String</span><span class="sxs-lookup"><span data-stu-id="f0d3d-122">System.String</span></span>

## <span data-ttu-id="f0d3d-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0d3d-123">OUTPUTS</span></span>

### <span data-ttu-id="f0d3d-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0d3d-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f0d3d-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0d3d-125">NOTES</span></span>

## <span data-ttu-id="f0d3d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0d3d-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0d3d-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0d3d-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="f0d3d-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0d3d-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="f0d3d-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f0d3d-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
