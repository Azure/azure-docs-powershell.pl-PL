---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899309"
---
# <span data-ttu-id="c4078-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4078-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="c4078-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4078-102">SYNOPSIS</span></span>
<span data-ttu-id="c4078-103">Dodaje konfigurację IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4078-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4078-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4078-104">SYNTAX</span></span>

### <span data-ttu-id="c4078-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4078-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4078-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c4078-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4078-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c4078-107">DESCRIPTION</span></span>
<span data-ttu-id="c4078-108">Polecenie cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** umożliwia dodanie konfiguracji IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4078-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="c4078-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4078-109">EXAMPLES</span></span>

### <span data-ttu-id="c4078-110">1:1</span><span class="sxs-lookup"><span data-stu-id="c4078-110">1:</span></span>
```

```

## <span data-ttu-id="c4078-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4078-111">PARAMETERS</span></span>

### <span data-ttu-id="c4078-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4078-112">-DefaultProfile</span></span>
<span data-ttu-id="c4078-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4078-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4078-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4078-114">-Name</span></span>
<span data-ttu-id="c4078-115">Określa nazwę konfiguracji IP bramy do dodania.</span><span class="sxs-lookup"><span data-stu-id="c4078-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="c4078-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4078-116">-PrivateIpAddress</span></span>
<span data-ttu-id="c4078-117">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="c4078-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="c4078-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4078-118">-PublicIpAddress</span></span>
<span data-ttu-id="c4078-119">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="c4078-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="c4078-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c4078-120">-PublicIpAddressId</span></span>
<span data-ttu-id="c4078-121">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c4078-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="c4078-122">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="c4078-122">-Subnet</span></span>
<span data-ttu-id="c4078-123">Określa obiekt **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="c4078-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="c4078-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c4078-124">-SubnetId</span></span>
<span data-ttu-id="c4078-125">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="c4078-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="c4078-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4078-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c4078-127">Określa obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c4078-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="c4078-128">To polecenie cmdlet modyfikuje określony obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c4078-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="c4078-129">Możesz użyć polecenia cmdlet Get-AzureRmVirtualNetworkGateway, aby pobrać obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="c4078-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4078-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4078-130">-Confirm</span></span>
<span data-ttu-id="c4078-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4078-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4078-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4078-132">-WhatIf</span></span>
<span data-ttu-id="c4078-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4078-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4078-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4078-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4078-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4078-135">CommonParameters</span></span>
<span data-ttu-id="c4078-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4078-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4078-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4078-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4078-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4078-138">INPUTS</span></span>

### <span data-ttu-id="c4078-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4078-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c4078-140">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c4078-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c4078-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4078-141">OUTPUTS</span></span>

### <span data-ttu-id="c4078-142">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4078-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c4078-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4078-143">NOTES</span></span>

## <span data-ttu-id="c4078-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4078-144">RELATED LINKS</span></span>

[<span data-ttu-id="c4078-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4078-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c4078-146">Nowe — AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4078-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="c4078-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4078-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


