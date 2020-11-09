---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308035"
---
# <span data-ttu-id="f8394-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f8394-101">New-AzPeering</span></span>

## <span data-ttu-id="f8394-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8394-102">SYNOPSIS</span></span>
<span data-ttu-id="f8394-103">Tworzy nowy zasób ARM w sieci równorzędnej</span><span class="sxs-lookup"><span data-stu-id="f8394-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="f8394-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8394-104">SYNTAX</span></span>

### <span data-ttu-id="f8394-105">Exchange (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f8394-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8394-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="f8394-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8394-107">Łącza</span><span class="sxs-lookup"><span data-stu-id="f8394-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8394-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8394-108">DESCRIPTION</span></span>
<span data-ttu-id="f8394-109">Tworzy komunikację między użytkownikami ARM w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f8394-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="f8394-110">Aby uzyskać więcej informacji na temat tworzenia obiektu połączenia, zobacz [Nowość-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) lub [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .</span><span class="sxs-lookup"><span data-stu-id="f8394-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="f8394-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8394-111">EXAMPLES</span></span>

### <span data-ttu-id="f8394-112">Tworzenie nowej bezpośredniej komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="f8394-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="f8394-113">Tworzenie nowej bezpośredniej komunikacji równorzędnej przy użyciu jednego połączenia w obiekcie Seattle przy użyciu programu PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="f8394-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="f8394-114">Tworzenie nowego elementu równorzędnego programu Exchange</span><span class="sxs-lookup"><span data-stu-id="f8394-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="f8394-115">Tworzenie nowego elementu równorzędnego programu Exchange</span><span class="sxs-lookup"><span data-stu-id="f8394-115">Create a new exchange peering</span></span>

### <span data-ttu-id="f8394-116">Konwertowanie starszych elementów równorzędnych na ramię</span><span class="sxs-lookup"><span data-stu-id="f8394-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="f8394-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8394-117">PARAMETERS</span></span>

### <span data-ttu-id="f8394-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8394-118">-AsJob</span></span>
<span data-ttu-id="f8394-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="f8394-119">Run in the background.</span></span>

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

### <span data-ttu-id="f8394-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8394-120">-DefaultProfile</span></span>
<span data-ttu-id="f8394-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8394-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8394-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="f8394-122">-DirectConnection</span></span>
<span data-ttu-id="f8394-123">Tworzenie nowych połączeń bezpośrednich przy użyciu New-AzExchangePeeringConnection i potoku do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="f8394-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="f8394-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="f8394-124">-ExchangeConnection</span></span>
<span data-ttu-id="f8394-125">Utwórz nowe połączenia programu Exchange przy użyciu New-AzExchangePeeringConnection i potoku do tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="f8394-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="f8394-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8394-126">-InputObject</span></span>
<span data-ttu-id="f8394-127">Użyj Get-AzLegacyPeering, aby pobrać ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="f8394-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="f8394-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="f8394-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="f8394-129">Wybierz sieć firmy Microsoft, z którą chcesz się połączyć.</span><span class="sxs-lookup"><span data-stu-id="f8394-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="f8394-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8394-130">-Name</span></span>
<span data-ttu-id="f8394-131">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f8394-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f8394-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="f8394-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="f8394-133">Identyfikator zasobu elementu równorzędnego ASN. Użyj Get-AzPeerAsn, aby pobrać identyfikator.</span><span class="sxs-lookup"><span data-stu-id="f8394-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="f8394-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="f8394-134">-PeeringLocation</span></span>
<span data-ttu-id="f8394-135">Lokalizacja fizyczna różna od obszaru Azure region.</span><span class="sxs-lookup"><span data-stu-id="f8394-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="f8394-136">Użyj Get-AzPeeringLocation-Kind \<kind\> Nazwa miasta jako klucza.</span><span class="sxs-lookup"><span data-stu-id="f8394-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="f8394-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8394-137">-ResourceGroupName</span></span>
<span data-ttu-id="f8394-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8394-138">The resource group name.</span></span>

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

### <span data-ttu-id="f8394-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="f8394-139">-Sku</span></span>
<span data-ttu-id="f8394-140">Wybierz pozycję Basic_Direct_Free lub Premium_Direct_Free, chyba że użytkownik jawnie poinformuje Cię, że wybierzesz inną opcję.</span><span class="sxs-lookup"><span data-stu-id="f8394-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="f8394-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8394-141">-Tag</span></span>
<span data-ttu-id="f8394-142">Tagi, które mają zostać skojarzone z usługą Microsoft peer.</span><span class="sxs-lookup"><span data-stu-id="f8394-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="f8394-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8394-143">-Confirm</span></span>
<span data-ttu-id="f8394-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8394-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8394-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8394-145">-WhatIf</span></span>
<span data-ttu-id="f8394-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8394-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8394-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8394-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8394-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8394-148">CommonParameters</span></span>
<span data-ttu-id="f8394-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8394-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8394-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8394-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8394-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8394-151">INPUTS</span></span>

### <span data-ttu-id="f8394-152">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f8394-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f8394-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8394-153">OUTPUTS</span></span>

### <span data-ttu-id="f8394-154">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f8394-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="f8394-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8394-155">NOTES</span></span>

## <span data-ttu-id="f8394-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8394-156">RELATED LINKS</span></span>
