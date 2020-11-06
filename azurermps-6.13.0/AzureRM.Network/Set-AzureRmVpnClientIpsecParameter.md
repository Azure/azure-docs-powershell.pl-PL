---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547443"
---
# <span data-ttu-id="ea8f4-101">Set-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ea8f4-101">Set-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="ea8f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8f4-103">Ustawia parametry protokołu IPsec sieci VPN dla istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea8f4-104">SYNTAX</span></span>

### <span data-ttu-id="ea8f4-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea8f4-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8f4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ea8f4-106">ByFactoryObject</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8f4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea8f4-107">ByResourceId</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8f4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea8f4-108">DESCRIPTION</span></span>
<span data-ttu-id="ea8f4-109">Polecenie cmdlet **Set-AzureRmVpnClientIpsecParameter** ustawia parametry protokołu IPsec sieci VPN dla istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-109">The **Set-AzureRmVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="ea8f4-110">Po utworzeniu bramy sieci wirtualnej ustawia ona zestaw domyślnych zasad IPSec sieci VPN w bramie.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="ea8f4-111">W przypadku wskazywania, że użytkownik witryny chce użyć pewnych niestandardowych zasad IPSec do łączenia się z bramą VPN, użytkownik musi najpierw ustawić zasady IPSec w bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="ea8f4-112">**Set-AzureRmVpnClientIpsecParameter** umożliwia wykonanie tej czynności.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-112">**Set-AzureRmVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="ea8f4-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea8f4-113">EXAMPLES</span></span>

### <span data-ttu-id="ea8f4-114">Przykład 1: ustawia niestandardową zasadę IPSec sieci VPN na istniejącą bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="ea8f4-115">W tym przykładzie ustawiono niestandardowe zasady IPSec sieci VPN do istniejącej bramy sieci wirtualnej o nazwie ContosoVirtualGateway z grupy zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="ea8f4-116">Polecenie cmdlet New-AzureRmVpnClientIpsecParameter służy do tworzenia obiektu parametry IPsec sieci VPN z użyciem wartości przekazanych jeden lub wszystkie parametry, które użytkownik może ustawić dla dowolnej istniejącej bramy sieci wirtualnej w obszarze zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-116">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="ea8f4-117">Ten obiekt VpnClientIPsecParameters został przekazany do polecenia Set-AzureRmVpnClientIpsecParameter w celu ustawienia określonych zasad niestandardowych IPSec VPN w bramie sieci wirtualnej, jak pokazano na przykładzie powyżej.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-117">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="ea8f4-118">To polecenie zwraca obiekt VpnClientIPsecParameters, w którym pokazano parametry Set.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="ea8f4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea8f4-119">PARAMETERS</span></span>

### <span data-ttu-id="ea8f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8f4-120">-DefaultProfile</span></span>
<span data-ttu-id="ea8f4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8f4-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea8f4-122">-InputObject</span></span>
<span data-ttu-id="ea8f4-123">Obiekt wirtualnej sieci Gateaway</span><span class="sxs-lookup"><span data-stu-id="ea8f4-123">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="ea8f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea8f4-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-125">The resource group name.</span></span>

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

### <span data-ttu-id="ea8f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea8f4-126">-ResourceId</span></span>
<span data-ttu-id="ea8f4-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ea8f4-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ea8f4-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ea8f4-129">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="ea8f4-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="ea8f4-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="ea8f4-131">Parametry protokołu IPSec klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="ea8f4-132">Ta wartość parametru może być konstruowana za pomocą polecenia PS Let: New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="ea8f4-132">This parameter value can be constructed using PS command let:New-AzureRmVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8f4-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea8f4-133">-Confirm</span></span>
<span data-ttu-id="ea8f4-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8f4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8f4-135">-WhatIf</span></span>
<span data-ttu-id="ea8f4-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8f4-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8f4-138">CommonParameters</span></span>
<span data-ttu-id="ea8f4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8f4-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8f4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8f4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea8f4-141">INPUTS</span></span>

### <span data-ttu-id="ea8f4-142">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ea8f4-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>
<span data-ttu-id="ea8f4-143">Parametry: VpnClientIPsecParameter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea8f4-143">Parameters: VpnClientIPsecParameter (ByValue)</span></span>

### <span data-ttu-id="ea8f4-144">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea8f4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="ea8f4-145">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea8f4-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ea8f4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8f4-146">System.String</span></span>

## <span data-ttu-id="ea8f4-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea8f4-147">OUTPUTS</span></span>

### <span data-ttu-id="ea8f4-148">Microsoft. Azure. Commands. Network. models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="ea8f4-148">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="ea8f4-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea8f4-149">NOTES</span></span>

## <span data-ttu-id="ea8f4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea8f4-150">RELATED LINKS</span></span>

[<span data-ttu-id="ea8f4-151">Nowe — AzureRmVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="ea8f4-151">New-AzureRmVpnClientIpsecParameters</span></span>](./New-AzureRmVpnClientIpsecParameters.md)
