---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 5457f330409c760b0e249b99ae5b0d77cf67ffce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709058"
---
# <span data-ttu-id="c21c0-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c21c0-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="c21c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c21c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c21c0-103">Usuwa niestandardową zasadę IPSec VPN ustawioną dla zasobu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c21c0-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="c21c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c21c0-104">SYNTAX</span></span>

### <span data-ttu-id="c21c0-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c21c0-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c21c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c21c0-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c21c0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c21c0-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c21c0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c21c0-108">DESCRIPTION</span></span>
<span data-ttu-id="c21c0-109">Brama sieci wirtualnej to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c21c0-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c21c0-110">Polecenie cmdlet **Remove-AzVpnClientIpsecParameter** usuwa niestandardowe parametry IPsec sieci VPN ustawione na bramie sieci wirtualnej, które z kolei ustawia domyślne zasady IPSec sieci VPN w BRAMie VPN na podstawie przekazana nazwy VirtualNetworkGateway i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c21c0-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="c21c0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c21c0-111">EXAMPLES</span></span>

### <span data-ttu-id="c21c0-112">1: usuwa ustawienia ustaw parametry protokołu IPsec sieci VPN ustawione w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c21c0-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c21c0-113">Usuwa niestandardowe parametry IPsec sieci VPN ustawione dla bramy sieci wirtualnej o nazwie "Moja brama" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="c21c0-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="c21c0-114">To polecenie zwraca obiekt bool wskazujący, że usunięcie się powiodło lub nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="c21c0-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="c21c0-115">Uwaga: spowoduje to ustawienie domyślnych zasad IPSec sieci VPN w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c21c0-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="c21c0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c21c0-116">PARAMETERS</span></span>

### <span data-ttu-id="c21c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21c0-117">-DefaultProfile</span></span>
<span data-ttu-id="c21c0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c21c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c21c0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c21c0-119">-InputObject</span></span>
<span data-ttu-id="c21c0-120">Obiekt wirtualnej sieci Gateaway</span><span class="sxs-lookup"><span data-stu-id="c21c0-120">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="c21c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c21c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="c21c0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c21c0-122">The resource group name.</span></span>

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

### <span data-ttu-id="c21c0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c21c0-123">-ResourceId</span></span>
<span data-ttu-id="c21c0-124">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c21c0-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c21c0-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c21c0-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c21c0-126">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c21c0-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="c21c0-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c21c0-127">-Confirm</span></span>
<span data-ttu-id="c21c0-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c21c0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c21c0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c21c0-129">-WhatIf</span></span>
<span data-ttu-id="c21c0-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c21c0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c21c0-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c21c0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c21c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21c0-132">CommonParameters</span></span>
<span data-ttu-id="c21c0-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21c0-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c21c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21c0-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c21c0-135">INPUTS</span></span>

### <span data-ttu-id="c21c0-136">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c21c0-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="c21c0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c21c0-137">System.String</span></span>

## <span data-ttu-id="c21c0-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c21c0-138">OUTPUTS</span></span>

### <span data-ttu-id="c21c0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c21c0-139">System.Boolean</span></span>

## <span data-ttu-id="c21c0-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c21c0-140">NOTES</span></span>

## <span data-ttu-id="c21c0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c21c0-141">RELATED LINKS</span></span>

[<span data-ttu-id="c21c0-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c21c0-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="c21c0-143">Nowe — AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c21c0-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="c21c0-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c21c0-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
