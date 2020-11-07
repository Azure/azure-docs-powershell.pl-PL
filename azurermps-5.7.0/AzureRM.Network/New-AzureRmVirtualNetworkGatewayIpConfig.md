---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: eba8cd39c621cd2e7b959e54cf20a26ec3434af0
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93719677"
---
# <span data-ttu-id="38059-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="38059-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="38059-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38059-102">SYNOPSIS</span></span>
<span data-ttu-id="38059-103">Tworzy konfigurację IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="38059-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38059-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38059-104">SYNTAX</span></span>

### <span data-ttu-id="38059-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="38059-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38059-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="38059-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38059-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38059-107">DESCRIPTION</span></span>
<span data-ttu-id="38059-108">Polecenie cmdlet **New-AzureRmVirtualNetworkGatewayIpConfig** tworzy konfigurację przypisaną do bramy sieci wirtualnej za pomocą (utworzonego wcześniej) publicznego adresu IP na podstawie identyfikatora podsieci.</span><span class="sxs-lookup"><span data-stu-id="38059-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="38059-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38059-109">EXAMPLES</span></span>

### <span data-ttu-id="38059-110">1: Tworzenie konfiguracji adresów IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="38059-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="38059-111">Konfiguruje wirtualną bramę sieciową z publicznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="38059-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="38059-112">Zmienna $myGWsubnet jest uzyskiwana przy użyciu polecenia cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** na "GatewaySubnet" w sieci wirtualnej, w której zamierzasz utworzyć wirtualną bramę sieciową.</span><span class="sxs-lookup"><span data-stu-id="38059-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="38059-113">Zmienna $myGWpip jest uzyskiwana przy użyciu polecenia cmdlet **New-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="38059-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="38059-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38059-114">PARAMETERS</span></span>

### <span data-ttu-id="38059-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38059-115">-DefaultProfile</span></span>
<span data-ttu-id="38059-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38059-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38059-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38059-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38059-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="38059-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="38059-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="38059-119">-PublicIpAddress</span></span>
```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38059-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="38059-120">-PublicIpAddressId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38059-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="38059-121">-Subnet</span></span>
```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38059-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="38059-122">-SubnetId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38059-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38059-123">CommonParameters</span></span>
<span data-ttu-id="38059-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38059-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38059-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38059-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38059-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38059-126">INPUTS</span></span>

### <span data-ttu-id="38059-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="38059-127">None</span></span>
<span data-ttu-id="38059-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="38059-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38059-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38059-129">OUTPUTS</span></span>

### <span data-ttu-id="38059-130">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="38059-130">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="38059-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38059-131">NOTES</span></span>

## <span data-ttu-id="38059-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38059-132">RELATED LINKS</span></span>

