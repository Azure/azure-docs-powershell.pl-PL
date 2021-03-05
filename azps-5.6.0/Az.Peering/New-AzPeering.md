---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: d8ef4378ed0032012a64d015855ca0287d608a6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989444"
---
# <span data-ttu-id="3aa0c-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="3aa0c-101">New-AzPeering</span></span>

## <span data-ttu-id="3aa0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aa0c-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa0c-103">Tworzy nowy zasób ARM komunikacji ARM komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="3aa0c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3aa0c-104">SYNTAX</span></span>

### <span data-ttu-id="3aa0c-105">Exchange (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3aa0c-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa0c-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="3aa0c-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa0c-107">Direct</span><span class="sxs-lookup"><span data-stu-id="3aa0c-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3aa0c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3aa0c-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa0c-109">Tworzy ARM równorzędną dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="3aa0c-110">Aby uzyskać więcej informacji na temat tworzenia obiektu połączenia, zobacz [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) lub [New-AzPeeringExchangeConnectionObject.](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject)</span><span class="sxs-lookup"><span data-stu-id="3aa0c-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="3aa0c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3aa0c-111">EXAMPLES</span></span>

### <span data-ttu-id="3aa0c-112">Tworzenie nowej bezpośredniej komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="3aa0c-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="3aa0c-113">Tworzenie nowej bezpośredniej komunikacji równorzędnej z jednym połączeniem w obiekcie Seattle przy użyciu usługi PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="3aa0c-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="3aa0c-114">Tworzenie nowej komunikacji równorzędnej programu Exchange</span><span class="sxs-lookup"><span data-stu-id="3aa0c-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="3aa0c-115">Tworzenie nowej komunikacji równorzędnej programu Exchange</span><span class="sxs-lookup"><span data-stu-id="3aa0c-115">Create a new exchange peering</span></span>

### <span data-ttu-id="3aa0c-116">Konwertowanie starszej komunikacji równorzędnej na ARM równorzędną</span><span class="sxs-lookup"><span data-stu-id="3aa0c-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="3aa0c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aa0c-117">PARAMETERS</span></span>

### <span data-ttu-id="3aa0c-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3aa0c-118">-AsJob</span></span>
<span data-ttu-id="3aa0c-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-119">Run in the background.</span></span>

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

### <span data-ttu-id="3aa0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa0c-120">-DefaultProfile</span></span>
<span data-ttu-id="3aa0c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aa0c-122">- DirectConnection</span><span class="sxs-lookup"><span data-stu-id="3aa0c-122">-DirectConnection</span></span>
<span data-ttu-id="3aa0c-123">Utwórz nowe połączenia bezpośrednie, używając New-AzExchangePeeringConnection i potoku do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-124">- ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="3aa0c-124">-ExchangeConnection</span></span>
<span data-ttu-id="3aa0c-125">Utwórz nowe połączenia programu Exchange, używając New-AzExchangePeeringConnection i potoku do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa0c-126">-InputObject</span></span>
<span data-ttu-id="3aa0c-127">Użyj Get-AzLegacyPeering, aby pobrać ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-128">— MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="3aa0c-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="3aa0c-129">Wybierz sieć firmy Microsoft, z którą chcesz się schować.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3aa0c-130">-Name</span></span>
<span data-ttu-id="3aa0c-131">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa0c-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="3aa0c-133">Identyfikator zasobu równorzędnego asn. Użyj Get-AzPeerAsn, aby pobrać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3aa0c-134">-PeeringLocation</span></span>
<span data-ttu-id="3aa0c-135">Lokalizacja fizyczna inna niż region platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="3aa0c-136">Użyj Get-AzPeeringLocation -Rodzaj \<kind\> użyj nazwy miasta jako klucza.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa0c-137">-ResourceGroupName</span></span>
<span data-ttu-id="3aa0c-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-139">- SKU</span><span class="sxs-lookup"><span data-stu-id="3aa0c-139">-Sku</span></span>
<span data-ttu-id="3aa0c-140">Wybierz Basic_Direct_Free lub Premium_Direct_Free, chyba że jawnie zasuń inną opcję.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-141">— Tag</span><span class="sxs-lookup"><span data-stu-id="3aa0c-141">-Tag</span></span>
<span data-ttu-id="3aa0c-142">Tagi do skojarzenia z usługą komunikacji równorzędnej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-142">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa0c-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3aa0c-143">-Confirm</span></span>
<span data-ttu-id="3aa0c-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa0c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa0c-145">-WhatIf</span></span>
<span data-ttu-id="3aa0c-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3aa0c-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa0c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa0c-148">CommonParameters</span></span>
<span data-ttu-id="3aa0c-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa0c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa0c-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aa0c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa0c-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aa0c-151">INPUTS</span></span>

### <span data-ttu-id="3aa0c-152">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="3aa0c-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3aa0c-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aa0c-153">OUTPUTS</span></span>

### <span data-ttu-id="3aa0c-154">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="3aa0c-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3aa0c-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3aa0c-155">NOTES</span></span>

## <span data-ttu-id="3aa0c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3aa0c-156">RELATED LINKS</span></span>
