---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2ce0cb130e6c4d25d4b076d06224364011ced2b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552731"
---
# <span data-ttu-id="f3a94-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a94-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f3a94-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3a94-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a94-103">Dodaje konfigurację IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3a94-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3a94-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3a94-104">SYNTAX</span></span>

### <span data-ttu-id="f3a94-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3a94-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a94-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f3a94-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3a94-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f3a94-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a94-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** umożliwia dodanie konfiguracji IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3a94-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="f3a94-109">Konfiguracje protokołu IP zawierają podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3a94-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="f3a94-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3a94-110">EXAMPLES</span></span>

### <span data-ttu-id="f3a94-111">Przykład 1: Dodawanie konfiguracji sieci wirtualnej do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f3a94-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="f3a94-112">Pierwsze polecenie powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f3a94-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="f3a94-113">Drugie polecenie tworzy podsieć przy użyciu utworzonej wcześniej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f3a94-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="f3a94-114">Trzecia komenda uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f3a94-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f3a94-115">Polecenie Fouth dodaje konfigurację adresu IP do bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f3a94-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f3a94-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3a94-116">PARAMETERS</span></span>

### <span data-ttu-id="f3a94-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3a94-117">-ApplicationGateway</span></span>
<span data-ttu-id="f3a94-118">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację IP.</span><span class="sxs-lookup"><span data-stu-id="f3a94-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="f3a94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a94-119">-DefaultProfile</span></span>
<span data-ttu-id="f3a94-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a94-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3a94-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3a94-121">-Name</span></span>
<span data-ttu-id="f3a94-122">Określa nazwę konfiguracji IP, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="f3a94-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="f3a94-123">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="f3a94-123">-Subnet</span></span>
<span data-ttu-id="f3a94-124">Określa podsieć.</span><span class="sxs-lookup"><span data-stu-id="f3a94-124">Specifies a subnet.</span></span>
<span data-ttu-id="f3a94-125">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3a94-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="f3a94-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f3a94-126">-SubnetId</span></span>
<span data-ttu-id="f3a94-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="f3a94-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="f3a94-128">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3a94-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="f3a94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a94-129">CommonParameters</span></span>
<span data-ttu-id="f3a94-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3a94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a94-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a94-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a94-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3a94-132">INPUTS</span></span>

### <span data-ttu-id="f3a94-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3a94-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f3a94-134">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3a94-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f3a94-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3a94-135">OUTPUTS</span></span>

### <span data-ttu-id="f3a94-136">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3a94-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3a94-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3a94-137">NOTES</span></span>

## <span data-ttu-id="f3a94-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3a94-138">RELATED LINKS</span></span>

[<span data-ttu-id="f3a94-139">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a94-139">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f3a94-140">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a94-140">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f3a94-141">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a94-141">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f3a94-142">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a94-142">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


