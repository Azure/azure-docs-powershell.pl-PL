---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528098"
---
# <span data-ttu-id="909d9-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="909d9-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="909d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="909d9-102">SYNOPSIS</span></span>
<span data-ttu-id="909d9-103">Dodaje konfigurację IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="909d9-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="909d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="909d9-104">SYNTAX</span></span>

### <span data-ttu-id="909d9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="909d9-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="909d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="909d9-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="909d9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="909d9-107">DESCRIPTION</span></span>
<span data-ttu-id="909d9-108">Polecenie cmdlet **Add-AzureRmVirtualNetworkGatewayIpConfig** umożliwia dodanie konfiguracji IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="909d9-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="909d9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="909d9-109">EXAMPLES</span></span>

## <span data-ttu-id="909d9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="909d9-110">PARAMETERS</span></span>

### <span data-ttu-id="909d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909d9-111">-DefaultProfile</span></span>
<span data-ttu-id="909d9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="909d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="909d9-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="909d9-113">-Name</span></span>
<span data-ttu-id="909d9-114">Określa nazwę konfiguracji IP bramy do dodania.</span><span class="sxs-lookup"><span data-stu-id="909d9-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="909d9-115">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="909d9-115">-PrivateIpAddress</span></span>
<span data-ttu-id="909d9-116">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="909d9-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="909d9-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="909d9-117">-PublicIpAddress</span></span>
<span data-ttu-id="909d9-118">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="909d9-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="909d9-119">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="909d9-119">-PublicIpAddressId</span></span>
<span data-ttu-id="909d9-120">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="909d9-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="909d9-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="909d9-121">-Subnet</span></span>
<span data-ttu-id="909d9-122">Określa obiekt **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="909d9-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="909d9-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="909d9-123">-SubnetId</span></span>
<span data-ttu-id="909d9-124">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="909d9-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="909d9-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="909d9-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="909d9-126">Określa obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="909d9-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="909d9-127">To polecenie cmdlet modyfikuje określony obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="909d9-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="909d9-128">Możesz użyć polecenia cmdlet Get-AzureRmVirtualNetworkGateway, aby pobrać obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="909d9-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="909d9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="909d9-129">-Confirm</span></span>
<span data-ttu-id="909d9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="909d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="909d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="909d9-131">-WhatIf</span></span>
<span data-ttu-id="909d9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="909d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="909d9-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="909d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="909d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909d9-134">CommonParameters</span></span>
<span data-ttu-id="909d9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="909d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909d9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="909d9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909d9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="909d9-137">INPUTS</span></span>

### <span data-ttu-id="909d9-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="909d9-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="909d9-139">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="909d9-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="909d9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="909d9-140">OUTPUTS</span></span>

### <span data-ttu-id="909d9-141">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="909d9-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="909d9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="909d9-142">NOTES</span></span>

## <span data-ttu-id="909d9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="909d9-143">RELATED LINKS</span></span>

[<span data-ttu-id="909d9-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="909d9-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="909d9-145">Nowe — AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="909d9-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="909d9-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="909d9-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


