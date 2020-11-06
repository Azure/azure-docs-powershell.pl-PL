---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 08dc5728e13423fdd9e05c5d5b5d843b963c4aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550904"
---
# <span data-ttu-id="5d6a8-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d6a8-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="5d6a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6a8-103">Dodaje konfigurację IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d6a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d6a8-104">SYNTAX</span></span>

### <span data-ttu-id="5d6a8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d6a8-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d6a8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5d6a8-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d6a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d6a8-107">DESCRIPTION</span></span>
<span data-ttu-id="5d6a8-108">Polecenie cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** umożliwia dodanie konfiguracji IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="5d6a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d6a8-109">EXAMPLES</span></span>

## <span data-ttu-id="5d6a8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d6a8-110">PARAMETERS</span></span>

### <span data-ttu-id="5d6a8-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d6a8-111">-Name</span></span>
<span data-ttu-id="5d6a8-112">Określa nazwę konfiguracji IP bramy do dodania.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-112">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="5d6a8-113">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d6a8-113">-PrivateIpAddress</span></span>
<span data-ttu-id="5d6a8-114">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-114">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a8-115">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5d6a8-115">-PublicIpAddress</span></span>
<span data-ttu-id="5d6a8-116">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-116">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a8-117">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5d6a8-117">-PublicIpAddressId</span></span>
<span data-ttu-id="5d6a8-118">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-118">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="5d6a8-119">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="5d6a8-119">-Subnet</span></span>
<span data-ttu-id="5d6a8-120">Określa obiekt **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="5d6a8-120">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="5d6a8-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5d6a8-121">-SubnetId</span></span>
<span data-ttu-id="5d6a8-122">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-122">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="5d6a8-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5d6a8-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5d6a8-124">Określa obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="5d6a8-124">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="5d6a8-125">To polecenie cmdlet modyfikuje określony obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="5d6a8-125">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="5d6a8-126">Możesz użyć polecenia cmdlet Get-AzureRmVirtualNetworkGateway, aby pobrać obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="5d6a8-126">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d6a8-127">-Confirm</span></span>
<span data-ttu-id="5d6a8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d6a8-129">-WhatIf</span></span>
<span data-ttu-id="5d6a8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d6a8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6a8-132">-DefaultProfile</span></span>
<span data-ttu-id="5d6a8-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d6a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6a8-134">CommonParameters</span></span>
<span data-ttu-id="5d6a8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6a8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d6a8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6a8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d6a8-137">INPUTS</span></span>

### <span data-ttu-id="5d6a8-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5d6a8-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="5d6a8-139">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5d6a8-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="5d6a8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d6a8-140">OUTPUTS</span></span>

### <span data-ttu-id="5d6a8-141">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5d6a8-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5d6a8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d6a8-142">NOTES</span></span>

## <span data-ttu-id="5d6a8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d6a8-143">RELATED LINKS</span></span>

[<span data-ttu-id="5d6a8-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5d6a8-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5d6a8-145">Nowe — AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d6a8-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="5d6a8-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="5d6a8-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


