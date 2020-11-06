---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e06d91fe55d8288b4f123202e2e32d90c51af3eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549367"
---
# <span data-ttu-id="8f3d1-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d1-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8f3d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3d1-103">Umożliwia utworzenie konfiguracji IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f3d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f3d1-104">SYNTAX</span></span>

### <span data-ttu-id="8f3d1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3d1-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f3d1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8f3d1-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f3d1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8f3d1-107">DESCRIPTION</span></span>
<span data-ttu-id="8f3d1-108">Polecenie cmdlet **New-AzureRmApplicationGatewayIPConfiguration** umożliwia utworzenie konfiguracji IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="8f3d1-109">Konfiguracja IP zawiera podsieć, w której wdrożono bramkę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="8f3d1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f3d1-110">EXAMPLES</span></span>

### <span data-ttu-id="8f3d1-111">Przykład 1: Tworzenie konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="8f3d1-112">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="8f3d1-113">Drugie polecenie pobiera konfigurację podsieci dla podsieci, do której należy Sieć wirtualna w poprzednim poleceniu, i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="8f3d1-114">W trzecim poleceniu jest tworzona Konfiguracja adresu IP przy użyciu $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="8f3d1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f3d1-115">PARAMETERS</span></span>

### <span data-ttu-id="8f3d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3d1-116">-DefaultProfile</span></span>
<span data-ttu-id="8f3d1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f3d1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f3d1-118">-Name</span></span>
<span data-ttu-id="8f3d1-119">Określa nazwę konfiguracji IP, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-119">Specifies the name of the IP configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3d1-120">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="8f3d1-120">-Subnet</span></span>
<span data-ttu-id="8f3d1-121">Określa obiekt podsieci.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-121">Specifies the subnet object.</span></span>
<span data-ttu-id="8f3d1-122">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3d1-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8f3d1-123">-SubnetId</span></span>
<span data-ttu-id="8f3d1-124">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="8f3d1-125">Jest to podsieć, w której zostanie wdrożona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3d1-126">CommonParameters</span></span>
<span data-ttu-id="8f3d1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f3d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3d1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f3d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3d1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f3d1-129">INPUTS</span></span>

### <span data-ttu-id="8f3d1-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8f3d1-130">None</span></span>

## <span data-ttu-id="8f3d1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f3d1-131">OUTPUTS</span></span>

### <span data-ttu-id="8f3d1-132">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d1-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8f3d1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f3d1-133">NOTES</span></span>

## <span data-ttu-id="8f3d1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f3d1-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f3d1-135">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d1-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f3d1-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d1-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f3d1-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d1-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8f3d1-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d1-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


