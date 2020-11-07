---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 17938a8fe4ee5a279554758cc36cc7a234a359ce
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898908"
---
# <span data-ttu-id="03bfa-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bfa-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="03bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="03bfa-103">Dodaje konfigurację IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03bfa-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03bfa-104">SYNTAX</span></span>

### <span data-ttu-id="03bfa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03bfa-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03bfa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="03bfa-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03bfa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03bfa-107">DESCRIPTION</span></span>
<span data-ttu-id="03bfa-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** umożliwia dodanie konfiguracji IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03bfa-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="03bfa-109">Konfiguracje protokołu IP zawierają podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03bfa-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="03bfa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03bfa-110">EXAMPLES</span></span>

### <span data-ttu-id="03bfa-111">Przykład 1: Dodawanie konfiguracji sieci wirtualnej do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="03bfa-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="03bfa-112">Pierwsze polecenie powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03bfa-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="03bfa-113">Drugie polecenie tworzy podsieć przy użyciu utworzonej wcześniej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03bfa-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="03bfa-114">Trzecia komenda uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="03bfa-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="03bfa-115">Polecenie Fouth dodaje konfigurację adresu IP do bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="03bfa-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="03bfa-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03bfa-116">PARAMETERS</span></span>

### <span data-ttu-id="03bfa-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03bfa-117">-ApplicationGateway</span></span>
<span data-ttu-id="03bfa-118">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację IP.</span><span class="sxs-lookup"><span data-stu-id="03bfa-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03bfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bfa-119">-DefaultProfile</span></span>
<span data-ttu-id="03bfa-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03bfa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bfa-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03bfa-121">-Name</span></span>
<span data-ttu-id="03bfa-122">Określa nazwę konfiguracji IP, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="03bfa-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="03bfa-123">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="03bfa-123">-Subnet</span></span>
<span data-ttu-id="03bfa-124">Określa podsieć.</span><span class="sxs-lookup"><span data-stu-id="03bfa-124">Specifies a subnet.</span></span>
<span data-ttu-id="03bfa-125">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03bfa-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="03bfa-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="03bfa-126">-SubnetId</span></span>
<span data-ttu-id="03bfa-127">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="03bfa-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="03bfa-128">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03bfa-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="03bfa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bfa-129">CommonParameters</span></span>
<span data-ttu-id="03bfa-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bfa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bfa-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bfa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bfa-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03bfa-132">INPUTS</span></span>

### <span data-ttu-id="03bfa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="03bfa-133">System.String</span></span>

## <span data-ttu-id="03bfa-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03bfa-134">OUTPUTS</span></span>

### <span data-ttu-id="03bfa-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03bfa-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="03bfa-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03bfa-136">NOTES</span></span>

## <span data-ttu-id="03bfa-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03bfa-137">RELATED LINKS</span></span>

[<span data-ttu-id="03bfa-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bfa-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="03bfa-139">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bfa-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="03bfa-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bfa-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="03bfa-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="03bfa-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


