---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 4020f6aa32a7dda31f97831badf9f7916f3db10f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899222"
---
# <span data-ttu-id="8f02e-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8f02e-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="8f02e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f02e-102">SYNOPSIS</span></span>
<span data-ttu-id="8f02e-103">Usuwa konfigurację podsieci z sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8f02e-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f02e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f02e-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f02e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f02e-105">DESCRIPTION</span></span>
<span data-ttu-id="8f02e-106">Polecenie cmdlet **Remove-AzureRmVirtualNetworkSubnetConfig** usuwa podsieć z sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="8f02e-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="8f02e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f02e-107">EXAMPLES</span></span>

### <span data-ttu-id="8f02e-108">1: usuwanie podsieci z sieci wirtualnej i aktualizowanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8f02e-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="8f02e-109">W tym przykładzie jest tworzona Grupa zasobów i Sieć wirtualna z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="8f02e-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="8f02e-110">Następnie używa polecenia Remove-AzureRmVirtualNetworkSubnetConfig w celu usunięcia podsieci wewnętrznej z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="8f02e-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="8f02e-111">Następnie Set-AzureRmVirtualNetwork jest wywoływana w celu zmodyfikowania sieci wirtualnej po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="8f02e-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="8f02e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f02e-112">PARAMETERS</span></span>

### <span data-ttu-id="8f02e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f02e-113">-DefaultProfile</span></span>
<span data-ttu-id="8f02e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f02e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f02e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f02e-115">-Name</span></span>
<span data-ttu-id="8f02e-116">Określa nazwę konfiguracji podsieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8f02e-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f02e-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f02e-117">-VirtualNetwork</span></span>
<span data-ttu-id="8f02e-118">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8f02e-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f02e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f02e-119">CommonParameters</span></span>
<span data-ttu-id="8f02e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f02e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f02e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f02e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f02e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f02e-122">INPUTS</span></span>

### <span data-ttu-id="8f02e-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f02e-123">PSVirtualNetwork</span></span>
<span data-ttu-id="8f02e-124">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8f02e-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="8f02e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f02e-125">OUTPUTS</span></span>

### <span data-ttu-id="8f02e-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f02e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="8f02e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f02e-127">NOTES</span></span>

## <span data-ttu-id="8f02e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f02e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f02e-129">Dodaj-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8f02e-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8f02e-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8f02e-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8f02e-131">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8f02e-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="8f02e-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8f02e-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


