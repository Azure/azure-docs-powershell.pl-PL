---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356134"
---
# <span data-ttu-id="e4271-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4271-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="e4271-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4271-102">SYNOPSIS</span></span>
<span data-ttu-id="e4271-103">Pobiera bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="e4271-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="e4271-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4271-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4271-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4271-105">DESCRIPTION</span></span>
<span data-ttu-id="e4271-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="e4271-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="e4271-107">Polecenie cmdlet **Get-AzLocalNetworkGateway** zwraca obiekt reprezentujący bramę on-środowisku na podstawie nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4271-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="e4271-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4271-108">EXAMPLES</span></span>

### <span data-ttu-id="e4271-109">Przykład 1: uzyskiwanie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="e4271-109">Example 1: Get a Local Network Gateway</span></span>
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

<span data-ttu-id="e4271-110">Zwraca obiekt bramy sieci lokalnej o nazwie "myLocalGW1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e4271-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="e4271-111">Przykład 2: uzyskiwanie lokalnych bram sieciowych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="e4271-111">Example 2: Get Local Network Gateways using filtering</span></span>
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

<span data-ttu-id="e4271-112">Zwraca obiekt bramy sieci lokalnej o nazwie rozpoczynającej się od ciągu "myLocalGW" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e4271-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="e4271-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4271-113">PARAMETERS</span></span>

### <span data-ttu-id="e4271-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4271-114">-DefaultProfile</span></span>
<span data-ttu-id="e4271-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4271-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4271-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4271-116">-Name</span></span>
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

### <span data-ttu-id="e4271-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4271-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e4271-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4271-118">CommonParameters</span></span>
<span data-ttu-id="e4271-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4271-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4271-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4271-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4271-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4271-121">INPUTS</span></span>

### <span data-ttu-id="e4271-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e4271-122">System.String</span></span>

## <span data-ttu-id="e4271-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4271-123">OUTPUTS</span></span>

### <span data-ttu-id="e4271-124">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4271-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e4271-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4271-125">NOTES</span></span>

## <span data-ttu-id="e4271-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4271-126">RELATED LINKS</span></span>

[<span data-ttu-id="e4271-127">Nowe — AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4271-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="e4271-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4271-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="e4271-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e4271-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
