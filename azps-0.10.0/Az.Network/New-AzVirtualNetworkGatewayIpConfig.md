---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 8def7a737bd3d97cb4250cb9be0a1d7bcc781d50
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890406"
---
# <span data-ttu-id="4547e-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4547e-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="4547e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4547e-102">SYNOPSIS</span></span>
<span data-ttu-id="4547e-103">Tworzy konfigurację IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4547e-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="4547e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4547e-104">SYNTAX</span></span>

### <span data-ttu-id="4547e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4547e-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4547e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4547e-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4547e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4547e-107">DESCRIPTION</span></span>
<span data-ttu-id="4547e-108">Polecenie cmdlet **New-AzVirtualNetworkGatewayIpConfig** tworzy konfigurację przypisaną do bramy sieci wirtualnej za pomocą (utworzonego wcześniej) publicznego adresu IP na podstawie identyfikatora podsieci.</span><span class="sxs-lookup"><span data-stu-id="4547e-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="4547e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4547e-109">EXAMPLES</span></span>

### <span data-ttu-id="4547e-110">1: Tworzenie konfiguracji adresów IP dla bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4547e-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="4547e-111">Konfiguruje wirtualną bramę sieciową z publicznym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="4547e-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="4547e-112">Zmienna $myGWsubnet jest uzyskiwana przy użyciu polecenia cmdlet **Get-AzVirtualNetworkSubnetConfig** na "GatewaySubnet" w sieci wirtualnej, w której zamierzasz utworzyć wirtualną bramę sieciową.</span><span class="sxs-lookup"><span data-stu-id="4547e-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="4547e-113">Zmienna $myGWpip jest uzyskiwana przy użyciu polecenia cmdlet **New-AzPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="4547e-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="4547e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4547e-114">PARAMETERS</span></span>

### <span data-ttu-id="4547e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4547e-115">-DefaultProfile</span></span>
<span data-ttu-id="4547e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4547e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4547e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4547e-117">-Name</span></span>
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

### <span data-ttu-id="4547e-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4547e-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="4547e-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4547e-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="4547e-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4547e-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="4547e-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="4547e-121">-Subnet</span></span>
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

### <span data-ttu-id="4547e-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4547e-122">-SubnetId</span></span>
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

### <span data-ttu-id="4547e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4547e-123">CommonParameters</span></span>
<span data-ttu-id="4547e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4547e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4547e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4547e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4547e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4547e-126">INPUTS</span></span>

## <span data-ttu-id="4547e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4547e-127">OUTPUTS</span></span>

### <span data-ttu-id="4547e-128">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4547e-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="4547e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4547e-129">NOTES</span></span>

## <span data-ttu-id="4547e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4547e-130">RELATED LINKS</span></span>

