---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202234"
---
# <span data-ttu-id="84843-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="84843-101">Update-AzPeering</span></span>

## <span data-ttu-id="84843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84843-102">SYNOPSIS</span></span>
<span data-ttu-id="84843-103">Ustawia komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="84843-103">Sets the Peering.</span></span> <span data-ttu-id="84843-104">Użyj tego polecenia w połączeniu z `Set-AzDirectPeeringConnectionObject` `Set-AzExchangePeeringConnectionObject` lub.</span><span class="sxs-lookup"><span data-stu-id="84843-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="84843-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84843-105">SYNTAX</span></span>

### <span data-ttu-id="84843-106">DefaultExchange (Default)</span><span class="sxs-lookup"><span data-stu-id="84843-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84843-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="84843-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84843-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="84843-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84843-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="84843-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84843-110">Direct</span><span class="sxs-lookup"><span data-stu-id="84843-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84843-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="84843-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84843-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="84843-112">DESCRIPTION</span></span>
<span data-ttu-id="84843-113">Ustawia obiekt PSPeering</span><span class="sxs-lookup"><span data-stu-id="84843-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="84843-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84843-114">EXAMPLES</span></span>

### <span data-ttu-id="84843-115">Aktualizowanie klucza uwierzytelniania Md5</span><span class="sxs-lookup"><span data-stu-id="84843-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="84843-116">Ustawia klucz uwierzytelniania Md5</span><span class="sxs-lookup"><span data-stu-id="84843-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="84843-117">Update UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="84843-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="84843-118">Ustawianie flagi usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="84843-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="84843-119">Aktualizowanie adresu IPv4 dla komunikacji równorzędnej programu Exchange</span><span class="sxs-lookup"><span data-stu-id="84843-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="84843-120">Ustawia adres Ipv4 dla komunikacji równorzędnej programu Exchange przy użyciu usługi ResourceId</span><span class="sxs-lookup"><span data-stu-id="84843-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="84843-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84843-121">PARAMETERS</span></span>

### <span data-ttu-id="84843-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84843-122">-DefaultProfile</span></span>
<span data-ttu-id="84843-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84843-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84843-124">- DirectConnection</span><span class="sxs-lookup"><span data-stu-id="84843-124">-DirectConnection</span></span>
<span data-ttu-id="84843-125">Utwórz nowe połączenia bezpośrednie, używając New-AzDirectPeeringConnectionObject i potoku do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="84843-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84843-126">- ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="84843-126">-ExchangeConnection</span></span>
<span data-ttu-id="84843-127">Utwórz nowe połączenie programu Exchange, używając New-AzExchangePeeringConnectionObject i potoku do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="84843-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84843-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84843-128">-InputObject</span></span>
<span data-ttu-id="84843-129">Obiekt komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="84843-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84843-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="84843-130">-Name</span></span>
<span data-ttu-id="84843-131">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="84843-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84843-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84843-132">-ResourceGroupName</span></span>
<span data-ttu-id="84843-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84843-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84843-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84843-134">-ResourceId</span></span>
<span data-ttu-id="84843-135">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="84843-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84843-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84843-136">-Confirm</span></span>
<span data-ttu-id="84843-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84843-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84843-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84843-138">-WhatIf</span></span>
<span data-ttu-id="84843-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84843-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84843-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84843-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84843-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84843-141">CommonParameters</span></span>
<span data-ttu-id="84843-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84843-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84843-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84843-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84843-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84843-144">INPUTS</span></span>

### <span data-ttu-id="84843-145">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="84843-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="84843-146">System.String</span><span class="sxs-lookup"><span data-stu-id="84843-146">System.String</span></span>

## <span data-ttu-id="84843-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84843-147">OUTPUTS</span></span>

### <span data-ttu-id="84843-148">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="84843-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="84843-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84843-149">NOTES</span></span>

## <span data-ttu-id="84843-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84843-150">RELATED LINKS</span></span>
