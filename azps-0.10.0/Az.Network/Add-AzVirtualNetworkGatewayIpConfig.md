---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890950"
---
# <span data-ttu-id="2a109-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a109-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="2a109-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a109-102">SYNOPSIS</span></span>
<span data-ttu-id="2a109-103">Dodaje konfigurację IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a109-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="2a109-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a109-104">SYNTAX</span></span>

### <span data-ttu-id="2a109-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a109-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a109-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2a109-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a109-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a109-107">DESCRIPTION</span></span>
<span data-ttu-id="2a109-108">Polecenie cmdlet **Add-AzVirtualNetworkGatewayIpConfig** umożliwia dodanie konfiguracji IP do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a109-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="2a109-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a109-109">EXAMPLES</span></span>

### <span data-ttu-id="2a109-110">1:1</span><span class="sxs-lookup"><span data-stu-id="2a109-110">1:</span></span>
```

```

## <span data-ttu-id="2a109-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a109-111">PARAMETERS</span></span>

### <span data-ttu-id="2a109-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a109-112">-DefaultProfile</span></span>
<span data-ttu-id="2a109-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a109-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a109-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a109-114">-Name</span></span>
<span data-ttu-id="2a109-115">Określa nazwę konfiguracji IP bramy do dodania.</span><span class="sxs-lookup"><span data-stu-id="2a109-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="2a109-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a109-116">-PrivateIpAddress</span></span>
<span data-ttu-id="2a109-117">Określa prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a109-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="2a109-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a109-118">-PublicIpAddress</span></span>
<span data-ttu-id="2a109-119">Określa publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="2a109-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="2a109-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2a109-120">-PublicIpAddressId</span></span>
<span data-ttu-id="2a109-121">Określa identyfikator publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="2a109-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="2a109-122">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="2a109-122">-Subnet</span></span>
<span data-ttu-id="2a109-123">Określa obiekt **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="2a109-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="2a109-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2a109-124">-SubnetId</span></span>
<span data-ttu-id="2a109-125">Określa identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="2a109-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="2a109-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a109-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2a109-127">Określa obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2a109-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="2a109-128">To polecenie cmdlet modyfikuje określony obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2a109-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="2a109-129">Możesz użyć polecenia cmdlet Get-AzVirtualNetworkGateway, aby pobrać obiekt **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2a109-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="2a109-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a109-130">-Confirm</span></span>
<span data-ttu-id="2a109-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a109-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a109-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a109-132">-WhatIf</span></span>
<span data-ttu-id="2a109-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a109-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a109-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a109-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a109-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a109-135">CommonParameters</span></span>
<span data-ttu-id="2a109-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a109-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a109-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a109-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a109-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a109-138">INPUTS</span></span>

### <span data-ttu-id="2a109-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a109-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="2a109-140">Parametr "VirtualNetworkGateway" akceptuje wartość typu "PSVirtualNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2a109-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="2a109-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a109-141">OUTPUTS</span></span>

### <span data-ttu-id="2a109-142">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a109-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2a109-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a109-143">NOTES</span></span>

## <span data-ttu-id="2a109-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a109-144">RELATED LINKS</span></span>

[<span data-ttu-id="2a109-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a109-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2a109-146">Nowe — AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a109-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="2a109-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a109-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


