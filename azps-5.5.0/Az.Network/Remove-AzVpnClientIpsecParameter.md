---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191698"
---
# <span data-ttu-id="b1179-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="b1179-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="b1179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1179-102">SYNOPSIS</span></span>
<span data-ttu-id="b1179-103">Usuwa niestandardowe zasady ipsec vpn ustawione dla zasobu wirtualnej bramy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="b1179-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="b1179-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b1179-104">SYNTAX</span></span>

### <span data-ttu-id="b1179-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="b1179-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1179-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b1179-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1179-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1179-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1179-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b1179-108">DESCRIPTION</span></span>
<span data-ttu-id="b1179-109">Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b1179-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="b1179-110">Polecenie cmdlet **Remove-AzVpnClientIpsecParameters** usuwa niestandardowe parametry ipsec połączenia vpn ustawione na wirtualnej bramie sieciowej, które z kolei ustawiają domyślne zasady ipsec sieci vpn dla bramy VPN na podstawie przekazanych nazw VirtualNetworkGateway i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1179-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="b1179-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b1179-111">EXAMPLES</span></span>

### <span data-ttu-id="b1179-112">Przykład 1. Usunięcie zestawu parametrów ipsec połączenia vpn ustawionego w bramie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b1179-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b1179-113">Usuwa niestandardowe parametry ipsec sieci vpn ustawione na wirtualnej bramie sieciowej o nazwie "myGateway" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="b1179-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="b1179-114">To polecenie zwraca obiekt bool pokazujący, czy usunięcie zakończyło się pomyślnie, czy nie.</span><span class="sxs-lookup"><span data-stu-id="b1179-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="b1179-115">Uwaga: Spowoduje to ustawienie domyślnych zasad ipsec sieci vpn w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1179-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="b1179-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1179-116">PARAMETERS</span></span>

### <span data-ttu-id="b1179-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1179-117">-DefaultProfile</span></span>
<span data-ttu-id="b1179-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1179-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1179-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1179-119">-InputObject</span></span>
<span data-ttu-id="b1179-120">Obiekt bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b1179-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="b1179-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1179-121">-ResourceGroupName</span></span>
<span data-ttu-id="b1179-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1179-122">The resource group name.</span></span>

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

### <span data-ttu-id="b1179-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1179-123">-ResourceId</span></span>
<span data-ttu-id="b1179-124">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="b1179-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b1179-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="b1179-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="b1179-126">Nazwa bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b1179-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="b1179-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1179-127">-Confirm</span></span>
<span data-ttu-id="b1179-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b1179-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1179-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1179-129">-WhatIf</span></span>
<span data-ttu-id="b1179-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1179-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1179-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b1179-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1179-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1179-132">CommonParameters</span></span>
<span data-ttu-id="b1179-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1179-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1179-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1179-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1179-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1179-135">INPUTS</span></span>

### <span data-ttu-id="b1179-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b1179-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b1179-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b1179-137">System.String</span></span>

## <span data-ttu-id="b1179-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1179-138">OUTPUTS</span></span>

### <span data-ttu-id="b1179-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1179-139">System.Boolean</span></span>

## <span data-ttu-id="b1179-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b1179-140">NOTES</span></span>

## <span data-ttu-id="b1179-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1179-141">RELATED LINKS</span></span>

[<span data-ttu-id="b1179-142">Get-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="b1179-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b1179-143">New-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="b1179-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="b1179-144">Set-AzVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="b1179-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
