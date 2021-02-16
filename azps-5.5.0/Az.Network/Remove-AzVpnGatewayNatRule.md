---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGatewayNatRule.md
ms.openlocfilehash: 35a59b24297efe3fd94a66d19a778913f488b800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179402"
---
# <span data-ttu-id="632f0-101">Remove-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="632f0-101">Remove-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="632f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="632f0-102">SYNOPSIS</span></span>
<span data-ttu-id="632f0-103">Usuwa regułę NAT skojarzoną z siecią VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="632f0-103">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="632f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="632f0-104">SYNTAX</span></span>

### <span data-ttu-id="632f0-105">ByVpnGatewayNatRuleName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="632f0-105">ByVpnGatewayNatRuleName (Default)</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="632f0-106">ByVpnGatewayNatRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="632f0-106">ByVpnGatewayNatRuleResourceId</span></span>
```
Remove-AzVpnGatewayNatRule -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="632f0-107">ByVpnGatewayNatRuleObject</span><span class="sxs-lookup"><span data-stu-id="632f0-107">ByVpnGatewayNatRuleObject</span></span>
```
Remove-AzVpnGatewayNatRule -InputObject <PSVpnGatewayNatRule> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="632f0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="632f0-108">DESCRIPTION</span></span>
<span data-ttu-id="632f0-109">Usuwa regułę NAT skojarzoną z siecią VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="632f0-109">Removes a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="632f0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="632f0-110">EXAMPLES</span></span>

### <span data-ttu-id="632f0-111">Przykład1</span><span class="sxs-lookup"><span data-stu-id="632f0-111">Example1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Remove-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"
```

<span data-ttu-id="632f0-112">Powyższe spowoduje utworzenie grupy zasobów, wirtualnej sieci WAN, sieci wirtualnej, centrum wirtualnego, vpnGateway i reguły NAT skojarzonej z tą bramą VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="632f0-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub,VpnGateway and NAT rule associated with that VpnGateway.</span></span>
<span data-ttu-id="632f0-113">Następnie usuwa regułę NAT przy użyciu nazwy reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="632f0-113">Then it removes the NAT rule using the NAT rule name.</span></span>


## <span data-ttu-id="632f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="632f0-114">PARAMETERS</span></span>

### <span data-ttu-id="632f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632f0-115">-DefaultProfile</span></span>
<span data-ttu-id="632f0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="632f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="632f0-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="632f0-117">-Force</span></span>
<span data-ttu-id="632f0-118">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="632f0-118">Do not ask for confirmation if you want to delete a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="632f0-119">-InputObject</span></span>
<span data-ttu-id="632f0-120">Obiekt VpnGatewayNatRule do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="632f0-120">The VpnGatewayNatRule object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule
Parameter Sets: ByVpnGatewayNatRuleObject
Aliases: VpnGatewayNatRule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="632f0-121">-Name</span></span>
<span data-ttu-id="632f0-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="632f0-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ResourceName, VpnGatewayNatRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="632f0-123">-ParentResourceName</span></span>
<span data-ttu-id="632f0-124">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="632f0-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="632f0-125">-PassThru</span></span>
<span data-ttu-id="632f0-126">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="632f0-126">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="632f0-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="632f0-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="632f0-129">-ResourceId</span></span>
<span data-ttu-id="632f0-130">Identyfikator zasobu obiektu VpnGatewayNatRule do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="632f0-130">The resource id of the VpnGatewayNatRule object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNatRuleResourceId
Aliases: VpnGatewayNatRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="632f0-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="632f0-131">-Confirm</span></span>
<span data-ttu-id="632f0-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="632f0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="632f0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="632f0-133">-WhatIf</span></span>
<span data-ttu-id="632f0-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="632f0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="632f0-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="632f0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="632f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632f0-136">CommonParameters</span></span>
<span data-ttu-id="632f0-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632f0-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="632f0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632f0-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="632f0-139">INPUTS</span></span>

### <span data-ttu-id="632f0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="632f0-140">System.String</span></span>

### <span data-ttu-id="632f0-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="632f0-141">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="632f0-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="632f0-142">OUTPUTS</span></span>

### <span data-ttu-id="632f0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="632f0-143">System.Boolean</span></span>

## <span data-ttu-id="632f0-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="632f0-144">NOTES</span></span>

## <span data-ttu-id="632f0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="632f0-145">RELATED LINKS</span></span>
