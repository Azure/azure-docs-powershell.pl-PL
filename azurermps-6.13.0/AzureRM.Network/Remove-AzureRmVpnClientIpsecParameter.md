---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543604"
---
# <span data-ttu-id="e7035-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="e7035-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="e7035-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7035-102">SYNOPSIS</span></span>
<span data-ttu-id="e7035-103">Usuwa niestandardową zasadę IPSec VPN ustawioną dla zasobu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7035-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7035-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7035-104">SYNTAX</span></span>

### <span data-ttu-id="e7035-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7035-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7035-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e7035-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7035-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7035-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7035-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e7035-108">DESCRIPTION</span></span>
<span data-ttu-id="e7035-109">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e7035-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="e7035-110">Polecenie cmdlet **Remove-AzureRmVpnClientIpsecParameter** usuwa niestandardowe parametry IPsec sieci VPN ustawione na bramie sieci wirtualnej, które z kolei ustawia domyślne zasady IPSec sieci VPN w BRAMie VPN na podstawie przekazana nazwy VirtualNetworkGateway i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7035-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="e7035-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7035-111">EXAMPLES</span></span>

### <span data-ttu-id="e7035-112">1: usuwa ustawienia ustaw parametry protokołu IPsec sieci VPN ustawione w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7035-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="e7035-113">Usuwa niestandardowe parametry IPsec sieci VPN ustawione dla bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e7035-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="e7035-114">To polecenie zwraca obiekt bool wskazujący, że usunięcie się powiodło lub nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e7035-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="e7035-115">Uwaga: spowoduje to ustawienie domyślnych zasad IPSec sieci VPN w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7035-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="e7035-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7035-116">PARAMETERS</span></span>

### <span data-ttu-id="e7035-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7035-117">-DefaultProfile</span></span>
<span data-ttu-id="e7035-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7035-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7035-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e7035-119">-InputObject</span></span>
<span data-ttu-id="e7035-120">Obiekt wirtualnej sieci Gateaway</span><span class="sxs-lookup"><span data-stu-id="e7035-120">The virtual network gateaway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7035-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7035-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7035-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7035-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7035-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7035-123">-ResourceId</span></span>
<span data-ttu-id="e7035-124">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e7035-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7035-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e7035-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e7035-126">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7035-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7035-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7035-127">-Confirm</span></span>
<span data-ttu-id="e7035-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7035-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7035-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7035-129">-WhatIf</span></span>
<span data-ttu-id="e7035-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7035-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7035-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7035-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7035-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7035-132">CommonParameters</span></span>
<span data-ttu-id="e7035-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7035-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7035-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7035-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7035-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7035-135">INPUTS</span></span>

### <span data-ttu-id="e7035-136">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e7035-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="e7035-137">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7035-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e7035-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e7035-138">System.String</span></span>

## <span data-ttu-id="e7035-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7035-139">OUTPUTS</span></span>

### <span data-ttu-id="e7035-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7035-140">System.Boolean</span></span>

## <span data-ttu-id="e7035-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7035-141">NOTES</span></span>

## <span data-ttu-id="e7035-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7035-142">RELATED LINKS</span></span>
