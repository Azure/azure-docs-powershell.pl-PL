---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 61c6a99a100f8d6f2a28dfa40cf8c600c3517b64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709370"
---
# <span data-ttu-id="75c3d-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c3d-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="75c3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="75c3d-103">Umożliwia utworzenie konfiguracji IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c3d-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="75c3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75c3d-104">SYNTAX</span></span>

### <span data-ttu-id="75c3d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="75c3d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75c3d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="75c3d-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75c3d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="75c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="75c3d-108">Polecenie cmdlet **New-AzApplicationGatewayIPConfiguration** umożliwia utworzenie konfiguracji IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c3d-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="75c3d-109">Konfiguracja IP zawiera podsieć, w której wdrożono bramkę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c3d-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="75c3d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="75c3d-111">Przykład 1: Tworzenie konfiguracji adresów IP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c3d-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="75c3d-112">Pierwsze polecenie uzyskuje sieć wirtualną o nazwie VNet01, która należy do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="75c3d-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="75c3d-113">Drugie polecenie pobiera konfigurację podsieci dla podsieci, do której należy Sieć wirtualna w poprzednim poleceniu, i zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="75c3d-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="75c3d-114">W trzecim poleceniu jest tworzona Konfiguracja adresu IP przy użyciu $Subnet.</span><span class="sxs-lookup"><span data-stu-id="75c3d-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="75c3d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75c3d-115">PARAMETERS</span></span>

### <span data-ttu-id="75c3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c3d-116">-DefaultProfile</span></span>
<span data-ttu-id="75c3d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75c3d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c3d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75c3d-118">-Name</span></span>
<span data-ttu-id="75c3d-119">Określa nazwę konfiguracji IP, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="75c3d-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="75c3d-120">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="75c3d-120">-Subnet</span></span>
<span data-ttu-id="75c3d-121">Określa obiekt podsieci.</span><span class="sxs-lookup"><span data-stu-id="75c3d-121">Specifies the subnet object.</span></span>
<span data-ttu-id="75c3d-122">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c3d-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="75c3d-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="75c3d-123">-SubnetId</span></span>
<span data-ttu-id="75c3d-124">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="75c3d-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="75c3d-125">Jest to podsieć, w której zostanie wdrożona Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="75c3d-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="75c3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c3d-126">CommonParameters</span></span>
<span data-ttu-id="75c3d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c3d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c3d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c3d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75c3d-129">INPUTS</span></span>

### <span data-ttu-id="75c3d-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="75c3d-130">None</span></span>

## <span data-ttu-id="75c3d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75c3d-131">OUTPUTS</span></span>

### <span data-ttu-id="75c3d-132">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c3d-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="75c3d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75c3d-133">NOTES</span></span>

## <span data-ttu-id="75c3d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75c3d-134">RELATED LINKS</span></span>

[<span data-ttu-id="75c3d-135">Dodaj-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c3d-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="75c3d-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c3d-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="75c3d-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c3d-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="75c3d-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="75c3d-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

