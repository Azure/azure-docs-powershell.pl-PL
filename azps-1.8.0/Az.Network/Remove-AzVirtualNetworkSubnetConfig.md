---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 92550eb08fb6abf704d450f323e3fd0b724d9942
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709062"
---
# <span data-ttu-id="579ea-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="579ea-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="579ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="579ea-102">SYNOPSIS</span></span>
<span data-ttu-id="579ea-103">Usuwa konfigurację podsieci z sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="579ea-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="579ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="579ea-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="579ea-105">DESCRIPTION</span></span>
<span data-ttu-id="579ea-106">Polecenie cmdlet **Remove-AzVirtualNetworkSubnetConfig** usuwa podsieć z sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="579ea-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="579ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="579ea-107">EXAMPLES</span></span>

### <span data-ttu-id="579ea-108">1: usuwanie podsieci z sieci wirtualnej i aktualizowanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="579ea-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="579ea-109">W tym przykładzie jest tworzona Grupa zasobów i Sieć wirtualna z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="579ea-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="579ea-110">Następnie używa polecenia Remove-AzVirtualNetworkSubnetConfig w celu usunięcia podsieci wewnętrznej z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="579ea-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="579ea-111">Następnie Set-AzVirtualNetwork jest wywoływana w celu zmodyfikowania sieci wirtualnej po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="579ea-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="579ea-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="579ea-112">PARAMETERS</span></span>

### <span data-ttu-id="579ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579ea-113">-DefaultProfile</span></span>
<span data-ttu-id="579ea-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="579ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579ea-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="579ea-115">-Name</span></span>
<span data-ttu-id="579ea-116">Określa nazwę konfiguracji podsieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="579ea-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="579ea-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="579ea-117">-VirtualNetwork</span></span>
<span data-ttu-id="579ea-118">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="579ea-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="579ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579ea-119">CommonParameters</span></span>
<span data-ttu-id="579ea-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579ea-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="579ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579ea-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="579ea-122">INPUTS</span></span>

### <span data-ttu-id="579ea-123">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="579ea-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="579ea-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="579ea-124">OUTPUTS</span></span>

### <span data-ttu-id="579ea-125">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="579ea-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="579ea-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="579ea-126">NOTES</span></span>

## <span data-ttu-id="579ea-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="579ea-127">RELATED LINKS</span></span>

[<span data-ttu-id="579ea-128">Dodaj-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="579ea-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="579ea-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="579ea-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="579ea-130">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="579ea-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="579ea-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="579ea-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)

