---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 98e2249c3577d49a140d31b4287507e0e46185f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550924"
---
# <span data-ttu-id="4d6be-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d6be-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4d6be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d6be-102">SYNOPSIS</span></span>
<span data-ttu-id="4d6be-103">Dodaje konfigurację IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d6be-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d6be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d6be-104">SYNTAX</span></span>

### <span data-ttu-id="4d6be-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d6be-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d6be-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4d6be-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d6be-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4d6be-107">DESCRIPTION</span></span>
<span data-ttu-id="4d6be-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayIPConfiguration** umożliwia dodanie konfiguracji IP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d6be-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="4d6be-109">Konfiguracje protokołu IP zawierają podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d6be-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="4d6be-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d6be-110">EXAMPLES</span></span>

### <span data-ttu-id="4d6be-111">Przykład 1: Dodawanie konfiguracji sieci wirtualnej do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4d6be-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="4d6be-112">Pierwsze polecenie powoduje utworzenie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d6be-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="4d6be-113">Drugie polecenie tworzy podsieć przy użyciu utworzonej wcześniej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d6be-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="4d6be-114">Trzecia komenda uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d6be-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4d6be-115">Polecenie Fouth dodaje konfigurację adresu IP do bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d6be-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4d6be-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d6be-116">PARAMETERS</span></span>

### <span data-ttu-id="4d6be-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d6be-117">-ApplicationGateway</span></span>
<span data-ttu-id="4d6be-118">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację IP.</span><span class="sxs-lookup"><span data-stu-id="4d6be-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="4d6be-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d6be-119">-Name</span></span>
<span data-ttu-id="4d6be-120">Określa nazwę konfiguracji IP, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="4d6be-120">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="4d6be-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="4d6be-121">-Subnet</span></span>
<span data-ttu-id="4d6be-122">Określa podsieć.</span><span class="sxs-lookup"><span data-stu-id="4d6be-122">Specifies a subnet.</span></span>
<span data-ttu-id="4d6be-123">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d6be-123">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4d6be-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4d6be-124">-SubnetId</span></span>
<span data-ttu-id="4d6be-125">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="4d6be-125">Specifies a subnet ID.</span></span>
<span data-ttu-id="4d6be-126">To jest podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d6be-126">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4d6be-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d6be-127">-DefaultProfile</span></span>
<span data-ttu-id="4d6be-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d6be-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d6be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d6be-129">CommonParameters</span></span>
<span data-ttu-id="4d6be-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d6be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d6be-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d6be-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d6be-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d6be-132">INPUTS</span></span>

### <span data-ttu-id="4d6be-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d6be-133">System.String</span></span>

## <span data-ttu-id="4d6be-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d6be-134">OUTPUTS</span></span>

### <span data-ttu-id="4d6be-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d6be-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d6be-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d6be-136">NOTES</span></span>

## <span data-ttu-id="4d6be-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d6be-137">RELATED LINKS</span></span>

[<span data-ttu-id="4d6be-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d6be-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d6be-139">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d6be-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d6be-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d6be-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4d6be-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d6be-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


