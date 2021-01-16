---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329140"
---
# <span data-ttu-id="dbfb6-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfb6-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="dbfb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbfb6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfb6-103">Dodaje konfigurację IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="dbfb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbfb6-104">SYNTAX</span></span>

### <span data-ttu-id="dbfb6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbfb6-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbfb6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dbfb6-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbfb6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dbfb6-107">DESCRIPTION</span></span>
<span data-ttu-id="dbfb6-108">Polecenie cmdlet **Add-AzApplicationGatewayIPConfiguration** umożliwia dodanie konfiguracji IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="dbfb6-109">Konfiguracje protokołu IP zawierają podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="dbfb6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbfb6-110">EXAMPLES</span></span>

### <span data-ttu-id="dbfb6-111">Przykład 1: Dodawanie konfiguracji sieci wirtualnej do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="dbfb6-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="dbfb6-112">Pierwsze polecenie uzyskuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="dbfb6-113">Drugie polecenie pobiera podsieć przy użyciu utworzonej wcześniej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="dbfb6-114">Trzecia komenda uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dbfb6-115">Czwarte polecenie dodaje konfigurację adresu IP do bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="dbfb6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbfb6-116">PARAMETERS</span></span>

### <span data-ttu-id="dbfb6-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbfb6-117">-ApplicationGateway</span></span>
<span data-ttu-id="dbfb6-118">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację IP.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbfb6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfb6-119">-DefaultProfile</span></span>
<span data-ttu-id="dbfb6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbfb6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dbfb6-121">-Name</span></span>
<span data-ttu-id="dbfb6-122">Określa nazwę konfiguracji IP, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="dbfb6-123">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="dbfb6-123">-Subnet</span></span>
<span data-ttu-id="dbfb6-124">Określa podsieć.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-124">Specifies a subnet.</span></span>
<span data-ttu-id="dbfb6-125">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="dbfb6-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dbfb6-126">-SubnetId</span></span>
<span data-ttu-id="dbfb6-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="dbfb6-128">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="dbfb6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfb6-129">CommonParameters</span></span>
<span data-ttu-id="dbfb6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfb6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfb6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbfb6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfb6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbfb6-132">INPUTS</span></span>

### <span data-ttu-id="dbfb6-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbfb6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dbfb6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbfb6-134">OUTPUTS</span></span>

### <span data-ttu-id="dbfb6-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbfb6-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dbfb6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbfb6-136">NOTES</span></span>

## <span data-ttu-id="dbfb6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbfb6-137">RELATED LINKS</span></span>

[<span data-ttu-id="dbfb6-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfb6-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dbfb6-139">Nowe — AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfb6-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dbfb6-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfb6-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="dbfb6-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfb6-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


